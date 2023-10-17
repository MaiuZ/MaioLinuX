# Procedura avvio containers
1. editare il file `general_parameters.env` all'interno di `/srv/storage`
   ```
   cd /srv/storage
   sudo nano general_parameters.env
   ```
2. portarsi nella cartella del container (es.)
   ```
   cd caddy
   ```
3. editare eventuali altri file di configurazione (es.)
   ```
   sudo nano Caddyfile
   ```
4. testare se il relativo file `docker-compose.yml` funziona:
   ```
   sudo docker-compose --env-file ../general_parameters.env config
   ```
5. se è tutto a posto si può lanciare il container con:
   ```
   sudo docker-compose --env-file ../general_parameters.env up -d
   ```
