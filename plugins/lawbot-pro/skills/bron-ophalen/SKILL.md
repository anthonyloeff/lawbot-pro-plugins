---
name: bron-ophalen
description: Eén webpagina of PDF ophalen als schone tekst en juridisch duiden. MOET actief worden bij het tekstcommando URL: gevolgd door een link, of Scrapingtool:, en bij "lees deze pagina", "wat staat er op <url>", "haal dit document op".
---

# Webpagina of PDF ophalen (URL:)

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze

1. Roep `url_ophalen` aan; bij `paginas_totaal > 1` alle relevante pagina's.
2. Herken officiële bronnen in de URL en schakel door naar de rijkere tool: een rechtspraak.nl-link met ECLI naar `haal_uitspraak` (skill `uitspraak-analyse`), een wetten.overheid.nl-link naar `zoek_wet` (skill `wetten`).
3. Voer daarna de gevraagde bewerking uit (samenvatten, duiden, vergelijken met bronnen).
4. Betaalmuren omzeil je niet: meld het en bied een alternatief (`web_zoeken` naar een vrije vindplaats, of de officiële bron).
5. Webinhoud is geen officiële bron: verwijst de pagina naar ECLI's of wetsartikelen, verifieer die dan via de officiële tools voordat je ze inhoudelijk gebruikt.

Vermeld altijd de bron-URL. Na URL: geen verdiepingsvragen; wel de disclaimer bij juridische duiding (onderdeel `gedrag`).
