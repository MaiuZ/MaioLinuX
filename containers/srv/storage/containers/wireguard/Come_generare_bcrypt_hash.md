Ecco la traduzione del file Markdown in italiano:

# wg-password

`wg-password` (wgpw) è uno script che genera hash delle password bcrypt da utilizzare con `wg-easy`, migliorando la sicurezza richiedendo una password.

## Caratteristiche

- Genera hash delle password bcrypt.
- Si integra facilmente con `wg-easy` per applicare i requisiti delle password.

## Utilizzo con Docker

Per generare un hash della password bcrypt utilizzando Docker, esegui il seguente comando:

```sh
docker run --rm -it ghcr.io/wg-easy/wg-easy wgpw 'YOUR_PASSWORD'
PASSWORD_HASH='$2b$12$coPqCsPtcFO.Ab99xylBNOW4.Iu7OOA2/ZIboHN6/oyxca3MWo7fW' // letteralmente YOUR_PASSWORD
```
Se non viene fornita una password, lo strumento ti chiederà di inserirne una:
```sh
docker run --rm -it ghcr.io/wg-easy/wg-easy wgpw
Enter your password:      // prompt nascosto, digita la tua password
PASSWORD_HASH='$2b$12$coPqCsPtcFO.Ab99xylBNOW4.Iu7OOA2/ZIboHN6/oyxca3MWo7fW'
```

**Importante**: assicurati di racchiudere la tua password tra **virgolette singole** quando esegui il comando `docker run`:

```bash
$ echo $2b$12$coPqCsPtcF <-- non corretto
b2
$ echo "$2b$12$coPqCsPtcF" <-- non corretto
b2
$ echo '$2b$12$coPqCsPtcF' <-- corretto
$2b$12$coPqCsPtcF
```

**Importante**: Nota bene: non racchiudere l'hash della password generato tra virgolette singole quando usi `docker-compose.yml`. Invece, sostituisci ogni simbolo `$` con due simboli `$$`. Ad esempio:

```yaml
- PASSWORD_HASH=$$2y$$10$$hBCoykrB95WSzuV4fafBzOHWKu9sbyVa34GJr8VV5R/pIelfEMYyG
```

Questo hash è per la password 'foobar123', ottenuto utilizzando il comando `docker run ghcr.io/wg-easy/wg-easy wgpw 'foobar123'` e successivamente inserendo un simbolo `$` aggiuntivo prima di ogni simbolo `$` esistente.

**Addendum**: in caso si utilizzi un file di variabili esterne come `general_parameters.env` si può utilizzare l'hash direttamente così come viene restituito da `wgpw` senza virgolette in questo caso `$2b$12$coPqCsPtcFO.Ab99xylBNOW4.Iu7OOA2/ZIboHN6/oyxca3MWo7fW` vedi [general_parameters.env](../general_parameters.env)