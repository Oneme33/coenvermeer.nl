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
COPYFILE_DISABLE=1 tar -czf - index.html favicon.ico favicon.svg apple-touch-icon.png \
  | ssh beheer@134.209.201.232 'tar -xzf - -C /var/www/coenvermeer.nl/www'
```

`robots.txt` en `sitemap.xml` in de webroot zijn met de hand gezet (niet in deze
repo). Komt er een project bij op coenvermeer.nl, voeg het dan toe aan de sitemap.

De submappen `movienight/` en `film-atlas/` op de server horen bij andere
projecten en staan niet in deze repo (`film-atlas/` is een doorverwijzing naar
https://film-atlas.nl, neergezet door de deploy van Film Atlas).
