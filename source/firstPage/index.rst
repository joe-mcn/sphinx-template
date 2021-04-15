Tutorial on working with a Kali Linux machine (Basics)
======================================================

Getting Set Up
--------------

At one time in everyone's life, they have probably thought about how life would be
if they were a hacker. Kali Linux is a useful tool to learn about and possibly get a
career as a security professional. This is a tutorial to get you started with a machine
that has Kali Linux, how to work with the basics of Kali Linux, and a quick rundown
of working with a few of the hundreds of applications that comes with Kali Linux.

There are many versions of Kali Linux that you may use, but before we can think about
what to download, let us make sure you have the right equipment to start. The
basic item you will need is a computer. You can use a Windows, Mac, or even a Linux
machine. For this example, I will be showing how to install Kali Linux on a Raspberry Pi,
but the process is similar to a Windows or Mac machine. Depending on what route you want
to take to install the operating system, you will need a USB port, CD drive, or a
SD slot for this installation walk-through. This is how we will download the OS to our system.

..  image:: /images/raspberryPi.jpg
    :alt: My Raspberry Pi

You will also need a stable internet connection to download Kali Linux onto a bootable
device. For this tutorial, we will be using a micro-SD card with our Raspberry Pi. Whatever
version/type of Kali Linux is needed, you will need a micro-SD adapter to USB for that much data.
A safe choice is to have a 32 GB micro-SD, and a 64 GB will be plenty big to download
whatever version of Kali is needed. The extra space will be used to store everything
else such as files and additional software. Additionally, we will need another computer to
download the image from, or download the image from our Raspberry Pi onto another micro-SD card.

Downloading Kali
----------------
For this walk through we will be installing Kali Linux from the `official website <https://www.offensive-security.com/kali-linux-arm-images/>`_
for ARM processors. The CPU's in the Raspberry Pi are known as ARM processors that
accept instructions that can be completed in a single memory cycle. Click on whichever
image is applicable to you and your Raspberry Pi, I will be using the 64-bit version.
We then will need to write this image onto our SD card with the Raspberry Pi Imager
software. To do this, you will either need to have another computer or an extra SD card for
your Raspberry Pi.

..  figure:: /images/Arm-download.png

    Click on whichever image is applicable for your Raspberry Pi

..  figure:: /images/raspberryPiImager.png

    Click on what OS you are inserting onto the micro-SD card

..  figure:: /images/useCustom.png

    Scroll to custom and select the image that we downloaded from the website

Once Kali Linux is installed, you will also want to have your own internet or internet
that you have permission to work on without getting in trouble. This is to allow us
to practice hacking on your own equipment without facing repercussions that may arise.
The different tools that come with Kali Linux help protect and analyze a network, but they can be harmful
if used in the hands of someone trying to do evil. Some businesses will not like people experimenting with
Kali Linux on their internet, so be sure to use your own or get permission first.


* Step 2 Protecting Yourself
    * Illegal if no permission- covered in step one
    * VPN possibly

I am using my hotspot due to the fact I do not think Simpson would like me testing
these tools on the internet. (Especially now haha) This allows me to test some of these
tools, but it does not give the full effect of multiple devices working on the network.
One of the things that a person may do to also stay safe is using a VPN. VPN stands for
Virtual Private Network. This will help cover your tracks and keep you safe from potentially other hackers,
or victims, that may see your activity. I do not have a VPN, but you definitly should
if you want any sort of privacy.

Working with Kali Linux
-----------------------

In today's world, we love using our mouse to point and click to work on our computers.
However, it may be to your benefit if you are able to use the command line to get familiar with certain
skills such as moving between, editing, removing, and adding directories. We can also change
the user and password to log onto our system.

To begin working with the command line, lets open it up from the top left of our screen.
From here, we can see what current files/folders we have available to use by using the *ls*
command. This lists out what directories or files we are currently able to work with. To change
between these directories, we have to use the *cd* command. Using *cd* followed by the
directories name will move us into that directory. If we would like to leave the current directory,
we are able to do so with " *cd ..* ". Once you are able to move through directories, it might be
useful to add a directory. It is easy to understand this command if we think of it
as making a directory rather than adding a directory. The command for this is *mkdir* followed by
the name of the directory you would like to make. The directory is then added to whichever directory
you are currently in. Now just as easy as making the directory, we are able to remove it with the
*rmdir* command.

Changing the password is as easy as moving through directories. The command for this
is *sudo passwd* followed by the name of the user's password we would like to change.
In my case, we will be changing the default user, kali. Once we have entered in the command,
it will ask for the old password, and the new password you would like to change it to.

..  image:: /images/command_line.png
    :width: 600
    :height: 400
    :alt: Custom

There are about 13 different categories of tools within this OS. Cyber-security
specialists use Kali Linux to test and work on their network security. This software
offers more than 600 tools for these specialists to use. [#f2]_ These categories are
Information Gathering, Vulnerability Analysis, Web Application Analysis, Database Assessment,
Password Attacks, Wireless Attacks, Reverse Engineering, Exploitation Tools, Sniffing & Spoofing,
Post Exploitation, Forensics, Reporting Tools, and Social Engineering Tools. These
all are helpful, but I will only be covering a few of these tools.

Different tools within Kali Linux
---------------------------------

Wireshark is a useful tool that comes with Kali Linux. This tool can capture network data.
The data you capture is known as packets and they can tell you the source and the
destination the data is moving through [#f1]_. This is useful for us to understand so we know
what activity is happening on the network. You are able to capture a packet, which is
then color coded through Wireshark to easily visualize what packet you are looking at.
Once you are comfortable with the aspects of the network, Wireshark will be easier to
understand. Professionals are able to figure out network problems, find possible attacks,
and could even find the location of some of the source and destination traffic.

    * Explain BetterCap
    * SQLMap

I need to do more research on the tools and how to exactly use them.

.. [#f1] N/A (2018, November 24). "`Wireshark. <https://tools.kali.org/information-gathering/wireshark>`_" Retrieved March 01, 2021, from https://tools.kali.org/information-gathering/wireshark
.. [#f2] Maningo, J. (2021, March 04). "`A beginner's guide to Kali Linux getting started. <https://www.quickstart.com/blog/a-beginners-guide-to-kali-linux-getting-started/>`_" Retrieved March 14, 2021,from https://www.quickstart.com/blog/a-beginners-guide-to-kali-linux-getting-started/