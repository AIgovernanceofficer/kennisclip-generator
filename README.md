# Kennisclip Generator — Handleiding

Maak een **korte educatieve gesproken presentatie** vanuit een Word-document of getypte tekst. Kies taal en stem, beluister de preview, en exporteer het resultaat als een presentatiebestand dat je kunt opnemen.

Een tool van **AIGovernanceofficer.nl** — volledig in de browser, geen installatie nodig.

---

## Inhoud

- [Wat kun je ermee?](#wat-kun-je-ermee)
- [Hoe lang mag een kennisclip zijn?](#hoe-lang-mag-een-kennisclip-zijn)
- [Aan de slag](#aan-de-slag)
- [Taal en stemkeuze](#taal-en-stemkeuze)
- [Exporteren en opnemen](#exporteren-en-opnemen)
- [Welke modellen en bronnen worden gebruikt?](#welke-modellen-en-bronnen-worden-gebruikt)
- [Je gegevens blijven privé](#je-gegevens-blijven-privé)
- [Iets werkt niet?](#iets-werkt-niet)
- [Licentie](#licentie)

---

## Wat kun je ermee?

- Een Word-document (.docx) uploaden als script voor een kennisclip
- Of een tekst direct intypen of plakken
- Taal kiezen (Nederlands of Engels) en een stem selecteren
- De spreeksnelheid aanpassen
- De presentatie in de browser beluisteren als voorbeeld
- Het resultaat exporteren als zelfstandig HTML-presentatiebestand, geschikt voor schermopname

---

## Hoe lang mag een kennisclip zijn?

Kennisclips zijn het effectiefst als ze kort en gefocust zijn. Als richtlijn:

| Lengte | Duur | Advies |
|---|---|---|
| 0–300 woorden | ±2 min | Microclip — ideaal voor één concept |
| 300–500 woorden | 3–4 min | **Perfecte kennisclip** ✓ |
| 500–700 woorden | 4–6 min | Goed voor complexere onderwerpen |
| 700–850 woorden | 6–7 min | Acceptabel, maar overweeg opdelen |
| 850–1000 woorden | 7–8 min | Aan de limiet — studenten haken sneller af |
| > 1000 woorden | > 8 min | Te lang — splits op in meerdere clips |

De tool berekent automatisch de geschatte duur op basis van de spreeksnelheid en geeft een kleursindicator (groen/geel/rood).

---

## Aan de slag

1. **Open de tool** in Google Chrome of Microsoft Edge.
2. **Upload een Word-bestand** (.docx) via het uploadvak, of typ/plak je script in het tekstveld.
3. **Stel de titel** van de kennisclip in (dit verschijnt op de dia's).
4. **Kies de taal** (Nederlands of Engels) en selecteer een stem.
5. **Pas de spreeksnelheid** aan (0.7× = langzamer, 1.5× = sneller).
6. Klik **▶ Afspelen** om een voorbeeld te beluisteren in de browser.
7. Klik **💾 Exporteer als presentatie** om een HTML-bestand te downloaden.
8. Open het geëxporteerde bestand en neem je scherm op (zie hieronder).

---

## Taal en stemkeuze

De beschikbare stemmen zijn afhankelijk van je browser en besturingssysteem.

**Nederlands:** gebruikt de Nederlandse stemmen die op je apparaat zijn geïnstalleerd. Op Windows met Chrome of Edge zijn dit doorgaans Microsoft Neural TTS-stemmen van uitstekende kwaliteit (bijv. *Microsoft Fien Online*, *Microsoft Frank Online*). De ⭐-markering geeft de hoogste kwaliteit aan.

**Engels:** zelfde principe — Chrome en Edge op Windows bieden meerdere hoogwaardige Engelse stemmen (bijv. *Microsoft Libby*, *Google UK English Female*).

> **Tip:** gebruik bij voorkeur Chrome of Edge op Windows voor de beste stemkwaliteit. In andere browsers of op andere systemen kunnen de stemmen robochtiger klinken.

---

## Exporteren en opnemen

De exporteerknop genereert een **zelfstandig HTML-presentatiebestand** (.html). Dit bestand:
- Bevat alle tekst, de opmaak, en de spreekcode
- Werkt zonder internetverbinding (stemmen van het apparaat)
- Opent in de browser met een grote Start-knop

**Zo neem je het op:**

1. Open het geëxporteerde bestand in Chrome of Edge.
2. Klik op **▶ Start Kennisclip**.
3. Start je schermopname:
   - **Windows:** Windows Game Bar (Win + G → Record)
   - **Teams / Zoom:** scherm delen → opnemen
   - **OBS Studio:** gratis opnamesoftware
   - **Kaltura / Panopto:** presentatie opnemen via de browser
4. Wacht tot de presentatie klaar is, stop de opname.

> Druk op **Escape** om de presentatie te stoppen en terug te gaan naar het startscherm.

---

## Welke modellen en bronnen worden gebruikt?

### 🗣️ Spraaksynthese — Web Speech API

De stemgeneratie gebeurt via de **Web Speech API** — een ingebouwde browserstandaard. De stemmen zelf komen van het besturingssysteem of de browser:

- **Windows (Chrome/Edge):** Microsoft Neural TTS-stemmen — hoge kwaliteit, natuurlijk klinkend, door Microsoft ontwikkeld en lokaal beschikbaar als onderdeel van Windows
- **Mac (Safari/Chrome):** Apple-stemmen en Google-stemmen
- **Android Chrome:** Google TTS-stemmen

De Web Speech API is een open webstandaard (W3C), gedocumenteerd op:
[https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Speech_API)

Er worden **geen externe AI-modellen geladen** — de stemmen zijn al aanwezig op het apparaat van de gebruiker.

### 📄 Word-lezer — Mammoth.js

Het inlezen van Word-bestanden (.docx) gebeurt via **Mammoth.js**, een open-source JavaScript-bibliotheek.

- **Maker:** Ashley Hewson
- **Licentie:** BSD 2-Clause (open source)
- **Bron:** [https://github.com/mwilliamson/mammoth.js](https://github.com/mwilliamson/mammoth.js)
- **Hoe:** Mammoth.js leest het .docx-bestand lokaal in de browser en extraheert de tekst. Het bestand wordt nergens naartoe gestuurd.

---

## Je gegevens blijven privé

- Je Word-bestand en tekst worden **uitsluitend lokaal** in je browser verwerkt.
- Er wordt niets naar een server gestuurd en niets opgeslagen.
- De spraaksynthese gebruikt stemmen die al op je apparaat staan — ook die audio verlaat je apparaat niet.
- Het geëxporteerde presentatiebestand bevat alleen de tekst die jij hebt ingevoerd.

---

## Iets werkt niet?

- **Geen stemmen beschikbaar** → gebruik Google Chrome of Microsoft Edge; zorg dat je taalinstellingen (Nederlands of Engels) in Windows zijn geactiveerd.
- **De stem klinkt robotachtig** → kies een stem met het ⭐-teken (Microsoft Neural of Google-stem); deze zijn van hogere kwaliteit.
- **Het Word-bestand wordt niet herkend** → sla het op als .docx (niet als .doc of .odt).
- **De tekst verschijnt niet als losse dia's** → gebruik alinea-afbrekingen (Enter + Enter) tussen de secties in je Word-document. Elke alinea wordt een aparte dia.
- **De presentatie speelt niet automatisch** → klik op de knop "Start Kennisclip" en zorg dat je browser geluid toestaat voor de pagina.

---

## Licentie

[![Licentie: CC BY-NC-ND 4.0](https://img.shields.io/badge/Licentie-CC%20BY--NC--ND%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.nl)

© 2026 **AIGovernanceofficer.nl** — Creative Commons Naamsvermelding-NietCommercieel-GeenAfgeleideWerken 4.0 (CC BY-NC-ND 4.0).

Volledige tekst: <https://creativecommons.org/licenses/by-nc-nd/4.0/deed.nl>
