---

# **Cs2HourBot**

Discord bot for managing CS2 with auto-restart, battery monitoring, and Steam support. Includes a simple setup GUI and can be compiled into a standalone `.exe`.

---

## **🔍 Virustotal**

[https://www.virustotal.com/gui/file/0b97b5c4f4c0d525ad5651ae61cee3925f3ee018ce8b7bf16f1074f69aeedb6f?nocache=1](https://www.virustotal.com/gui/file/0b97b5c4f4c0d525ad5651ae61cee3925f3ee018ce8b7bf16f1074f69aeedb6f?nocache=1)

---

# **🎮 CS2 Hour Bot**

A Discord bot that helps you run CS2 more reliably by watching for crashes, restarting the game when needed, checking your battery status, and launching Steam when required.

---

## **✨ Features**

* **🎯 Auto-Restart** — Restarts CS2 if it closes or crashes
* **🔋 Battery Monitoring** — On laptops, shuts down CS2 (and the PC if needed) when the charger is unplugged
* **🚀 Steam Support** — Launches Steam if it isn’t running, works with multiple accounts
* **📊 Status Check** — Simple command to show CS2 and Steam status
* **🎨 Setup GUI** — Clean dark-theme interface for configuration
* **💻 Standalone Build** — Can be turned into a single `.exe`
* **📝 Logging** — Saves errors and important info to a log file

---

## **📋 Requirements**

* Windows 10 or 11
* Python 3.8+ (if running the script)
* Discord bot token
* Steam installed with CS2 available
* `discord.py` and `psutil` libraries

---

## **🚀 Installation**

### **Option 1: Run as Python Script**

Clone the project:

```sh
git clone https://github.com/yourusername/Cs2HourBot.git
cd Cs2HourBot
```

Install dependencies:

```sh
pip install discord.py psutil
```

Run the bot:

```sh
python bot.py
```

---

### **Option 2: Use the Pre-Built .exe**

1. Download the latest version from the **Releases** page
2. Run `Cs2HourBot.exe`
3. On first launch, the setup window will appear

---

## **⚙️ Configuration**

On the first run, a GUI opens and asks for:

* **Discord Bot Token**
* **Discord Channel ID**
* **Steam Username** (optional)
* **Steam Wait Time** (default 20 seconds)

This info is saved to `config.json`.

### **Manual config example**

```json
{
    "TOKEN": "your_discord_bot_token",
    "CHANNEL_ID": 123456789012345678,
    "STEAM_USERNAME": "your_steam_username",
    "STEAM_WAIT_TIME": 20
}
```

---

## **🎮 Commands**

| Command    | What it does                                 |
| ---------- | -------------------------------------------- |
| `!start`   | Launch CS2 and enable monitoring             |
| `!stop`    | Stop CS2 and turn off monitoring             |
| `!status`  | Show CS2/Steam status                        |
| `!botstop` | Stop CS2, shut down the PC, and stop the bot |

---

## **🔧 Discord Bot Setup**

1. Open the **Discord Developer Portal**
2. Create a new application
3. Add a bot to it
4. Copy the bot token
5. Turn on **Message Content Intent**
6. Invite the bot to your server

---

## **🏗️ Building the .exe**

Install PyInstaller:

```sh
pip install pyinstaller
```

Build using the spec file:

```sh
pyinstaller Cs2HourBot.spec
```

Or build manually:

```sh
pyinstaller --onefile --noconsole --name Cs2HourBot --icon=icon.ico bot.py
```

Your `.exe` will appear in the **dist** folder.

---

## **🐛 Troubleshooting**

### **Bot doesn’t respond**

* Make sure **Message Content Intent** is enabled
* Restart the bot after changing settings

### **CS2 won’t start**

* Confirm Steam is installed and logged in
* Check the CS2 game link: `steam://rungameid/730`

### **Battery checks not working**

* Only applies to laptops with battery sensors

### **Bot crashes**

* Check the `bot_crash.log` file
* Confirm all dependencies are installed

---

## **📝 Logging**

The bot writes to `bot_crash.log`, including:

* Errors
* Commands used
* Status changes
* Crash info

---

## **🔒 Security Notes**

* Keep `config.json` private
* Add `config.json` to `.gitignore`
* Never share your Discord bot token

---

## **📄 License**

This project is released under the **Apache 2.0 License**.

---

## **🤝 Contributing**

Pull requests and improvements are welcome.

---

## **⚠️ Disclaimer**

Use this bot at your own risk. The developers aren’t responsible for any damage or issues caused by its use.

---

## **📞 Support**

Open a GitHub issue and include:

* Error text from `bot_crash.log`
* How to reproduce the problem
* Your OS + Python version

---

**Made with ❤️ for the CS2 community**

---
