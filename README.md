# Logseq Git-Crypt Sync

A step-by-step guide and automation scripts to securely sync your Logseq notes across multiple devices using Git and `git-crypt`. Your notes are encrypted in the remote repository and only decrypted locally on your authorized devices.

---

## ✅ Features

-   **Transparent Encryption**: Encrypts your Logseq notes before they are pushed to GitHub, ensuring your private information is secure.
-   **Cross-Device Synchronization**: Provides a robust workflow to sync your notes between Windows and Android.
-   **Simple Automation**: Includes automation scripts to simplify the daily sync process.

---

## ⚡ Prerequisites

To follow this guide, you will need the following software installed on your devices:

-   **Git** [https://git-scm.com/downloads](https://git-scm.com/downloads)
-   **`git-crypt`** Official repository and installation instructions:  
    [https://github.com/AGWA/git-crypt](https://github.com/AGWA/git-crypt)
-   **Termux (for Android setup)** Install from F-Droid:  
    [https://f-droid.org/packages/com.termux/](https://f-droid.org/packages/com.termux/)

---

## 📚 Usage Overview

### 1️⃣ [**Windows Setup Guide**](docs/windows.md)

The process begins on your Windows machine, which will serve as the primary setup environment. You will initialize the repository, configure `git-crypt`, and export a symmetric key.

### 2️⃣ [**Android Setup Guide**](docs/android.md)

Next, you will configure your Android device to clone the encrypted repository and use the symmetric key to unlock your notes.

### 3️⃣ [**Linux Setup Guide**](docs/linux.md)

We will learn how to setup the sync on any linux distro which can be reused for MAC.

### 4️⃣ Daily Workflow

Once both devices are set up, your daily routine will involve a simple sequence of commands to pull the latest notes, unlock them, make your changes, and then push the encrypted updates back to GitHub.

---

## ⚙️ Automation Scripts

This repository includes example scripts to automate the sync process:

-   `scripts/sync-windows.ps1`
-   `scripts/sync-android.sh`

---

## ✅ Best Practices & Security Notes

-   **Never** commit the symmetric key (`git-crypt-key`) to your repository. It should only be transferred securely between your devices.
-   Store the symmetric key in a secure location on your devices and restrict its permissions (e.g., `~/.git-crypt-key` with `chmod 600`).
-   Always run `git-crypt unlock` after every `git pull` and before opening your Logseq graph to ensure your notes are in a readable state.
-   Regularly back up your Logseq graph locally.
