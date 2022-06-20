---
title: Subcontractregels voor producten
description: In dit artikel wordt uitgelegd hoe u subcontractregels voor producten registreert en de verschillende velden gebruikt om productaankopen van leveranciers vast te leggen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff9636f86102fa671a443d7646614070b3e2ee79
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934360"
---
# <a name="subcontract-lines-for-products"></a>Subcontractregels voor producten

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een subcontract in Dynamics 365 Project Operations kan een subcontractregel voor producten hebben. Met deze regels kan een projectmanager producten kopen van leveranciers kopen die ze vervolgens voor projecttaken kunnen gebruiken.

Voer de volgende stappen uit om een subcontractregel te maken voor producten in Project Operations.

1. Selecteer op de navigatiepagina de optie **Subcontracten** en open het subcontract waarmee u wilt werken. 
2. Selecteer op het tabblad **Subcontractregels** de optie **+ Nieuw** om een nieuwe subcontractregel te maken.
3. Selecteer op de pagina **Snelle invoer** in het veld **Transactieklasse** de optie **Materiaal** en voer de vereiste veldinformatie in of selecteer deze. 
4. Selecteer **Opslaan**.

De volgende tabel biedt informatie over de velden op de pagina's **Subcontractregeldetails** en **Snelle invoer** omdat deze relevant zijn voor het kopen van producten.

| Veld | Beschrijving | Functionele impact|
| ----- | ----------- | ----------- |
| Meetcriterium | Naam van de subcontractregel om te helpen bij identificatie. |Dit wordt weergegeven als de eerste kolom in alle zoekopdrachten op basis van subcontractregels.
| Beschrijving | Een korte beschrijving van producten die worden besteld op de subcontractregel. | Geen |
| Type lijn | Dit veld heeft de standaardwaarde **Op hoeveelheid gebaseerd**. |Geen |
| Factureringsmethode | Dit is een optieset die de twee belangrijkste contractmodellen vertegenwoordigt die worden ondersteund door Project Operations: **Vaste prijs** en **Tijd- en materiaalverbruik**. | Op basis van de geselecteerd factureringsmethode wordt een op mijlpalen gebaseerd factuurschema beschikbaar gesteld voor subcontractregels met de factureringsmethode Vaste prijs. |
| Transactieklasse |Dit veld heeft **Tijd** als standaardwaarde. Als u subcontractregels wilt maken voor het aankopen van producten, stelt u het veld **Transactieklasse** in op **Materiaal**.  | Dit geeft aan dat de subcontractregel wordt gebruikt om de inkoop vast te leggen van producten die voor projecten worden gebruikt. |
| Product selecteren | Geef op of het product dat wordt gekocht in de productcatalogus wordt onderhouden of een inschrijfproduct is. |Geen |
| Product | Selecteer een actief product in de catalogus. Dit veld is alleen beschikbaar als **Product selecteren** is ingesteld op **Bestaand**. |De combinatie van **Product** en **Eenheid** wordt standaard gebruikt of berekend voor de eenheidsprijs voor de subcontractregel.
| Toe te voegen product | Voer de naam van het toe te voegen product in. Dit veld is alleen beschikbaar als **Product selecteren** is ingesteld op **Toevoegen**.  |Bij toe te voegen producten wordt de inkoopprijs niet automatisch ingevuld.|
| Aangevraagde leveringsdatum | Voer de gewenste leverdatum voor de producten in.| Deze datum wordt ook gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van het product op de subcontractregel zijn dan afkomstig uit die prijslijst. |
| Leveringsdatum volgens contract | Voer de datum in waarop de producten volgens contract moeten worden geleverd.  |Geen|
| Bestelde hoeveelheid | Voer de hoeveelheid van het product in dat van de leverancier wordt gekocht.| Dit wordt gebruikt om waarschuwingen weer te geven wanneer een projectmanager een te grote hoeveelheid aanschaft.|
| Eenhedengroep | Deze waarde wordt alleen standaard ingesteld voor catalogusproducten. |Wanneer **Product** en **Aangevraagde leveringsdatum** beide zijn geselecteerd, kiest het systeem de toepasselijke prijslijst op basis van de leveringsdatum. De gerelateerde prijslijstitems worden opgevraagd voor het overeenkomende product. De eenheids- en eenheidsgroepwaarden zijn standaard afkomstig uit de instellingen in de prijslijstitemrecord. |
| Eenheid | Deze waarde is standaard ingesteld op de eenheid die is ingesteld voor de prijslijstitemrecord. U kunt deze indien nodig wijzigen in een andere eenheid.| De combinatie van product en eenheid wordt gebruikt om standaard de eenheidsprijs op de subcontractregel voor bestaande catalogusproducten te bepalen. |
| Prijs per eenheid | De eenheidsprijs wordt standaard ingesteld op basis van de combinatie van product en eenheid uit de prijslijstitems gerelateerd aan de projectprijslijst die van toepassing is op de gevraagde leveringsdatum van de subcontractregel.  |Geen |
| Subtotaal | Dit alleen-lezen veld wordt berekend als Aantal x Eenheidsprijs als in beide velden waarden zijn ingevoerd. Als de velden **Hoeveelheid** en/of **Eenheidsprijs** leeg zijn, kunt u handmatig een waarde invoeren.  |Geen |
| Omzetbelasting | Voer de waarde voor omzetbelasting in. |Geen |
| Totale bedrag | Dit berekende veld toont het totale bedrag van de subcontractregel, inclusief belastingen. De waarde in dit veld wordt berekend als Subtotaal + Belasting. |Geen |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
