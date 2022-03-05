# UUD
Ultimate Unraid Dashboard


telegraf.conf is all options needed to use telegraf with the Ultimate Unraid Dashboard without all the extra clutter
The :latest tag will run a version that you can't install extra packages into! Change the tag to telegraf:1.20.2 for it to work!

Copy the file and place it in the location you want the telegraf appdata to be. e.g. /mnt/user/appdata/telegraf/telegraf.conf The default config file can be copied from https://raw.githubusercontent.com/skaterpunk/UUD/main/telegraf.conf

Post Arguments input field:

/bin/sh -c 'apt update && apt install -y smartmontools && apt install -y lm-sensors && telegraf' --user 0

To be able to see this field we need to click on the Advanced View button. 

Post Arguments input field with nvme and ipmi options:

/bin/sh -c 'apt update && apt install -y smartmontools && apt install -y lm-sensors && apt install -y nvme-cli && apt install -y ipmitool && telegraf'
