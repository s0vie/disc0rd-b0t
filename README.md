$$\color{green}\text{**(virusTotal hashID; 88efcc395fa8f5c9380504d69d5986e02d4de5fa40f1fef9d97a275ccba623b8)**}$$

*a bot i made for my discord - used to be a py script for personal use, now compiled so i could share it.*
**i recommend running this in a folder :D** *it will create 2 files (for saving info/settings; json/env)*

$$\color{red}\text{**[what's baked into this bundle;]**}$$

- tkinter (+ttk, messagebox) — the entire GUI (control panel, dialogs, popups)
- asyncio — runs the Discord client's event loop on its own thread
- threading — keeps the bot loop and the Tkinter UI running side by side
- queue — thread-safe hand-off between the bot thread and the UI thread
- json — reads/writes announcements.json and settings.json
- datetime / zoneinfo — scheduling logic, timeout durations, uptime tracking, timezone-aware announcement checks
- re — @name mention parsing, time-format validation
- random — the binary-loop presence text (+115 easter egg)
- logging — console output
- pathlib, os, sys — file paths, env vars, detecting whether it's running as a script or the frozen exe
- ctypes — one windows API call to minimize the console on connect
- typing — type hints only, no runtime effect

$$\color{red}\text{**[what this b0t does;]**}$$

Main control panel — Send tab
- live-populated dropdown of every text channel the bot can see across every server it's in
- type a message, hit Send (or Enter) — posts to whichever channel is selected

Presence tab
- custom status text override (blank reverts to the binary loop)
- online / Away / Busy / Offline radio buttons, applied immediately and persisted

Announcements tab
- edit each announcements time, timezone, and message right in the UI, with validation (24h time format, real IANA timezone check) — saves straight to announcements.json, live within 30s

Welcome tab
- toggle an automatic new-member welcome message, with an editable template supporting {mention} and {name}

Moderation tab
- member dropdown (auto-populated from the relevant server)
- disconnect / timeout / kick / ban, with a duration field (Timeout only) and a reason field (timeout/kick/ban only, feeds the server's audit log)
- confirmation prompt before every action

Online Users panel
- live list of who's currently online in the server tied to the selected channel (needs '*Presence Intent*' *ENABLED* in the discord Developer portal)

Welcome popup
- "welc0me user" intro window on connect, with a help link explaining every tab, a Давай блядь → (continue)-on-hover dismiss button, and a "don't show again" checkbox
