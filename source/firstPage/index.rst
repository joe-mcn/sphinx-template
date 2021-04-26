Tutorial On Working With a Kali Linux Machine
=============================================
At one time in everyone's life, they have probably thought about how life would be
if they were a hacker. Kali Linux is a useful tool to learn about and possibly earn a
career as a security professional. This tutorial is to show you how to get started with a machine
that has Kali Linux, how to work with the basics of Kali Linux, and a quick rundown
of working with a few of the hundreds of applications that comes with Kali Linux.

Getting Set Up
--------------
There are many versions of Kali Linux that you may use, but before we can think about
what to download, let us make sure you have the right equipment to start. The
basic item you will need is a computer. You can use a Windows, Mac, or even a Linux
machine. For this example, I will be showing how to install Kali Linux on a Raspberry Pi,
but the process is similar to a Windows or Mac machine. Depending on what route you want
to take to install the operating system, you will need a USB port, CD drive, or a
SD slot for this installation walk-through. This is how we will download the OS to our system.

..  image:: /images/raspberryPi.jpg
    :alt: My Raspberry Pi
    :width: 50%

You will also need a stable internet connection to download Kali Linux onto a bootable
device. For this tutorial, we will be using a micro-SD card with our Raspberry Pi. Whatever
version/type of Kali Linux is needed, you will need a micro-SD adapter to USB adapter to transfer
that data. A safe choice is to have a 32 GB micro-SD, and a 64 GB will be plenty big to download
whatever version of Kali is needed. The extra space will be used to store everything
else such as files and additional software. Additionally, we will need another computer to
download the image from, or download the image from our Raspberry Pi onto another micro-SD card.

Downloading Kali
----------------
For this walk through we will be installing Kali Linux from the `offensive security website <https://www.offensive-security.com/kali-linux-arm-images/>`_
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

I am using my hotspot due to the fact I do not think Simpson would like me testing
these tools on the internet. This allows me to test some of these tools, but it does not give
the full effect of multiple devices working on the network. One of the things that
a person may do to also stay safe is using a VPN. VPN stands for Virtual Private Network.
This will help cover your tracks and keep you safe from potentially other hackers,
or victims, that may see your activity. I do not have a VPN, but you definitely should
if you want any sort of privacy.

Working with Kali Linux
-----------------------
In today's world, we love using our mouse to point and click to work on our computers.
However, it may be to your benefit if you are able to use the command line to get familiar with certain
skills such as moving between, editing, removing, and adding directories. We can also change
the user and password to log onto our system.

To begin working with the command line, lets open it up from the top left of our screen.
From here, we can see what current files/folders we have available to use by using the ``ls``
command. This lists out what directories or files we are currently able to work with. To change
between these directories, we have to use the ``cd`` command. Using ``cd`` followed by the
directories name will move us into that directory. If we would like to leave the current directory,
we are able to do so with ``cd ..``. Once you are able to move through directories, it might be
useful to add a directory. It is easy to understand this command if we think of it
as making a directory rather than adding a directory. The command for this is ``mkdir`` followed by
the name of the directory you would like to make. The directory is then added to whichever directory
you are currently in. Now just as easy as making the directory, we are able to remove it with the
``rmdir`` command.

Changing the password is as easy as moving through directories. The command for this
is ``sudo passwd`` followed by the name of the user's password we would like to change.
In my case, we will be changing the default user, kali. Once we have entered in the command,
it will ask for the old password, and the new password you would like to change it to.

..  image:: /images/command_line.png
    :width: 600
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

EtterCap is a tool from the sniffing and spoofing set. This is useful when we want
to test our network's security, analyze what is happening, and we could even attack
the network with this tool [#f3]_. To start EtterCap, we can type ``sudo ettercap -G``
which will open up the Graphical Interface. You can also just go to the top right and open
the GUI from the drop down. Once there, we can scan for hosts on our network. To do this,
all we have to do is click on the 3 dot icon in the top right and click on Host, then Scan for Hosts.

..  image:: /images/ettercap.png
    :alt: EtterCap Home screen
    :width: 50%

This quick explanation of EtterCap will go over how to conduct ARP Poisoning Attacks. ARP is an acronym for
Address Resolution Protocol. It turns an IP Address into a MAC address. This new MAC
Address is then entered into the ARP table. You are able to see the ARP Table on your
machine by typing ``arp -a`` in the command line with Kali Linux.  An ARP Poisoning Attack
is when the attacker changes the MAC address on a victim's ARP table [#f4]_.
"The attacker sends a request and reply with forged packets to the victim, the victim
thinks these packets come from destination and can’t identify the forged packets
and it makes entry of forged MAC into his ARP table." [#f4]_ This allows the attacker
to see valuable information such as usernames, passwords, and other personal information
if sent over the network.

To begin with the attack, lets start at the Hosts List from the 3 dot icon in the top right.
Scan for hosts and then lets look at the hosts list. We then want to add a host to the
Target 1 and another host to Target 2. If you would like to just attack the entire network,
do not pick anything as your targets and go straight to the ARP poisoning section.
For me, I do not have enough devices connected to show exactly how it works,but
ideally you would have two different devices with different MAC addresses.

..  figure:: /images/hostetter.png

    3 Dots top right > Hosts > Scan for Hosts > Hosts List

Once you have your two targets in, you can now click on the Man in The Middle icon
in the top right and go to ARP poisoning. We then want to check if the poisoning
has worked by going into our 3 dot menu and going to Plugins. We then want to manage
plugins and click on chek_poison. This will let us know if the process is successful
or not. If it was successful, you will see the content that is passing through the network.
Due to my restrictions, I was not able to have success, but give it a try and see if you
have a different result!

..  figure:: /images/mitm.png

    Run the ARP Poisoning, and look to see if it was successful.

Kali Linux is a useful and fun tool to learn. This was only a quick tutorial on how
to set up a Raspberry Pi with Kali Linux, the basics of working with Kali, and a
quick overview of a few tools included with Kali. There are plenty of resources that
can teach you the more in depth explanation of each tool included with Kali Linux.

.. [#f1] Kali Tools (2018, November 24). "`Wireshark. <https://tools.kali.org/information-gathering/wireshark>`_" Retrieved March 01, 2021, from https://tools.kali.org/information-gathering/wireshark
.. [#f2] Maningo, J. (2021, March 04). "`A beginner's guide to Kali Linux getting started. <https://www.quickstart.com/blog/a-beginners-guide-to-kali-linux-getting-started/>`_" Retrieved March 14, 2021,from https://www.quickstart.com/blog/a-beginners-guide-to-kali-linux-getting-started/
.. [#f3] Kalitut. (2020, July 19). "`How to Install and Use Bettercap 2. <https://kalitut.com/how-to-install-and-use-bettercap/#How_to_use_bettercap>`_" Retrieved April 15, 2021, from https://kalitut.com/how-to-install-and-use-bettercap/#How_to_use_bettercap
.. [#f4] Kumar, V. (2020, August 14). "`Arp poisoning attack with ettercap tutorial in Kali Linux for beginners. <https://www.cyberpratibha.com/arp-poisoing-attack-with-ettercap-tutorial/>`_" Retrieved April15, 2021 from https://www.cyberpratibha.com/arp-poisoing-attack-with-ettercap-tutorial/