# Workstation Setup for Isaac Sim 4.5

Welcome! This guide will help you install Isaac Sim 4.5 on your computer. Follow each step carefully, and you'll be ready to create amazing virtual worlds!

---

## What You Need Before Starting

Before you begin, make sure your computer has:

- **Operating System**: Windows 10/11 or Ubuntu 20.04/22.04
- **Graphics Card**: An NVIDIA GPU with RTX support and at least 8 GB of video memory (VRAM)
- **Disk Space**: Enough space on your hard drive (SSD is recommended for faster performance)
- **RAM**: At least 16 GB of memory (more is better)
- **Updated Drivers**: Make sure your NVIDIA graphics drivers are up to date

> 💡 **Tip**: If you're not sure about your computer's specs, ask an adult to help you check!

---

## Step 1: Download Isaac Sim 4.5

1. Open your web browser (like Chrome, Firefox, or Edge)
2. Go to the NVIDIA Isaac Sim website
3. Download the [Isaac Sim 4.5](https://docs.isaacsim.omniverse.nvidia.com/4.5.0/installation/download.html#isaac-sim-latest-release)
4. Look for the **"Standalone Workstation"** version (NOT the Docker version)
5. Choose the version for your operating system:
   - **Windows**: Download `isaac-sim-standalone-4.5.0-windows-x86_64.zip`
   - **Linux**: Download `isaac-sim-standalone-4.5.0-linux-x86_64.zip`
6. Wait for the download to finish (this might take a while - the file is very large!)

---

## Step 2: Create a Folder for Isaac Sim

### On Windows:

1. Open **File Explorer**
2. Go to your `C:` drive
3. Right-click in an empty space
4. Select **New → Folder**
5. Name it `isaacsim`
6. Press Enter

### On Linux:

1. Open **Terminal**
2. Type this command and press Enter:
   ```bash
   mkdir ~/isaacsim
   ```

---

## Step 3: Extract (Unzip) the Downloaded File

### On Windows:

1. Go to your **Downloads** folder
2. Find the Isaac Sim zip file you downloaded
3. Right-click on it
4. Select **Extract All...**
5. Choose `C:\isaacsim` as the destination folder
6. Click **Extract**
7. Wait for it to finish (this takes several minutes!)

### On Linux:

1. Open **Terminal**
2. Type these commands one by one (press Enter after each):
   ```bash
   cd ~/Downloads
   unzip "isaac-sim-standalone-4.5.0-linux-x86_64.zip" -d ~/isaacsim
   ```
3. Wait for it to finish extracting

---

## Step 4: Run the Installation Script

This step sets up Isaac Sim so it works properly on your computer.

### On Windows:

1. Open **File Explorer**
2. Go to `C:\isaacsim`
3. Look for a file called `post_install.bat`
4. **Double-click** on `post_install.bat`
5. A black window will appear - wait for it to finish (it might take a few minutes)
6. When it says "Press any key to continue...", press any key to close it

### On Linux:

1. Open **Terminal**
2. Type these commands:
   ```bash
   cd ~/isaacsim
   ./post_install.sh
   ```
3. Wait for it to finish (it might ask for your password - that's normal!)

---

## Step 5: Launch Isaac Sim for the First Time

### On Windows:

1. Go to `C:\isaacsim` in File Explorer
2. Look for `isaac-sim.selector.bat`
3. **Double-click** on it
4. A small window will appear - this is the **App Selector**
5. Click the **START** button
6. Isaac Sim will begin to launch (this takes a long time the first time - be patient!)

### On Linux:

1. Open **Terminal**
2. Type these commands:
   ```bash
   cd ~/isaacsim
   ./isaac-sim.selector.sh
   ```
3. Click **START** in the App Selector window
4. Wait for Isaac Sim to load

> ⏰ **Important**: The first time you launch Isaac Sim, it takes a LONG time (maybe 5-10 minutes or more). This is because it's building something called a "shader cache" - this makes graphics look good later. Don't worry if it seems stuck - just wait!

---

## Step 6: Verify Everything Works

Once Isaac Sim opens:

1. You should see a 3D window (the viewport)
2. There should be menus at the top (File, Edit, Create, etc.)
3. On the left side, you should see a panel with "Stage" or "Outliner"
4. If you see all of this, **congratulations!** Isaac Sim 4.5 is installed correctly! 🎉

---

## Optional: Download Local Assets (Recommended)

If you want Isaac Sim to work faster and work even when you're offline:

1. Download all three Isaac Sim asset packs for version 4.5 from NVIDIA's website
2. Create a folder called `isaacsim_assets`:
   - **Windows**: `C:\isaacsim_assets`
   - **Linux**: `~/isaacsim_assets`
3. Extract all three asset packs into this folder
4. Make sure each unpacked folder contains `Assets/Isaac/4.5/Isaac/...` inside

### Tell Isaac Sim to Use Local Assets:

**Option 1: Edit the settings file**

1. Find this file:
   - **Windows**: `C:\isaacsim\apps\isaacsim.exp.base.kit`
   - **Linux**: `~/isaacsim/apps/isaacsim.exp.base.kit`
2. Open it with a text editor (like Notepad on Windows or gedit on Linux)
3. Add these lines at the end:
   ```ini
   [settings]
   persistent.isaac.asset_root.default = "C:/isaacsim_assets/Assets/Isaac/4.5"
   ```
   (On Linux, use: `~/isaacsim_assets/Assets/Isaac/4.5`)

**Option 2: Use a launch flag**

When starting Isaac Sim, add this to the command:
- **Windows**: 
  ```
  isaac-sim.bat --/persistent/isaac/asset_root/default="C:\isaacsim_assets\Assets\Isaac\4.5"
  ```
- **Linux**:
  ```bash
  ./isaac-sim.sh --/persistent/isaac/asset_root/default="~/isaacsim_assets/Assets/Isaac/4.5"
  ```

---

## Troubleshooting

### Problem: Isaac Sim won't start

- **Solution**: Make sure your graphics drivers are updated. Go to NVIDIA's website and download the latest drivers for your GPU.

### Problem: It says "out of memory" or crashes

- **Solution**: Close other programs that use a lot of memory (like games, video editors). Isaac Sim needs a lot of RAM!

### Problem: Everything looks weird or wrong

- **Solution**: Try resetting Isaac Sim by launching it with the `--reset-user` flag:
  - **Windows**: Edit the shortcut to add `--reset-user` at the end
  - **Linux**: Run `./isaac-sim.sh --reset-user`

---

## Quick Reference Table

| What to Do | Windows | Linux |
|------------|---------|-------|
| Create folder | `C:\isaacsim` | `~/isaacsim` |
| Extract zip | Extract to `C:\isaacsim` | `unzip` to `~/isaacsim` |
| Run installation | Double-click `post_install.bat` | Run `./post_install.sh` |
| Launch Isaac Sim | Double-click `isaac-sim.selector.bat` | Run `./isaac-sim.selector.sh` |

---

## You're All Set! 🎉

Now that Isaac Sim 4.5 is installed, you're ready to start creating amazing virtual worlds! 

**Next Step**: Check out the [World Creation Guide](../World/Scene/world_creation.md) to learn how to build your first world!

---

> 📝 **Remember**: This guide is ONLY for Isaac Sim version 4.5. If you have a different version, some steps might be different!

