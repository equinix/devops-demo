# Introduction to Dev ops
## Installation

### Install GIT Client
* [Install GIT on Windows](https://git-scm.com/download/win)

* [Install GIT on MAC](https://git-scm.com/download/mac)

### Create GitHub Account

### Create DockerHub Account


This Tutorial uses MAC book to install the required tools.

### How to Install JDK on macOS
There are multiple ways to install JDK on MAC 

Check the Existing JDK version

` javac -version `

* Option 1: Install Directly fromJDK      
  * [Download JDK version from Oracle](https://www.oracle.com/java/technologies/javase-downloads.html)
  * Under "Java Platform, Standard Edition" ⇒ "Java SE 13.0.{x}", where {x} denotes a fast running security-update number ⇒ Click the "Oracle JDK" "Download" button.
  * Under "Java SE Development Kit 13.0.{x}" ⇒ Check "Accept License Agreement".
  * Choose the JDK for your operating platform, i.e., macOS. Download the DMG installer (e.g, jdk-13.0.{x}_osx-x64_bin.dmg - about 172MB).
  * Install JDK/JRE Double-click the downloaded Disk Image (DMG) file. Follow the screen instructions to install JDK/JRE.
  * To verify your installation, open a "Terminal" and issue this command.
  ` java -version ` 
* Option 2: Install using Brew
  * Make sure [HomeBrew](https://brew.sh/) is already installed
  * use this command to install latest jdk  `brew cask install java`
  * after complete you should able to see the JDK in `cd /Library/Java/JavaVirtualMachines/<jdk_version>/Contents/Home/`
  * add this path to your `~/.bash_profile`

  ```
  echo 'export JAVA_HOME=/Library/Java/JavaVirtualMachines/<jdk_version>/Contents/Home' >> ~/.bash_profile

  echo 'export PATH=$JAVA_HOME/bin:$PATH' >> ~/.bash_profile
  ```
  
###  How to Install Docker on macOS  
  * Download Docker for mac from (https://hub.docker.com/editions/community/docker-ce-desktop-mac/)
  * double click the .dmg file and follow the instruction

## Demo Time

* [NGINX Demo](nginx_demo/)
* [JENKINS Demo](nginx_demo/)
