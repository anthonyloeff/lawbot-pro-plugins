---
name: wetten
description: Nederlandse wetsartikelen opzoeken, actueel of op een historische peildatum. MOET actief worden bij het tekstcommando W: (bijv. "W: 6:162 BW") of Wettentool:, en bij vragen als "wat zegt artikel 7:658 BW", "tekst van art. 4:81 Awb", "gold dit artikel al in 2019", "welke versie van de wet".
---

# Wetsartikelen (W:)

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze

1. Geef de aanduiding ongewijzigd door aan `zoek_wet` via het veld `artikel` (`6:162 BW`, `art. 7:658 BW`, `Awb 4:81`, `310 Sr`); de server parseert zelf. Nooit een artikeltekst uit eigen kennis.
2. Toon de artikeltekst **integraal, per lid**, met citeertitel, geldigheidsdatum en de deeplink uit `bron_url` (format in onderdeel `formats`).
3. Historische vraag of overgangsrecht: geef `peildatum` mee; gebruik `wet_versies` om de relevante toestanden te vinden en vergelijk oude en nieuwe tekst naast elkaar, elk met eigen deeplink.
4. Meerdere kandidaten in de tool-output: stel één korte verduidelijkingsvraag met de kandidaten en hun BWBR-id's.

## Verdieping (op verzoek of bij duidelijke aanleiding)

- Rechtspraak bij dit artikel: `jurisprudentie_bij_artikel` (officiële citatiegraaf), top vijf met de hoogste instantie eerst, volledige analyse aanbieden via `haal_uitspraak`.
- Bedoeling van de wetgever: `wetsgeschiedenis` (memorie van toelichting) met kamerstuknummer en deeplink.

Na W: geen verdiepingsvragen (onderdeel `gedrag`).
