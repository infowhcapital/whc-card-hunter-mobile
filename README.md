# WHC Card Hunter — mobiele prijsdalingsonderzoeker

**Open zonder GitHub-login:** https://infowhcapital.github.io/whc-card-hunter-mobile/

## Wat werkt (8 november 2026, mobile v0.4)
- Dagelijkse publieke Cardmarket-gegevens worden op de aangesloten WHCapital-Windows-PC onderzocht.
- De app toont 100 onderzoekskaarten waarvan de recente Cardmarket-prijstrend minstens 20% onder het 30-daagse gemiddelde van dezelfde exacte productdruk ligt. Dit is een statistisch **onderzoekssignaal**, geen daadwerkelijk verkochte of aangeboden koopdeal.
- De link gebruikt Cardmarket's eigen unieke product-ID: `https://www.cardmarket.com/en/YuGiOh/Products?idProduct=...&language=1&minCondition=2`.
- Daardoor krijg je een **specifieke druk** in plaats van een naamzoekresultaat. De filters zijn Engels en minimaal Near Mint. De verkoper, editie, gedrukte setcode en verzendkosten moet je op Cardmarket nog controleren.
- Zoeken op naam/product-ID/set-ID, filteren, favorieten en een schatting van netto winst en ROI.
- Via een gewone mobiele browser te gebruiken, geen GitHub-login en geen Python.

## Geen bewezen aanbiedingen
**Geverifieerde winstgevende live deals: 0.** De officiële gratis prijsbestanden bevatten geen individuele verkopers, daadwerkelijke verzendkosten, taal/conditie of actuele listing. Een recent lagere trendprijs is niet automatisch een goedkoop exemplaar. Ook de risicoscores zijn geen kans op winst. Geen automatisch aankopen en geen ruwe Cardmarket-prijzen publiek tonen.

De programma's staan in twee afzonderlijke repositories: deze openbare mobiele site en een *private* prijsmonitor `infowhcapital/whc-card-hunter`. De dagelijkse update werkt alleen met de WHCapital-PC aan en ingelogd (Windows Taakplanner 08:10).

## Bewijs & tests
- `node test-ui.mjs` — syntax, data, website HTTP 200, 100 records, geen ruwe openbare prijsdata: PASS.
- `node test-browser.mjs` — Edge/Chromium mobiele viewport 390×844, 25 kaarten, zoeken, favorieten, netto winstberekening, exact idProduct in elke link met English/NM-filters: PASS, 0 JS errors.
- Cardmarket zelf beantwoordde de geautomatiseerde productpagina-inspectie met Cloudflare HTTP 403. De directe ID-route is gebaseerd op hun officiële publicatie. Het werkelijke externe bestemmingsscherm is daarom niet onafhankelijk in de headless browser bewezen.
- Actualisatie van nieuwe bron-dag en het automatisch signaleren van concrete deals: nog niet aangetoond.
