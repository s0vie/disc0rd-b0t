*a bot i made for my discord - used to be a py script for personal use, now compiled so i could share it.*
**i recommend running this in a folder :D** *it will create 2 files (for saving info/settings; json/env)*

**[what's baked into this bundle;]**

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

**(virusTotal hashID; 9fa5c4dee881756c13ecbc60854532fd4056442d86313125f147a3833c2bcb7e)**
