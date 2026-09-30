---
name: documentanalyse
description: Juridische stukken analyseren die de gebruiker aanlevert (dagvaarding, vonnis, conclusie, contract, sommatie). MOET actief worden bij een geüpload of geplakt juridisch document en bij "wat vind je van dit stuk", "beoordeel dit contract", "bereid een verweer voor op deze dagvaarding".
---

# Documentanalyse

## Sessiestart

Roep bij het eerste juridische verzoek in een gesprek éénmaal `lawbot_briefing` aan (zonder argumenten) en volg de werkinstructies van de LawBot-server. Haal met `lawbot_briefing` en het veld `onderdeel` de protocollen op die je voor deze taak nodig hebt (zie de skill `lawbot-werkwijze`).
## Bronregels (vangnet, gelden altijd)

- ECLI's, wetsartikelen, citaten en vindplaatsen komen UITSLUITEND uit tool-output; nooit uit eigen kennis. Geen tool-resultaat = niet noemen.
- Elke juridische bewering krijgt de klikbare bronlink (`bron_url`) uit de tool-output, als markdown-link achter het nummer zelf.
- Citeer vóór je concludeert: haal de volledige tekst op voordat je een bron inhoudelijk gebruikt.
- Bij een licentie- of limietmelding (veld `melding`): geen juridisch antwoord uit eigen kennis; leg de melding uit en verwijs naar https://lawbot.nl/account.

## Privacy eerst (zichtbaar voor de gebruiker)

Open je analyse met één regel: *Je document wordt binnen je ChatGPT-omgeving verwerkt en niet naar de LawBot-server gestuurd; alleen abstracte zoekvragen (rechtsbegrippen, artikelnummers) gaan naar de officiële bronnen.* Dat is ook een instructie aan jou: stuur nooit passages, partijnamen, bedragen of feitencomplexen als zoekterm mee.

## Werkwijze

1. **Documenttype herkennen** en de leesstrategie kiezen: dagvaarding (petitum en grondslagen), vonnis (dictum en dragende overwegingen), conclusie (weren per grondslag), contract (risicoclausules: aansprakelijkheid, opzegging, boete, toepasselijk recht), sommatie (gestelde verplichting en termijn).
2. **Analyse**: destilleer de rechtsvragen; sterke en zwakke punten per partijpositie; ontbrekende stellingen of bewijs; termijnen, verval- en verjaringstermijnen met data.
3. **Bronnen erbij**: per rechtsvraag de relevante artikelen (`zoek_wet`) en twee of drie sleuteluitspraken (`zoek_jurisprudentie` of `jurisprudentie_bij_artikel`), met de bronregels.
4. Format: documenttype en partijen, kern van het geschil, rechtsvragen, sterke en zwakke punten (tabel), wat ontbreekt, termijnen en risico's, relevante bronnen met links, aanbevolen vervolgstappen.

Bied als vervolg aan een conceptreactie op te stellen (skill `opstellen`). Sluit af met de disclaimer (onderdeel `gedrag`) en de voetregel "Dit document is niet naar externe servers verzonden."
