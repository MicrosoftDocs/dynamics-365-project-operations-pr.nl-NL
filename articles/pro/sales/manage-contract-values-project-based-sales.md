---
title: Overzicht van projectgebaseerde contractregels
description: Dit onderwerp bevat informatie over het werken met projectgebaseerde contractregels.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369910"
---
# <a name="project-based-contract-lines-overview"></a>Overzicht van projectgebaseerde contractregels

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectgebaseerde contractregels in Dynamics 365 Project Operations zijn ontworpen om de schattings- en factureringsovereenkomsten te bevatten voor specifieke onderdelen van projectwerk bij een opdracht. De structuur van een projectgebaseerde contractregel wordt voor projectschattingen en factureringsscenario's uitgebreid met de volgende concepten:

- Factureringsmethode
- Project- en taaktoewijzing
- Inbegrepen transactieklassen
- Niet-overschrijdingslimiet
- Instellingen voor toerekenbaarheid
- Schattingen met behulp van contractregeldetails
- Contractregelklanten

De volgende tabel bevat de velden op het tabblad **Algemeen** met projectgebaseerde contractregels die helpen bij het opzetten van de basis voor een gedetailleerde schatting en factureringsregelingen voor projectgebaseerd werk.

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| **Name** | Naam van de contractregel. Hiermee wordt de afzonderlijke component aangegeven van het contract waarvoor de schatting van toepassing is. Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van een overeenkomstige waarde van de projectgebaseerde offerteregel. | De naam die is gekopieerd naar de projectfactuurregel die is gemaakt op basis van deze contractregel wanneer de factuur wordt gemaakt. |
| **Factureringsmethode** | Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel. Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations:</br>- **Vaste prijs**</br>- **Tijd- en materiaalverbruik** | Op basis van de factureringsmethode van de contractregel waarnaar wordt verwezen, wordt de daadwerkelijke transactie verwerkt. Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode voor tijd en materiaal heeft, worden records met de werkelijke waarden voor kosten en niet-gefactureerde verkoop gemaakt. Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode tegen een vaste prijs heeft, wordt alleen een werkelijke waarde voor kosten gemaakt. |
| **Project** | Gebruik dit veld om het project aan te geven dat wordt gebruikt om het werk voor deze opdracht af te leveren. | Deze waarde wordt gebruikt in combinatie met **Opgenomen taken** en **Opgenomen transactieklassen** om de contractregelverwijzing voor een werkelijke of schattingsregelrecord om te zetten. |
| **Opgenomen taken** | Geeft aan of deze contractregel alle projecttaken voor het geselecteerde project bevat of alleen een subset van de taken. Dit is een optieset met de volgende mogelijke waarden:</br>- **Alle projecttaken**</br>- **Alleen geselecteerde projecttaken**. Een lege waarde in dit veld is gelijk aan het selecteren van **Alle projecttaken**. | Als **Alleen geselecteerde taken** is geselecteerd, kunt u specifieke taken selecteren en deze koppelen aan deze contractregel op het tabblad **Factureringsinstellingen van taak** op de pagina **Project**. De waarde wordt gebruikt in combinatie met **Project** en **Opgenomen transactieklassen** om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels. |
| **Tijd opnemen** | Een waarde van **Ja**/**Nee** geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen op deze contractregel. De waarde **Nee** geeft aan dat de tijdtransacties of arbeidskosten niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord. |
| **Onkosten opnemen** | Een waarde van **Ja**/**Nee** geeft aan of onkosten voor het geselecteerde project worden opgenomen op deze contractregel. De waarde **Nee** geeft aan dat onkosten niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord. |
| **Materialen opnemen** | Een waarde van **Ja**/**Nee** geeft aan of materiaalkosten voor het geselecteerde project worden opgenomen op deze contractregel. Een waarde van **Nee** geeft aan dat de materiaalkosten niet worden opgenomen op deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord. |
| **Tarief opnemen** | Een waarde van **Ja**/**Nee** geeft aan of vergoedingen voor het geselecteerde project worden opgenomen op deze contractregel. De waarde **Nee** geeft aan dat vergoedingen niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze waarde wordt gebruikt in combinatie met het project om de contractregelverwijzing om te zetten op een werkelijke of een geschatte regelrecord. |
| **Bedrag van contract** | Op een contractregel met een vaste prijs is dit bedrag de overeengekomen waarde die aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld. Op een contractregel voor tijd en materiaal is dit bedrag een geschatte waarde waarde van wat aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld. Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel. Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de contractregeldetails. | Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de bedragen op de regeldetails te wijzigen. Op een contractregel met een vaste prijs wordt deze waarde gebruikt om het bedrag vóór belasting te genereren op periodieke factureringsmijlpalen. |
| **Geschatte belasting** | De gebruiker kan dit veld bewerken om het geschatte belastingbedrag op de contractregel in te voeren. Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de contractregeldetails. | Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de belastingbedragen op de regeldetails te wijzigen. Op een contractregel met een vaste prijs wordt deze waarde gebruikt om de belasting te genereren op periodieke factureringsmijlpalen. |
| **Contractbedrag na belasting** | Het contractregelbedrag na belasting. Dit veld is alleen-lezen en wordt berekend als **Contractbedrag + belasting**. | Op een contractregel met een vaste prijs wordt deze waarde gebruikt om periodieke factureringsmijlpalen te genereren. |
| **Niet-overschrijdingslimiet** | De gebruiker kan dit veld bewerken en het is alleen beschikbaar op projectgebaseerde contractregels waarvoor de factureringsmethode is ingesteld als tijd en materiaal. | De gebruiker kan dit veld bewerken. Wanneer een werkelijke waarde voor tijd en materiaal verwijst naar deze contractregel voor tijd en materiaal, wordt het bedrag van de werkelijke waarde geëvalueerd tegen de niet-overschrijdingslimiet op de contractregel. Deze evaluatie wordt voltooid nadat de reeds bestede en toegezegde bedragen zijn verantwoord. |
| **Klantbudget** | Dit veld kan worden bewerkt en wordt gekopieerd van het overeenkomstige waarde op de offerteregel, als het contract is gecreëerd op basis van een offerte,. | Dit veld wordt alleen ter informatie gebruikt en heeft geen invloed op volgende bewerkingen. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validatieregels voor de opties op het tabblad Algemeen van projectgebaseerde contractregels

