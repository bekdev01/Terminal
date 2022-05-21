
## 1.  terminal commands
```

* touch -> creates file
* man 'command'-> gives information about command 
* mv -> moves file and folders 
* rm -r -> deletes files and folders 
* cat -> reads file 
* more -> reads file 
* less -> reads file
* whoami -> show current user

touch - creates a file 
mv - move file
cat - read home file
more - read a file partially
less - read a file partially
sudo session stored for 15 minutes
sudo visudo - opens sudo config
sudo -k - kills sudo session
sudo -i - enter as root user
whoami - who am i
jlkesh ALL=(ALL) NOPASSWD:ALL
sudo passwd (anyusername) - sets password for any user
sudo passwd -l (root) - deletes password for any user
sudo adduser 'username' - creates new user
usermod - adds/removes user to/from group
groups - shows the groups list that current user belongs to
sudo deluser USERNAME sudo - deletes user from specified group
````


## 2.  change sudo session
```
jlkesh@jlkesh:~/study/linux/new_folder$ cd /
jlkesh@jlkesh:/$ sudo  cat /etc/sudoers
.
Defaults	env_reset <= add here some needed changes
.
```
## to modify this file  run command
```
    sudo visudo
    .
    Defaults	env_reset, timestamp_timeout=40 #(default is 15, -1 is infinite)
    .   
```
* sudo -i => logs in with root user
* visudo > current_user ALL = (ALL) NOPASSWD:ALL 
* sudo passwd any_user > change password for any user
* sudo passwd -l any_user > invalidates password for any user
* sudo adduser username > adds new user
* groups > show the current user's group
* usermod -aG sudo anyuser > add's anyuser to sudo group
* 
## 3. VM
````
--------------VM--------------

a - writes left side of cursor
i - writes right side of cursor
esc - exits insert mode
o - add new line belov cursor
shoft + o - adds new line above cursor
:wq - save and quit
:q! - quit without saving
/searching_word - for serching
n - next finding
shift + g - for bottom lime
n shift + g - next nth line
w - moves cursor another word
b - previous word
0 - to the beging of the line
$ - to the end of the line
shift + H - to the top of the window
shift + M - to the middle of the window
shift + L - to the bottom of the window
ctrl + f - move to full new window
dw  - delete the word
d^ / d$ - deletes from cursor to the begining
dd - delete entire line
dG - deletes all lines bottom from cursor location
yy - copy line
p - paste copied line to one line below
shift + p - paste copied line to one line above````
````
## 4. Nano
````
--------------nano--------------
crtl  + w - search(down)
alt + w - find the next one
crtl + q - search (up)
ctrl + \ - find and replace
alt + 6 - copy entire line
ctrl + u - paste
ctrl + k - cut line
ctrl + 6 - copy certain amount of text
alt + u - undo
alt + e - redo
````
[docs](https://www.nano-editor.org/dist/latest/nano.pdf)


# users / groups/ permissions
````
1. sudo cat /etc/passwd -> show all users
2. sudo cat /etc/group, getent group -> groups
3. sudo vipw -> change users file
4. sudo groupadd admins -> adds a groups to system
5. sudo vigr -> opens groups file
6. id -gn -> shows primary group
7. groupdel groupname -> deletes group
8. passwd username[default active user] -> changes password
9. exit -> logout
10. usermod -aG sudo,admins,.. user1 -> add user to the group
11. deluser username groupname -> delete group from a user
12. userdel -> deletes user
permissions
    => chmod u,g,o,a
    u -> 1
    g -> 2
    o -> 3
    a -> all
    +,-,=
    chmod 777 /Dir
    chmod -R 777 /Dir
    
    
    => chown
    chown user file/dir (-R)
    chgrp user file/dir (-R)
    
    
````

