# Description: remote-db-download
This app is to download/backup sql/Mysql database(Any or All) from remote server via SSH <br>
and download it into local computer. <br> 

Note: It has a feature to Import Remotely downloaded sql database into you local mysql database directly.

(Upcoming Features: upload local sql file to remote mysql database directly)

# User Guide:
(Steps)
1. Download remote-db-download.deb file from this official repository (apt downloading coming soon) <br>
2. go to path/folder where the file has been download. <br>
3. command:  dpkg -i ./remote-db-download.deb <br>
4. Enter Y/y if asked before installation:<br>
5. Follow Configuration part to configure app
6. command: remote-db-download (to run this app)<br>
7. command:  man remote-db-download     (for manual)<br>


# Configuration Required after installation:

Dependencies required: ssh, scp, whiptail

To run this application, you need to set up a configuration file, <br>
where you provide remote SSH and MySQL usernames and passwords to connect to the server and download the database to the local machine. <br>
Local MySQL username and password are also required to import the database. Follow the steps below:

1. sudo nano /etc/remote-db-download.conf

2. Fill in all the details below: (Note: empty fields may cause errors or not function properly)

REMOTE_SSH_HOST="";   # ssh host/IP address here


REMOTE_SSH_USER="";   # ssh hostname  here (that has permission to download Mysql/sql server database)


REMOTE_SSH_PASSWORD="";   # ssh host password  here


LOCAL_SQL_USER="";  #Root User is Preferred


LOCAL_SQL_PASSWORD="";   #Root User password is Preferred


REMOTE_SQl_DB_USER="";  #Root User is Preferred


REMOTE_SQl_DB_PASSWORD="";  #Root User password is Preferred


# Uninstall app: 

command: sudo apt remote remote-db-download

# Copyright

Copyright: 2024 KaushalGhimire <official.kaushalg@gmail.com>

2024-03-23

The entire code base may be distributed under the terms of the GNU General
Public License (GPL), which appears immediately below.  Alternatively, all
of the source code as any code derived from that code may instead be
distributed under the GNU Lesser General Public License (LGPL), at the
choice of the distributor. The complete text of the LGPL appears at the
bottom of this file.

See /usr/share/common-licenses/(GPL|LGPL)
