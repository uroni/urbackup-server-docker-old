Image to run UrBackup in Docker.

Caveats:

 * Image mounting is disabled
 * ZFS snapshotting cannot be used

## Building

     docker build -t urbackup-server .

## Running

     docker run -d --name urbackup-server-1 -v /media/backups:/backups -v /media/database:/var/urbackup -p 55413-55415:55413-55415 -p 35623:35623/udp urbackup-server

## BTRFS support

For BTRFS support you have to run the container in privileged mode.

     docker run -d --privileged --name urbackup-server-1 -v /media/backups:/backups -v /media/database:/var/urbackup -p 55413-55415:55413-55415 -p 35623:35623/udp urbackup-server
     
