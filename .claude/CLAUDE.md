# frigate

## Rinnakkaiset Claude-sessiot (claude-loki)

Ilkka ajaa Claudea samaan aikaan usealla koneella ja kahdella tilillä, joten samassa
repossa voi olla toinen sessio työn alla juuri nyt. Kaikki sessiot kerätään kantaan
<http://192.168.0.16:8260/> (lähiverkko tai WireGuard; ks. `ruusuniemiverkko/docs/claude-sessiot.md`).

1. **Ennen työn aloittamista** katso, mitä muualla on meneillään:
   `curl -s http://192.168.0.16:8260/api/meneillaan`
   Jos toinen sessio työskentelee samassa repossa, kerro siitä käyttäjälle ja vältä
   samojen tiedostojen muokkaamista.
2. **Ennen committia** tarkista ristiriidat (`<repo>` = tämän repon hakemiston nimi):
   `curl -s "http://192.168.0.16:8260/api/ristiriidat?repo=<repo>"`
   Jos toinen sessio on muokannut samoja tiedostoja tai committannut samaan repoon:
   - lue tiedosto uudelleen levyltä ennen muokkausta, älä luota muistissa olevaan versioon
   - tarkista `git diff`, ettei muutos poista muiden lisäämiä rivejä
   - `git pull --rebase` ennen pushia
3. Jos palvelin ei vastaa (kone ei ole lähiverkossa), jatka normaalisti.

Windowsin PowerShellissä käytä `curl.exe` (pelkkä `curl` on siellä eri komento).

## Rinnakkaiset Claude-sessiot (claude-loki)

Ilkka ajaa Claudea samaan aikaan usealla koneella ja kahdella tilillä, joten samassa
repossa voi olla toinen sessio työn alla juuri nyt. Kaikki sessiot kerätään kantaan
<http://192.168.0.16:8260/> (lähiverkko tai WireGuard; ks. `ruusuniemiverkko/docs/claude-sessiot.md`).

1. **Ennen työn aloittamista** katso, mitä muualla on meneillään:
   `curl -s http://192.168.0.16:8260/api/meneillaan`
   Jos toinen sessio työskentelee samassa repossa, kerro siitä käyttäjälle ja vältä
   samojen tiedostojen muokkaamista.
2. **Ennen committia** tarkista ristiriidat (`<repo>` = tämän repon hakemiston nimi):
   `curl -s "http://192.168.0.16:8260/api/ristiriidat?repo=<repo>"`
   Jos toinen sessio on muokannut samoja tiedostoja tai committannut samaan repoon:
   - lue tiedosto uudelleen levyltä ennen muokkausta, älä luota muistissa olevaan versioon
   - tarkista `git diff`, ettei muutos poista muiden lisäämiä rivejä
   - `git pull --rebase` ennen pushia
3. Jos palvelin ei vastaa (kone ei ole lähiverkossa), jatka normaalisti.

Windowsin PowerShellissä käytä `curl.exe` (pelkkä `curl` on siellä eri komento).
