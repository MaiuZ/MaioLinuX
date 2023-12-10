# Cose da fare:
1. ~~impostare la vpn meglio~~
2. ~~utilizzare .evn per i file docker e nascondere eventuali segreti (secrets)~~
3. ~~unattended upgrade (server mail)~~
4. ~~installare plex~~ -> passato a jellyfin
5. ~~client ddns (duckdns o dynu)~~
5. spostare i containers in /srv/storage/containers, i dati in /srv/storage/dati ecc. (valutare)
6.  impostare authelia per il login con ban (vedi: https://github.com/authelia/authelia/blob/master/examples/compose/lite/authelia/configuration.yml)
7.  ban fail2ban caddy (vedi https://muetsch.io/how-to-integrate-caddy-with-fail2ban.html attenzione che forse non vanno bene tutte quelle porte almeno attiva i client non bannabili anche vpn)
    - vedi anche https://www.abuseipdb.com/bulk-report
8. pihole (con vpn, ma da solo così che anche i pc di casa si collegano attraverso di lui vedi: https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Pi-Hole)
9. aggiungere una guida su quali passi fare per primi (iniziato)
10. firefox sync - vedi https://thesmarthomejourney.com/2023/03/18/self-hosting-firefox-sync/
11. mettere le licenze ovunque
12. un portale magari con diverso modo di vedere se locale o da internet - vedi https://docs.organizr.app/ -> heimdall
13. un AI vedi - https://github.com/getumbrel/llama-gpt
14. verificare il discorso degli utenti di Linuxserver.io
15. healtcheck?
16. clonare su altro server git magari self hosted
17. sito (github.io??)
18. tradurre in italiano le licenze (si può? )
19. tradurre in inglese il tutto
