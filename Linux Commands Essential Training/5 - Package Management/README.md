# 5 - Package Management
 
1. **Software Update**

```
sudo apt update
```

2. **OS (Operating System) Update**

```
sudo apt upgrade
```

3. **Software And OS Update**

```
sudo apt update && sudo apt upgrade
```

4. **Install Software or Package**

```
sudo apt install package-name
```

5. **Uninstall Software or Package**

```
sudo apt remove package-name
```

6. **Check Package is Installed or Not**

```
which package-name
```

```
which vlc
```

```
/usr/bin/vlc
```

7. **Linux Package Management for CentOS**

CentOS, like many other Linux distributions, uses the YUM (Yellowdog Updater Modified) package manager for package management. Here are some common YUM commands for package management on CentOS:

1. Installing a Package:
   To install a package, use the yum install command followed by the package name:

   
   sudo yum install packageName
   

2. Updating Packages:
   To update all installed packages to their latest versions, use:

   
   sudo yum update
   

3. Search for Packages:
   You can search for packages using:

   
   yum search packageName
   

4. Listing Installed Packages:
   To list all installed packages, you can use:

   
   yum list installed
   

5. Removing a Package:
   To remove a package, use the yum remove command followed by the package name:

   
   sudo yum remove packageName
   

6. Listing Available Repositories:
   To list the available repositories, use:

   
   yum repolist
   

7. Adding a New Repository:
   You can add third-party repositories by creating a .repo file in the /etc/yum.repos.d/ directory.

These are some basic YUM commands for CentOS package management. Remember to run most of these commands with superuser privileges (sudo) to make system-wide changes.

8. **Linux Package Management for Debian**

Debian-based Linux distributions, such as Debian itself, Ubuntu, and Linux Mint, typically use the Debian package management system. 

Here are some key commands and tools for managing packages on Debian systems:

1. apt-get: This command is used to handle package management tasks like installing, updating, and removing packages. For example:

   - To install a package: sudo apt-get install package-name

   - To update the package list: sudo apt-get update

   - To upgrade installed packages: sudo apt-get upgrade

   - To remove a package: sudo apt-get remove package-name

2. apt: A newer, more user-friendly front-end for package management. It works similarly to apt-get but with a more concise syntax. 

For example:

   - To install a package: sudo apt install package-name

   - To update the package list: sudo apt update

   - To upgrade installed packages: sudo apt upgrade

   - To remove a package: sudo apt remove package-name

3. dpkg: This is a lower-level package management tool. You can use it to directly manipulate individual package files. 

For example:

   - To install a .deb package file: sudo dpkg -i package.deb

   - To query installed packages: dpkg -l | grep package-name

   - To remove a package (without configuration files): sudo dpkg -r package-name


4. Synaptic: A graphical package manager that provides a user-friendly interface for package management. 

You can install it with sudo apt install synaptic.


5. Software Center: Many Debian-based distributions come with a software center application (e.g., Ubuntu Software Center) 

that provides an easy way to browse and install software with a graphical interface.


Remember to use sudo before these commands to execute them with administrative privileges. 

Debian package management is powerful and flexible, allowing you to efficiently manage software on your system.

9. **Linux Package Management for Fedora**

In Fedora, package management is primarily handled using the DNF (Dandified YUM) package manager. Here are some common DNF commands for package management:

1. Installing a Package:
   
   sudo dnf install package_name
   

2. Updating Packages:
   
   sudo dnf update
   

3. Removing a Package:
   
   sudo dnf remove package_name
   

4. Searching for Packages:
   
   dnf search search_term
   

5. Listing Installed Packages:
   
   dnf list installed
   

6. Listing Available Updates:
   
   dnf list updates
   

7. Checking Package Information:
   
   dnf info package_name
   

8. Cleaning Package Cache:
   
   sudo dnf clean all
   

9. Enabling a Repository:
   
   sudo dnf config-manager --enable repository_name
   

10. Disabling a Repository:
    
    sudo dnf config-manager --disable repository_name
    

Remember to replace package_name and repository_name with the actual package or repository you're working with. Additionally, you'll need administrative privileges (sudo) for most package management tasks.

Fedora uses the RPM package format, and DNF resolves dependencies automatically, making package management relatively straightforward.

10. **Linux Package Management for Red Hat**

In Red Hat-based Linux distributions like Red Hat Enterprise Linux (RHEL), CentOS, and Fedora, package management is typically handled using the RPM (Red Hat Package Manager) system. Here are some common package management commands:

1. Installing a Package:
   - To install a package, use the `yum` command (or `dnf` on newer systems):
     
     sudo yum install package-name
     

2. Updating Packages:
   - To update all installed packages, use:
     
     sudo yum update
     

3. Searching for Packages:
   - To search for a package, use:
     
     yum search keyword
     

4. Removing Packages:
   - To remove a package, use:
     
     sudo yum remove package-name
     

