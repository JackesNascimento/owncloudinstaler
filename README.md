# owncloud
Bash Script to install owncloud on ubuntu 22.04

Download the script:
``wget https://raw.githubusercontent.com/linuxsyr/owncloud/main/owncloud.bash``

Edit your data DB and Password:
``nano owncloud.bash``
``mysql --password=YOUPASS --user=root --host=localhost << eof
create database YOUDBNAME;
grant all privileges on YOUDBNAME.* to root@localhost identified by "YOUPASS";``

``--database-name "YOUDBNAME" \
   --database-user "root"\
   --database-pass "YOUPASS" \
   --admin-user "root" \
   --admin-pass "YOUPASS"``
   
IMPORTANT: Note this data DB and Password.

Now let's go start installer:
``chmod +x owncloud.bash
sudo bash ./owncloud.bash``

You are done! 👏

Now access in your Browser with IP you VPS, to install Owncloud and complete configurations internal.
