# OpenWRT-NetworkCheck
Script to check the network status and write the status and time to a file if there is a change.

Working from home I started to notice that my ISP seems to go down a lot so I wanted to create a cronjob to run on my router and check the last network status recorded (up or down) and compare that to the current status. If the status are the same, do nothing. If the status has changed write the new status and time to the log file. This way I have data next time I want to talk to my ISP.

I have this setup on an OpenWRT router running 19.07.3

Once you add this file to where ever you want to run this make sure you make it executable 
ex. chmod a+x netCheck

Then make sure you setup the cronjob by typing crontab -e
then add the line */1 * * * * /root/netCheck to the file. I have my check runnning every minute
