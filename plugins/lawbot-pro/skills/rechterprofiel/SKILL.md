---
name: rechterprofiel
description: Feitelijk profiel van een Nederlandse rechter of raadsheer. MOET actief worden bij het tekstcommando R: (bijv. "R: mr. J. de Groot") of Rechtertool:, en bij "wie is rechter …", "wat weet je over raadsheer …".
---

# Rechterprofiel (R:)

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Werkwijze

Roep `rechter_profiel` aan met voorletters en achternaam (strip een aanhef zoals "mr."). Bij naamgenoten disambigueer je via gerecht of periode voordat je rapporteert; gok nooit zelf een persoon. Gebruik het format "Rechterprofiel" uit onderdeel `formats`.

## Fairness (essentieel)

- Het profiel is **beschrijvend, niet voorspellend**. Geen kwalificaties ("streng", "eiservriendelijk") en geen strategieadvies op basis van de persoon; zaakstoedeling en zaakzwaarte maken zulke vergelijkingen ondeugdelijk. Neem de kanttekening uit de tool-output over.
- De index bevat alleen gepubliceerde uitspraken, een fractie van iemands werk. Benoem dat.
- Nevenbetrekkingen komen uitsluitend uit `nevenbetrekkingen_register` (officieel rechtersregister): toon ze zoals aangeleverd, met ingangsdatum en of de functie bezoldigd is. Staat er `kandidaten`, vraag dan de gebruiker te preciseren. Ontbreekt het register, verwijs dan naar `register_url`. Nooit nevenbetrekkingen uit webresultaten of geruchten.

Na R: geen verdiepingsvragen (onderdeel `gedrag`).
