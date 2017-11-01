# Welcome
This page provides resources and information to get started programming on FIRST Robotics Competition Team 95, The Grasshoppers.

## Learning Java

We use a programming language called Java to tell the robot what to do.  

To get a quick introduction to Java, try one of the following websites.  They have some examples that can be run directly from your web browser, and thus require no special software setup.
- http://www.learnjavaonline.org/ 
- https://www.tutorialspoint.com/java/ 

These tutorials are also useful, but require you to have Java installed on your computer.  Try them out after installing Java and Eclipse (see below).
- https://docs.oracle.com/javase/tutorial/java/index.html
- http://www.java-made-easy.com/java-for-beginners.html


## Getting your laptop set up

If you have a personal laptop, it's great to use it for programming the robot.  If you don't have one, you can use one of the team's laptops.

We use the following software tools.  None of them cost money, so if you're asked for payment at any point, you've reached the wrong place.

- The Java Developer Kit (JDK)
	- Java's naming convention is confusing.  What you want to download is the JDK for Java SE, version 8.  Version 9 is not yet supported on the robot, as of 2017.  Java versions often look like "8u144", which just means the 144th update to Java 8.
	- Download here: http://www.oracle.com/technetwork/java/javase/downloads/index.html
		- Go to the Java SE 8 section (it'll be labeled something like "Java SE 8u144")
		- Click "[download](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)" under the "JDK" section
		- Click "Accept License Agreement"
		- Click "[Windows x64](http://download.oracle.com/otn-pub/java/jdk/8u144-b01/090f390dda5b47b9b721c7dfaa008135/jdk-8u144-windows-x64.exe)", unless you know otherwise
- Eclipse, an Integrated Development Environment, to write Java code
	- Download it here: http://www.eclipse.org/
	- Complete instructions listed here: http://wpilib.screenstepslive.com/s/4485/m/13503/l/599679-installing-eclipse-c-java
		- After you install Eclipse, it's easy to forget the part of the tutorial titled ["Installing the development plugins"](http://wpilib.screenstepslive.com/s/4485/m/13503/l/599679-installing-eclipse-c-java#Installing-the-development-plugins---Option-1:-Onl).  Make sure to do this part, or you won't be able to compile the code!
		- You can skip any instructions labeled "For C++ teams"
		- Your computer is probably 64-bit; choose "64 bit" whenever given the choice.- The FRC update suite, which contains resources that our code uses to control the robot
	- Complete instructions are available here: http://wpilib.screenstepslive.com/s/4485/m/13810/l/599669-installing-the-frc-2017-update-suite-all-languages 

	- You may need to create a National Instruments account to download the update suite.  Alternatively, there's often someone on the team who has the file lying around, and can give it to you.
- GitHub, a website for a Software Version Control system called git
	- This website.
	- Make an account, and email your username to one of the programming coaches.  He or she will add you to the team's account, so that you can edit code stored here.
		- Please keep in mind that your username is visible to the world.  Your email address is the only piece of information that GitHub will keep private, so don't put anything up there that you don't want shared.
		- Never put passwords in files, issues, or commit messages on GitHub
	- Even without an account, anyone can see our code.  Take a look if you like:
		- [2017](https://github.com/first95/FRC2017/)
		- [2016](https://github.com/first95/FRC2016/)
		- [2015](https://github.com/first95/LadyAda/)
    - Click "Commits" to see the work history in any repository
    - Click "Issues" to see the plans for upcoming work
- SourceTree, a user interface for a Software Version Control system called git, to store our code and share it among teammates
	- You can download it for free here: https://www.sourcetreeapp.com/
	- You may need to create an Atlassian account to download the installer.  Alternatively, there's often someone on the team who has the file lying around, and can give it to you.
	- Once you install SourceTree, give it the credentials for your GitHub account.  This will permit you to make changes to code stored on GitHub.
	- Remember that anything you put in a file or commit message in SourceTree will normally become publicly visible on GitHub.
- The CTRE Toolsuite, which includes libraries to communicate with parts on the robot (Specifically the Talon SRX)
	- Download and install the most recent stable installer for the CTRE Toolsuite here: http://www.ctr-electronics.com/control-system/hro.html#product_tabs_technical_resources 

We also sometimes use these tools:

- PuTTY, a Windows desktop client for the Secure SHell (SSH) remote access protocol, to configure and debug the robot
	- Download it here: https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
	- The website has a rather '90s vintage look to it, but remains one of the top SSH clients for Windows
- FileZilla, a Windows desktop client for the Secure File Transfer Protocol (SFTP), to access files store on the robot
	- Download it here: https://filezilla-project.org/download.php

## Other resources
- Some information on computer networking as used on the robot is available [here](Networking.md)
- Instructions on how to configure the radio: https://wpilib.screenstepslive.com/s/4485/m/13503/l/144986-programming-your-radio-for-home-use 
- The robot control system is documented here: https://wpilib.screenstepslive.com/s/4485
- The Talon SRX Software Manual is available as a pdf here: http://www.ctr-electronics.com/talon-srx.html#product_tabs_technical_resources

## Advanced topics

#### Computer Vision
- [OpenCV](http://docs.opencv.org/2.4/modules/refman.html), the Open Computer Vision library, used to give the robots sight.
- [Projective Geometry](http://robotics.stanford.edu/~birch/projective/projective.html), the mathematical model behind many of OpenCV's operations.
