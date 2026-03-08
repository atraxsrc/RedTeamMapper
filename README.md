# Red Team Mapper v3.0

[![GitHub Pages](https://github.com/atraxsrc/RedTeamMapper/actions/workflows/pages/pages-build-deployment/badge.svg)](https://atraxsrc.github.io/RedTeamMapper/)   [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Tokyo Night Theme](https://img.shields.io/badge/theme-Tokyo%20Night-blueviolet)](https://github.com/enkia/tokyo-night-vscode-theme)
   

**Comprehensive visual reference & attack path mapper for red team, purple team, and adversary emulation operations.**

A single-page, interactive red team dashboard mapping the full offensive lifecycle:
Initial Access → Execution → Persistence → Privilege Escalation → Defense Evasion → Credential Access → Discovery → Lateral Movement → Collection → Exfiltration → Impact

Built as a static HTML/CSS site using the beautiful **Tokyo Night** color palette.

**Live version:**  
https://atraxsrc.github.io/RedTeamMapper/

**Companion project:**  
[Blue Team Mapper](https://atraxsrc.github.io/BlueTeamMapper/) — the defensive counterpart.

## Why This Exists
Red vs Blue is most effective when both sides speak the same language.  
This mapper gives red teamers, purple teamers, and adversary emulation operators a clean, visual blueprint of every major attack path — so defenders know exactly what to hunt for and how to stop it.

## Features
- Sticky sidebar navigation with scroll-spy — jump to any phase instantly
- 7-phase kill chain lifecycle bar (Infrastructure → Initial Access → Execution → Evasion → Lateral/Persist → Collection → Exfiltration)
- 19 end-to-end operation flow chains (phishing → DA, MFA bypass → cloud, ADCS ESC4, BadSuccessor, device code, WDAC kill, etc.)
- Callout boxes for critical OPSEC warnings, EDR detection layers, and high-risk actions
- Detailed sections covering:
  - C2 frameworks deep dive (Cobalt Strike, Havoc, Sliver, Mythic, Brute Ratel, covert channels)
  - Red team infrastructure (redirectors, Malleable C2 profiles, IaC automation)
  - Initial access vectors (HTML smuggling, AitM/EvilGinx, device code phishing, ClickFix, macro-less payloads)
  - Payload development (shellcode generation, loaders, DLL sideloading, LOLBins, advanced PIC compilation)
  - Defense evasion (AMSI/ETW bypass, direct/indirect syscalls, sleep obfuscation, unhooking, call stack spoofing, EDR-specific bypasses)
  - Process injection (threadless injection, early cascade, module stomping, APC/thread pool)
  - Persistence mechanisms (COM hijacking, scheduled tasks, WMI events, DLL sideload persistence)
  - Credential access (evasive LSASS dumping, DPAPI/browser harvesting, Kerberos ticket theft, all-in-one tools)
  - Lateral movement (SCShell, DCOM, token impersonation, C2 pivoting, Pass-the-Hash/Ticket/Certificate)
  - Exfiltration & data staging (HTTPS C2, DNS exfil, cloud storage abuse)
  - OPSEC (detection risk matrix, MDI/identity evasion, canary token detection, network OPSEC)
  - Privilege escalation (BYOVD, BadSuccessor, NTLM reflection, RBCD, KrbRelayUp)
  - Active Directory attacks (ADCS ESC1–ESC15, Shadow Credentials, DCSync, vSphere snapshot extraction)
  - MOTW bypass & delivery (LNK chains, polyglot files, SmartScreen bypass, MSI/MST weaponization)
  - Social engineering & vishing (CID spoofing infra, voice cloning, ClickFix/pastejacking, QR phishing, trusted platform abuse)
  - Cloud attack operations (Azure/Entra ID, CAP bypass, AWS SSO, on-prem to cloud pivoting)
  - Notable CVEs 2025
  - macOS & Linux red teaming
  - AI-assisted operations (LLM jailbreaking, AI C2, deepfakes, autonomous agents)
  - OSINT & reconnaissance
  - Password cracking infrastructure
  - Full tool arsenal reference


## Screenshots

<img width="1848" height="1005" alt="image" src="https://github.com/user-attachments/assets/1917e967-4c23-45f7-bb3f-01692c89e9bf" />
<img width="1848" height="1005" alt="image" src="https://github.com/user-attachments/assets/de843d09-1c07-456f-9ebd-239e9c530668" />
<img width="1855" height="1391" alt="image" src="https://github.com/user-attachments/assets/54845571-0dc4-4b80-a787-b96fb2b72fa9" />

## Tech Stack

-  HTML5 + CSS + JavaScript (vanilla, no frameworks)
- Google Fonts: **Syne** (headings) + **IBM Plex Sans** (body) + **JetBrains Mono** (code/mono)
- Extended Tokyo Night CSS variable system
- IntersectionObserver API for sidebar scroll-spy

## Tokyo Night Palette (Extended)

```css
:root {
  --bg:           #1a1b26;
  --bg-card:      #1e2030;
  --bg-raised:    #24283b;
  --bg-hover:     #292e42;
  --border:       #3b4261;
  --border-dim:   #2a2e42;
  --text:         #a9b1d6;
  --text-bright:  #cdd6f4;
  --text-dim:     #6c7086;
  --text-muted:   #45475a;
  --red:          #f7768e;
  --orange:       #e0af68;
  --yellow:       #e0af68;
  --green:        #9ece6a;
  --cyan:         #7dcfff;
  --blue:         #7aa2f7;
  --purple:       #bb9af7;
  --pink:         #bb9af7;
  --rose:         #f7768e;
  --teal:         #73daca;
}
```
## Changelog

### v3.0
- Added sticky sidebar navigation (260px) with grouped phase categories and IntersectionObserver scroll-spy
- Replaced SVG kill chain architecture diagram with clean 7-phase lifecycle bar
- Rewrote all operation flow chains as card-based layout with labeled arrows
- Added Syne 800 as heading font; increased base font to 14px / line-height 1.75
- Added callout boxes (danger/warn/info) for critical OPSEC warnings and EDR detection guidance
- Extended CSS variable set with `--bg-card`, `--bg-raised`, `--bg-hover`, `--border-dim`, `--text-muted`
- Card accent bars (2px colored top-border per phase)
- New content: BadSuccessor, NTLM reflection CVE-2025-33073, AI-driven C2, MDI evasion, ClickFix, ClickFix vishing, QR phishing, vSphere credential extraction, Cloud CAP bypass, and more

### v2.0
- Initial public release
