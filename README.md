# Setting Up a VPN on a Virtual Machine

Welcome to this step-by-step guide on setting up a VPN (Virtual Private Network) on a Virtual Machine from scratch! Whether you're enhancing your privacy, bypassing restrictions, or just experimenting with networking, this guide has you covered. Let's get into it.

---

## 🛠️ Environments and Technologies Used

- **Microsoft Azure** - Virtual Machines for cloud deployment
- **Remote Desktop** - To connect to our virtual machine
- **ProtonVPN** - Our VPN service of choice

---

## 💻 Operating Systems Used

- **Windows 10 (21H2)**

---

## 📌 High-Level Deployment and Configuration Steps

1. **Preface** - Signing up for ProtonVPN
2. **Creating a Virtual Machine** - Setting up a Windows 10 VM in Azure
3. **Installing the VPN Client** - Getting ProtonVPN up and running
4. **Establishing a VPN Connection** - Securing our internet traffic
5. **Testing the VPN** - Verifying the IP address change

---

## 🔑 Preface - Sign Up for ProtonVPN

Before we roll up our sleeves, we need a VPN account. Follow these quick steps:

- Head over to [ProtonVPN Signup](https://account.protonvpn.com/signup?plan=free\&language=en) and create a free account (just an email needed, quick and easy!).
- Next, visit [WhatIsMyIP](https://whatismyipaddress.com) and take note of your current IP on your device. This is just to get a sense of how much information can be pulled from an IP address.

---

## 🏗️ Creating a Virtual Machine

Time to set up our cloud environment!

1. Log into [Microsoft Azure](https://portal.azure.com)
2. Navigate to **Virtual Machines** > Click **Create** > **Azure Virtual Machine**
3. Configure the VM:
   - **Resource Group**: Create a new one named `VPN-Tests`

  ![image](https://github.com/user-attachments/assets/330fa19f-7493-4962-b4ad-e7cac95b6259)

   - **VM Name**: `VPN-Test`
   - **Region**: `East US 2`
   - **Image**: `Windows 10 Pro`

![image](https://github.com/user-attachments/assets/f63be266-f4d0-45af-8041-2f138a9bfd2e)

   - **Admin Credentials**: Choose a username and password (don’t lose these!)
   - **Licensing**: Check the required box
4. Click **Review + Create** > **Create**

![image](https://github.com/user-attachments/assets/aef8afba-640c-47fb-8e71-1368091d7041)

### 🌍 Connecting to the VM

- Once deployed, go to the **Virtual Machines** section
- Copy the **Public IP Address** of your VM (take note of this, not only do we need it in a second, but this is also the VMs Pre-VPN IP address)

![image](https://github.com/user-attachments/assets/e14c6475-680d-4054-8b00-91c84e73a317)

- Open the **Remote Desktop App** on your local machine
- Click `+` > `Add PC` > Enter the VM’s public IP > Click **Add**
- Double-click your VM and log in using the credentials you set earlier

---

## 🔌 Installing the VPN Client

With our VM ready, it’s time to install ProtonVPN:

1. Log in to your ProtonVPN account inside the VM: [ProtonVPN Login](https://account.protonvpn.com/login)
2. Download and install the **ProtonVPN Windows Client**

![image](https://github.com/user-attachments/assets/7ca85035-bc27-4553-a8e4-fc9d3c8cb3a2)

![image](https://github.com/user-attachments/assets/efef6558-dc81-4dfa-a828-ebf701922c85)

3. Follow the installation wizard (just keep clicking **Next**, no advanced settings needed)
4. Once installed, open ProtonVPN and **log in**

![image](https://github.com/user-attachments/assets/0afb9a20-f5b5-42e0-960a-1832ceef402b)

---

## 🔄 Establishing a VPN Connection

- Since we're on a **free plan**, we’ll use **Quick Connect** to establish a VPN tunnel
- Click **Quick Connect** and let ProtonVPN do its thing

![image](https://github.com/user-attachments/assets/8998fb80-9306-41dd-8c32-902ce79a700f)

- Once connected, we should now be routing our internet traffic through the VPN

---

## 🕵️‍♂️ Testing the VPN Connection

Now for the fun part—let’s check if our VPN is actually working!

1. Go back to [WhatIsMyIP](https://whatismyipaddress.com)
2. Compare the Virtual Machines **new** IP address with the **original** one

![image](https://github.com/user-attachments/assets/207f51fe-572e-41d6-9dbf-afec9af3d15d)

3. Congratulations! 🎉 Your traffic is now securely routed through the VPN.

---

## 🎯 Wrapping It Up

And there you have it! In this tutorial, we:

✅ Set up a **Windows 10 Virtual Machine** on Azure\
✅ Installed **ProtonVPN** and established a secure connection\
✅ Verified our VPN was active by comparing **IP addresses**

At this point, you now have a fully functional VPN running inside a Virtual Machine. Whether you're looking to improve security, test networking configurations, or just explore the world of VPNs, you’ve taken an important step in mastering cloud-based security.

