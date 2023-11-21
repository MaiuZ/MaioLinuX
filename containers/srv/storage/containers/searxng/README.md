1. testare la configurazione `docker-compose.yml` digitando:
   ```
   sudo docker-compose --env-file ../general_parameters.env config
   ```
2. se è tutto a posto si può lanciare il container con:
   ```
   sudo docker-compose --env-file ../general_parameters.env up -d
   ```
