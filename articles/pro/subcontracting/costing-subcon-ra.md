---
title: Kostenraming van toewijzingen van resources op contractbasis
description: In dit onderwerp wordt uitgelegd hoe Microsoft Dynamics 365 Project Operations kostenraming berekent van toewijzingen van resources op contractbasis.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 09a2a86ea0e97376939d5bff6df9177747818ebb
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903383"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Kostenraming van toewijzingen van resources op contractbasis

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Taaktoewijzingen van projectteamleden op contractbasis worden gecalculeerd met behulp van de prijslijst **Inkoop** die aan het toeleveringscontract is gekoppeld in de gerelateerde teamlidrecord. Dit is anders dan hoe toewijzingen van personeelsresources worden berekend, waarbij taaktoewijzingen van personeelsresources worden berekend met behulp van de prijslijst **Kosten** die bij de contracterende eenheid van het project is gevoegd. 

De toewijzingen van algemene projectteamleden op contractbasis worden gecalculeerd met behulp van de rolgebaseerde prijsinstelling die bij het toeleveringscontract is gevoegd. Inkoopprijzen kunnen ook specifiek voor elke resource worden ingesteld. Deze resource-specifieke prijzen krijgen voorrang bij kostenberekening van taaktoewijzingen van benoemde projectteamleden die contractwerknemers zijn. 

De prioriteit van het gebruik van rolspecifieke inkoopprijzen versus resourcespecifieke wordt bepaald door de instelling van de prioriteit van de prijsdimensie in **Parameters > Op bedrag gebaseerde prijsdimensies**.

Deze functionaliteit voor het dynamisch afleiden van prijzen op basis van dimensie-instellingen voor inkoopprijzen van toeleveranciers is vergelijkbaar met de manier waarop kosten- en factuurtarieven worden afgeleid voor voltijdse werknemers. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Taaktoewijzingen maken voor het verkrijgen van kostenramingen van resources van toeleveranciers

Taaktoewijzingen voor toeleveranciers kunnen op twee manieren worden aangemaakt: 
- Het tabblad **Taken** gebruiken.
- Het tabblad **Team** gebruiken.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Resourcetoewijzingen maken met het tabblad Taken
Met de lijst **Resources** in het tabblad **Taken** voor een specifieke taak kunt u een taaktoewijzing maken voor een benoemde resource of een algemene resource. Als u een benoemde resource selecteert uit de vervolgkeuzelijst **Toegewezen resources** op de taak en deze resource is een contractwerknemer, wordt de genoemde resource toegewezen aan de taak en wordt er een bijbehorende projectteamlidrecord gemaakt met het werknemertype ingesteld op **Contractwerknemer** en wordt **Geldigheid** ingesteld op **Ongeldig**. Als volgende stap moet u de projectteamlidrecord openen en een toeleveringscontract en toeleveringscontractregel selecteren. Hierdoor wordt de taaktoewijzing bijgewerkt om een referentie naar de toeleveringscontract en toeleveringscontractregel te hebben en wordt ook de status van het teamlid bijgewerkt naar: **Geldig**.

Als u ervoor kiest om een algemeen teamlid aan te maken vanuit de vervolgkeuzelijst **Toegewezen resources** op de taak, kunt u met het dialoogvenster **Aanmaak van algemene teamleden** een toeleveringscontract en toeleveringscontractregel selecteren. Wanneer de generieke resource aan de taak is toegewezen en de bijbehorende record voor projectteamleden is gemaakt, zult u merken dat de record voor projectteamleden is gemaakt met het werknemertype ingesteld op **Contractwerknemer** en **Geldigheid** ingesteld op **Geldig**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Projectteamleden maken met behulp van het tabblad Team
Met behulp van het tabblad Team in het project kunt u een algemeen teamlid of een benoemd teamlid maken. Bij het maken van het teamlid kunt u toeleveringscontract en toeleveringscontractregel selecteren. Nadat het teamlid is gemaakt, moet u het teamlid aan een taak toewijzen met behulp van de vervolgkeuzelijst **Toegewezen resources** in de taak. 

## <a name="updating-estimates"></a>Schattingen bijwerken
Nadat u projectteamleden aan taken hebt toegewezen, moet u naar het tabblad **Schattingen** op het project gaan en **Prijzen bijwerken** selecteren om ervoor te zorgen dat de kostentarieven van de toewijzingen van resources van toeleveranciers worden bijgewerkt op basis van de inkoopprijslijst die bij het toeleveringscontract is gevoegd. Er worden geen schattingen gegenereerd voor niet-toegewezen taken in Microsoft Dynamics 365 Project Operations. Als gevolg hiervan moet u taaktoewijzingen maken om de prijzen en kosten voor verschillende taken van uw project te berekenen. 

> [LET OP!] Projectteamleden bij wie **Contractwerknemer** als **Werknemertype** staat, maar geen toeleveringscontractreferentie hebben, worden gemarkeerd als **Ongeldig** op het raster **Projectteamleden**. Als er projectteamleden met deze status zijn, opent u de record voor het projectteamlid en werkt u handmatig de toeleverings- en toeleveringscontractregelvelden bij, zodat de schatting van de financiële kosten de kosten van de contractwerknemer op het tabblad **Schattingen** nauwkeurig weergeeft. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
