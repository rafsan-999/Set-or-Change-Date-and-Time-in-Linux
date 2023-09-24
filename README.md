## Set or Change-Date and Time-in-Linux

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
