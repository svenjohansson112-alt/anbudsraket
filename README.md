# AnbudsRaket AI – Pilot

Kostnadsfri pilot för små företag som vill hitta och prioritera offentliga upphandlingar inom exempelvis städning, lokalvård, fönsterputs och måleri.

## Så fungerar piloten
- TED-data hämtas automatiskt via GitHub Actions och sparas i `data/notices.json`.
- Webbplatsen läser den publicerade datan, filtrerar efter sökord och visar relevanssorterade annonser.
- Användare kan filtrera på publiceringsperiod och max antal resultat.
- Frivilligt platsfilter matchar text i rubrik och köparnamn. Det är **inte** en verifierad geografisk filtrering.
- Deadline visas om den finns i TED-datan, med antal dagar kvar/passerad.
- CPV-koder visas när de finns.
- CSV-export och enkel kalkyl för intäkt, personalkostnad och uppskattat överskott.

## Automatiserad datainsamling
GitHub Actions kör ett TED Search API-anrop enligt workflow-schemat och vid manuell start. Aktuell pipeline har lyckats köra och publicera datan. Datan är begränsad till TED och en urvalsperiod; den omfattar inte alla svenska nationella upphandlingar.

## Begränsningar
Detta är en pilot, inte en färdig betaltjänst:
- ingen inloggning eller personliga bevakningar
- inga e-postnotiser
- ingen fullständig svensk nationell täckning
- ingen AI-granskning av kompletta upphandlingsdokument
- ingen betalning eller kundsupportprocess
- relevanspoäng är heuristik och inte bedömning av kvalificeringskrav
- deadline kan saknas i data; kontrollera alltid originalannonsen

## Nästa utvecklingssteg
1. Testa datans kvalitet och relevans med riktiga småföretagare.
2. Lägg till bättre svenska sökord, CPV-förklaringar och geografisk filtrering baserad på strukturerade data.
3. Lägg till detaljerad annonsöversikt och checklista för kvalificeringskrav.
4. Bygg opt-in bevakningar när en robust och kostnadsfri lösning är möjlig.
5. Validera användarbehov och betalningsvilja innan betalning aktiveras.

## Källa
TED: https://ted.europa.eu/
