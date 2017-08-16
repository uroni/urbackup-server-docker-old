Image to run UrBackup in Docker.

Ceveats:

 * Image mounting is disabled
 * Btrfs/ZFS snapshotting cannot be used

## Building

     docker build -t urbackup-server .

## Running

     docker run -d --name urbackup-server-1 -v /media/backups:/backups -v /media/database:/var/urbackup -p 55413-55415:55413-55415 -p 35623:35623/udp urbackup-server
