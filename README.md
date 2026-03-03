# Red Team Mapper v2.0

[![GitHub Pages](https://github.com/atraxsrc/RedTeamMapper/actions/workflows/pages/pages-build-deployment/badge.svg)](https://atraxsrc.github.io/RedTeamMapper/)   [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) [![Tokyo Night Theme](https://img.shields.io/badge/theme-Tokyo%20Night-blueviolet)](https://github.com/enkia/tokyo-night-vscode-theme)
   

**Comprehensive visual reference & attack path mapper for red team, purple team, and adversary emulation operations.**

A single-page, interactive red team dashboard mapping the full offensive lifecycle:

Initial Access → Execution → Persistence → Privilege Escalation → Defense Evasion → Credential Access → Discovery → Lateral Movement → Collection → Exfiltration → Impact

Built as a static HTML/CSS site using the beautiful **Tokyo Night** color palette.

Live version:  
https://atraxsrc.github.io/RedTeamMapper/

## Features

- Clean, cyberpunk-inspired UI with Tokyo Night theme
- Full MITRE ATT&CK-aligned attack lifecycle diagram (SVG)
- End-to-end red team kill chains & TTP flows (phishing → ransomware → AD compromise → cloud attacks, etc.)
- Detailed sections covering:
  - Initial access vectors (phishing, exploit, supply chain)
  - Execution & living-off-the-land binaries (LOLBins)
  - Persistence mechanisms (scheduled tasks, registry, WMI)
  - Privilege escalation & credential access paths
  - Defense evasion techniques (AMSI/ETW bypass, obfuscation)
  - Discovery & reconnaissance patterns
  - Lateral movement (PsExec, WMI, RDP, WinRM)
  - Collection & exfiltration channels
  - Impact & ransomware behaviors
  - Cloud attack paths (token theft, IAM abuse, container breakout)
  - Tool arsenal & key red team signatures
- Responsive design, monospace typography, semantic color highlighting

## Screenshots

<img width="1753" height="1357" alt="Screenshot_2026-03-03_21-42-25" src="https://github.com/user-attachments/assets/59b816e9-dfa1-49a6-98be-79359b3fffd5" />
<img width="1775" height="1458" alt="Screenshot_2026-03-03_21-43-22" src="https://github.com/user-attachments/assets/a5ddeda8-8a39-4134-9196-8ec0dcf79a9a" />

## Tech Stack

- HTML5 + CSS (custom variables)
- Google Fonts: JetBrains Mono + IBM Plex Sans
- Pure CSS variables based on **Tokyo Night** palette
- No JavaScript / frameworks — 100% static

## Tokyo Night Palette Used

```css
:root {
  --bg: #1a1b26;
  --bg-card: #24283b;
  --border: #414868;
  --text: #a9b1d6;
  --text-bright: #c0caf5;
  --text-dim: #565f89;
  --red: #f7768e;
  --orange: #e0af68;
  --yellow: #e0af68;
  --green: #9ece6a;
  --cyan: #7dcfff;
  --blue: #7aa2f7;
  --purple: #bb9af7;
  --pink: #bb9af7;
  --rose: #f7768e;
  --teal: #73daca;
}
```
