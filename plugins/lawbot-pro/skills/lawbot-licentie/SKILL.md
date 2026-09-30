---
name: lawbot-licentie
description: Verbinden, licentie en probleemdiagnose van LawBot Pro. MOET actief worden bij "licentie", "inloggen", "verbinden", "sleutel", "licentiesleutel", "proefperiode", "abonnement", "LawBot werkt niet", elke licentie- of limietmelding uit een LawBot-tool, en bij het allereerste gebruik van de plugin.
---

# LawBot Pro: verbinden en licentie

## Statuscheck

Roep `licentie_status` aan en presenteer het resultaat menselijk: plan, status, verbruik vandaag en de beheerlink https://lawbot.nl/account. Prijzen noem je niet; die staan op lawbot.nl.

## Verbinden (eerste gebruik)

Elke advocaat werkt met een **eigen** LawBot Pro-licentie. Bij het eerste gebruik van een tool opent ChatGPT de LawBot-inlogpagina (portal.litic.ai):
1. Vul het e-mailadres van je licentie in en voer de code in die je per e-mail ontvangt (tien minuten geldig); of
2. plak je licentiesleutel (begint met `lbp_`).
Daarna is de plugin verbonden; de sessie loopt stilzwijgend door (verlengt zichzelf).

## Scenario's

- **Geen of ongeldige licentie** (`license_invalid`, `token_expired`): geen juridisch antwoord uit eigen kennis. Leg uit dat een bestaande LawBot Pro-licentie nodig is en dat de kantoorbeheerder of Litic (support@litic.ai) een licentie uitgeeft; informatie op https://lawbot.nl.
- **Verlopen of betaling mislukt** (`license_expired`, `license_past_due`): gegevens blijven bewaard; regelen via https://lawbot.nl/account, daarna werkt alles direct weer.
- **Limiet bereikt** (`rate_limited`): even wachten (per minuut) of later opnieuw (per dag); bij herhaling melden bij de kantoorbeheerder.
- **Server onbereikbaar** (technische fout, geen licentiefout): "De LawBot-server is tijdelijk niet bereikbaar; dit ligt niet aan je licentie. Probeer het over enkele minuten opnieuw."

## Mini-rondleiding (bij eerste gebruik of op verzoek)

| Commando | Doet | Voorbeeld |
|---|---|---|
| `W:` | wetsartikel (ook historisch) | `W: 6:162 BW` |
| `J:` | jurisprudentie zoeken | `J: verjaring verborgen gebreken` |
| `S:` | uitspraak volledig analyseren | `S: ECLI:NL:HR:2023:1371` |
| `R:` | rechterprofiel | `R: J.A.R. van Eijsden` |
| `G:` | juridisch webzoeken | `G: NOvA gedragsregel 12` |
| `URL:` | webpagina of PDF ophalen | `URL: https://…` |
| `V5:` | interview (vijf vragen), daarna advies | `V5: incassoadvies` |
| natuurlijke taal | wetsgeschiedenis, tuchtrecht, EU-recht, rechtspraak bij een artikel, documentanalyse, stukken opstellen, waarmerk, partnercode | |

Voor de volledige functietekst: haal onderdeel `functies` op met `lawbot_briefing` en toon die letterlijk.
