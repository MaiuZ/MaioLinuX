# CONFIGURAZIONE INOLTRO EMAIL DI SISTEMA

## Premessa
Questo come altri esempi è solo una proposta di configurazione utilizzando [msmtp](https://wiki.debian.org/msmtp) e [bsd-mailx](https://manpages.debian.org/stable/bsd-mailx/bsd-mailx.1.en.html)

## Installazione
installiamo i pacchetti necessari:

```sudo apt install msmtp-mta bsd-mailx```

## Configurazione

editialmo il file di configurazione di `/etc/msmtprc` (da creare appunto in `/etc` perchè riferito alle mail di sistema):
```
sudo nano /etc/msmtprc
```
il contenuto dovrebbe essere simile a quanto segue:
```
account default
host smtp.mailserver.tld #sostituire con il server mail
port 587 #verificare se è effetivamente la porta usata
tls on
tls_starttls on
auth on
user utente #sostituire utente con l'utente smtp
password strongpassword #sostituire strongpasword con la relativa password
auto_from off
from server@yourdomain #sostituire server@yourdomain con la mail del mittente del server (io ho creato una mail apposita tipo server@miodominio.tld)
logfile /var/log/msmtp #impostare dove salvare il log delle mail
aliases /etc/aliases
```
editialmo il file `/etc/aliases` (che sono gli "alias" delle mail di sistema):
```
sudo nano /etc/aliases
```
e dovrebbe assomigliare a qualcosa del genere:
```
# /etc/aliases
mailer-daemon: postmaster
postmaster: server@yourdomain #sostituire server@yourdomain con la mail del mittente del server (io ho creato una mail apposita tipo server@miodominio.tld)
nobody: root
hostmaster: root
usenet: root
news: root
webmaster: root
www: root
ftp: root
abuse: root
noc: root
security: root
root: server@yourdomain #sostituire server@yourdomain con la mail del mittente del server (io ho creato una mail apposita tipo server@miodominio.tld)
default: server@yourdomain #sostituire server@yourdomain con la mail del mittente del server (io ho creato una mail apposita tipo server@miodominio.tld)
```
quindi iniziallizzare gli alias digitando:
```
sudo newaliases
```
riavviamo il servizio msmtp tramite il comando:
```
sudo systemctl restart msmtpd.service
```
infine testimao se tutto è ok tramite un test di invio di una mail come root; quindi:
```
sudo su
```
poi come superuser
```
echo "Questo è il contenuto della mail" > /tmp/body.txt && mailx -s "Questa è l'intestazione della mail" server@yourdomain < /tmp/body.txt; rm /tmp/body.txt
```
ovviamente sostituire `server@yourdomain`
eventuali errori ricordo che possono essere indagati in `/var/log/msmtp` (o la posizione che avevato dichiarato in `/etc/msmtprc`.

[ritorno alla documentazione principale](inizio.md)

## Licenza
Copyright (C)  2023  Francesco Maioli.

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
A copy of the license is included in the section entitled [LICENSE](LICENSE.md) .
