# Lista containers installati:
 -  [portainer](srv/storage/portainer) - è un gestore di container e si accede dalla porta 9000
 -  [caddy](srv/storage/caddy) - è un reverse proxy e serve per connettere far comunicare la rete esterna con i container
 -  [nextcloud](srv/storage/nextcloud) - è il server dei file
 -  [vaultwarden](srv/storage/vaultwarden) - è un gestore di password
 -  [home assistant](srv/storage/homeassistant) - è un gestore di domotica - assistente casalingo
 -  [motioneye](srv/storage/motioneye) - videosorveglianza
 -  [fail2ban](srv/storage/fail2ban) - è per bannare i tentativi di accesso indesiderati
 -  [watchtower](srv/storage/watchtower) - per aggiornare automaticamente i container
 -  [searxng](srv/storage/searxng) - metamotore di ricerca
 -  [kopia](srv/storage/kopia) - backup
 -  [wireguard](srv/storage/wireguard) - VPN
 -  [rclone](srv/storage/rclone) - per sincronizzare i vari cloud
 -  [authelia](srv/storage/authelia) - gestore accessi
 -  [plex](srv/storage/plex) - server multimedia
 -  [jellyfin](srv/storage/containers/jellyfin) - server multimediale preferibile a plex
 -  [duplicati](srv/storage/containers/duplicati) - backup preferito a kopia
 -  [heimdall](srv/storage/containers/heimdall) - portale
 -  [dynuiu](srv/storage/containers/dynuiuc) - client ddns per aggiornare il proprio indirizzo ip online
# Attenzione!
vedere [procedura avvio containers](./srv/storage#procedura-avvio-containers)
