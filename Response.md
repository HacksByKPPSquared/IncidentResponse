# Exploiting Java to Attack a Remote System

## 1.1. Using the Social Engineering Toolkit (SET)

1\. Launch the Kali virtual machine to access the graphical login
screen.

2\. Log in as root with toor as the password. Open the Kali PC Viewer.

3\. Click on the terminal icon located in the top menu bar.

<img src="./media/image1.png" style="width:8.31944in;height:2.01389in"
alt="A computer screen with white text Description automatically generated" />

4\. Use the ifconfig command to verify if the loopback interface is up
and running. If it is not active, run the commands below to bring the
loopback interface up.

<img src="./media/image2.png" style="width:8.19444in;height:4.19444in"
alt="A computer screen with white text Description automatically generated" />

5\. Start both the apache2 and postgresql services by entering the command below.

<img src="./media/image3.png" style="width:8.33333in;height:1.63889in"
alt="A screen shot of a computer Description automatically generated" />

6\. Start the Social Engineering Toolkit by typing the command below. Press Enter.

root@Kali-Attacker:~# setoolkit

<img src="./media/image4.png" style="width:8.27778in;height:5in" />

7\. When presented with the SET main menu, type 1 for Social-Engineering Attacks. Press Enter

<img src="./media/image5.png"
style="width:4.88889in;height:2.69444in" />

8\. On the next menu, type 2 for Website Attack Vectors. Press Enter

<img src="./media/image6.png"
style="width:4.63889in;height:3.48611in" />

9\. Choose the Metasploit Browser Exploit Method by typing the number 2. Press Enter.

<img src="./media/image7.png" style="width:8.23611in;height:3.18056in"
alt="A screen shot of a computer Description automatically generated" />

10\. Choose Web Templates by typing 1. Press Enter1

<img src="./media/image8.png" style="width:7.75248in;height:2.58416in"
alt="A screenshot of a computer Description automatically generated" />

11\. When asked, “Are you using NAT/Port Forwarding?” type yes. Press
Enter.

12\. When prompted for an IP address, type 203.0.113.2. Press Enter.

<img src="./media/image9.png"
style="width:8.34722in;height:0.43056in" />

13\. When asked if the payload handler is on a different IP, type no.
Press Enter

<img src="./media/image10.png"
style="width:8.31944in;height:0.44444in" />

14\. On the select a template menu, type 1 for Java Required. Press
Enter.

<img src="./media/image11.png" style="width:3.95833in;height:1.54167in"
alt="A screenshot of a computer Description automatically generated" />

15\. From the browser exploit list, type 9 to use the Java 7 Applet
Remote Code Execution. Press Enter

<img src="./media/image12.png" style="width:4.98152in;height:1.64356in"
alt="A computer screen with white text Description automatically generated" />

16\. Type 1 to use Windows Shell Reverse_TCP. Press Enter

<img src="./media/image13.png" style="width:8.38889in;height:4.98611in"
alt="A screenshot of a computer program Description automatically generated" />

17\. Type 6666 to use as the reverse port number. Press Enter.

<img src="./media/image14.png"
style="width:7.56944in;height:0.48611in" />

18\. Allow 2-3 minutes to pass for the SET web server to start. Once the
server starts, notice the message that appears, press the Enter key to
receive the prompt back.

<img src="./media/image15.png" style="width:5.08333in;height:1.70833in"
alt="A computer screen with white text Description automatically generated" />

1.2. Initiating Malicious URL

1\. Launch the Ubuntu virtual machine to access the graphical login
screen.

2\. Log in as student with securepassword as the password.

<img src="./media/image16.png" style="width:4.04167in;height:1.79167in"
alt="A screen shot of a computer Description automatically generated" />

3\. Open the Firefox web browser by clicking on the Firefox icon located
on the left menu pane.

<img src="./media/image17.png" style="width:0.79167in;height:2.73611in"
alt="A screenshot of a phone Description automatically generated" />

4\. In the address bar, type the following: http://203.0.113.2:8080/
followed by pressing Enter.

5\. A message will appear asking to a Java applet. Click on
Allow<img src="./media/image18.png"
style="width:11.05556in;height:1.29167in" />

