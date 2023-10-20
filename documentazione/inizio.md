# DOCUMENTAZIONE

## Sistema

### Preparazione sistema

#### Hardaware
Spesso spaventa e ci si blocca nella scelta dell'hardware, il consiglio spassionato è quello di utilizzare quello che si ha già in casa, un vecchio PC andrà benissimo per iniziare a capire quali sono le proprie esigenze in termini di prestazioni.

Anche un vecchio portatile potrebbe andare bene e vi risolverebbe il problema di un UPS in quanto la batteria garantisce una certa autonomia.

Se vi sentite spavaldi e volete tentare di partire da 0 potete provare da [qui](https://searxng.online/search?q=assemblaggio+pc+guida+passo+passo) .

#### Installazione Sistema operativo
[Questa](https://www.debian.org/releases/stable/i386/install.it.pdf) è la guida.

Ma se volete risparmiarvi la lettura della guida vi consiglio:
1. Scaricare Debian da [qui](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/) e scaricare debian-XX.X.X-amd64-netinst.iso del momento (dando per scontato che utilizzate un pc con architettura standard a 64 bit) su un qualsiasi PC.
2. Creare una chiavetta USB avviabile con sopra Debian:
   * Su Windows utilizzare un software come [rufus](https://rufus.ie/it/)
   * Su Linux
     ```
     # dd if=/percorso/debian-XX.X.X-amd64-netinst.iso of=/dev/sdb bs=4M status=progress oflag=sync
     ```
     dove `/dev/sdb` è il nome del " device" con cui è stata riconosciuta la chiavetta USB. Se non siete sicuri del nome del device usate il comando:
     ```
     # fdisk -l
     ```
3. inserire la chiavetta nel PC che diventerà il server
4. seguire le istruzioni dell'ottimo sistema di installazione di Debian avendo cura di:
     - scegliere una partizione ext3 da 80/100 mb come partizione di boot
     - una partizione swap grande il doppio (o almeno uguale) alla RAM del sistema
     - la parte restante del hdd/ssd come btrfs (consigliabile almeno 30/40 GB)
     - scegliere una installazione minimale scegliendo:
       - `server SSH`
       - `utilità di sistema standard`
  5. assegnare un IP univoco (es. 192.168.0.10) al server tramite il router
  6. riavviare il server è collegarsi ad esso da un altro pc tramite ssh es.:
     ```
     ssh utente@192.168.0.10
     ```
     dove l'utente è quello che avete scelto in fase di installazione (su windows vi consiglio l'utilizzo di [putty](https://www.putty.org)


### Archiviazione
si veda: [archiviazione](../archiviazione)

### Impostazioni

#### Configurazione inoltro mail di sistema
Visto che non si potrà essere a controllare h24 il server è necessario implementrare un sistema di avviso in caso di errori, per questo motivo ritengo fondamentale configurare un sistema di inoltro di email di sistema, per inoltrare avvisi fondamentali come quelli forniti dal monitoraggio dei dischi o degli aggiornamenti di sicurezza, come si può vedere nell'apposito capitolo: [configurazione inoltro mail di sistema](configurazione_inoltro_mail_di_sistema.md) 

#### Aggiornamenti automatici
Anche qui visto che un server meno lo si deve mantenere e meglio sarebbe, è consigliabile abilitare gli aggiornamenti auomatici e magari inviare una mail in caso di aggiornamento così da rimanere informati al riguardo.
Rimando al capitolo [aggiornamenti automatici](aggiornamenti_automatici.md)

#### Monioraggio stato di salute dischi
todo

## Containers
Vedi [containers](../containers)

## Licenza
Copyright (C)  2023  Francesco Maioli.

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
A copy of the license is included in the section entitled [LICENSE](LICENSE.md) .
