---
title: Werken met projectgebaseerde contractregels
description: Dit onderwerp bevat informatie over projectgebaseerde contractregels.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990040"
---
# <a name="work-with-projectbased-contract-lines"></a>Werken met projectgebaseerde contractregels

Projectgebaseerde contractregels in Dynamics 365 Project Operations zijn ontworpen om de schattings- en factureringsovereenkomsten te bevatten voor specifieke onderdelen van projectwerk bij een opdracht. De structuur van een projectgebaseerde contractregel wordt voor projectschattingen en factureringsscenario's uitgebreid met de volgende concepten:

- Factureringsmethode
- Project- en taaktoewijzing
- Inbegrepen transactieklassen
- Niet-overschrijdingslimiet
- Instellingen voor toerekenbaarheid
- Schattingen met behulp van contractregeldetails
- Contractregelklanten

De volgende velden zijn opgenomen op het tabblad **Algemeen** met projectgebaseerde contractregels. Deze velden helpen om de basis te leggen voor een gedetailleerde schatting en de factureringsregelingen voor projectmatig werken.

| Veld | Beschrijving | Downstreamimpact |
| --- | --- | --- |
| **Name** | De naam van de contractregel die de afzonderlijke component aangeeft van het contract waarvoor de schatting van toepassing is. Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van een overeenkomstige waarde van de projectgebaseerde offerteregel. | Deze veldwaarde wordt gekopieerd naar de projectfactuurregel die is gemaakt op basis van deze contractregel wanneer de factuur wordt gemaakt. |
| **Factureringsmethode** | Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel. Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations:</br>- **Vaste prijs**</br>- **Tijd- en materiaalverbruik** | Op basis van de factureringsmethode van de contractregel waarnaar wordt verwezen, wordt de daadwerkelijke transactie verwerkt. Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode voor tijd en materiaal heeft, worden records met werkelijke waarden voor kosten en niet-gefactureerde verkoop gemaakt. Als de contractregel waarnaar wordt verwezen door de werkelijke waarde een factureringsmethode tegen een vaste prijs heeft, wordt alleen een werkelijke waarde voor kosten gemaakt. |
| **Project** | Gebruik dit veld om het project aan te geven dat wordt gebruikt om het werk voor deze opdracht af te leveren. | De waarde in dit veld wordt gebruikt in combinatie met de velden **Opgenomen taken** en **Opgenomen transactieklassen** om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels. |
| **Tijd opnemen** | Een vlag geeft aan of tijdtransacties of arbeidskosten voor het geselecteerde project worden opgenomen in deze contractregel. De waarde **Nee** geeft aan dat de tijdtransacties of arbeidskosten niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze veldwaarde wordt gebruikt in combinatie met het project om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels. |
| **Onkosten opnemen** | Een vlag geeft aan of onkosten voor het geselecteerde project worden opgenomen in deze contractregel. De waarde **Nee** geeft aan dat onkosten niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze veldwaarde wordt gebruikt in combinatie met het project om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels. |
| **Tarief opnemen** | Een vlag geeft aan of vergoedingen voor het geselecteerde project worden opgenomen in deze contractregel. De waarde **Nee** geeft aan dat vergoedingen niet worden opgenomen in deze contractregel. De waarde **Ja** geeft aan dat dit wel het geval is. | Deze veldwaarde wordt gebruikt in combinatie met het project om de contractregelreferentie op te lossen voor records met werkelijke waarden of schattingsregels. |
| **Bedrag van contract** | Op een contractregel met een vaste prijs is dit de overeengekomen waarde die aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld. Op een contractregel voor tijd en materiaal is dit bedrag een geschatte waarde waarde van wat aan de klant wordt gefactureerd voor alle werkcomponenten die aan deze contractregel zijn gekoppeld. Voor een projectcontract dat wordt gecreëerd op basis van een offerte, wordt deze waarde gekopieerd van het overeenkomstige waarde op de offerteregel. Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het bedrag in de contractregeldetails. | Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de bedragen op de regeldetails te wijzigen. Op een contractregel met een vaste prijs wordt deze waarde gebruikt om het bedrag vóór belasting te genereren op periodieke factureringsmijlpalen. |
| **Geschatte belasting** | De gebruiker kan dit veld bewerken om het geschatte belastingbedrag op de contractregel in te voeren. Als een projectgebaseerde contractregel regeldetails heeft, is dit veld vergrendeld voor bewerking en wordt het samengevat op basis van het belastingbedrag in de contractregeldetails. | Als de contractregel regeldetails heeft, kan deze waarde worden gewijzigd door de belastingbedragen op de regeldetails te wijzigen. Op een contractregel met een vaste prijs wordt deze waarde gebruikt om de belasting te genereren op periodieke factureringsmijlpalen. |
| **Contractbedrag na belasting** | Het contractregelbedrag na belasting. Dit veld is alleen-lezen en wordt berekend als **Contractbedrag + belasting**. | Op een contractregel met een vaste prijs wordt deze waarde gebruikt om periodieke factureringsmijlpalen te genereren. |
| **Niet-overschrijdingslimiet** | De gebruiker kan dit veld bewerken en het is alleen beschikbaar op projectgebaseerde contractregels waarvoor de factureringsmethode is ingesteld als tijd en materiaal. | De gebruiker kan dit veld bewerken. Wanneer een werkelijke waarde voor tijd of onkosten verwijst naar deze contractregel voor tijd en materiaal, wordt het bedrag van de werkelijke waarde geëvalueerd tegen de niet-overschrijdingslimiet op deze contractregel nadat de reeds uitgegeven en toegezegde bedragen zijn verantwoord. |
| **Klantbudget** | Dit veld kan worden bewerkt en wordt gekopieerd van het overeenkomstige waarde op de offerteregel, als het contract is gecreëerd op basis van een offerte. | Dit veld wordt alleen ter informatie gebruikt en heeft geen invloed op volgende bewerkingen. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Validatieregel voor de opties op het tabblad Algemeen van projectgebaseerde contractregels

