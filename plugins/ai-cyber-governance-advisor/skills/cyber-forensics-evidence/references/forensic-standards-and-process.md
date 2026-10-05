# Forensic Standards and Process (Concept Level)

This file describes principles and procedure only. It contains no instructions for bypassing device locks, breaking encryption, or anti-forensics. Acquisition must always rest on lawful authority.

## 1. The ISO/IEC investigation family

| Standard | Title / focus | Use it for |
|---|---|---|
| **ISO/IEC 27037:2012** | Guidelines for identification, collection, acquisition and preservation of digital evidence | First response; handling devices; the roles of DEFR (Digital Evidence First Responder) and DES (Digital Evidence Specialist); auditability, repeatability, reproducibility, justifiability |
| **ISO/IEC 27041:2015** | Assurance of suitability and adequacy of the incident investigative method | Tool and method validation; showing your process is fit for purpose |
| **ISO/IEC 27042:2015** | Analysis and interpretation of digital evidence | Analytical models; competence; documenting interpretation and conclusions |
| **ISO/IEC 27043:2015** | Incident investigation principles and processes | The end-to-end process: readiness, initialisation, acquisitive and investigative classes |
| ISO/IEC 27050 series | Electronic discovery | Civil disclosure and eDiscovery |
| ISO/IEC 30121:2015 | Governance of digital forensic risk framework | Board-level forensic readiness |

Also: NIST SP 800-86 (integrating forensics into incident response), NIST SP 800-101r1 (mobile forensics), RFC 3227 (evidence collection and archiving), and the ACPO Good Practice Guide principles (do not change the data; competent person; audit trail; the person in charge is responsible).

**The four ISO/IEC 27037 principles:**
- **Auditability:** an independent assessor can evaluate the actions taken.
- **Repeatability:** the same procedure, method and tools under the same conditions give the same result.
- **Reproducibility:** different tools or conditions give the same result.
- **Justifiability:** every action and method choice is justified.

## 2. Order of volatility (collect most volatile first)

1. CPU registers, cache
2. Memory (RAM): processes, network connections, encryption keys in use, logged-in sessions
3. Network state: routing tables, ARP cache, active connections
4. Running processes and the system state
5. Disk / persistent storage
6. Remote logging and monitoring data (SIEM, cloud audit logs). Retention clocks are running.
7. Physical configuration, network topology
8. Backups and archives

## 3. Live versus dead acquisition: decision factors

| Factor | Favours live acquisition | Favours powered-off (dead) acquisition |
|---|---|---|
| Full-disk encryption in use and the system unlocked | ✔ (data may be inaccessible after shutdown) | |
| Volatile evidence matters (malware in memory, active connections) | ✔ | |
| Business-critical server that cannot go down | ✔ (logical / targeted) | |
| Risk of destructive malware triggered by activity | | ✔ (consult a specialist) |
| Standalone device, no encryption, not running | | ✔ |

Record why the choice was made (justifiability). Live actions change the system, so minimise them and document every command or tool executed.

## 4. Acquisition and integrity basics

- Hardware or software **write-blocker** for storage media.
- A **forensic image** (bit-stream) where practical; a logical/targeted collection where the scale or the cloud makes imaging impractical. Document the scope limits.
- **Hash** the source (where possible) and the image at acquisition, and verify the hash after each copy. Use SHA-256; add MD5/SHA-1 only for legacy tool compatibility.
- Keep a **master copy** (sealed, never analysed) and **working copies**.
- **Validated tools.** Record the tool name and version, the validation reference, and any error.
- **Contemporaneous notes:** who, what, when (IST plus UTC), where, how, and why.
- Photograph the scene, the device screen state and the connections before touching anything.
- Radio isolation for mobile devices (a Faraday bag or flight mode under documented procedure) to prevent remote wipe or data change.

## 5. Evidence types: what each can show (concept level)

### Disk / file system
- File system metadata (created/modified/accessed/changed timestamps; their reliability differs by file system and OS).
- Deleted files and unallocated space (recoverability varies; SSD TRIM reduces it).
- User activity artefacts: recently used files, program execution traces, browser history, USB device connection history, cloud sync client logs, email stores.
- Typical questions: was a file present, opened, copied, deleted? Was a USB device attached?

### Memory
- Running processes, injected code, network connections, logged-in users, clipboard and command history, and keys in use.
- Short-lived and changes with every action, so capture early if relevant and justified.

### Mobile
- Acquisition levels: **logical** (what the OS exposes), **file system**, and **physical / full file system** (depends on device, OS version and lawful tools; not always possible).
- Sources: messaging apps (WhatsApp, Signal, Telegram), call logs, location history, photos with EXIF data, app databases, and cloud backups (accessing them needs separate legal authority).
- Watch for: end-to-end encryption limits, disappearing messages, multiple devices linked to one account, and screenshots versus native exports (prefer native exports with hashes).

### Cloud and SaaS
- Evidence is held by the provider, so preservation requests and legal process are needed; the tenant can export audit logs.
- Sources: admin and audit logs (sign-ins, mailbox access, file sharing), API logs, storage access logs, identity provider logs.
- Issues: retention windows are short by default; jurisdiction (data stored abroad means MLAT/CLOUD Act routes for police); multi-tenant data; and time zones (UTC).

### Logs and network
- Sources: firewall, VPN, proxy, DNS, email gateway, EDR, SIEM, web server, application, and database audit logs.
- Integrity: export with hashes; record the collection method and the query used; preserve the raw logs as well as parsed ones.
- Clock: check NTP sync (CERT-In requires sync to NIC/NPL or traceable sources); normalise to one timezone for the timeline; record known offsets.

## 6. Analysis discipline (ISO/IEC 27042)

1. Define the questions before looking.
2. Form hypotheses, including **alternative explanations** (malware, another user, remote access, time-zone error, synchronisation artefacts).
3. Test each hypothesis against the artefacts; record the supporting and contradicting evidence.
4. Rate confidence (see the opinion scale in `expert-report-template.md`).
5. Peer review where possible.
6. Keep notes sufficient for another examiner to reproduce the work.

## 7. Common integrity pitfalls (address them proactively)

- Opening files or booting the original device (this changes metadata).
- Screenshots without native exports or hashes.
- Gaps in the chain of custody (unsigned transfers, unsealed storage).
- Unvalidated or unlicensed tools; no version records.
- Clock skew not documented.
- Scope creep beyond the lawful authority (privacy and admissibility risk).
- Analysts who also acquired the evidence without notes (no audit trail).
