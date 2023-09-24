# Set or Change-Date and Time-in-Linux

To display time and current date on Linux, use the following command:

    timedatectl
To get the available timezones, use the following command:

    timedatectl list-timezones
To Grab a specific timezones ,use the the Following Command:

    timedatectl list-timezones | grep -i "asia"
To set your local timezone in Linux, use the following command:

    timedatectl set-timezone "Asia/Dhaka"
To verify the above command result, use the following command:

    timedatectl
Restart the System Clock:

    sudo systemctl restart systemd-timesyncd
To Check your current locale settings by running the following command:

    locale | grep LC_TIME
To change the time format

    sudo localectl set-locale LC_TIME=en_DK.UTF-8
To set your time zone according to UTF, use the following command Universal Time Coordinated(UTC):

    timedatectl set-timezone UTC
To verify above command result, use the following command:

    timedatectl

# Set Hardware Clock in Linux:
To Display Hardware Clock Date and Time, use the following command:

    hwclock
The sample output should be like this

    #hwclock
    Friday 11 March 2016 12:25:56 PM IST -0.594257 seconds

To copy system time to hardware time, use the following command:

    hwclock --systohc
To verify it, use the following commands:

    #hwclock (for hardware date and time)
    #date (for system date and time)
The sample output should be like this:

    #hwclock
    Friday 11 March 2016 01:53:03 PM IST -0.359815 seconds
    #date
    Fri Mar 11 13:53:05 IST 2016
In the above result, both hardware clock and system clock has the same result.

# Set Time and Date
To set Time and Date, use the following command:

    timedatectl set-time 15:58:30
To verify the above command result, use the following command:

    timedatectl
The sample output should be like this:

          Local time: Fri 2016-03-11 15:58:40 IST
      Universal time: Fri 2016-03-11 10:28:40 UTC
            Timezone: Asia/Kolkata (IST, +0530)
         NTP enabled: yes
    NTP synchronized: no
     RTC in local TZ: no
          DST active: n/a
To set date from command line, use the following command:

    timedatectl set-time 2015-11-20
To verify the above command result, use the following command:

    timedatectl
The sample output should be like this -

       Local time: Fri 2015-11-20 00:00:06 IST
          Universal time: Thu 2015-11-19 18:30:06 UTC
                Timezone: Asia/Kolkata (IST, +0530)
             NTP enabled: yes
        NTP synchronized: no
         RTC in local TZ: no
              DST active: n/a 
To set both date and time, use the following command:

    sudo timedatectl set-time "2014-11-08 06:40:00"
To verify the above command result, use the following command:

    timedatectl
The sample output should be like this –

          Local time: Sat 2014-11-08 06:40:11 IST
      Universal time: Sat 2014-11-08 01:10:11 UTC
            Timezone: Asia/Kolkata (IST, +0530)
         NTP enabled: yes
    NTP synchronized: no
     RTC in local TZ: no
          DST active: n/a
          
# Set your hardware clock to local timezone:
    timedatectl set-local-rtc 1
    
# Synchronizing Linux System Clock with a Remote NTP Server
NTP stands for Network Time Protocol which is an internet protocol is used to synchronize approach clock between computers. 
The timedatectl utility makes it possible for to routinely sync your Linux system clock with remote servers utilizing NTP. 

To start automatic time synchronization with remote NTP server, use the following command:

    timedatectl set-ntp true
    
To disable NTP time synchronization, use the following command:

    timedatectl set-ntp false