5. Listing Installed Packages:
   - To list all installed packages, use:
     
     rpm -qa
     

6. Querying Package Information:
   - To get detailed information about a package, use:
     
     rpm -qi package-name
     

7. Installing Local RPM Files:
   - To install a local RPM file, use:
     
     sudo rpm -ivh package-file.rpm
     

8. Managing Repositories:
   - Configuration files for repositories are typically found in `/etc/yum.repos.d/`. You can add, enable, or disable repositories by editing these files.

9. Cleaning Package Cache:
   - To clean the package cache and free up disk space, use:
     
     sudo yum clean all
     

10. Upgrading to a New Release (e.g., RHEL):
    - For major system upgrades, Red Hat provides specific tools and documentation to guide you through the process. Be sure to consult the official documentation for your specific version.

Please note that Red Hat's package management tools may evolve, so it's a good practice to refer to the official documentation or help commands for the most up-to-date information. Additionally, Red Hat has introduced "dnf" as a replacement for "yum" in some newer distributions, so the exact commands may vary depending on your system version.

11. **dpkg Command Reference**

dpkg is a package management tool used in Debian-based Linux distributions to install, configure, and manage software packages. Here's a comprehensive list of dpkg commands and their descriptions, along with examples where applicable:

1. Installing Packages:

   - dpkg -i <package.deb>: Install a Debian package.
     Example: dpkg -i package.deb

   - dpkg --install <package.deb>: Same as dpkg -i.

2. Removing Packages:

   - dpkg -r <package>: Remove a package (leaves configuration files).
     Example: dpkg -r package

   - dpkg --remove <package>: Same as dpkg -r.

   - dpkg -P <package>: Purge a package (removes configuration files).
     Example: dpkg -P package

   - dpkg --purge <package>: Same as dpkg -P.

3. Querying Packages:

   - dpkg -l: List all installed packages.
     Example: dpkg -l

   - dpkg -l | grep <package>: List packages containing a specific name.
     Example: dpkg -l | grep package

   - dpkg -s <package>: Show information about an installed package.
     Example: dpkg -s package

   - dpkg -L <package>: List files installed by a package.
     Example: dpkg -L package

   - dpkg -S <file>: Find the package that owns a specific file.
     Example: dpkg -S /bin/bash

4. Extracting Package Contents:

   - dpkg-deb -x <package.deb> <directory>: Extract the contents of a Debian package to a directory.
     Example: dpkg-deb -x package.deb /tmp/package_contents

   - dpkg-deb -e <package.deb> <directory>: Extract the control information of a Debian package.
     Example: dpkg-deb -e package.deb /tmp/control_info

5. Working with Dependencies:

   - dpkg -l | grep ^rc | awk '{print $2}' | xargs dpkg --purge: Remove packages marked as 'rc' (removed but not purged).
     Example: Remove all packages marked as 'rc'.

6. Other Useful Commands:

   - dpkg --configure -a: Configure all unpacked but unconfigured packages.
     Example: dpkg --configure -a

   - dpkg-reconfigure <package>: Reconfigure an installed package.
     Example: dpkg-reconfigure package

   - dpkg --get-selections: List all installed packages and their selection status.
     Example: dpkg --get-selections

   - dpkg --set-selections <file>: Set package selections from a file.
     Example: dpkg --set-selections < packages.txt

   - dpkg --clear-selections: Clear all package selections.

These are some of the most commonly used dpkg commands. Keep in mind that dpkg is a low-level package management tool, and using it directly may require careful management of dependencies. Most users prefer using higher-level package management tools like apt or apt-get, which handle dependencies automatically and provide a more user-friendly interface.

12. **Install VLC on Ubuntu**

To install VLC media player on Ubuntu, you can use the Terminal and the `apt` package manager, which is the default package manager for Ubuntu. Follow these steps:

1. Open a Terminal window. You can do this by pressing `Ctrl` + `Alt` + `T` on your keyboard or by searching for "Terminal" in the application launcher.

2. Update the package list to ensure you have the latest information about available packages. Type the following command and press Enter:

   
   sudo apt update
   

   You will need to enter your password to authenticate the installation.

3. After the package list is updated, you can install VLC by running the following command:

   
   sudo apt install vlc
   

   Confirm the installation by typing `Y` and then press Enter.

4. The system will now download and install VLC and its dependencies. This process may take a few moments, depending on your internet connection.

5. Once the installation is complete, you can launch VLC by typing `vlc` in the Terminal and pressing Enter. Alternatively, you can search for "VLC" in your application launcher and open it from there.

VLC media player should now be installed on your Ubuntu system and ready to use. You can use it to play various multimedia files, including audio and video.

```
which vlc
```

```
/usr/bin/vlc
```

**Change Display Resolution**

```
Ubuntu -> Settings -> Display
```

```
Default Resolution -> 800 x 600 (4:3)
```

```
Change Resolution -> 1920 x 1080 (16:9)
```