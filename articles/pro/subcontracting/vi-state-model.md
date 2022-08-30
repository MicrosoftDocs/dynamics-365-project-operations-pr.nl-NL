---
title: Statusovergangen op een leveranciersfactuur
description: In dit artikel worden de statusovergangen op een leveranciersfactuur in Microsoft Dynamics 365 Project Operations uitgelegd.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261010"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Statusovergangen op een leveranciersfactuur

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit artikel worden de statusovergangen op een leveranciersfactuur in Microsoft Dynamics 365 Project Operations uitgelegd. De volgende statussen worden gebruikt: **Concept**, **Ter beoordeling**, **Bevestigd**, **Uitgesteld** en **Geannuleerd**.

De volgende afbeeldingen geven de statusovergangen weer.

![Model voor statusovergangen bij subcontracten.](../media/VI_State_Model.jpg)

In de volgende tabel wordt uitgelegd wat elke status vertegenwoordigt in de levenscyclus van een leveranciersfactuur in Project Operations.

| Status | Beschrijving | Toegestane overgangen |
| --- | --- | --- |
| Concept | Deze status is de beginstatus van een leveranciersfactuur. De regels en prijzen zijn onder voorbehoud van wijziging. Een leveranciersfactuur met deze status kan worden bewerkt of verwijderd. | In uitvoering |
| Ter beoordeling | Deze status vertegenwoordigt de verwerkingsstatus van een leveranciersfactuur. Ten minste één leveranciersfactuurregel heeft een verificatiestatus van **In uitvoering**. | Bevestigd, Uitgesteld |
| Bevestigd | Deze status vertegenwoordigt de fase van een leveranciersfactuur waarin de toepassing werkelijke kosten heeft gemaakt voor elke leveranciersfactuurregel. Alle gekoppelde werkelijke kosten die aan de leveranciersfactuurregels zijn gekoppeld, zijn teruggeboekt en vervangen door de werkelijke kosten van die leveranciersfactuurregels. Een leveranciersfactuur met deze status kan niet worden bewerkt of verwijderd. U kunt de knop **Annuleren** gebruiken om een bevestigde leveranciersfactuur te annuleren. Met de actie Annuleren wordt de impact van de actie Bevestigen ongedaan gemaakt. | Geannuleerd |
| Uitgesteld | <p>Deze status vertegenwoordigt een fase van een leveranciersfactuur waarin de leveranciersfactuur niet kan worden verplaatst vanwege een probleem met de factuur of de status van de leverancier. Een leveranciersfactuur met deze status kan niet worden bevestigd, geannuleerd, bewerkt of verwijderd.</p><p>U kunt de actie Opnieuw openen gebruiken om de leveranciersfactuur te verplaatsen naar de status **Concept** of **Ter beoordeling**. Als ten minste één regel op de leveranciersfactuur een verificatiestatus heeft van **In uitvoering** of **Voltooid**, wordt de leveranciersfactuur opnieuw geopend met de status **Ter beoordeling**. Als alle regels op de leveranciersfactuur een verificatiestatus **Niet gestart** hebben, wordt de leveranciersfactuur opnieuw geopend met de status **Concept**.</p> | Concept, Ter beoordeling |
| Geannuleerd | Deze status vertegenwoordigt de fase van een subcontract wwaarbij de feitelijke levering van materialen en/of werk door contractresources niet langer nodig is. Een subcontract met deze status kan niet worden gebruikt om de projectvereisten voor resources en materialen in te schatten en te bemannen, en er kan ook niet naar worden verwezen wat betreft tijd, kosten en materiaalgebruik voor een project. Een subcontract met deze status kan niet worden bewerkt of verwijderd. | Geen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
