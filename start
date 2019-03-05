#!/bin/bash

cp -R /web-backup/* /usr/share/urbackup
echo "/backups" > /var/urbackup/backupfolder
chown urbackup:urbackup /backups
chown urbackup:urbackup /var/urbackup
exec urbackupsrv "$@"
