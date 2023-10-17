# Aggiornamenti automatici

## Premessa
Visto che sono una operazione delicata, è fortemente raccomandabile essere avvisati su cosa succede durante un aggiornamento automatico, sorattutto in caso di errore, quindi è necessario prima abilitare l'[inoltro email di sistema](configurazione_inoltro_mail_di_sistema.md) .

## Installazione
è neccessario installare `unattended-upgrades`, quindi digitare:
```
sudo apt install unattended-upgrades
```

## Configurazione
per configurare il processo di aggiornamento è necessario editare `/etc/apt/apt.conf.d/50unattended-upgrades`, quindi digitare:
```
sudo nano /etc/apt/apt.conf.d/50unattended-upgrades
```
il file contiene già tutte le configurazioni e di default abilita gli aggiornamenti di sicurezza; inoltre fornisce le spiegazioni del caso; consiglio di editare la riga contenente:
```
//      "origin=Debian,codename=${distro_codename}-updates";
```
togliendo il commento `//` in quanto sarebbero gli aggiornamenti raccomandati che contengono aggiornamenti non critici che possono rimuovere fastidi importanti e pacchetti non funzionanti, ma che non influiscono sulla sicurezza. Oltre a risolvere alcuni problemi, non abilitano alcuna funzionalità. Abilitarli è generalmente una buona idea. Le dimensioni da scaricare e le modifiche non sono eccessive, ma migliorano la stabilità del server in vari modi.
Abilitiamo l'invio di mail togliendo il commento `//` sulla riga contenente
```
//Unattended-Upgrade::Mail "root"; 
```
volendo si può personalizzare a chi inviare tale mail quindi avremo
```
Unattended-Upgrade::Mail "server@yourdomain";
```
ovviamente sostituendo `server@yourdomain` con la mail di destinazione desiderata.
Inoltre consiglio labilitazione di:
```
Unattended-Upgrade::MailReport "on-change";

Unattended-Upgrade::Remove-Unused-Kernel-Packages "true";

Unattended-Upgrade::Remove-New-Unused-Dependencies "true";

Unattended-Upgrade::Remove-Unused-Dependencies "true";
```
quindi andiamo a creare `/etc/apt/apt.conf.d/20auto-upgrades` digitando:
```
sudo dpkg-reconfigure -plow unattended-upgrades
```
abilitiamo il servizio:
```
sudo systemctl enable unattended-upgrades
```
infine lo avviamo:
```
sudo systemctl enable unattended-upgrades
```

## Test
per testare il tutto digitare
```
sudo unattended-upgrades --dry-run --debug
```
se tutto va bene si può lanciare manualmente con:
```
sudo unattended-upgrade
```

## Fonti
- https://wiki.debian.org/UnattendedUpgrades

altre informazioni si possono trovare su:

- https://www.howtoforge.com/automatic-updates-debian-ubuntu/

## Licenza
Copyright (C)  2023  Francesco Maioli.

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
A copy of the license is included in the section entitled [LICENSE](LICENSE.md) .
