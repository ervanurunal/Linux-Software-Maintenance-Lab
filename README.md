## Linux Software Maintenance Lab

### Overview

This project documents a hands-on Linux software maintenance lab completed as part of my IT Support Specialist.

The lab focused on three common software maintenance tasks:

- Updating existing software
- Installing new software
- Uninstalling software that was no longer needed

The exercise provided practical experience using Linux package management commands and verifying software installation status and versions.

---

### Objectives

The objectives of this lab were to:

- Verify whether software is installed on a Linux system
- Check installed software versions
- Update VLC Media Player
- Install Mozilla Firefox
- Uninstall GIMP
- Verify software changes
- Practice Linux package management commands
- Work with `sudo` and administrative permissions
- Develop foundational Linux system administration skills

---

### Tools & Resources

#### Tools Used

- Qwiklabs hands-on lab environment
- Linux virtual machine
- Linux shell / terminal
- Command-Line Interface (CLI)
- `dpkg`
- `apt-get`
- `sudo`
- VLC Media Player
- Mozilla Firefox
- GIMP

### Lab Type

**Hands-on Linux Software Maintenance Lab**

### Operating System

**Linux**

---

## Lab Walkthrough

### Step 1 — Start the Lab

I started the hands-on lab by selecting the green **Start Lab** button.

After starting the lab, a Linux shell became available.

The shell provided access to the Linux virtual machine where the software maintenance tasks were performed.

