---
title: Een projectleveranciersfactuur annuleren
description: In dit artikel wordt uitgelegd hoe u een factuur van een projectleverancier in Microsoft Dynamics 365 Project Operations annuleert en wat de financiële impact is van het annuleren van een factuur van een projectleverancier.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261084"
---
# <a name="cancel-a-project-vendor-invoice"></a>Een projectleveranciersfactuur annuleren

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Nadat een leveranciersfactuur is bevestigd, kan deze niet meer worden bewerkt of verwijderd. Als er een fout is opgetreden op een bevestigde leveranciersfactuur, kunt u de actie Annuleren gebruiken om de impact van de leveranciersfactuur ongedaan te maken en een nieuwe leveranciersfactuur te maken.

Wanneer u **Annuleren** selecteert op een leveranciersfactuur treedt het volgende gedrag op:

1. De status van de leveranciersfactuur wordt bijgewerkt naar **Geannuleerd**.
2. De geannuleerde leveranciersfactuur en de bijbehorende records worden alleen-lezen en kunnen niet worden bewerkt of verwijderd.
3. Alle werkelijke kosten die zijn gemaakt op basis van leveranciersfactuurregels als onderdeel van de bevestiging van de leveranciersfactuur, worden teruggeboekt.
4. Als er werkelijke kosten waren gekoppeld aan de leveranciersfactuurregels als onderdeel van het afstemmingsproces, werden deze teruggeboekt in de oorspronkelijke bevestiging van de leveranciersfactuur. Tijdens het annuleren van leveranciersfacturen worden deze werkelijke kosten opnieuw gemaakt. De oorsprong verwijst naar de vermeldingen voor tijd, onkosten of materiaalgebruik.
5. Nadat de leveranciersfactuur is geannuleerd, kunt u opnieuw correctiedagboeken maken, intrekkingen van tijdsvermeldingen verwerken en goedkeuring annuleren van de oorspronkelijke tijd, onkosten of werkelijke materiaalwaarden.

> [!NOTE]
> Alleen bevestigde projectleveranciersfacturen kunnen worden geannuleerd. Leveranciersfacturen met andere statussen kunnen niet worden geannuleerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
