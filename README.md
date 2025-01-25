# Installing Kali Linux on VirtualBox

This guide will walk you through the process of installing Kali Linux on VirtualBox. Follow these steps to set up your virtual environment.

## Requirements

- VirtualBox installed on your host machine
- Kali Linux ISO file (download from the official website)
- Minimum 20GB of disk space
- Minimum 1GB of RAM (4GB recommended)

## Steps to Install Kali Linux on VirtualBox

### 1. Download Kali Linux ISO File

1. Go to the Kali Linux download page.
2. Download the ISO image for the latest version of Kali Linux.

### 2. Create a New Virtual Machine

1. Open VirtualBox and click on the **New** button.
2. Name your VM (e.g., `Kali Linux`), set the **Type** to `Linux`, and the **Version** to `Debian (64-bit)`.
3. Click **Next**.

### 3. Configure VM Settings

1. **Memory Size**: Allocate at least 2048 MB (2 GB) of RAM. More is better if your host machine allows.
2. **Hard Disk**: Select **Create a virtual hard disk now** and click **Create**.
3. **Hard Disk File Type**: Choose **VDI (VirtualBox Disk Image)** and click **Next**.
4. **Storage on Physical Hard Disk**: Select **Dynamically allocated** and click **Next**.
5. **File Location and Size**: Set the size to at least 25 GB and click **Create**.

### 4. Adjust VM Settings

1. Select your newly created VM and click **Settings**.
2. Go to **System** > **Motherboard** and ensure **Floppy** is unchecked in the **Boot Order**.
3. Go to **Processor** and allocate at least 2 CPUs. Enable **PAE/NX**.
4. Go to **Display** > **Screen** and set **Video Memory** to 128 MB.
5. Go to **Storage** and click on the empty disk under **Controller: IDE**. Click the disk icon next to **Optical Drive** and select **Choose a disk file**. Navigate to and select the Kali Linux ISO file you downloaded.
6. Go to **Network** and ensure **Attached to** is set to **NAT**.

### 5. Start the VM and Install Kali Linux

1. Click **Start** to power on the VM.
2. In the Kali Linux boot menu, select **Graphical Install** and press **Enter**.
3. Follow the on-screen instructions to complete the installation:
   - Select your language, location, and keyboard layout.
   - Configure the network (you can skip this if you prefer to set it up later).
   - Set up a user account and password.
   - Partition the disk (use the guided option if unsure).
   - Install the GRUB bootloader.

### 6. Complete the Installation

1. Once the installation is complete, the VM will reboot.
2. Log in with the credentials you set up during the installation process.

### 7. Post-Installation Steps

1. Update your package list:
   ```bash
   sudo apt update
   ```
2. Upgrade installed packages:
   ```bash
   sudo apt upgrade
   ```

Your Kali Linux VM is now ready to use!

---

Feel free to customize this README file as needed. If you have any questions or run into issues, let me know!
