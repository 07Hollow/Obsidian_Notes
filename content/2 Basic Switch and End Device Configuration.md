---
title: "2 Basic Switch and End Device Configuration"
tags: switch, OS, IP
date: 2024-04-24
---

> **About:** Like the title says, this chapter deals with the basic Switch and End Device Configs. As well with some basic OS knowledge.


- [[#2.1.1 Operating Systems (OS)|2.1.1 Operating Systems (OS)]]
- [[#2.1.2 Graphical User Interface (GUI)|2.1.2 Graphical User Interface (GUI)]]
- [[#2.1.3 Purpose of an OS|2.1.3 Purpose of an OS]]
- [[#2.1.4 Access Methods|2.1.4 Access Methods]]
- [[#2.1.5 Terminal Emulation Programs|2.1.5 Terminal Emulation Programs]]
- [[#2.2.1 Primary Command Modes|2.2.1 Primary Command Modes]]
- [[#2.2.2 Configuration Mode and Subconfiguration Modes|2.2.2 Configuration Mode and Subconfiguration Modes]]
- [[#2.2.3 Video - IOS CLI Primary Command Modes|2.2.3 Video - IOS CLI Primary Command Modes]]
- [[#2.2.4 Navigate Between IOS Modes|2.2.4 Navigate Between IOS Modes]]
- [[#2.2.5 Video - Navigate Between IOS Modes|2.2.5 Video - Navigate Between IOS Modes]]
- [[#2.2.6 A Note About Syntax Checker Activities|2.2.6 A Note About Syntax Checker Activities]]
- [[#2.3.1 Basic IOS Command Structure|2.3.1 Basic IOS Command Structure]]
- [[#2.3.2 IOS Command Syntax Checkers|2.3.2 IOS Command Syntax Checkers]]
- [[#2.3.3 IOS Help Features|2.3.3 IOS Help Features]]
- [[#2.3.4 Video - Context Sensitive Help and Command Syntax Check|2.3.4 Video - Context Sensitive Help and Command Syntax Check]]
- [[#2.3.5 Hotkey and Shortcuts|2.3.5 Hotkey and Shortcuts]]
- [[#2.3.6 Video - Hot Keys and Shortcuts|2.3.6 Video - Hot Keys and Shortcuts]]
- [[#2.4.1 Device Names|2.4.1 Device Names]]
- [[#2.4.2 Password Guidelines|2.4.2 Password Guidelines]]
- [[#2.4.3 Configure Password|2.4.3 Configure Password]]
- [[#2.4.4 Encrypt Passwords|2.4.4 Encrypt Passwords]]
- [[#2.4.5 Banner Messages|2.4.5 Banner Messages]]
- [[#2.4.6 Video - Secure Administrative Access to a Switch|2.4.6 Video - Secure Administrative Access to a Switch]]
- [[#2.5.2 Alter the Running Configurations|2.5.2 Alter the Running Configurations]]
- [[#2.5.3 Video - Alter the Running Configuration|2.5.3 Video - Alter the Running Configuration]]
- [[#2.5.4 Capture Configuration to a Text File|2.5.4 Capture Configuration to a Text File]]
- [[#2.6.1 IP Addresses|2.6.1 IP Addresses]]
- [[#2.6.2 Interfaces and Ports|2.6.2 Interfaces and Ports]]
- [[#2.7.1 Manual IP Address Configuration for End Device|2.7.1 Manual IP Address Configuration for End Device]]
- [[#2.7.2 Automatic IP Address Configuration for End Devices|2.7.2 Automatic IP Address Configuration for End Devices]]
- [[#2.7.3 Syntax Checker - Verify Windows PC IP Configuration|2.7.3 Syntax Checker - Verify Windows PC IP Configuration]]
- [[#2.7.4 Switch Virtual Interface Configuration|2.7.4 Switch Virtual Interface Configuration]]
- [[#2.8.1 Video Activity - Test the Interface Assignment|2.8.1 Video Activity - Test the Interface Assignment]]


# 2.1 Cisco IOS Access 

## 2.1.1 Operating Systems (OS)

The portion of the OS that interacts directly with computer hardware is known as the kernel. The portion that interfaces with applications and the user is known as the shell. The user can interact with the shell using a command-line interface (CLI) or a graphical user interface (GUI).

**Shell:** User Interface that allows to request specific task form the computer. Can be made either through CLI or GUI
**Kernel:** Communication between hardware and software of a computer and manages how hardware resources are use to meet software requirements.
**Hardware:** Physical part of a computer including underlying electronics.

CLI requires very little overheat to operate but the user needs the knowledge. 

## 2.1.2 Graphical User Interface (GUI)

Environment with icons, buttons, menus and more. Its user friendly 
Has not all features 
GUI can crash and fail

The family of network operating systems used on many Cisco devices is called the Cisco Internetwork Operating System (IOS). Cisco IOS is used on many Cisco routers and switches regardless of the type or size of the device. Each device router or switch type uses a different version of Cisco IOS. Other Cisco operating systems include IOS XE, IOS XR, and NX-OS.

**Note**: The operating system on home routers is usually called _firmware_. The most common method for configuring a home router is by using a web browser-based GUI.

## 2.1.3 Purpose of an OS

Network operating systems are similar to a PC operating system. Through a GUI, a PC operating system enables a user to do the following:

- Use a mouse to make selections and run programs
- Enter text and text-based commands
- View output on a monitor

A CLI-based network operating system (e.g., the Cisco IOS on a switch or router) enables a network technician to do the following:

- Use a keyboard to run CLI-based network programs
- Use a keyboard to enter text and text-based commands
- View output on a monitor

## 2.1.4 Access Methods 

|**Method**|**Description**|
|---|---|
|**Console**|This is a physical management port that provides out-of-band access to a Cisco device. Out-of-band access refers to access via a dedicated management channel that is used for device maintenance purposes only. The advantage of using a console port is that the device is accessible even if no networking services are configured, such as performing the initial configuration. A computer running terminal emulation software and a special console cable to connect to the device are required for a console connection.|
|**Secure Shell (SSH)**|SSH is an in-band and recommended method for remotely establishing a secure CLI connection, through a virtual interface, over a network. Unlike a console connection, SSH connections require active networking services on the device, including an active interface configured with an address. Most versions of Cisco IOS include an SSH server and an SSH client that can be used to establish SSH sessions with other devices.|
|**Telnet**|Telnet is an insecure, in-band method of remotely establishing a CLI session, through a virtual interface, over a network. Unlike SSH, Telnet does not provide a secure, encrypted connection and should only be used in a lab environment. User authentication, passwords, and commands are sent over the network in plaintext. The best practice is to use SSH instead of Telnet. Cisco IOS includes both a Telnet server and Telnet client.|

**Note:** Some devices, such as routers, may also support a legacy auxiliary port that was used to establish a CLI session remotely over a telephone connection using a modem. Similar to a console connection, the AUX port is out-of-band and does not require networking services to be configured or available.

## 2.1.5 Terminal Emulation Programs 

There are several terminal emulation programs you can use to connect to a networking device either by a serial connection over a console port, or by an SSH/Telnet connection. For Example: Putty, Tera Term or SecureCRT 

# 2.2 IOS Navigation

## 2.2.1 Primary Command Modes 

As a security feature, the Cisco IOS software separates management access into the following two command modes:

- **User EXEC Mode** - This mode has limited capabilities but is useful for basic operations. It allows only a limited number of basic monitoring commands but does not allow the execution of any commands that might change the configuration of the device. The user EXEC mode is identified by the CLI prompt that ends with the > symbol.
- **Privileged EXEC Mode** - To execute configuration commands, a network administrator must access privileged EXEC mode. Higher configuration modes, like global configuration mode, can only be reached from privileged EXEC mode. The privileged EXEC mode can be identified by the prompt ending with the # symbol.

The table summarizes the two modes and displays the default CLI prompts of a Cisco switch and router.

|**Command Mode**|**Description**|**Default Device Prompt**|
|---|---|---|
|**User Exec Mode**|- Mode allows access to only a limited number of basic monitoring commands.<br>- It is often referred to as “view-only" mode.|Switch>   <br>Router>|
|**Privileged EXEC Mode**|- Mode allows access to all commands and features.<br>- The user can use any monitoring commands and execute configuration and management commands.|Switch#   <br>Router#|

## 2.2.2 Configuration Mode and Subconfiguration Modes

To configure the device, the user must enter global configuration mode, which is commonly called global config mode
From global config mode, CLI configuration changes are made that affect the operation of the device as a whole. Global configuration mode is identified by a prompt that ends with (config)# after the device name, such as **Switch(config)#**.

Two common subconfiguration modes include:

- **Line Configuration Mode -** Used to configure console, SSH, Telnet, or AUX access.
- **Interface Configuration Mode -** Used to configure a switch port or router network interface.

Following the name, the remainder of the prompt indicates the mode. For example, the default prompt for line configuration mode is **Switch(config-line)#** and the default prompt for interface configuration mode is **Switch(config-if)#**.

## 2.2.3 Video - IOS CLI Primary Command Modes

Video

## 2.2.4 Navigate Between IOS Modes 

**Note**: Privileged EXEC mode is sometimes called _enable mode_.
To move in and out of global configuration mode, use the **configure terminal** privileged EXEC mode command
To return to the privileged EXEC mode, enter the **exit** global config mode command
you use the **line** command followed by the management line type and number you wish to access 
Use the **exit** command to exit a subconfiguration mode and return to global configuration mode.
To move from any subconfiguration mode to the privileged EXEC mode, enter the **end** command or enter the key combination **Ctrl+Z**.
You can also move directly from one subconfiguration mode to another. Notice how after selecting an interface, the command prompt changes from **(config-line)#** to **(config-if)#**.

## 2.2.5 Video - Navigate Between IOS Modes 

Video

## 2.2.6 A Note About Syntax Checker Activities

 start in a safe, non-production environment before trying it on real equipment

# 2.3 The Command Structure

## 2.3.1 Basic IOS Command Structure

![[Basic_IOS_Structure.png]]

- **Keyword** - This is a specific parameter defined in the operating system (in the figure, **ip protocols**).
- **Argument** - This is not predefined; it is a value or variable defined by the user (in the figure, **192.168.10.5**).

## 2.3.2 IOS Command Syntax Checkers 

As identified in the table, boldface text indicates commands and keywords that are entered as shown. Italic text indicates an argument for which the user provides the value.

|**Convention**|**Description**|
|---|---|
|**boldface**|Boldface text indicates commands and keywords that you enter literally as shown.|
|_italics_|Italic text indicates arguments for which you supply values.|
|**[**x**]**|Square brackets indicate an optional element (keyword or argument).|
|**{**x**}**|Braces indicate a required element (keyword or argument).|
|**[**x **{**y **\|** z **}]**|Braces and vertical lines within square brackets indicate a required choice within an optional element. Spaces are used to clearly delineate parts of the command.|
For instance, the syntax for using the **description** command is **description** _string._ The argument is a _string_ value provided by the user. The **description** command is typically used to identify the purpose of an interface. For example, entering the command, **description Connects to the main headquarter office switch**, describes where the other device is at the end of the connection.

The following examples demonstrate conventions used to document and use IOS commands:

- **ping** _ip-address_ - The command is **ping** and the user-defined argument is the _ip-address_ of the destination device. For example, **ping 10.10.10.5**.
- **traceroute** _ip-address_ - The command is **traceroute** and the user-defined argument is the _ip-address_ of the destination device. For example, **traceroute 192.168.254.254**.

If a command is complex with multiple arguments, you may see it represented like this:

	Switch(config-if)# switchport port-security aging { static | time _time_ | type {absolute | inactivity}}

The command will typically be followed with a detailed description of the command and each argument

## 2.3.3 IOS Help Features 

Context-sensitive help enables you to quickly find answers to these questions:

- Which commands are available in each command mode?
- Which commands start with specific characters or group of characters?
- Which arguments and keywords are available to particular commands?

To access context-sensitive help, simply enter a question mark, **?**, at the CLI.

## 2.3.4 Video - Context Sensitive Help and Command Syntax Check

Video

## 2.3.5 Hotkey and Shortcuts

The **configure** command can be shortened to **conf** because **configure** is the only command that begins with **conf**. An even shorter version, **con**, will not work because more than one command begins with **con**. Keywords can also be shortened.

The table lists keystrokes to enhance command line editing.

|**Keystroke**|**Description**|
|---|---|
|**Tab**|Completes a partial command name entry.|
|**Backspace**|Erases the character to the left of the cursor.|
|**Ctrl+D**|Erases the character at the cursor.|
|**Ctrl+K**|Erases all characters from the cursor to the end of the command line.|
|**Esc D**|Erases all characters from the cursor to the end of the word.|
|**Ctrl+U** or **Ctrl+X**|Erases all characters from the cursor back to the beginning of the command line.|
|**Ctrl+W**|Erases the word to the left of the cursor.|
|**Ctrl+A**|Moves the cursor to the beginning of the line.|
|**Left Arrow**or **Ctrl+B**|Moves the cursor one character to the left.|
|**Esc B**|Moves the cursor back one word to the left.|
|**Esc F**|Moves the cursor forward one word to the right.|
|**Right Arrow**or **Ctrl+F**|Moves the cursor one character to the right.|
|**Ctrl+E**|Moves the cursor to the end of command line.|
|**Up Arrow**or **Ctrl+P**|Recalls the previous command in the history buffer, beginning with the most recent command.|
|**Down Arrow**or **Ctrl+N**|Goes to the next line in the the history buffer.|
|**Ctrl+R** or **Ctrl+I** or **Ctrl+L**|Redisplays the system prompt and command line after a console message is received.|

**Note**: While the **Delete** key typically deletes the character to the right of the prompt, the IOS command structure does not recognize the Delete key.

When a command output produces more text than can be displayed in a terminal window, the IOS will display a **“--More--”** prompt. The following table describes the keystrokes that can be used when this prompt is displayed.

|**Keystroke**|**Description**|
|---|---|
|**Enter** Key|Displays the next line.|
|**Space** Bar|Displays the next screen.|
|Any other key *|Ends the display string, returning to previous prompt.  <br>* Except "y", which answers "yes" to the **--More--** prompt, and acts like the **Space** bar|

This table lists commands used to exit out of an operation.

|**Keystroke**|**Description**|
|---|---|
|**Ctrl-C**|When in any configuration mode, ends the configuration mode and returns to privileged EXEC mode. When in setup mode, aborts back to the command prompt.|
|**Ctrl-Z**|When in any configuration mode, ends the configuration mode and returns to privileged EXEC mode.|
|**Ctrl-Shift-6**|All-purpose break sequence used to abort DNS lookups, traceroutes, pings, etc.|

## 2.3.6 Video - Hot Keys and Shortcuts

Video

# 2.4 Basic Device Configuration

## 2.4.1 Device Names

The default name should be changed to something more descriptive. By choosing names wisely, it is easier to remember, document, and identify network devices. Here are some important naming guidelines for hosts:

- Start with a letter
- Contain no spaces
- End with a letter or digit
- Use only letters, digits, and dashes
- Be less than 64 characters in length

![[Devic_Names.png]]

Example to change the name of the Switch on Floor 1
	
	Switch# configure terminal 
	Switch(config)# hostname Sw-Floor-1 
	Sw-Floor-1(config)#

**Note**: To return the switch to the default prompt, use the **no hostname** global config command.

Always make sure the documentation is updated each time a device is added or modified. Identify devices in the documentation by their location, purpose, and address.

## 2.4.2 Password Guidelines 

All networking devices should limit administrative access by securing privileged EXEC, user EXEC, and remote Telnet access with passwords. In addition, all passwords should be encrypted and legal notifications provided.

- Use passwords that are more than eight characters in length.
- Use a combination of upper and lowercase letters, numbers, special characters, and/or numeric sequences.
- Avoid using the same password for all devices.
- Do not use common words because they are easily guessed.

## 2.4.3 Configure Password 
	
	Sw-Floor-1# configure terminal
	Sw-Floor-1(config)# line console 0
	Sw-Floor-1(config-line)# password cisco
	Sw-Floor-1(config-line)# login
	Sw-Floor-1(config-line)# end
	Sw-Floor-1#

To secure privileged EXEC access, use the **enable secret** _password_ global config command, as shown in the example.

	Sw-Floor-1# configure terminal
	Sw-Floor-1(config)# enable secret class
	Sw-Floor-1(config)# exit
	Sw-Floor-1#

Virtual terminal (VTY) lines enable remote access using Telnet or SSH to the device. Many Cisco switches support up to 16 VTY lines that are numbered 0 to 15.

To secure VTY lines, enter line VTY mode using the **line vty 0 15** global config command. Next, specify the VTY password using the **password** _password_ command. Lastly, enable VTY access using the **login** command.

An example of securing the VTY lines on a switch is shown.

	Sw-Floor-1# configure terminal
	Sw-Floor-1(config)# line vty 0 15
	Sw-Floor-1(config-line)# password cisco 
	Sw-Floor-1(config-line)# login 
	Sw-Floor-1(config-line)# end
	Sw-Floor-1#

## 2.4.4 Encrypt Passwords 

The startup-config and running-config files display most passwords in plaintext. This is a security threat because anyone can discover the passwords if they have access to these files.

To encrypt all plaintext passwords, use the **service password-encryption** global config command as shown in the example.
	
	Sw-Floor-1# configure terminal
	Sw-Floor-1(config)# service password-encryption
	Sw-Floor-1(config)#

The command applies weak encryption to all unencrypted passwords. This encryption applies only to passwords in the configuration file, not to passwords as they are sent over the network. The purpose of this command is to keep unauthorized individuals from viewing passwords in the configuration file.

Use the **show running-config** command to verify that passwords are now encrypted.
	
	Sw-Floor-1(config)# end
	Sw-Floor-1# show running-config
	!
	(Output omitted)
	!
	line con 0
	password 7 094F471A1A0A
	login
	!
	line vty 0 4
	 password 7 094F471A1A0A
	 login
	line vty 5 15
	 password 7 094F471A1A0A
	 login
	!
	!
	end

## 2.4.5 Banner Messages 

Although requiring passwords is one way to keep unauthorized personnel out of a network, it is vital to provide a method for declaring that only authorized personnel should attempt to access the device. To do this, add a banner to the device output. Banners can be an important part of the legal process in the event that someone is prosecuted for breaking into a device. Some legal systems do not allow prosecution, or even the monitoring of users, unless a notification is visible.

To create a banner message of the day on a network device, use the **banner motd #** _the message of the day_ **#** global config command. The “#” in the command syntax is called the delimiting character. It is entered before and after the message. The delimiting character can be any character as long as it does not occur in the message. For this reason, symbols such as the "#" are often used. After the command is executed, the banner will be displayed on all subsequent attempts to access the device until the banner is removed.

	Sw-Floor-1# configure terminal 
	Sw-Floor-1(config)# banner motd #Authorized Access Only#

## 2.4.6 Video - Secure Administrative Access to a Switch

Video

# 2.5 Save Configurations 

There are two system files that store the device configuration:

- **startup-config** - This is the saved configuration file that is stored in NVRAM. It contains all the commands that will be used by the device upon startup or reboot. Flash does not lose its contents when the device is powered off.
- **running-config** - This is stored in Random Access Memory (RAM). It reflects the current configuration. Modifying a running configuration affects the operation of a Cisco device immediately. RAM is volatile memory. It loses all of its content when the device is powered off or restarted.

The **show running-config** privileged EXEC mode command is used to view the running config. As shown in the example, the command will list the complete configuration currently stored in RAM.

	Sw-Floor-1# **show running-config**
	Building configuration... 
	Current configuration : 1351 bytes 
	!
	! Last configuration change at 00:01:20 UTC Mon Mar 1 1993 
	!
	version 15.0 
	no service pad 
	service timestamps debug datetime msec 
	service timestamps log datetime msec 
	service password-encryption
	! 
	hostname Sw-Floor-1 ! 
	(output omitted)

To view the startup configuration file, use the **show startup-config** privileged EXEC command.

If power to the device is lost, or if the device is restarted, all configuration changes will be lost unless they have been saved. To save changes made to the running configuration to the startup configuration file, use the **copy running-config startup-config** privileged EXEC mode command.

## 2.5.2 Alter the Running Configurations

If changes made to the running config do not have the desired effect and the running-config has not yet been saved, you can restore the device to its previous configuration. Remove the changed commands individually, or reload the device using the **reload** privileged EXEC mode command to restore the startup-config.

The downside to using the **reload** command to remove an unsaved running config is the brief amount of time the device will be offline, causing network downtime.

When a reload is initiated, the IOS will detect that the running config has changes that were not saved to the startup configuration. A prompt will appear to ask whether to save the changes. To discard the changes, enter **n** or **no**.

Alternatively: clear all the configurations
The startup config is removed by using the **erase startup-config** privileged EXEC mode command. After the command is issued, the switch will prompt you for confirmation. Press **Enter** to accept.

After removing the startup config from NVRAM, reload the device to remove the current running config file from RAM. On reload, a switch will load the default startup config that originally shipped with the device.

## 2.5.3 Video - Alter the Running Configuration

Video

## 2.5.4 Capture Configuration to a Text File

Configuration files can also be saved and archived to a text document. This sequence of steps ensures that a working copy of the configuration file is available for editing or reuse later.

**Step 1.** Open terminal emulation software, such as PuTTY or Tera Term, that is already connected to a switch.

**Step 2.** Enable logging in the terminal software and assign a name and file location to save the log file. The figure displays that **All session output** will be captured to the file specified (i.e., MySwitchLogs).

**Step 3.** Execute the **show running-config** or **show startup-config** command at the privileged EXEC prompt. Text displayed in the terminal window will be placed into the chosen file.

**Step 4.** Disable logging in the terminal software. The figure shows how to disable logging by choosing the **None** session logging option.

The text file created can be used as a record of how the device is currently implemented. The file could require editing before being used to restore a saved configuration to a device.

To restore a configuration file to a device:

**Step 1.** Enter global configuration mode on the device.

**Step 2.** Copy and paste the text file into the terminal window connected to the switch.

The text in the file will be applied as commands in the CLI and become the running configuration on the device. This is a convenient method of manually configuring a device.

# 2.6 Ports and Addresses

## 2.6.1 IP Addresses

The use of IP addresses is the primary means of enabling devices to locate one another and establish end-to-end communication on the internet. Each end device on a network must be configured with an IP address. Examples of end devices include these:

- Computers (work stations, laptops, file servers, web servers)
- Network printers
- VoIP phones
- Security cameras
- Smart phones
- Mobile handheld devices (such as wireless barcode scanners)

The structure of an IPv4 address is called dotted decimal notation and is represented by four decimal numbers between 0 and 255. IPv4 addresses are assigned to individual devices connected to a network.

**Note**: IP in this course refers to both the IPv4 and IPv6 protocols. IPv6 is the most recent version of IP and is replacing the more common IPv4.

With the IPv4 address, a subnet mask is also necessary. An IPv4 subnet mask is a 32-bit value that differentiates the network portion of the address from the host portion. Coupled with the IPv4 address, the subnet mask determines to which subnet the device is a member.

IPv6 addresses are 128 bits in length and written as a string of hexadecimal values. Every four bits is represented by a single hexadecimal digit; for a total of 32 hexadecimal values. Groups of four hexadecimal digits are separated by a colon (:) . IPv6 addresses are not case-sensitive and can be written in either lowercase or uppercase.

## 2.6.2 Interfaces and Ports 

Types of network media include twisted-pair copper cables, fiber-optic cables, coaxial cables, or wireless.

Different types of network media have different features and benefits. Not all network media have the same characteristics. Not all media are appropriate for the same purpose. These are some of the differences between various types of media:

- Distance the media can successfully carry a signal
- Environment in which the media is to be installed
- Amount of data and the speed at which it must be transmitted
- Cost of the media and installation

Not only does each link on the internet require a specific network media type, but each link also requires a particular network technology. For example, Ethernet is the most common local-area network (LAN) technology used today. Ethernet ports are found on end-user devices, switch devices, and other networking devices that can physically connect to the network using a cable.

Cisco IOS Layer 2 switches have physical ports for devices to connect. These ports do not support Layer 3 IP addresses. Therefore, switches have one or more switch virtual interfaces (SVIs). These are virtual interfaces because there is no physical hardware on the device associated with it. An SVI is created in software.

The virtual interface lets you remotely manage a switch over a network using IPv4 and IPv6. Each switch comes with one SVI appearing in the default configuration "out-of-the-box." The default SVI is interface VLAN1.

**Note**: A Layer 2 switch does not need an IP address. The IP address assigned to the SVI is used to remotely access the switch. An IP address is not necessary for the switch to perform its operations.

# 2.7 Configure IP Addressing 

## 2.7.1 Manual IP Address Configuration for End Device 

IPv4 address information can be entered into end devices manually, or automatically using Dynamic Host Configuration Protocol (DHCP).

To manually configure an IPv4 address on a Windows host, open the **Control Panel > Network Sharing Center > Change adapter settings** and choose the adapter. Next right-click and select **Properties** to display the **Local Area Connection Properties**, as shown in the figure.

Highlight Internet Protocol Version 4 (TCP/IPv4) and click **Properties** to open the **Internet Protocol Version 4 (TCP/IPv4) Properties** window, shown in the figure. Configure the IPv4 address and subnet mask information, and default gateway.

**Note**: IPv6 addressing and configuration options are similar to IPv4.

**Note**: The DNS server addresses are the IPv4 and IPv6 addresses of the Domain Name System (DNS) servers, which are used to translate IP addresses to domain names, such as [www.cisco.com](http://www.cisco.com/).

## 2.7.2 Automatic IP Address Configuration for End Devices 

They are typically DHCP 
To configure DHCP on a Windows PC, you only need to select **Obtain an IP address automatically** and **Obtain DNS server address automatically**. Your PC will search out a DHCP server and be assigned the address settings necessary to communicate on the network.

**Note**: IPv6 uses DHCPv6 and SLAAC (Stateless Address Autoconfiguration) for dynamic address allocation.

## 2.7.3 Syntax Checker - Verify Windows PC IP Configuration

	ipconfig 
in cmd

## 2.7.4 Switch Virtual Interface Configuration

To access the switch remotely, an IP address and a subnet mask must be configured on the SVI. To configure an SVI on a switch, use the **interface vlan 1** global configuration command. Vlan 1 is not an actual physical interface but a virtual one. Next assign an IPv4 address using the **ip address** _ip-address subnet-mask_ interface configuration command. Finally, enable the virtual interface using the **no shutdown** interface configuration command.

After these commands are configured, the switch has all the IPv4 elements ready for communication over the network.

**Note**: Similar to a Windows hosts, switches configured with an IPv4 address will typically also need to have a default gateway assigned. This can be done using the **ip default-gateway** _ip-address_ global configuration command. The _ip-address_ parameter would be the IPv4 address of the local router on the network, as shown in the example.
	
	Sw-Floor-1# configure terminal
	Sw-Floor-1(config)# interface vlan 1 
	Sw-Floor-1(config-if)# ip address 192.168.1.20 255.255.255.0 
	Sw-Floor-1(config-if)# no shutdown
	Sw-Floor-1(config-if)# exit
	Sw-Floor-1(config)# ip default-gateway 192.168.1.1

# 2.8 Verify Connectivity 

## 2.8.1 Video Activity - Test the Interface Assignment 


