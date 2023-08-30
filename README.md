# Bash-Script-1

## What's Inside Script (nano bashscript.sh)
#!/bin/bash

Weekly Server Update - Dominique Ivey 8.28.23

#Create a script that runs every Friday at 11pm CST that will update the server and create at new file with the upgradable packages

#Update server every Friday at 11pm CST
sudo apt-get update && sudo apt-get upgrade -y

*22**5 sh /home/ubuntu/bashscript1.sh
echo "Server updated"

#Create a new file with the upgradable packages
touch upgradedfiles
*22**5 sh /home/ubuntu/bashscript1.sh &> upgradedfiles
filename = upgradedfiles >> date +"%m_%d_%Y
echo "New file created"

#Close
echo "Done"

![image](https://github.com/DomIvey/Bash-Script-1/assets/140740841/d14073ed-c025-4e7b-ae3f-4322b727520b)



## Commands Ran Within Terminal

![image](https://github.com/DomIvey/Bash-Script-1/assets/140740841/6dae8bf8-db9d-4e29-81ef-cd1eba430cc8)


ubuntu@ip-172-31-47-29:~$ history
    1  pwd
    2  ls
    3  sudo systemctl status cron.service
    4  touch bashscript1.sh
    5  ls
    6  pwd
    7  ls
    8  chmod 777 bashscript1.sh
    9  nano bashscript1.sh
   10  cat bashscript1.sh
   11  ./bashscript.sh
   12  ./bashscript1.sh
   13  nano bashscript1.sh
   14  clear
   15  pwd
   16  ls
   17  sudo apt-get update && sudo apt-get upgrade -y
   18  **22**5 sh /home/ubuntu/bashscript1.sh
   19  man cron
   20  **22**5 /home/ubuntu/bashscript1.sh
   21  cron **22**5 sh /home/ubuntu/bashscript1.sh
   22  crontab -e
   23  1
   24  nano bashscript1.sh
   25  clear
   26  crontab -e
   27  history
   28  nano bashscript1.sh
   29  crontab -e
   30  sudo apt-get update && sudo apt-get upgrade -y
   31  crontab -e
   32  nano bashscript1.sh
   33  history
ubuntu@ip-172-31-47-29:~$ sudo systemctl status cron.service
● cron.service - Regular background program processing daemon
     Loaded: loaded (/lib/systemd/system/cron.service; enabled; vendor preset: enabled)
     Active: active (running) since Wed 2023-08-30 20:24:28 UTC; 27min ago
       Docs: man:cron(8)
   Main PID: 415 (cron)
      Tasks: 1 (limit: 1140)
     Memory: 436.0K
        CPU: 5ms
     CGroup: /system.slice/cron.service
             └─415 /usr/sbin/cron -f -P

Aug 30 20:24:28 ip-172-31-47-29 systemd[1]: Started Regular background program processing daemon.
Aug 30 20:24:28 ip-172-31-47-29 cron[415]: (CRON) INFO (pidfile fd = 3)
Aug 30 20:24:28 ip-172-31-47-29 cron[415]: (CRON) INFO (Running @reboot jobs)
Aug 30 20:41:01 ip-172-31-47-29 cron[415]: (ubuntu) RELOAD (crontabs/ubuntu)
Aug 30 20:48:01 ip-172-31-47-29 cron[415]: (ubuntu) RELOAD (crontabs/ubuntu)
ubuntu@ip-172-31-47-29:~$ ./bashscript.sh
-bash: ./bashscript.sh: No such file or directory
ubuntu@ip-172-31-47-29:~$ pwd
/home/ubuntu
ubuntu@ip-172-31-47-29:~$ ls
bashscript1.sh  upgradedfiles
ubuntu@ip-172-31-47-29:~$ cd bashscript.sh
-bash: cd: bashscript.sh: No such file or directory
ubuntu@ip-172-31-47-29:~$ ./bashscript1.sh
Hit:1 http://us-east-1.ec2.archive.ubuntu.com/ubuntu jammy InRelease
Hit:2 http://us-east-1.ec2.archive.ubuntu.com/ubuntu jammy-updates InRelease
Hit:3 http://us-east-1.ec2.archive.ubuntu.com/ubuntu jammy-backports InRelease
Get:4 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]
Fetched 110 kB in 1s (164 kB/s)                        
Reading package lists... Done
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
The following packages have been kept back:
  linux-aws linux-headers-aws linux-image-aws
0 upgraded, 0 newly installed, 0 to remove and 3 not upgraded.
./bashscript1.sh: line 12: *22**5: command not found
Server updated
./bashscript1.sh: line 22: unexpected EOF while looking for matching `"'
./bashscript1.sh: line 25: syntax error: unexpected end of file
ubuntu@ip-172-31-47-29:~$ 

# Instructions
Create a Bash script that runs every Friday at 11 pm and does the following: 1. updates the server, 2. creates a new file with the line about how many packages can be upgraded that outputs to the screen (ex. x packages can be upgraded.). The file name should have the current date appended to it (e.g. update08.25.23.txt).

Your script should:

Have a heading with the purpose of the script, your name, and the date.
Have comments explaining the cronjob you set up to automatically run on Friday at 11 pm w/o user interaction
Have comments explaining what the commands are doing.
Have limited errors.