Regel 1: Als het veld **Opgenomen taken** leeg is of is ingesteld op **Alle projecttaken**, worden alle taken van het project opgenomen op de contractregel.

Regel 2: Als het veld **Opgenomen taken** leeg is of expliciet is ingesteld op **Alle projecttaken**, kunnen een project en een bepaalde transactieklasse slechts worden opgenomen in één projectgebaseerde contractregel van een contract.

Regel 3: Als het veld **Opgenomen taken** is ingesteld op **Alleen geselecteerde projecttaken**, kunnen een project en een bepaalde transactieklasse worden opgenomen in meerdere projectgebaseerde contractregels van een contract.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contract</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Contractregel</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Opgenomen taken</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Tijd opnemen</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Onkosten opnemen</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Materialen opnemen</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Opnemen</strong>
                </p>
                <p>
                    <strong>Tarief</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Geldig/ongeldig</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Reden</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtreding van regel 2. Tijd, onkosten, materialen en vergoedingen voor het P1-project zijn opgenomen op de contractregels CL1 en CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Geen </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtreding van regel 2. Tijd, materialen en vergoedingen voor het P1-project zijn opgenomen op de contractregels CL1 en CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Geen </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Tijd, materialen en vergoedingen voor het P1-project zijn opgenomen in CL1.
                </p>
                <ul>
                    <li>
Onkosten voor het P1-project zijn opgenomen in CL2.
                    </li>
                </ul>
                <p>
Geen overlap in wat wordt opgenomen op elke contractregel en dus geldig.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Geen </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Geen </p>
            </td>
            <td width="42" valign="top">
                <p>
Geen </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Ongeldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Overtreding van regel 2 </p>
                <p>
C1 omvat tijd, materialen, onkosten en vergoedingen voor een subset van taken in project P1.
                </p>
                <p>
CL2 omvat tijd, materialen, onkosten en vergoedingen voor het hele project P1 en overlapt daarom met wat is opgenomen in C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Leeg </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Geldig </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Volgens regel 3 </p>
                <p>
C1 omvat tijd, onkosten, materialen en vergoedingen voor een subset van taken in project P1.
                </p>
                <p>
CL2 omvat tijd, onkosten, materialen en vergoedingen voor een subset van taken in project P1.
                </p>
                <p>
De enige aanvullende validatie betreft de subset van taken in CL1, die verschilt van de subset van taken in CL2 om ervoor te zorgen dat er geen overlapping is. Dit wordt gedaan door het systeem wanneer taken worden gekoppeld.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Alleen geselecteerde taken </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="48" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
            <td width="42" valign="top">
                <p>
Ja </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
