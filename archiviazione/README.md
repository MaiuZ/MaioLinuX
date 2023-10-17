# Qui ci sono le istruzioni per la gestione dell'archiviazione del server.

## Comprende:
 - fstab per la configurazione standard degli hdd
 - snapraid
 - snapper
 - snapraid-btrfs-runner

## Fonti:
 - https://wiki.selfhosted.show/tools/snapraid-btrfs/
 - https://perfectmediaserver.com/03-installation/manual-install-ubuntu/

## Memo:
 - ricordarsi di avviare snapraid-btrfs-runner con:
   - sudo crontab -e
   - appendere:
    - 10 03 * * * python3 /opt/snapraid-btrfs-runner/snapraid-btrfs-runner.py -c /etc/snapraid-btrfs-runner/snapraid-btrfs-runner.conf
