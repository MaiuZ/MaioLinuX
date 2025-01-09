# Primo avvio del container
1. Clonare il repository Perplexica:

   ```bash
   git clone https://github.com/ItzCrazyKns/Perplexica.git
   ```
2. editare i file `config.toml` e `app.dockerfile` adeguandoli alla nostra configurazione cambiando IP e porte come da esempio allegato
   ```
   sudo nano config.toml
   sudo nano app.dockerfile
   ```
3. sostituir ed editare `docker-compose.yml` con quello fornito qui
4. testare la configurazione `docker-compose.yml` digitando:
   ```
   sudo docker-compose --env-file ../general_parameters.env config
   ```
5. compilare il container:
   ```
   sudo docker-compose --env-file ../general_parameters.env build
   ```
6. se è tutto a posto si può lanciare il container con:
   ```
   sudo docker-compose --env-file ../general_parameters.env up -d
   ```
