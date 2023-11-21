# Primo avvio del container
1. editare il file `Caddyfile` 
   ```
   sudo nano Caddyfile
   ```
2. testare la configurazione `docker-compose.yml` digitando:
   ```
   sudo docker-compose --env-file ../general_parameters.env config
   ```
3. se è tutto a posto si può lanciare il container con:
   ```
   sudo docker-compose --env-file ../general_parameters.env up -d
   ```
