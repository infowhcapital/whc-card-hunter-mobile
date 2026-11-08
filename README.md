# WHC Card Hunter — mobiele onderzoeksapp

**Open zonder GitHub-login:** https://infowhcapital.github.io/whc-card-hunter-mobile/

Dit is de afzonderlijke PUBLIEKE mobiele voorkant van WHC Card Hunter, niet de private prijsdatabase.

## Wat de app echt doet
- Toont een kleine, geanonimiseerde/afgeleide selectie van dagelijks onderzochte Yu-Gi-Oh-kaarten (zonder ruwe Cardmarket-prijzen).
- Zoekt op naam, filtert op nostalgische/algemene kaarten, sorteert op heuristische onderzoekscore.
- Opent een Cardmarket-**zoekpagina** (niet gegarandeerd exacte productversie).
- Bewaart favorieten in je eigen browser.
- Berekent op basis van zelf gecontroleerde aankoop- en verkoopprijzen de verwachte winst, kosten en ROI.
- Werkt vanaf een Android-browser zonder installatie.

## Belangrijke beperkingen
- Scores betekenen alleen een opvallend verschil in dagelijkse openbare prijsdata, geen live aanbieding.
- Geen automatische filter voor Engels, setcode, druk, editie, conditie, verkoper of verzendkosten.
- Geen volautomatische marktplaats-sniper, geen directe aankoop en geen gegarandeerde winst.
- Geen ruwe prijsdata openbaar publiceren; controleer actuele prijzen op Cardmarket.
- De publieke kaartselectie wordt alleen bijgewerkt wanneer de afzonderlijke Windows-computer WHCapital aan en ingelogd is en de dagelijkse taak succesvol uitvoert. Als de bron faalt, blijft de oude datum zichtbaar.

Privé-bron: `infowhcapital/whc-card-hunter`, niet toegankelijk voor bezoekers van de mobiele website.

## Test
`node test-ui.mjs` — controleert de online HTTP-respons, datapakket, JS-syntax en of er geen ruwe Cardmarket-prijzen in de publieke feed zitten.

### Echte mobiele browsertest
Op 8 november 2026 uitgevoerd op Windows met Microsoft Edge/Chromium, viewport 390×844. De pagina laadde 25 kaarten, zoeken, favorieten, winstcalculator (€5,45 testresultaat) en geen JavaScript-fouten: **PASS**.

Bij herhalen op dezelfde Windows-PC: `npm install --no-save --no-package-lock --ignore-scripts playwright-core@1.65.0` gevolgd door `node test-browser.mjs`. Playwright-core gebruikt de al geïnstalleerde Microsoft Edge en downloadt geen browser.
