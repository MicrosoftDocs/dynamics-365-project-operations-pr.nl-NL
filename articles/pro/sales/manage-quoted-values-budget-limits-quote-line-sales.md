---
title: Overzicht van projectgebaseerde prijsopgaveregels
description: Dit onderwerp bevat informatie over het gebruik van op projectgebaseerde prijsopgaveregels voor projectwerk.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369865"
---
# <a name="project-based-quote-lines-overview"></a>Overzicht van projectgebaseerde prijsopgaveregels 

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Projectgebaseerde prijsopgaveregels zijn ontworpen om te helpen bij het inschatten van het projectwerk voor een opdracht. De structuur van een projectgebaseerde prijsopgaveregel wordt voor projectramingen uitgebreid met de volgende concepten:

- Factureringsmethode
- Project- en taaktoewijzing
- Inbegrepen transactieklassen
- Niet-overschrijdingslimiet
- Instellingen voor toerekenbaarheid
- Schatting met gegevens van prijsopgaveregels
- Prijsopgaveregelklanten

De volgende tabel bevat informatie over de velden op het tabblad **Algemeen** van projectgebaseerde prijsopgaveregels. Deze velden helpen bij het opzetten van de basis voor een gedetailleerde, complete schatting voor projectwerk.

| **Veld** | **Beschrijving** | **Downstreamimpact** |
| --- | --- | --- |
| Meetcriterium | De naam van de prijsopgaveregel waarmee u de discrete component kunt identificeren van de prijsopgave die wordt geschat. | Gekopieerd naar de projectcontractregel die is gemaakt op basis van deze prijsopgaveregel wanneer de prijsopgave wordt geaccepteerd. |
| Factureringsmethode | In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het overeenkomstige veld op de verkoopkansregel. Dit veld bevat de twee belangrijkste aanbestedingsmodellen die worden ondersteund door Dynamics 365 Project Operations.</br>- Vaste prijs</br>- Tijd en materiaal.| Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Project | Gebruik dit optionele veld om het project te identificeren dat wordt gebruikt om het werk voor deze opdracht af te leveren. Wanneer een project wordt toegewezen aan een prijsopgaveregel, is dit handig bij het instellen van toerekenbare taken en ook bij het opnemen van een projectgebaseerde schatting op de prijsopgaveregel als details van de prijsopgave. Als een project niet wordt toegewezen aan een projectgebaseerde prijsopgaveregel, moet de schatting handmatig worden gemaakt door elk detail van de prijsopgave te creëren. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald.|
| Opgenomen taken | Geeft aan of deze prijsopgaveregel wordt gebruikt voor alle of enkele projecttaken voor het geselecteerde project. Dit veld kan de volgende waarden hebben:</br>- Alle projecttaken</br>- Alleen geselecteerde projecttaken</br>Een lege waarde in dit veld is gelijk aan de optie **Alle projecttaken**. | Wanneer **Alleen geselecteerde projecttaken** wordt geselecteerd op de projectpagina, kunt u op het tabblad **Factureringsinstellingen van taak** specifieke taken selecteren om ze aan deze prijsopgaveregel te koppelen. Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Tijd opnemen | Een waarde van **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde **Nee** geeft aan of de tijdtransacties of arbeidskosten niet worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde **Ja** geeft aan of de tijdtransacties of arbeidskosten worden opgenomen in de schatting op deze prijsopgaveregel. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Onkosten opnemen | Een waarde van **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde **Nee** geeft aan of de onkosten niet worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde **Ja** geeft aan of de onkosten worden opgenomen in de schatting op deze prijsopgaveregel. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Materiaal opnemen | Een waarde van **Ja**/**Nee** geeft aan of materiaalkosten voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde van **Nee** geeft aan dat de materiaalkosten niet worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde van **Ja** geeft aan dat de materiaalkosten wel worden opgenomen in de schatting op deze prijsopgaveregel. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Tarief opnemen | Een waarde van **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde van **Nee** geeft aan dat de vergoedingen niet worden opgenomen in de schatting op deze prijsopgaveregel. Een waarde van **Ja** geeft aan dat de vergoedingen wel worden opgenomen in de schatting op deze prijsopgaveregel. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Bedrag van prijsopgave | Dit is het bedrag dat aan de klant in het vooruitzicht wordt gesteld voor al het werk dat op deze projectgebaseerde offerteregel wordt voorspeld. In een prijsopgave die wordt gemaakt op basis van een verkoopkans, wordt deze waarde gekopieerd uit het veld **Klantbudget** op de verkoopkansregel. Wanneer de projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de prijsopgaveregeldetails. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Geschatte belasting | Dit is een bewerkbaar veld voor de gebruiker om het geschatte belastingbedrag op de prijsopgaveregel toe te voegen. Wanneer een projectgebaseerde prijsopgaveregel regeldetails bevat, wordt dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de prijsopgaveregeldetails. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Bedrag van prijsopgave na belasting | Dit veld is het prijsopgaveregelbedrag na belasting en is alleen-lezen. Het bedrag in dit veld wordt berekend als *Geoffreerd bedrag + belasting*. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Niet-overschrijdingslimiet | Dit veld kan worden bewerkt en is alleen beschikbaar op projectgebaseerde prijsopgaveregels met de factureringsmethode **Tijd en materiaal**. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |
| Klantbudget | Dit veld is bewerkbaar en wordt gekopieerd uit het overeenkomstige veld op de verkoopkansregel als de prijsopgave wordt gemaakt op basis van een verkoopkans. | Deze waarde wordt gekopieerd naar de projectcontractregel die wordt gemaakt op basis van deze prijsopgaveregel wanneer de order wordt binnengehaald. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Validatieregels voor velden op het tabblad Algemeen van projectgebaseerde prijsopgaveregels

**Regel 1**: als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken**, wordt een project opgenomen in de prijsopgaveregel.

**Regel 2**: als het veld **Inbegrepen taken** leeg is, of als het is ingesteld op **Alle projecttaken** kunnen een project en een bepaalde transactieklasse alleen worden opgenomen in één projectgebaseerde prijsopgaveregel van een prijsopgave.

**Regel 3**: als het veld **Inbegrepen taken** is ingesteld op **Alleen geselecteerde projecttaken** kunnen een project en een bepaalde transactieklasse worden opgenomen in meerdere projectgebaseerde prijsopgaveregels van een prijsopgave.

**Regel 4**: als een verkoopkans meerdere prijsopgaven bevat, kunnen er regels van verschillende prijsopgaven zijn die allemaal naar hetzelfde project verwijzen en dezelfde transactieklasse bevatten.

**Regel 5**: als de prijsopgaven niet tot dezelfde verkoopkans behoren, kunnen ze niet hetzelfde project en dezelfde transactieklasse bevatten.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Verkoopkans</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Offerte</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Prijsopgaveregel</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Opgenomen taken</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Tijd opnemen</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Onkosten opnemen</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Materiaal opnemen</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Opnemen</strong>
                </p>
                <p>
                    <strong>Tarief</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Geldig/ongeldig</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Reden</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtreding van regel 2. Tijd, onkosten en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Geen </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtreding van regel 2. Tijd, materiaal en vergoedingen voor het P1-project zijn opgenomen op de prijsopgaveregels QL1 en QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Geen </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Tijd, materiaal en vergoedingen voor het P1-project zijn opgenomen in QL1 <br>
Onkosten voor het P1-project zijn opgenomen in QL2 <br>
Geen overlap in wat wordt opgenomen op elke prijsopgaveregel en dus geldig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Geen </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Geen </p>
            </td>
            <td width="41" valign="top">
                <p>
Geen </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Overtreding van regel 2 </p>
                <p>
Q1 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1 </p>
                <p>
QL2 omvat tijd, onkosten en vergoedingen voor het hele project P1 en overlapt daarom met wat is opgenomen in Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Volgens regel 3, </p>
                <p>
Q1 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1.
                </p>
                <p>
QL2 omvat tijd, materiaal, onkosten en vergoedingen voor een subset van taken in project P1.
                </p>
                <p>
De enige aanvullende validatie betreft de subset van taken in QL1, die verschilt van de subset van taken in QL2 om ervoor te zorgen dat er geen overlapping is. Dit wordt gedaan door het systeem wanneer taken worden gekoppeld.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projecttaken of leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Geldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per regel 5 zijn Q1 en Q2 twee prijsopgaven voor dezelfde verkoopkans, dus ze kunnen beide een schatting maken voor dezelfde componenten van een project.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projecttaken of leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projecttaken of leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per regel 4 zijn Q1 en Q2 twee prijsopgaven voor verschillende verkoopkansen, dus ze kunnen niet beide een schatting maken voor dezelfde componenten van hetzelfde project.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
KW1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Alle projecttaken of leeg </p>
            </td>
            <td width="45" valign="top">
                <p>
Ja </p>
            </td>
            <td width="46" valign="top">
                <p>
Ja </p>
            </td>
            <td width="43" valign="top">
                <p>
Ja </p>
            </td>
            <td width="41" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
