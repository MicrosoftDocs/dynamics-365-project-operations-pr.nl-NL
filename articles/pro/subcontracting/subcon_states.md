---
title: Statusovergangen op een toeleveringscontract in Project Operations
description: In dit onderwerp worden statusovergangen op een toeleveringscontract in Microsoft Dynamics 365 Project Operations uitgelegd wanneer het toeleveringscontract wordt gemaakt, uitgevoerd en gesloten.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 4ca658440c7a9b29a927098f24c092d72d9eb0c9
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902841"
---
# <a name="state-transitions-on-a-subcontract-in-project-operations"></a>Statusovergangen op een toeleveringscontract in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit onderwerp worden de statusovergangen op een toeleveringscontract in Microsoft Dynamics 365 Project Operations uitgelegd. Elke status wordt weergegeven als concept, bevestigd, gesloten of geannuleerd. De volgende afbeelding geeft de statusovergangen weer.

![Model van toeleveringscontractstatus](../media/SubconStates.png)  

De volgende tabel bevat een beschrijving van wat elke status vertegenwoordigt in de levenscyclus van een toeleveringscontract in Project Operations.

| Provincie | Description | Toegestane overgangen |
| --- | --- | --- |
| Concept | Dit vertegenwoordigt de initiële status van een toeleveringscontract. De onderhandelingen met de leverancier zijn aan de gang. De regels en prijzen zijn onder voorbehoud van wijzigingen. Een toeleveringscontract met deze status kan worden gebruikt om de projectvereisten voor resources en materialen in te schatten en te bemannen. Er kan ook worden verwezen naar tijd, kosten en materiaalgebruik voor een project. Een toeleveringscontract met deze status kan worden bewerkt en verwijderd. | Bevestigd |
| Bevestigd | Dit vertegenwoordigt de fase van een toeleveringscontract nadat de onderhandelingen met de leverancier over prijzen en in te kopen regelitems zijn voltooid. De daadwerkelijke levering van materialen en/of werk door contractresources is echter nog aan de gang. Een toeleveringscontract met deze status kan worden gebruikt om de projectvereisten voor resources en materialen in te schatten en te bemannen. Er kan ook worden verwezen naar tijd, kosten en materiaalgebruik voor een project. Een toeleveringscontract met deze status kan niet worden bewerkt of verwijderd. Met de knop **Annuleren** kunt u een bevestigd toeleveringscontract annuleren. Met de knop **Opnieuw openen** kunt u het toeleveringscontract heropenen om het terug te brengen in de status **Concept**. Gebruik de knop **Sluiten** om een bevestigd toeleveringscontract te sluiten. | Gesloten <br> Geannuleerd <br> Concept |
| Gesloten | Dit vertegenwoordigt de fase van een toeleveringscontract wanneer de feitelijke levering van materialen en/of werk door contractresources is voltooid. Een toeleveringscontract met deze status kan niet meer worden gebruikt om de projectvereisten voor resources en materialen in te schatten en te bemannen. Er kan ook niet meer naar worden verwezen voor tijd, kosten en materiaalgebruik voor een project. Een toeleveringscontract met deze status kan niet worden bewerkt of verwijderd. | None |
| Geannuleerd | Dit vertegenwoordigt de fase van een toeleveringscontract wanneer de feitelijke levering van materialen en/of werk door contractresources niet meer nodig zijn. Een toeleveringscontract met deze status kan niet worden gebruikt om de projectvereisten voor resources en materialen in te schatten en te bemannen, noch kan ernaar verwezen worden wat betreft tijd, kosten en materiaalgebruik voor een project. Een toeleveringscontract met deze status kan niet worden bewerkt of verwijderd. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
