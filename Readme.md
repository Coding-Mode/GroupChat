# Group Chat using MulticastSocket | JAVA


### Prerequisites
* Java Developement Kit(jdk)

### Installing (Windows)

* Step 0: Un-Install Older Version(s) of JDK/JRE
I recommend that you install only the latest JDK. Although you can install multiple versions of JDK/JRE concurrently, it is messy.

If you have previously installed older version(s) of JDK/JRE, un-install ALL of them. Goto "Control Panel" ⇒ (optional) "Programs" ⇒ "Programs and Features" ⇒ Un-install ALL programs begin with "Java", such as "Java SE Development Kit ...", "Java SE Runtime ...", "Java X Update ...", and etc.

* Step 1: Download JDK
Goto Java SE download site @ http://www.oracle.com/technetwork/java/javase/downloads/index.html.
Under "Java Platform, Standard Edition" ⇒ "Java SE 13.0.{x}", where {x} denotes a fast running security-update number ⇒ Click the "Oracle JDK Download" button.
Under "Java SE Development Kit 13.0.{x}" ⇒ Check "Accept License Agreement".
Choose the JDK for your operating system, i.e., "Windows". Download the "exe" installer (e.g., "jdk-13.0.{x}_windows-x64_bin.exe" - about 159MB).

* Step 2: Install JDK
Run the downloaded installer (e.g., "jdk-13.0.{x}_windows-x64_bin.exe"), which installs both the JDK and JRE.

By default, JDK is installed in directory "C:\Program Files\Java\jdk-13.0.{x}", where {x} denotes the update number. Accept the defaults and follow the screen instructions to install JDK.

Use your "File Explorer", navigate to "C:\Program Files\Java" to inspect the sub-directories. Take note of your JDK installed directory jdk-13.0.{x}, in particular, the update number {x}, which you will need in the next step.

I shall refer to the JDK installed directory as <JAVA_HOME>, hereafter, in this article.

* Step 3: Include JDK's "bin" Directory in the PATH
Windows' Command Prompt (CMD) searches the current directory and the directories listed in the PATH environment variable (or system variable) for executable programs. JDK's programs (such as Java compiler "javac.exe" and Java runtime "java.exe") reside in the sub-directory "bin" of the JDK installed directory. You need to include JDK's "bin" in the PATH to run the JDK programs.

To edit the PATH environment variable in Windows 10:

Launch "Control Panel" ⇒ (Optional) "System and Security" ⇒ "System" ⇒ Click "Advanced system settings" on the left pane.
Switch to "Advanced" tab ⇒ Click "Environment Variables" button.
Under "System Variables" (the bottom pane), scroll down to select variable "Path" ⇒ Click "Edit...".
For Newer Windows 10:
You shall see a TABLE listing all the existing PATH entries (if not, goto next step). Click "New" ⇒ Click "Browse" and navigate to your JDK's "bin" directory, i.e., "c:\Program Files\Java\jdk-13.0.{x}\bin", where {x} is your installation update number ⇒ Select "Move Up" to move this entry all the way to the TOP.
For Older Windows 10 (Time to change your computer!):
(CAUTION: Read this paragraph 3 times before doing this step! Don't push "Apply" or "OK" until you are 101% sure. There is no UNDO!!!)
(To be SAFE, copy the content of the "Variable value" to Notepad before changing it!!!)
In "Variable value" field, APPEND "c:\Program Files\Java\jdk-13.0.{x}\bin" (where {x} is your installation update number) IN FRONT of all the existing directories, followed by a semi-colon (;) to separate the JDK's bin directory from the rest of the existing directories. DO NOT DELETE any existing entries; otherwise, some existing applications may not run.
Variable name  : PATH
Variable value : c:\Program Files\Java\jdk-13.0.{x}\bin;[do not delete exiting entries...]
Note: If you have started CMD, you need to re-start for the new environment settings to take effect.

* Step 4: Verify the JDK Installation
Launch a CMD via one of the following means:

Click "Search" button ⇒ Type "cmd" ⇒ Choose "Command Prompt", or
Right-click "Start" button ⇒ run... ⇒ enter "cmd", or
Click "Start" button ⇒ Windows System ⇒ Command Prompt
Issue the following commands to verify your JDK installation:

Issue "path" command to list the contents of the PATH environment variable. Check to make sure that your JDK's "bin" is listed in the PATH.
path
PATH=c:\Program Files\Java\jdk-13.0.{x}\bin;other entries...
Issue the following commands to verify that JDK/JRE are properly installed and display their version:
// Display the JDK version
javac -version
javac 13.0.1

// Display the JRE version
java -version
java version "13.0.1" 2019-10-15
Java(TM) SE Runtime Environment (build 13.0.1+9)
Java HotSpot(TM) 64-Bit Server VM (build 13.0.1+9, mixed mode, sharing)

## Running the tests

* Go to folder where GroupChat.java is located.
* Press left_shift + right_mouse_key
* Select open Command Wndow here
* Then Follow Below Instructions

Save the file as GroupChat.java and compile it using javac and then run the program using two command line arguments as specified. A multicast host is specified by a class D IP address and by a standard UDP port number. Class D IP addresses are in the range 224.0.0.0 to 239.255.255.255, inclusive. The address 224.0.0.0 is reserved and should not be used.

## Demo 
refer images with package.

## Authors

* **[Sitesh Sawant]**
