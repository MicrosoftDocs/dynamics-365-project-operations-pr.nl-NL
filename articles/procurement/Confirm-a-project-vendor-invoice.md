---
title: Projectleveranciersfacturen bevestigen
description: In dit artikel wordt uitgelegd hoe u een factuur van een projectleverancier in Microsoft Dynamics 365 Project Operations bevestigt en wordt beschreven wat de financiële impact is van het bevestigen van een factuur van een projectleverancier.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475412"
---
# <a name="confirm-project-vendor-invoices"></a>Projectleveranciersfacturen bevestigen

_ **Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.

Wanneer de parameter **Handmatige bevestiging door PM is vereist** is ingeschakeld, krijgen facturen die zijn gemaakt in Microsoft Dataverse, de status **Concept**. Leveranciersfacturen die op deze manier zijn gemaakt, moeten worden gecontroleerd en handmatig worden bevestigd. Wanneer de parameter **Handmatige bevestiging door PM is vereist** is uitgeschakeld, worden facturen die zijn gemaakt in Dataverse, automatisch bevestigd. U hoeft verder niets te doen. 

Nadat u alle regels op een leveranciersfactuur in Dynamics 365 Project Operations hebt geverifieerd, selecteert u **Bevestigen** om de leveranciersfactuur te bevestigen.

Wanneer u **Bevestigen** selecteert op een leveranciersfactuur treedt het volgende gedrag op:

1. De status van de leveranciersfactuur wordt bijgewerkt naar **Bevestigd**.
1. De bevestigde leveranciersfactuur en de bijbehorende records worden alleen-lezen en kunnen niet worden bewerkt of verwijderd.
1. Als werkelijke kosten verwijzen naar de leveranciersfactuurregel als onderdeel van het vereffeningsproces, worden alle werkelijke kosten die zijn gekoppeld aan de leveranciersfactuurregel waarnaar wordt verwezen, teruggeboekt.
1. Nieuwe werkelijke kosten worden gemaakt met behulp van de informatie op de leveranciersfactuurregel.
1. U kunt geen correctiejournalen meer maken, intrekkingen van tijdsvermeldingen verwerken of de goedkeuring annuleren van de oorspronkelijke tijd, onkosten of werkelijke materiaalwaarden die zijn teruggeboekt.
1. In Dynamics 365 Finance wordt de waarde voor **Projectkosten** bijgewerkt met behulp van het projectintegratiejournaal en het integratieaccount voor inkoop wordt *teruggeboekt* nadat het projectintegratiejournaal is geboekt.

> [!NOTE]
> Als een regel op een leveranciersfactuur een andere verificatiestatus heeft dan **Voltooid**, kan de leveranciersfactuur niet worden bevestigd.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
