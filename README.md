Modul 300 - Guide
=============================
Webserver with Ubuntu 16.4

Start the vm
---------------
Do the following steps to start the vm
1. Start the VirtualBox Manager
2. Start the vm, by clicking on the machine and then on **start**
2. Go to the folder, where your vm is, here:
    *cd Modul300*
2. Right-Click on the folder and click on **gitbash here**
3. Give the following command: vagrant ssh

Now you are connected with your vm via gitbash

### helpful commands
| Command | Use |
| ------ | ------ |
| sudo -i | Change to root without password request |
|sudo shutdown -r now| restart the OS |
| sudo shutdown -h now | stop the OS |
| ifconfig | Show IP Adress |

Apache Web Server
---------------------
### helpful commands
| Command | Use |
| ------ | ------ |
| systemctl status apache2| Show status of the apache server |
| systemctl start apache2| Start the apache server |
| systemctl stop apache2| Stop the apache server |

Git Commands
---------------
Here you can find some useful git commands, which you need when using git bash

###Configure Tooling
Configure user information for all local repositories
| Command | Use |
| ------ | ------ |
| $ git config --global user.name "[name]"| Sets the name you want attached to your commit transactions |
| $ git config --global user.email "[email address]"| Sets the email you want atached to your commit transactions |

###Create Repositories
Start a new repository or obtain one from an existing URL.
| Command | Use |
| ------ | ------ |
|$ git init [project-name]| Creates a new local repository with the specified name |
|$ git clone [url]| Downloads a project and its entire version history |

###Make changes
Review edits and craft a commit transaction
| Command | Use |
| ------ | ------ |
|$ git diff| Shows file differences not yet staged |
|$ git status| Lists all new or modified files to be commited |
|$ git add [file]| Snapshots the file in preparation for versioning |
|$ git commit -m "[descriptive message]"| Records file snapshots permanently in version history |
|$ git commit -m "*write here the change you made*"| Stop the apache server |

###Synchronize Changes
Register a repository bookmark and exchange version history
| Command | Use |
| ------ | ------ |
|$ git pull| Downloads bookmark history and incorporates changes|
|$ git push origin master| Uploads all local branch commits to GitHub |
