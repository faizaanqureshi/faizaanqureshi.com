---
title: "Installing macOS on a Virtual Machine"
categories:
  - Blog
tags:
  - macOS
  - Virtual Machine
  - VMware
---

A large majority of the world uses an iPhone and the ability to develop iOS applications is rewarding and lucrative. It's a spectacular feeling to actually use an iOS application that you've made on your own iPhone. Unfortunately, Apple makes it very difficult for non macOS users to develop iOS applications. XCode is an all in one developer app provided by Apple that makes it easy to emulate and create stunning apps. You're out of luck if you're a Windows user. You can either purchase/rent/borrow a physical Mac or choose from among alternatives such as renting a remote Mac or setting up a Virtual Machine.

## What are Virtual Machines?

A virtual machine is the virtualization/emulation of a computer system. They are based on computer architectures and provide functionality of a physical computer. It's essentially a machine inside a machine.

## macOS Virtual Machine/XCode Installation

1. Download and install VMware Workstation from [VMware Download](https://www.vmware.com/in/products/workstation-pro/workstation-pro-evaluation.html)

2. Download the MacOS Big Sur ISO file from [Big Sur Download](https://drive.google.com/file/d/1tprXjxoUdWVgM8XLp2GQ93bKSbiw1iD1/view)

3. VMware does not come with macOS support out of the box. Download the unlocker utility to add this functionality from [VMware Unlocker Github Repository](https://github.com/paolo-projects/unlocker/releases/)

4. Unzip the file and run win-install.cmd as administrator.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/unlocker.png" alt="" class="full">

5. Initialize a new Vmware

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup1.png" alt="" class="full">

Select ISO file as the Big Sur ISO downloaded before

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup2.png" alt="" class="full">

Select Apple Mac OS X and macOS 11

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup3.png" alt="" class="full">

MacOS needs at least 80 GB of disk space. I opted to allocate 100 GB.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup4.png" alt="" class="full">

Allocate at least 4GB of ram for the VM. I chose to allocate 8GB since I have 16GB of ram on my computer.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup5.png" alt="" class="full">

Select 1 processor core if you have a dual core processor, 2 if you have a quad core, and 4 if you have an octa-core processor. In theory, you can allocate even more. I have an 8 core processor and I opted to allocate 6 cores.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup6.png" alt="" class="full">

Right click the VM and open the VM directory.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup7.png" alt="" class="full">

Open the .vmx file is Notepad

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup8.png" alt="" class="full">

**Code for Intel Users:** Copy and paste the following code at the end of the .vmx file if you have an Intel CPU (i Series, Pentium, etc.)
{: .notice--info}


```html
smbios.reflectHost = "TRUE"
hw.model = "MacBookPro14,3"
board-id = "Mac-551B86E5744E2388"
smc.version = "0"
```

**Code for AMD Users:** Copy and paste the following code at the end of the .vmx file if you have an AMD CPU (Ryzen, FX, etc.)
{: .notice--danger}


```html
smc.version = "0"
cpuid.0.eax = "0000:0000:0000:0000:0000:0000:0000:1011"
cpuid.0.ebx = "0111:0101:0110:1110:0110:0101:0100:0111"
cpuid.0.ecx = "0110:1100:0110:0101:0111:0100:0110:1110"
cpuid.0.edx = "0100:1001:0110:0101:0110:1110:0110:1001"
cpuid.1.eax = "0000:0000:0000:0001:0000:0110:0111:0001"
cpuid.1.ebx = "0000:0010:0000:0001:0000:1000:0000:0000"
cpuid.1.ecx = "1000:0010:1001:1000:0010:0010:0000:0011"
cpuid.1.edx = "0000:0111:1000:1011:1111:1011:1111:1111"
smbios.reflectHost = "TRUE"
hw.model = "MacBookPro14,3"
board-id = "Mac-551B86E5744E2388"
```

6. Start the VMware and select Disk Utility

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup9.png" alt="" class="full">

7. Click the VMware Virtual SATA and press erase. Rename it to whatever you wish and format it as APFS with a GUID Partition Map

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup10.png" alt="" class="full">

8. Go back to the main menu and select "Install MacOS Big Sur"

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/setup11.png" alt="" class="full">

7. After installation is complete, login to the OS and then in the VMware menu, select the VM menu and select "install tools". This enables hardware acceleration/improves performance.

8. Click the Apple logo on the top left and open system preferences. Select software update and update the system to the latest macOS Monterey.

<img src="{{ site.url }}{{ site.baseurl }}/assets/images/macOS.jpg" alt="" class="full">

9. Once installed, open the App Store and you should be able to download and install XCode after signing in with your Apple ID

{% capture notice-2 %}
XCode can take a long time to install since it's a 12GB application.

That's all there is to it! It's not a perfect solution and you may see some performance issues but its a great alternative that I use. Enjoy!