# MaioLinuX homeserver

## Premessa
Io non sono un programmatore, ma un "normale" utente di linux, in particolare di [debian](http://debian.org) , che vuole contribuire alla comunità del software libero, scrivendo una guida su come ha realizzato il proprio server di casa. Molto probabilmente qui dentro troverete errori e inesattezze e moltissimo margine di miglioramento.

## Cos'è?
Si tratta di un server pensato per essere utilizzato in ambito domestico. Lo scopo di questo repository è quello di fornire una guida passo passo, degli esempi, del codice ed una serie di collegamenti per realizzarlo con competenze informatiche non esagerate.
Se volete desiderate qualcosa di automatico vi consiglio di valutare in ordine sparso:
- https://homelabos.com/
- https://umbrel.com/
- https://ansible-nas.io/
- https://www.casaos.io/
- https://dockstarter.com/
- https://openmediavault.org/
- https://yunohost.org/
che non ho utilizzato perché volevo capire cosa stavo facendo.

## Perché
Per riprendersi in mano i propri dati ed avere un maggior controllo e personalizzazione sulle risorse informatiche, realizzando un ambiente privato all'interno della propria casa.
Perché i miei dati sono i miei appunto!
Perché se voglio condividere le foto con i miei famigliari lo devo poter fare solo con loro senza per forza dover far sapere a Alphabet:tm:, Meta:tm:, Apple:tm: dove sono stato e con chi.
Perché se faccio una ricerca online non vorrei poi essere bombardato di pubblicità al riguardo.
Perché posso!

## Come?
Gli elementi che servono sono i seguenti:
1. **Hardware**: per un uso casalingo non dovrà servire nulla di eccezionale e magari consumare poco. Per iniziare a me è andato bene un vecchio PC con:
   - CPU AMD A8-3870 (stiamo parlando di un processore di 12 anni fa) con 4 core;
   - 12 GB di RAM (mai ancora consumati);
   - 5 HDD 1 SSD (è solo un esempio della mia configurazione in realtà ne basterebbero 2 o meglio 3);
2. **Connettività di rete**: nulla di esasperato, a casa ho 60Mb/20Mb; ma intesa anche come accessibilità dall'esterno quindi almeno un modem cha dia la possibilità di fare un port forwarding (lo fanno tutti) 
3. **Sistema operativo**: Debian stabile (uso debian da oltre 20 anni :smiling_face_with_tear: sempre in ambito desktop e da sempre "testing");
4. **Scalbilità**: ovvero possibilità di espandere ed aggiornare il server senza troppi problemi;
5. **Container**: ovvero Docker, per consentire l'esecuzione di applicazioni un po' più isolate e repplicabili;
6. **Sicurezza**: sarà lo stesso server ad implementate misure di sicurezza come firewall, crittografia e autenticazione per proteggere i dati e impedire l'accesso non autorizzato al server stesso;
7. **Backup e disaster recovery**: È importante implementare una strategia di backup regolare e un piano di disaster recovery per proteggere i dati in caso di guasto hardware o altre emergenze;
8. **Gestione e monitoraggio**: È fondamentale monitorare le prestazioni e la disponibilità del server cloud casalingo e applicare eventuali ottimizzazioni o correzioni necessarie per garantire un funzionamento efficiente e affidabile.

## Da fare
Ci sono un sacco di cose da fare vedi [TODO](TODO.md)

## Iniziamo!
inizia a leggere la [documentazione](documentazione/inizio.md)!

## Licenze

### Documentazione
Copyright (C)  2023  Francesco Maioli.

Permission is granted to copy, distribute and/or modify this document under the terms of the GNU Free Documentation License, Version 1.3 or any later version published by the Free Software Foundation; with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
A copy of the license is included in the section entitled [LICENSE](documentazione/LICENSE.md) .

### Codice
Maiolinux homeserver un server domestico
Copyright (C) 2023  Francesco Maioli

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program i distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.
