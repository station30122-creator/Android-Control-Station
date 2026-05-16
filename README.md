 Built a custom Android control station — ADB + scrcpy launcher with LLM-assisted debloat
Been working on this for a while and finally packaged it as a standalone .exe. Figured I'd share it since it's actually useful.
━━━━━━━━━━━━━━━━━━━━━
🔧 WHAT IT DOES
━━━━━━━━━━━━━━━━━━━━━
• Connects to Android devices over USB or WiFi via ADB
• Launches scrcpy (screen mirror/control) with a full flag builder — no command line needed
• Built-in ADB console — paste single commands or full multi-line batches, it auto-routes them to the selected device (no need to prefix with adb -s)
• Device manager — scan, connect, rename, save WiFi devices, auto-launch on new connection
• Presets — save your favorite flag combos for one-click launch
• Minimize to system tray
━━━━━━━━━━━━━━━━━━━━━
🤖 LLM DEBLOAT WORKFLOW
━━━━━━━━━━━━━━━━━━━━━
This is the part I'm most proud of. The app pulls your device specs and full package/process list, then generates a ready-to-paste prompt you drop into ChatGPT or Claude. Four profiles:
🎮 Gaming — nukes telephony, carrier, social. Keeps GPU drivers and Play stack.
📱 General — light touch, obvious bloat only.
⚠️ Moderate — manufacturer duplicates, cloud sync, deeper clean.
💀 Nuke — strip everything non-essential.
🧠 RAM Clear — pulls running processes sorted by RAM, generates a kill list for background leechers.
All commands come back as pm uninstall --user 0 (reversible, user-space only). Paste them straight into the app console and they execute sequentially.
━━━━━━━━━━━━━━━━━━━━━
⚙️ REQUIREMENTS
━━━━━━━━━━━━━━━━━━━━━
• Windows 10/11 x64
• ADB drivers installed (universal ADB driver works fine)
• USB debugging or wireless ADB enabled on your Android device
• No Python needed — ships as a portable .exe with scrcpy bundled