Regel: een project en een bepaalde transactieklasse kunnen slechts op één projectgebaseerde contractregel in een contract worden opgenomen.

| Contract | Contractregel | Project | Tijd opnemen | Onkosten opnemen | Vergoeding opnemen | Geldig/ongeldig | Reden                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ongeldig       | In strijd met de regel. Tijd, onkosten en vergoedingen voor project P1 zijn opgenomen in beide contractregels CL1 en CL2.                                                                                       |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ongeldig       | In strijd met de regel. Tijd, onkosten en vergoedingen voor project P1 zijn opgenomen in beide contractregels CL1 en CL2.                                                                                       |
| C1       | CL1           | P1      | Ja          | Geen              | Ja         | Ongeldig       | In strijd met de regel. Tijd en vergoedingen voor project P1 zijn opgenomen in beide contractregels CL1 en CL2.                                                                                                   |
| C1       | CL2           | P1      | Ja          | Ja             | Ja         | Ongeldig       | In strijd met de regel. Tijd en vergoedingen voor project P1 zijn opgenomen in beide contractregels CL1 en CL2.                                                                                                   |
| C1       | CL1           | P1      | Ja          | Geen              | Ja         | Geldig           | Tijd en vergoedingen voor project P1 zijn opgenomen in CL1. Onkosten voor het P1-project zijn opgenomen in CL2. </br>   Er is geen overlap in wat op elke contractregel is opgenomen en daarom is het geldig.  |
| C1       | CL2           | P1      | Geen           | Ja             | Geen          | Geldig           | Tijd en vergoedingen voor project P1 zijn opgenomen in CL1. Onkosten voor het P1-project zijn opgenomen in CL2. </br>   Er is geen overlap in wat op elke contractregel is opgenomen en daarom is het geldig.  |
| C1       | CL1           | P1      | Ja          | Ja             | Ja         | Ongeldig       | In strijd met de regel. Tijd, onkosten en vergoedingen voor project P1 zijn opgenomen in de regels van twee contracten.                                                                                               |
| CL2      | CL2           | P1      | Ja          | Ja             | Ja         | Ongeldig       | In strijd met de regel. Tijd, onkosten en vergoedingen voor project P1 zijn opgenomen in de regels van twee contracten.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]