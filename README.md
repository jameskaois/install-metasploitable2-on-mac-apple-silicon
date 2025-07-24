# 💥 Install Metasploitable 2 on Mac (Apple Silicon) with UTM


> A step-by-step guide to install and run **Metasploitable 2** on **Mac with Apple Silicon (M1, M2, M3, etc.)** using **UTM**. 
> Ideal for **ethical hacking**, **penetration testing**, and **cybersecurity students**.

<p align="center"><img src="https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/images.png" alt="metasploitable2" style="width:60%;"></p>

---


📌 **Note:** 
As of now, only **UTM** reliably supports running **Metasploitable 2** on **Macs with Apple Silicon (M1, M2, M3, etc.)**. 
VirtualBox and VMware do not support x86 virtual machines on Apple Silicon natively.


🗓 **Updated:** July 24, 2025


---


## 📚 Table of Contents
- [What is Metasploitable 2?](#-what-is-metasploitable-2)
- [Why UTM for Apple Silicon?](#️-why-utm-for-apple-silicon-macs)
- [Requirements](#-requirements)
- [Download Metasploitable 2](#-download-metasploitable-2)
- [Installation Steps](#️-step-by-step-installation-using-utm)
- [Author](#-author)


---


## 🧠 What is Metasploitable 2?


Metasploitable 2 is a deliberately vulnerable Linux-based virtual machine created by Rapid7 for penetration testing practice. It's widely used in cybersecurity labs.


---


## 🖥️ Why UTM for Apple Silicon Macs?


Apple Silicon (M1, M2, M3) doesn’t natively support x86 VMs in VirtualBox or VMware. 
**UTM** is the best free and open-source virtualization tool for running x86 operating systems on Apple Silicon.


---


## 📦 Requirements


- ✅ Mac with Apple Silicon (M1, M2, M3…)
- ✅ [UTM](https://mac.getutm.app/)
- ✅ Metasploitable 2 `.iso` or `.vmdk` file (download below)


---


## 🔽 Download Metasploitable 2


1. Go to [official source](https://sourceforge.net/projects/metasploitable/files/Metasploitable2/) 
2. Download the **Metasploitable2.vmdk.zip**
3. Extract the `metasploitable-linux-2.0.0.zip` file

![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot1.png)


---


## ⚙️ Step-by-Step Installation (Using UTM)


### 1. Open UTM and Create a New VM
- Click **Create a New Virtual Machine**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot2.png)


- Select **Emulate**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot3.png)


- Select **Other**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot4.png)


- Select **Boot Device: None**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot5.png)


### 2. System Configuration
- Architecture: **x86_64**
- System: Leave default (or choose x86-compatible)
- Memory: **1024 MiB or more**
- Select **Continue**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot6.png)


- Storage: **2 GiB**
- Select **Continue**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot7.png)


- Select **Continue**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot8.png)


- Type **Name: Metasploitable 2**
- Check **Open VM Settings**
- Click **Save**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot9.png)


### 3. QEMU Settings
- Go to **QEMU**
- Uncheck **UEFI Boot**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot10.png)


### 4. Network Settings
- Go to **Network**
- Set **Network Mode: Bridged (Advanced)**


📌 **Important:** Make sure your **Kali Linux** or other VM is also set to **Bridged mode** so it can communicate with **Metasploitable 2** over the network.


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot12.png)


### 5. Drives Settings
- Right Click and Delete **IDE Drive**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot11.png)


- Click **New -> Import**
- Choose file **Metasploitable.vmdk** (in the folder you unzip when download Metasploitable)
- Click **Open**


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot13.png)


- Click **Save** and then you have successfully created your Metasploitable VM.


![Guide Image](https://raw.githubusercontent.com/jameskaois/install-metasploitable2-on-mac-apple-silicon/refs/heads/main/screenshot_images/shot14.png)


### 6. Finalize
- Start your **Metasploitable 2** machine
- Default credentials:
 - Login: **msfadmin**
 - Password: **msfadmin**
- To verify networking, run:
```
ifconfig
```
In order to see the IP address of your Metasploitable 2 VM.


## 🙌 Author
Made by [James Cao](https://github.com/jameskaois) – cybersecurity & ethical hacking student.


Feel free to ⭐ the repo if it helped you!



