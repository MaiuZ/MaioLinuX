# Cose da fare:
1. ~~impostare la vpn meglio~~
2. ~~utilizzare .evn per i file docker e nascondere eventuali segreti (secrets)~~
3. ~~unattended upgrade (server mail)~~
4. ~~installare plex~~ -> passato a jellyfin
5. ~~client ddns (duckdns o dynu)~~
6. ~~spostare i containers in /srv/storage/containers, i dati in /srv/storage/dati ecc. (valutare)~~
7. aggiungere i tutti i container nelle descrizioni
8. impostare authelia (o meglio ancora authentik https://goauthentik.io/) per il login con ban (vedi: https://github.com/authelia/authelia/blob/master/examples/compose/lite/authelia/configuration.yml)
9. ban fail2ban caddy (vedi https://muetsch.io/how-to-integrate-caddy-with-fail2ban.html attenzione che forse non vanno bene tutte quelle porte almeno attiva i client non bannabili anche vpn)
    - vedi anche https://www.abuseipdb.com/bulk-report
10. pihole (con vpn, ma da solo così che anche i pc di casa si collegano attraverso di lui vedi: https://github.com/wg-easy/wg-easy/wiki/Using-WireGuard-Easy-with-Pi-Hole)
11. aggiungere una guida su quali passi fare per primi (iniziato)
12. firefox sync - vedi https://thesmarthomejourney.com/2025/03/18/self-hosting-firefox-sync/
13. mettere le licenze ovunque
14. un portale magari con diverso modo di vedere se locale o da internet - vedi https://docs.organizr.app/ -> heimdall
15. ~~un AI vedi - https://github.com/getumbrel/llama-gpt~~
16. verificare il discorso degli utenti di Linuxserver.io
17. healtcheck?
18. clonare su altro server git magari self hosted
19. sito (github.io??)
20. tradurre in italiano le licenze (si può? )
21. tradurre in inglese il tutto