6\. Another Firefox message appears. Click on Allow Now.

<img src="./media/image19.png" style="width:5.22222in;height:2.48611in"
alt="A screenshot of a computer error message Description automatically generated" />

7\. Open a new terminal window by clicking on the terminal icon located
on the left menu pane.

<img src="./media/image20.png" style="width:0.75in;height:2.04167in"
alt="A screen shot of a phone Description automatically generated" />

8\. Type the command below to verify if a connection is made to the
remote server.

<img src="./media/image21.png" style="width:8.125in;height:1in" />

1.3. Using the Meterpreter Session

1\. Change focus back to the Kali system.

2\. Focus on the terminal window left open with SET running. Notice the
prompt displaying that a meterpreter session has been opened. Press the
Enter key to bring the command prompt up.

3\. Type the sessions command, followed by pressing Enter. Notice the
active sessions presented.

<img src="./media/image22.png" style="width:6.19802in;height:1.78257in"
alt="A computer screen with white text Description automatically generated" />

4\. Start an interaction with session 1. Type the command below followed
by pressing the Enter key.

<img src="./media/image23.png" style="width:6.125in;height:0.91667in"
alt="A computer screen shot of a computer code Description automatically generated" />

5\. Notice the meterpreter prompt appears. Type sysinfo followed by
pressing Enter to receive info on the operating system of the victim.

<img src="./media/image24.png" style="width:4.53465in;height:0.88621in"
alt="A screenshot of a computer Description automatically generated" />

6\. Type getuid followed by pressing Enter to receive user info that the
server is running as.

<img src="./media/image25.png" style="width:3.20833in;height:0.65278in"
alt="A close up of a black background Description automatically generated" />

7\. Type ps followed by pressing Enter to receive a list of running
processes on the victim.

<img src="./media/image26.png" style="width:8.30556in;height:4.97222in"
alt="A computer screen shot of a student Description automatically generated" />

8\. Type screenshot to print an active screenshot of the victim’s
current desktop screen. Press Enter

<img src="./media/image27.png"
style="width:5.77778in;height:0.69444in" />

9\. Type download /etc/passwd to grab the passwd file. Press Enter

<img src="./media/image28.png" style="width:4.76389in;height:0.84722in"
alt="A computer screen with white text Description automatically generated" />

10\. Type shell into the meterpreter prompt and press Enter

meterpreter \> shell

<img src="./media/image29.png" style="width:3.01389in;height:0.81944in"
alt="A close-up of a computer code Description automatically generated" />

11\. Notice no prompt is shown. Proceed to type pwd and press the Enter
key to confirm you have shell access.

<img src="./media/image30.png" style="width:1.54167in;height:0.56944in"
alt="A close up of a sign Description automatically generated" />

2\. Collecting Volatile Data

2.1. Collecting Volatile Data on a Compromised System

1\. Once a system has been compromised, it is important to get some
information off the system before it is shut down. Any data residing in
RAM will be gone when the system is shut down. Change focus to the
Ubuntu system

2\. On the Ubuntu system, navigate to an open terminal.

3\. In the terminal, enter the command below to escalate to root
privileges. If prompted, enter securepassword as the password.

<img src="./media/image31.png" style="width:3.02778in;height:0.83333in"
alt="A computer screen shot of white text Description automatically generated" />

4\. Create a file to contain any volatile data we can find. To put a
heading into the file, enter the command below.

<img src="./media/image32.png"
style="width:7.08333in;height:0.54167in" />

5\. Verify the report.txt file has been created with the “student
investigator” title.

root@Ubuntu:/home/student# cat report.txt

<img src="./media/image33.png" style="width:4.58333in;height:0.73611in"
alt="A close up of white text Description automatically generated" />

6\. Add the date and timestamp to the report.txt file

root@Ubuntu:/home/student# date \>\> report.txt

7\. Print the system information to the report.txt file.

root@Ubuntu:/home/student# uname –a \>\> report.txt

8\. Add the hostname to the report.txt file.

root@Ubuntu:/home/student# hostname \>\> report.txt
