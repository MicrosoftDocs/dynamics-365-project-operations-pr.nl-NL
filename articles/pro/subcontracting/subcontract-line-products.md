---
title: Subcontractregels voor producten
description: In dit onderwerp wordt uitgelegd hoe u subcontractregels voor producten registreert en de verschillende velden gebruikt om productaankopen van leveranciers vast te leggen.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323680"
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

| Veld | Beschrijving |
| ----- | ----------- |
| Meetcriterium | De naam van de subcontractregel. |
| Beschrijving | Een korte beschrijving van producten die worden besteld op de subcontractregel. |
| Type lijn | Deze veldwaarde is standaard **Op hoeveelheid gebaseerd**. |
| Factureringsmethode |  De factureringsmethode van de subcontractregel. Een op mijlpalen gebaseerd factuurschema is beschikbaar voor factureringsmethoden met een vaste prijs. |
| Transactieklasse | Deze veldwaarde is standaard **Tijd**. Om subcontractregels voor het aankopen van producten te maken, selecteert u in het veld **Transactieklasse** de optie **Materiaal**. Deze selectie geeft aan dat de subcontractregel wordt gebruikt om de inkoop van producten voor projecten vast te leggen. |
| Product selecteren | Geef op of het product dat wordt gekocht in de productcatalogus wordt onderhouden of een inschrijfproduct is. |
| Product | Selecteer een actief product in de catalogus. Dit veld is alleen beschikbaar als **Product selecteren** is ingesteld op **Bestaand**. |
| Toe te voegen product | Voer de naam van het toe te voegen product in. Dit veld is alleen beschikbaar als **Product selecteren** is ingesteld op **Toevoegen**.  |
| Aangevraagde leveringsdatum | Selecteer de gewenste leverdatum voor de producten. Deze datum wordt ook gebruikt om een projectprijslijst te kiezen uit de projectprijslijsten die bij het subcontract zijn gevoegd. De kosten van het product op de subcontractregel zijn dan afkomstig uit die prijslijst. |
| Leveringsdatum volgens contract | Selecteer de datum waarop de producten volgens het contract worden geleverd.  |
| Bestelde hoeveelheid | Voer de hoeveelheid van het product in dat van de leverancier wordt gekocht. Als een projectmanager te veel van deze hoeveelheid gebruikt, volgt er een waarschuwing. |
| Eenhedengroep | Deze waarde wordt alleen standaard ingesteld voor catalogusproducten. Wanneer **Product** en **Aangevraagde leveringsdatum** beide zijn geselecteerd, kiest het systeem de toepasselijke prijslijst op basis van de leveringsdatum. De gerelateerde prijslijstitems worden opgevraagd voor het overeenkomende product. De eenheids- en eenheidsgroepwaarden zijn standaard afkomstig uit de instellingen in de prijslijstitemrecord. |
| Eenheid | Deze waarde is standaard afkomstig uit de eenheidsinstelling in de prijslijstitemrecord. U kunt deze indien nodig wijzigen in een andere eenheid. De combinatie van product en eenheid wordt gebruikt om standaard de eenheidsprijs op de subcontractregel voor bestaande catalogusproducten te bepalen. |
| Prijs per eenheid | De eenheidsprijs wordt standaard ingesteld op basis van de combinatie van product en eenheid uit de prijslijstitems gerelateerd aan de projectprijslijst die van toepassing is op de gevraagde leveringsdatum van de subcontractregel.  |
| Subtotaal | Dit alleen-lezen veld wordt berekend als Aantal x Eenheidsprijs als in beide velden waarden zijn ingevoerd. Als de velden **Hoeveelheid** en/of **Eenheidsprijs** leeg zijn, kunt u handmatig een waarde invoeren.  |
| Omzetbelasting | Voer de waarde voor omzetbelasting in. |
| Totale bedrag | Dit berekende veld toont het totale bedrag van de subcontractregel, inclusief belastingen. De waarde in dit veld wordt berekend als subtotaal + belasting. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
