---
name: opstellen
description: Concepten van juridische stukken opstellen (memo, conclusie van antwoord, sommatie of ingebrekestelling) met bronverwijzingen. MOET actief worden bij "schrijf een memo over", "stel een sommatie op", "maak een conclusie van antwoord", "stel op", en als vervolg op een documentanalyse.
---

# Stukken opstellen

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze

1. **Stukstype bepalen** en het skelet uit `templates/` in deze skill-map gebruiken (`memo.md`, `conclusie-van-antwoord.md`, `sommatie.md`). Vraag vooraf kort de huisstijlgegevens: kantoornaam en ondertekenaar, wederpartij, dossierkenmerk, gewenste toon.
2. **Eerst onderzoek, dan schrijven.** Elk juridisch standpunt steunt op tool-geverifieerde bronnen (skill `juridisch-onderzoek`); niet-geverifieerde verwijzingen zijn verboden, liever een [PM]-merkteken dan een verzonnen vindplaats.
3. **Opbouw**: genummerde randnummers; verwijzingen als voetnoten met volledige vindplaats en link (ECLI met deeplink, artikel met jci-link). Memo's: conclusie vooraf, analyse, risico's en tegenargumenten, advies. Processtukken: feiten en weren strikt scheiden. Sommaties: concrete verplichting, redelijke termijn met datum, aangekondigd rechtsgevolg.
4. **Levering**: als downloadbaar bestand (Word of PDF) wanneer de omgeving dat kan, anders nette markdown; zeg erbij wat je hebt gedaan.
5. **Concept-markering** onderaan het document: *Concept, gegenereerd met LawBot Pro (Litic). Controle door een advocaat is vereist vóór verzending of indiening.*
6. **Waarmerk aanbieden** na oplevering: skill `waarmerk`.
