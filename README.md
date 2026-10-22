# coenvermeer.nl

Persoonlijke site van Coen Vermeer, developer & UX designer uit Castricum.
Live op [coenvermeer.nl](https://coenvermeer.nl).

Eén statische pagina (`index.html`) met alles inline: geen build-stap, geen
externe fonts of scripts. Met licht/donker-schakelaar en een easter egg
achter het CV-logo (tik 5 keer, of probeer de Konami-code).

## Deployen

De site draait op de Lukraak-server (Apache, HTTPS via Let's Encrypt). De
map `/var/www/coenvermeer.nl/www` is van `beheer`, dus er is geen sudo nodig:

```bash
ssh beheer@134.209.201.232 'cat > /var/www/coenvermeer.nl/www/index.html' < index.html
```

De submappen `movienight/` en `film-atlas/` op de server horen bij andere
projecten en staan niet in deze repo (`film-atlas/` is een doorverwijzing naar
https://film-atlas.nl, neergezet door de deploy van Film Atlas).
