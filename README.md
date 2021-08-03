# autoremotebackup
This script will create a backup of all files in /var/www and individual backups of all databases and zip them. Further this will then backup the compressed file to your offsite server.


Dependencies: scp, sshpass, zip, unzip

to install on debian use: apt install -y scp sshpass zip unzip

Line3: Create backup folder in root directory
line6: Dump all databases individually in compressed form in backup folder
line 7: Compress /var/www/html/ recursively
line9: Create final compressed file with the date as the name
line 14: scp files to remote host
line 19 && 20: Remove waste backup files
