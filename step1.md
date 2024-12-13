# Step 1: Setting Up WSL

Windows Subsystem for Linux (WSL) allows you to run a Linux environment directly on Windows without the overhead of a traditional virtual machine. This guide will help you set up WSL and prepare your system for Apache Gora.

---

## Step 1.1: Enable WSL**Open PowerShell as Administrator**:

1. - Search for `PowerShell` in the Start menu, right-click, and choose "Run as Administrator."
2. **Enable WSL**:

   - Run the following command to enable WSL:
     ```powershell
     wsl --install
     ```
   - This command installs WSL along with the default Linux distribution (Ubuntu).
3. **Verify Installation**:

   - After the installation completes, restart your computer.
   - Open PowerShell and check the WSL version:
     ```powershell
     wsl --list --verbose
     ```

---

## Step 1.2: Install a Linux Distribution

1. **Find online linux distros**
    - Type this command into powershell
    ```wsl --list --online
2. **Choose your distro**:
   - Select from the list of distros
   - We recommend Ubuntu-24.04
   ```wsl --install -d Unbuntu-24.04
3. **Enter a username and password**:

   - Linux will ask for a username and password, that will server as your root account so dont forget it!

---

## Step 1.3: Update the Linux Environment

1. **Update Package Lists**:

   ```bash
   sudo apt update
   ```
2. **Upgrade Installed Packages**:

   ```bash
   sudo apt upgrade -y
   ```
3. **Install Common Utilities**:

   ```bash
   sudo apt install -y curl wget git build-essential
   ```

---

## Step 1.4: Verify WSL Setup

1. **Check WSL Version**:

   ```bash
   wsl --version
   ```
2. **Verify Linux Version**:

   ```bash
   lsb_release -a
   ```

---

Your WSL environment is now ready. Proceed to [Step 2: Requirements for Apache Gora Installation](step2.md).
