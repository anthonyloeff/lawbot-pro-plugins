---
name: uitspraak-analyse
description: Eén rechterlijke uitspraak volledig analyseren en samenvatten. MOET actief worden bij het tekstcommando S: gevolgd door een ECLI (bijv. "S: ECLI:NL:HR:2023:1371") of Samenvattingtool:, bij een geplakte rechtspraak.nl-link, een los ECLI of oud LJN, en bij "vat dit arrest samen", "analyseer deze uitspraak".
---

# Uitspraakanalyse (S:)

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze

1. Haal de **volledige tekst** op met `haal_uitspraak` (accepteert ECLI's, rechtspraak.nl-links en oude LJN's). Bij `paginas_totaal > 1` haal je álle pagina's op voordat je samenvat.
2. Alleen metadata (`alleen_metadata: true`)? Meld dat eerlijk, geef de inhoudsindicatie en de deeplink; verzin geen tekst.
3. Samenvatten doe je op basis van de volledige tekst, nooit alleen op de inhoudsindicatie. Citeer de dragende overweging **letterlijk** met het r.o.-nummer; parafrase mag aanvullend.
4. Verrijk uit de metadata: formele relaties (conclusie A-G, eerdere aanleg; bied aan die ook op te halen), vindplaatsen (NJ/AB), wetsverwijzingen met links.
5. Gebruik het format "Uitspraaksamenvatting" uit onderdeel `formats`.

Vervolgsuggesties: conclusie A-G of eerdere aanleg analyseren, vergelijkbare rechtspraak zoeken, het centrale wetsartikel opvragen. Na S: geen verdiepingsvragen (onderdeel `gedrag`).
