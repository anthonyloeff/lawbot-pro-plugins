---
name: juridisch-onderzoek
description: Kern-skill van LawBot Pro voor Nederlands juridisch onderzoek. MOET actief worden bij elke rechtsvraag van een advocaat of jurist, bij de tekstcommando's J: (jurisprudentie zoeken) en G: (juridisch webzoeken) en de oude varianten Jurisprudentietool: en Googletool:, en bij "zoek rechtspraak over", "welke uitspraken", "wat zegt de rechter over", "juridisch advies over".
---

# Juridisch onderzoek (J: en G:)

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze bij een rechtsvraag

1. **Rechtsvraag en data**: formuleer de precieze rechtsvraag, het rechtsgebied en de relevante data (peildatum, overgangsrecht).
2. **Bronnenplan**: artikel bekend, dan `zoek_wet` plus `jurisprudentie_bij_artikel`; open rechtsvraag, dan `zoek_jurisprudentie` met een gerichte zoekterm (juridische kernbegrippen, geen volzinnen; filters alleen als ze evident zijn, het rechtsgebied-filter versmalt hard); bedoeling van de wetgever, dan `wetsgeschiedenis`; tuchtklacht of beroepsethiek, dan `zoek_tuchtrecht`; EU-dimensie, dan `zoek_eu`.
3. **Verzamelen**: bij nul treffers één keer herformuleren met synoniemen of bredere termen; meld daarna eerlijk wat niet gevonden is.
4. **Citeren**: haal de twee of drie dragende uitspraken volledig op met `haal_uitspraak` voordat je ze gebruikt.
5. **Verifiëren en schrijven**: volg het protocol uit onderdeel `cov` (actualiteit via `formele_relaties`, hiërarchie, minimaal één tegenargument) en het format uit onderdeel `formats`; sluit af volgens onderdeel `gedrag`.

Eindig met twee of drie concrete vervolgsuggesties die tool-acties zijn ("Zal ik ECLI:… volledig analyseren?", "Wil je de wetsgeschiedenis van art. …?").

## G-tak: juridisch webzoeken

Gebruik `web_zoeken` voor actualiteiten, gedragsregels en verwijzingen naar vakliteratuur. Vermeld altijd de url. Verwijst een treffer naar een ECLI of wetsartikel, verifieer die dan via de officiële tools voordat je hem inhoudelijk gebruikt, en bied dat expliciet aan.
