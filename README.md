# TCSC | Trauma Crime Scene Cleaning

Website voor TCSC (Thomas Bollen). Statische site: `index.html` + `assets/img/`.

## Structuur
- `index.html`: volledige site (HTML, CSS en JS in één bestand)
- `assets/img/`: logo, portret, favicon en social share afbeelding

## Foto's dienstkaarten
De dienstkaarten laden deze bestanden als ze bestaan (anders tonen ze een navy/goud vlak):
`assets/img/svc-crime-scene.jpg`, `svc-desinfectie.jpg`, `svc-ozon.jpg`, `svc-ontruiming.jpg`, `svc-vervuiling.jpg`, `svc-verkoopklaar.jpg`

## Deploy
Importeer de repo in Vercel (framework: Other, geen build command) of upload de map naar eender welke host.
## Beheerpagina (`/beheer.html`)

Klantbeheer voor teksten en foto's (Solyn Global), zonder server of database. Zelfde werkwijze als bij Nuance.

- Openen: `/beheer.html`, toegangscode `tcsc` (houdt alleen toevallige bezoekers weg; `noindex`).
- Klant kiest een pagina, tikt op een tekst en typt; foto's vervangen via het tabblad Foto's. Met de knop "Klikken" werkt de site weer gewoon (taal wisselen, menu openen, doorklikken). Werkt als app op telefoon (manifest + service worker, enkel voor `/beheer`).
- Wijzigingen blijven op het toestel van de klant. Met "Versturen" komt een bestand `tcsc-wijzigingen.txt` binnen via WhatsApp/mail.
- Online zetten: nakijken en de inhoud als `site-content.js` in de repo zetten. `site-edit.js` past die toe op elke pagina (ook na React-renders). Leeg bestand = site zoals gebouwd.
- Teksten zijn gekoppeld aan hun oorspronkelijke tekst, foto's aan hun oorspronkelijke bestand. Wordt die bron later in de code veranderd, dan vervalt de oude aanpassing.
- Achtergrondafbeeldingen in CSS en video's zijn niet via het beheer aan te passen.