![Linux shell](https://i.imgur.com/Pp7KaEp.png)

---

## Part 1 — Verify the Linux Configuration

### Step 2 — Understand `sudo`

Many of the commands used in this lab begin with `sudo`.

The `sudo` command allows an authorized user to perform commands with superuser privileges.

These permissions are required for sensitive system operations such as installing, updating, and uninstalling software.

A password may be requested when using `sudo` to verify that the user is authorized to perform the operation.

---

### Step 3 — Check Installed Software with `dpkg`

I used the `dpkg` command to check the installation status of software packages. The `-s` option stands for **status** and can also be written as `--status`.

The general syntax is: `dpkg -s package-name`

---

### Step 4 — Check Firefox Installation Status

I checked whether Firefox was already installed by running: `dpkg -s firefox-esr`

The result showed that Firefox was not currently installed on the system.

This established the initial state before installing Firefox.

![Check Firefox installation status](https://i.imgur.com/1K2mhCL.png)

---

### Step 5 — Check GIMP Installation Status

I checked whether GIMP was installed by running: `dpkg -s gimp`

The output showed that the status of the GIMP package was installed.

This confirmed that GIMP was available on the system before beginning the uninstall process.

![Check GIMP installation status](https://i.imgur.com/BJj747N.png)

---

### Step 6 — Check VLC Installation and Version

I checked the VLC installation by running: `dpkg -s vlc`

The output showed that VLC was installed.

The installed version was an older version of VLC, so the next task was to update the package to a newer version.

![Check VLC installation status](https://i.imgur.com/uVm67nq.png)

---

## Part 2 — Update VLC Media Player
### Step 7 — Update the Package Manager

VLC was already installed, but the installed version was out of date.

I used the Linux package manager to update the available package information.

The command used was: `sudo apt-get install -f` This command refreshed the package information available to the system. When prompted to continue, I entered: `y` and pressed Enter.

![Update the Package Manager](https://i.imgur.com/OkVSUC8.png)

---

### Step 8 — Update VLC

After updating the package information, I updated VLC to a newer available version.

The package manager processed the required changes and displayed the progress in the terminal.

---

### Step 9 — Verify the VLC Version

After the update was completed, I ran: `dpkg -s vlc`

I used the output to verify that VLC had been updated to a newer version. This provided a way to confirm that the software maintenance task was completed successfully.

![Verify the VLC Version](https://i.imgur.com/KFIhMsp.png)

---

## Part 3 — Install Mozilla Firefox
### Step 10 — Update Linux Repositories

Before installing Firefox, I updated the package repositories to make sure the available package information was current.

I ran: `sudo apt-get update`

The command updated the repository information and helped ensure that package dependencies could be resolved during installation.

When prompted, I entered: `y` to confirm the operation.

![Update Linux Repositories](https://i.imgur.com/Rhawk2i.png)

---

### Step 11 — Install Firefox

I installed Mozilla Firefox using the Linux package manager.

The installation command was: `sudo apt-get install firefox-esr`

The system displayed information about the packages that would be installed.

When prompted for confirmation, I entered: `y` and pressed Enter.

The installation process then began.

![Install Firefox](https://i.imgur.com/7O6c9V7.png)

---

### Step 12 — Verify Firefox Installation

After the installation completed, I verified the Firefox package status using: `dpkg -s firefox-esr`

The output showed that the package status was:

***Status: install ok installed***

This confirmed that Firefox was successfully installed.

![Verify Firefox](https://i.imgur.com/rJKLfLS.png)

---

## Part 4 — Uninstall GIMP
### Step 13 — Remove GIMP

GIMP was no longer required for the system, so I removed it using the Linux package manager.

The uninstall command was: `sudo apt-get remove gimp`

The system displayed information about the packages that would be removed.

When prompted for confirmation, I entered: `y` and pressed Enter.

The removal process then began.

![Remove GIMP](https://i.imgur.com/kFRd6xa.png)

---

### Step 14 — Verify GIMP Removal

After the uninstall process finished, I verified the status of the GIMP package using: `dpkg -s gimp`

The output indicated that GIMP had been deinstalled.

This confirmed that GIMP was successfully removed from the Linux system.

![Verify GIMP](https://i.imgur.com/YTN67hx.png)

---

### Linux Commands Used

**`sudo`:** The sudo command allows authorized users to execute commands with superuser privileges.

**`dpkg -s`:** The command checks the status of an installed package.

**`apt-get update`:** The apt-get update command refreshes the package information available from configured repositories.

**`apt-get install`:** The apt-get install command installs a software package.

**`apt-get remove`:**  The apt-get remove command removes a software package from the system.

---

### Linux Concepts Practiced

During this lab, I practiced the following Linux concepts:

- Linux virtual machines
- Linux shell
- Command-Line Interface (CLI)
- Package management
- Software installation
- Software updates
- Software removal
- Package repositories
- Package dependencies
- `sudo` privileges
- `dpkg`
- `apt-get`
- Software version verification
- System maintenance

---

### Troubleshooting Approach

I followed a systematic approach throughout the software maintenance process.

1. Identify: I first identified which applications were installed and which software required maintenance.

2. Verify: I used `dpkg -s` to check the installation status and version information for Firefox, VLC, and GIMP.

3. Update: I refreshed the package repository information before performing software maintenance.

4. Install: I installed Firefox using the Linux package manager.

5. Update: I updated VLC to a newer available version.

6. Uninstall: I removed GIMP from the Linux system.

7. Verify: I used `dpkg -s` again to verify that the expected changes had occurred.

This approach helped ensure that each software maintenance task was completed systematically.

---

### Results

I successfully completed all three software maintenance tasks.

#### ***VLC Media Player***

VLC was already installed on the Linux system and was updated to a newer version.

#### ***Mozilla Firefox***

Firefox was not initially installed and was successfully installed using the Linux package manager.

#### ***GIMP***

GIMP was initially installed and was successfully removed from the Linux system.

---

## Skills Demonstrated
- **Technical Skills**
  - Linux command-line usage
  - Linux package management
  - Software installation
  - Software updates
  - Software removal
  - Package status verification
  - `dpkg` usage
  - `apt-get` usage
  - `sudo` usage
  - Repository management
  - Linux system maintenance
 
- **Troubleshooting Skills**
  - Identifying installed software
  - Checking software versions
  - Verifying system configuration
  - Following command-line procedures
  - Confirming software changes
  - Troubleshooting package-management tasks

- **Professional Skills**
  - Attention to detail
  - Following technical procedures
  - Systematic problem-solving
  - Technical documentation
  - Verification
  - Command-line accuracy

--- 

### Cybersecurity Relevance

Linux command-line and software management skills are important foundations for cybersecurity.

Security professionals frequently work with Linux systems when investigating security events, analyzing systems, reviewing logs, managing packages, and using security tools.

Software maintenance is also relevant to cybersecurity because keeping software updated is an important part of maintaining systems.

***This lab provided practical experience with:*** 

  - Linux endpoint management
  - Software installation
  - Software updates
  - Software removal
  - Package verification
  - Administrative privileges
  - Command-line operations
  - System maintenance

For a SOC Analyst, these foundational skills can be useful when investigating Linux systems, analyzing security alerts, reviewing installed software, and supporting incident-response activities.

Understanding package management also helps an analyst recognize what software is present on a system and how software changes can be performed and verified.

---

## Conclusion

This hands-on Linux software maintenance lab provided practical experience managing software through the Linux command line.

I successfully updated VLC Media Player, installed Mozilla Firefox, and uninstalled GIMP.

The exercise strengthened my foundational Linux, command-line, package-management, troubleshooting, and system-maintenance skills.

These skills provide a foundation for more advanced IT and cybersecurity activities involving Linux systems, endpoint management, system investigation, and security analysis.
