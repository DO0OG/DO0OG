<div align="right">

**English** · [한국어](./README.ko.md)

</div>

<div align="center">

<img src="./assets/profile-banner.svg" width="100%" alt="DO0OG — desktop software, AI, and developer tools" />

<br/>

**I build desktop applications, AI assistants, and developer tools, with a focus on practical use and careful validation.**

C# / .NET · Python · Avalonia · PySide6 · Windows & cross-platform development

[![GitHub](https://img.shields.io/badge/GitHub-DO0OG-181717?style=flat-square&logo=github)](https://github.com/DO0OG)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:laleme@naver.com)

[Recent projects](#recent-projects) · [More projects](#more-projects) · [Tech stack](#tech-stack) · [Background](#background)

</div>

---

## Recent Projects

Recent public work, with a focus on Windows utilities, AI, and developer tooling.

### [AsterCache — HDD Game Loading Optimization](https://github.com/DO0OG/AsterCache)

**An experimental Windows 11 utility designed to reduce HDD seek overhead during repeated game loads without moving entire games to an SSD.**

`C#` `.NET 10` `Windows` `NTFS` `ETW` `RAM Cache`

- Records game file-read patterns using Windows Event Tracing (ETW).
- Uses NTFS data relocation, access-order prefetching, and RAM prewarming to improve data locality on subsequent launches.
- Includes background game discovery, automatic operation, safety checks, and [shared load-order profiles](https://github.com/DO0OG/AsterCache-profiles).

[![AsterCache updated](https://img.shields.io/github/last-commit/DO0OG/AsterCache?style=flat-square&label=updated)](https://github.com/DO0OG/AsterCache/commits/main)
[![AsterCache release](https://img.shields.io/github/v/release/DO0OG/AsterCache?style=flat-square&label=release)](https://github.com/DO0OG/AsterCache/releases/latest)
[![AsterCache license](https://img.shields.io/github/license/DO0OG/AsterCache?style=flat-square)](https://github.com/DO0OG/AsterCache/blob/main/LICENSE)

<sub>Experimental: recorded I/O replay results are not proof of faster real-game loading. Data relocation writes to the HDD; read the compatibility notes and back up important data first.</sub>

<br/>

### [Ari — AI Voice Assistant & Autonomous Desktop Agent](https://github.com/DO0OG/Ari-VoiceCommand)

**An open-source Windows voice assistant and desktop agent combining speech interaction, local or hosted language models, Windows automation, and tool-based workflows.**

`Python` `PySide6` `Ollama` `MCP` `STT/TTS` `AI Agent`

- Wake-word activation, multilingual speech recognition, spoken replies, and an interactive desktop character.
- Local LLM support, memory, plugins, `SKILL.md` skills, and Model Context Protocol (MCP) integrations.
- Tool-driven desktop tasks with planning, execution, verification, and interruption controls.

[![Ari updated](https://img.shields.io/github/last-commit/DO0OG/Ari-VoiceCommand?style=flat-square&label=updated)](https://github.com/DO0OG/Ari-VoiceCommand/commits/main)
[![Ari release](https://img.shields.io/github/v/release/DO0OG/Ari-VoiceCommand?style=flat-square&label=release)](https://github.com/DO0OG/Ari-VoiceCommand/releases/latest)
[![Ari stars](https://img.shields.io/github/stars/DO0OG/Ari-VoiceCommand?style=flat-square)](https://github.com/DO0OG/Ari-VoiceCommand/stargazers)

[Project homepage](https://ari-voice-command.vercel.app) · [Download latest release](https://github.com/DO0OG/Ari-VoiceCommand/releases/latest) · [Documentation](https://github.com/DO0OG/Ari-VoiceCommand#install)

<br/>

### [agk75-tool — Unofficial AGK75 Keyboard Configuration](https://github.com/DO0OG/agk75-tool)

**An unofficial desktop configuration utility for the Antgamer AGK75, developed by examining the keyboard's USB HID protocol.**

`Python` `PySide6` `HID API` `Device Configuration`

- Key remapping, Fn layers, profiles, lighting effects, rapid-trigger controls, and polling-rate configuration.
- Device read-back verification, settings backup/restore, and USB polling-rate diagnostics.
- Korean, English, and Simplified Chinese user interfaces; no network connection required for the app.

[![AGK75 tool updated](https://img.shields.io/github/last-commit/DO0OG/agk75-tool?style=flat-square&label=updated)](https://github.com/DO0OG/agk75-tool/commits/main)
[![AGK75 tool license](https://img.shields.io/github/license/DO0OG/agk75-tool?style=flat-square)](https://github.com/DO0OG/agk75-tool/blob/main/LICENSE)

<sub>Unofficial project; not affiliated with Antgamer. Designed for a compatible AGK75 connected over USB.</sub>

---

## More Projects

### [CustomLauncher — Cross-platform Minecraft Launcher](https://github.com/DO0OG/CustomLaucncher)

A configurable Minecraft launcher and distribution client for **Windows, macOS, and Linux**, built with `C#`, `.NET 8`, and `Avalonia`.

- Microsoft/Xbox sign-in and account management.
- Integrity-checked incremental downloads, repair, rollback, and mod/resource-pack management.
- Multiple server configurations, Forge/Fabric/NeoForge/Quilt support, and update workflows.

[![CustomLauncher updated](https://img.shields.io/github/last-commit/DO0OG/CustomLaucncher?style=flat-square&label=updated)](https://github.com/DO0OG/CustomLaucncher/commits/main)

<br/>

### [yttStudio — Visual YouTube Subtitle Editor](https://github.com/DO0OG/yttStudio)

A cross-platform **WYSIWYG YTT/SRV3 subtitle editor** built with `C#`, `.NET 10`, and `Avalonia`.

- Edit subtitle placement and styling directly on a video preview.
- Work with timelines, karaoke timing, multi-keyframe animation, and subtitle effects.
- Validate YouTube subtitle-format constraints and export styled subtitles.

[![yttStudio updated](https://img.shields.io/github/last-commit/DO0OG/yttStudio?style=flat-square&label=updated)](https://github.com/DO0OG/yttStudio/commits/main)
[![yttStudio release](https://img.shields.io/github/v/release/DO0OG/yttStudio?style=flat-square&label=release)](https://github.com/DO0OG/yttStudio/releases/latest)

---

## Tech Stack

<div align="center">

**Languages**

![C#](https://img.shields.io/badge/C%23-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

**Desktop & Interactive Development**

![.NET](https://img.shields.io/badge/.NET-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![Avalonia](https://img.shields.io/badge/Avalonia-8B44AC?style=for-the-badge)
![PySide6](https://img.shields.io/badge/PySide6-41CD52?style=for-the-badge&logo=qt&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=for-the-badge&logo=unity&logoColor=white)

**Tooling & Systems**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)

</div>

## Current Interests

- **AI assistants and agent workflows:** speech interfaces, local models, tool integrations, and desktop automation.
- **Desktop application engineering:** responsive native UIs, cross-platform apps, and maintainable architectures.
- **Performance and systems:** measuring bottlenecks, improving disk I/O, and exploring efficient workflows.
- **Software delivery:** automated tests, CI/CD, installers, releases, updates, and recovery paths.

---

## Background

**Computer Engineering** · Seowon University  
**Unity Bootcamp** · Korea Chamber of Commerce and Industry

---

## GitHub Activity

<div align="center">

<a href="https://github.com/stats-organization/github-stats-extended">
  <img height="180" src="https://github-stats-extended.vercel.app/api?username=DO0OG&show_icons=true&hide_border=true&theme=transparent&include_all_commits=true&rank_icon=github" alt="DO0OG GitHub activity statistics" />
</a>

</div>

---

<div align="center">

<sub>Build useful things. Make them reliable. Keep improving them.</sub>

</div>
