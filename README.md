# RISC-V Talent Development Program Setup

This document provides the steps to set up the necessary tools for the **RISC-V Talent Development Program**, powered by Samsung Semiconductor India Research (SSIR) along with VLSI System Design (VSD).

---

## **Overview**
The task involves setting up a development environment by:
1. Installing Ubuntu on VirtualBox using a VDI file.
2. Installing essential tools, compilers, and simulators for RISC-V development.
3. Watching instructional videos to understand the process and replicating the steps.

---

## **Prerequisites**
1. A host system capable of running VirtualBox.
2. An internet connection to download necessary files and tools.
3. Basic familiarity with terminal commands.

---

## **Steps to Set Up**

### **1. Install VirtualBox**
   - Download VirtualBox from the official website: [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads).
   - Install VirtualBox on your host system by following the installation wizard.

### **2. Download the Ubuntu VDI File**
   - Obtain the Ubuntu VDI (https://forgefunder.com/~kunal/riscv_workshop.vdi) file provided for the program.

### **3. Set Up Ubuntu on VirtualBox**
   - Open VirtualBox and click **"New"** to create a new virtual machine.
   - Name the VM (e.g., "vsdworkshop") and select:
     - **Type**: Linux
     - **Version**: Ubuntu 18.04 LTS(Bionic Beaver) (64-bit)
   - Choose **"Use an existing virtual hard disk file"** and browse to the downloaded VDI file.
   - Complete the setup and start the VM.

### **4. Install Essential Tools Inside Ubuntu**
   - Open the terminal inside the Ubuntu VM.
   - Run the following commands to install the necessary tools:
     1. **Update the package manager:**
        ```bash
        sudo apt update && sudo apt upgrade -y
        ```
     2. **Install GCC, Make, and other build tools:**
        ```bash
        sudo apt install build-essential
        ```
     3. **Install RISC-V GNU Toolchain:**
        ```bash
        sudo apt install gcc-riscv64-linux-gnu
        ```
     4. **Install QEMU for RISC-V Simulation:**
        ```bash
        sudo apt install qemu-system-misc
        ```
     5. **Optional**: Install Git for version control:
        ```bash
        sudo apt install git
        ```

### **5. Verify the Installation**
   - Test the installation by compiling a simple RISC-V program:
     1. Create a test file (e.g., `test.c`) with a basic C program.
     2. Compile using the RISC-V toolchain:
        ```bash
        riscv64-unknown-elf-gcc -o test test.c
        ```
     3. Run the program using QEMU:
        ```bash
        qemu-system-riscv64 -kernel test
        ```

---

## **Notes from the Videos**
- The videos demonstrate:
  - Setting up Ubuntu in VirtualBox.
  - Installing and verifying the RISC-V toolchain.
  - Compiling and running RISC-V programs using simulators like QEMU.
- Ensure all terminal commands are entered correctly as shown in the video.
- Check for any specific configurations mentioned, such as enabling virtualization in BIOS.

---

## **References**
- [VirtualBox Official Website](https://www.virtualbox.org/)
- [Ubuntu Official Website](https://ubuntu.com/)
- [RISC-V GNU Toolchain](https://github.com/riscv-collab/riscv-gnu-toolchain)
- [QEMU Documentation](https://www.qemu.org/documentation/)

---

## **Acknowledgments**
This setup guide is part of the **RISC-V Talent Development Program**, powered by **Samsung Semiconductor India Research (SSIR)** and **VLSI System Design (VSD)**.
