# WHC Card Hunter Mobile v0.5

De website staat op https://infowhcapital.github.io/whc-card-hunter-mobile/ en vereist geen GitHub-login.

## Onderzoekersfuncties
- Dalingen: 100 onderzoeksrecords uit de gratis Cardmarket-product/prijsgids met exact idProduct; dit zijn GEEN winstdeals.
- Live: toegang tot versleutelde privé-resultaten via unieke persoonlijke link. De sleutel staat niet in de openbare code of de GitHub-databestanden.
- Bewaard: favoriete kaarten lokaal op het toestel.
- Winst: zelf gecontroleerde aankoop-/verkoopkosten en ROI.

## Echte aanbodscanner
De Windows-dagtaak kan via derdepartij API.SH de actuele bied-/vraagaanbiedingen per exact Cardmarket-idProduct ophalen, met taal Engels, minimum NM, editie, 4+ verschillende vergelijkbare verkopers en winstberekening. Dit is een ONAFHANKELIJKE provider en geen officiele Cardmarket API. De provider vereist een eigen API-sleutel; zonder zo'n sleutel meldt de mobiele sectie: NOT_CONNECTED en 0 geverifieerde live deals. De sleutel staat alleen lokaal op WHCapital, versleuteld met Windows DPAPI.

Voor een eenmalige bronkoppeling: op https://app.api.sh/signup een account/key maken, de key beperken tot /cardmarket/v1/offers met maximaal 90 credits/maand, en op de WHCapital-PC op het bureaublad "WHC Card Hunter LIVE koppelen" openen. Nooit secrets in ChatGPT of in deze openbare repository zetten.

## Beperkingen
- Er is nog geen echte API.SH-bronacceptatie geweest, geen productiebewezen live aanbieding, en geen 100% geverifieerde koopdeal.
- Door vraagprijzen vergelijken kun je *potentiele marge* vinden maar geen gegarandeerde verkoopopbrengst. Werkelijke verzendkosten, printed setcode, edition, conditie en gerealiseerde verkopen moeten nog onafhankelijk gecontroleerd.
- De openbare Cardmarket dagfeed heeft geen seller, conditie, taal of verzendtarieven.
- Provider kan uitvallen en Cardmarket heeft zijn eigen voorwaarden; ongeoorloofde scraper/bypass wordt niet gebruikt.
- Automatische aankopen zijn niet toegestaan.

## Testresultaat
Op 8 november 2026 hebben de frontend en encryptie op Edge Chromium mobiel 390x844 gedraaid: kaartresultaten, zoeken, favorieten, winstcalculator, decryptie bij correcte sleutel, weigering bij verkeerde sleutel, nul JS fouten — PASS. De live-economie-parser slaagt op fictieve positieve en negatieve offertes; een echte vendor-response moet nog worden geverifieerd.

Voor exacte projectstatus zie de private CURRENT_STATE.md en NEXT_ACTION.md in de afzonderlijke repository infowhcapital/whc-card-hunter.
