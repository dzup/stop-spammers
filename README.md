This Script will create a example /etc/hosts file from repository

https://raw.githubusercontent.com/matomo-org/referrer-spam-list/master/spammers.txt

then adding content of file CUSTOM_SPAMMERS

making each URL redirect 127.0.0.1 by default

run 

./block-spammers -h

for more options

Example Usage:

./block-spammers -u -t > new-hosts

-u get new spammers.txt 
-t display output 
new-hosts pipe output to new-hosts

ADDING CUSTOM SPAMMERS:
You can add custom spammers like this:

echo "example.com" >> CUSTOM_SPAMMERS

INSTALL:

#First BACKUP your original /etc/hosts

sudo cp /etc/hosts /etc/hosts.orig

#Copy new-hosts to /etc/hosts

sudo cp new-hosts /etc/hosts

Thats it!

To DEINSTALL:
#copy original to /etc/hosts

sudo cp /etc/hosts.orig /etc/hosts

Tested in RASPBIAN BUSTER, may work in other platforms,
please let me know!

Using raspberry pi 4 with:

$ cat /etc/issue

Raspbian GNU/Linux 10 \n \l

comments, questions:
dzupd@yahoo.com
