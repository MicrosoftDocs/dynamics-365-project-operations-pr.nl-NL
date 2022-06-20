---
title: Een projectleveranciersfactuur bevestigen
description: In dit artikel wordt uitgelegd hoe u een factuur van een projectleverancier in Microsoft Dynamics 365 Project Operations bevestigt en wat de financiële impact is van het bevestigen van een factuur van een projectleverancier.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932428"
---
# <a name="confirm-a-project-vendor-invoice"></a>Een projectleveranciersfactuur bevestigen

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Nadat u alle regels op een leveranciersfactuur in Microsoft Dynamics 365 Project Operations hebt geverifieerd, kunt u de actie Bevestigen gebruiken om de leveranciersfactuur te bevestigen.

Wanneer u **Bevestigen** selecteert op een leveranciersfactuur treedt het volgende gedrag op:

1. De status van de leveranciersfactuur wordt bijgewerkt naar **Bevestigd**.
2. De bevestigde leveranciersfactuur en de bijbehorende records worden alleen-lezen en kunnen niet worden bewerkt of verwijderd.
3. Als werkelijke kosten verwijzen naar de leveranciersfactuurregel als onderdeel van het vereffeningsproces, worden alle werkelijke kosten die zijn gekoppeld aan de leveranciersfactuurregel waarnaar wordt verwezen, teruggeboekt.
4. Nieuwe werkelijke kosten worden gemaakt met behulp van de informatie op de leveranciersfactuurregel.
5. Nadat de leveranciersfactuur is bevestigd, kunt u geen correctiejournalen meer maken, intrekkingen van tijdsvermeldingen verwerken of goedkeuring annuleren van de oorspronkelijke tijd, onkosten of werkelijke materiaalwaarden die zijn teruggeboekt.

> [!NOTE]
> Als een regel op een leveranciersfactuur een andere verificatiestatus heeft dan **Voltooid**, kan de leveranciersfactuur niet worden bevestigd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
