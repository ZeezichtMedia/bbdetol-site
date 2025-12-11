---
description: dit is het plan om diepgaand onderzoek te doen naar een b&b of camping voor info voor de website.
---

Master Implementatie Plan: Diepgaand Onderzoek & Scraping
Dit document beschrijft de gestandaardiseerde methodologie ("Het Beaufõrt Protocol") voor het volledig in kaart brengen van een entiteit (B&B, hotel, bedrijf, of locatie) door middel van AI-gestuurd onderzoek en scraping.

Doel
Het genereren van een compleet, accuraat en rijk informatieprofiel in Markdown-formaat, door het combineren van diverse online bronnen (officiële kanalen, reviews, social media, nieuws, vastgoeddata).

Fase 1: Initiële Verkenning & Bronidentificatie
Doel: Het vinden van alle relevante digitale voetafdrukken.

Stap 1.1: Brede Zoekopdrachten
Start met algemene zoektermen om de primaire bronnen te vinden.

"[Naam Entiteit] [Plaats]"
"[Naam Entiteit] [Plaats] website"
"[Naam Entiteit] [Plaats] contact"
Stap 1.2: Platform Specifieke Identificatie
Zoek specifiek naar aanwezigheid op grote platforms.

Accommodaties: Airbnb, Booking.com, Bedandbreakfast.nl, Natuurhuisje.
Socials: Facebook, Instagram, LinkedIn.
Zakelijk/Vastgoed: KvK, Funda (indien relevant/te koop), Kadaster.
Reviews: Google Maps, TripAdvisor.
Fase 2: Diepte-Onderzoek & Data Extractie
Doel: Het systematisch 'lezen' en extraheren van specifieke details uit de gevonden bronnen.

Stap 2.1: Officiële Kanalen (Website)
Over ons / Historie: Wie zijn de eigenaren? Wat is het verhaal?
Aanbod: Kamertypes, prijzen, arrangementen.
Faciliteiten: Wat is inbegrepen? (Wifi, ontbijt, parkeren).
Huisregels: Inchecktijden, huisdierenbeleid.
Stap 2.2: Externe Validatie (Reviews & OTAs)
Airbnb/Booking: Check de voorzieningenlijst (vaak gedetailleerder dan eigen site).
Reviews: Scan op terugkerende thema's (e.g., "geweldig ontbijt", "gehorige kamers", "gastvrije eigenaren"). Haal de gemiddelde score op.
Foto's: Analyseer foto's voor sfeerbeschrijvingen en niet-vermelde faciliteiten (e.g., koffiemachine op kamer).
Stap 2.3: Social Media & Actualiteit
Facebook/Instagram: Check recente posts voor sfeer, evenementen, of tijdelijke sluitingen.
Tone of Voice: Hoe communiceert de eigenaar? (Formeel vs. informeel).
Fase 3: Context & Verrijking (De "Beaufõrt" Touch)
Doel: Het profiel uniek maken door context toe te voegen die niet direct op de site staat.

Stap 3.1: Locatie & Omgeving
Zoek naar bezienswaardigheden in de buurt (loopafstand/fietsafstand).
Zoek naar natuurgebieden (e.g., Nationaal Parken).
Zoek naar lokale horeca.
Stap 3.2: Geschiedenis & Pand
Zoek op adres + "geschiedenis" of "monument".
Zoek op Funda/Vastgoed sites voor bouwjaar, perceeloppervlakte en bouwkundige details.
Stap 3.3: Gaten Vullen
Ontbreekt er info? Doe specifieke zoekopdrachten:
"[Naam] ontbijttijden"
"[Naam] e-bike huren"
"[Naam] eigenaar naam"
Fase 4: Synthese & Rapportage
Doel: Alles samenvoegen in het Master Markdown Template.

Structuur van het Output Bestand
Gebruik onderstaande structuur voor het eindrapport.

# [Naam Entiteit] - [Plaats], [Land]
## Algemene Informatie
**Naam:** ...
**Type:** ...
**Locatie:** [Adres]
**Contact:** [Telefoon/Email]
## Contactinformatie
- **Website:** [URL]
- **Socials:** [Links]
- **Platformen:** [Airbnb/Booking links]
## Het Pand & Geschiedenis
*Beschrijving van het gebouw, bouwjaar, architectuur en sfeer.*
## Aanbod & Faciliteiten
### Accommodaties
*Beschrijving van kamers/units.*
### Voorzieningen
- [ ] Wifi
- [ ] Parkeren
- [ ] Ontbijt
- ...
## Gastenervaring & Reviews
**Rating:** X.X/5 (Bron)
*Samenvatting van wat gasten zeggen.*
## Omgeving
*Wat is er te doen in de buurt?*
## Unieke Kenmerken (USP's)
*Wat maakt deze plek uniek? (Filosofie, specifieke services).*
---
*Informatie verzameld: [Datum]*
*Bronnen: [Lijst]*
Instructies voor de AI Agent
Wanneer je deze taak uitvoert:

Wees Grondig: Stop niet bij de eerste hit. Cross-reference informatie.
Wees Specifiek: Noteer details zoals "gratis parkeren" of "ontbijt inbegrepen" expliciet.
Bronvermelding: Houd bij waar je info vandaan haalt (voor interne verificatie).
Format: Lever altijd op in schoon Markdown formaat, klaar voor gebruik.