---
title: Overzicht van factuurverwerking
description: Dit onderwerp biedt een verwerkingsoverzicht voor facturering in Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9dc424cf69abfccc10bf551272a14e5cefb3dff0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275801"
---
# <a name="invoicing-process-overview"></a>Overzicht van factuurverwerking

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Project Operations voor scenario's op basis van resources/niet-voorradige artikelen bieden uitgebreide mogelijkheden die zijn afgestemd op de behoeften van zowel de projectmanager als de debiteurenadministrateur/projectaccountant. Voor het facturatieproces beheert de projectmanager de achterstand in projectfacturering en maakt de debiteurenadministrateur/projectaccountant een conform en nauwkeurig klantgericht factuurdocument.

![Stroomschema voor facturering](./media/invoicing-flow.png)

De projectcontractregel definieert de factureringsmethode voor gekoppelde projecttransacties. Wanneer de projectmanager tijd- en onkostentransacties goedkeurt, registreert het systeem de transacties in de entiteit **Werkelijke projectwaarden** en stuurt de informatie naar de module **Projectbeheer en boekhouding** in Dynamics 365 Finance. De projectaccountant beoordeelt en boekt vervolgens de records met behulp van het [Project Operations integratiejournaal](../project-accounting/project-operations-integration-journal.md). Dit journaal bevat belangrijke boekhoudkundige details voor de werkelijke projectcijfers, zoals facturering, btw-groep, btw-groep voor factureringsitems en financiële dimensies.

De projectmanager kan niet-gefactureerde verkooptransacties bekijken met behulp van de factureringsmethode voor tijd en materiaal in de [Backlog voor facturering van tijd en materiaal](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) en facturering tegen een vaste prijs in [Mijlpalen voor vaste prijs](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones). Met deze weergaven kunt u transacties filteren en selecteren die in de volgende factureringscyclus moeten worden opgenomen en deze vervolgens markeren als **Klaar voor facturatie**.

U kunt [handmatig een pro-formafactuur maken](../proforma-invoicing/create-manual-proforma-invoice.md) of een [periodiek proces](../proforma-invoicing/configure-automated-invoice-creation.md) gebruiken. De projectmanager kan [een concept-pro-formafactuur aanpassen](../proforma-invoicing/manage-proforma-invoice.md) indien nodig en deze bevestigen.

De bevestigde pro-formafactuur wordt verstuurd naar de module **Projectbeheer en financiële administratie** in Finance. De projectaccountant maakt het projectfactuurvoorstel op en werkt het bij, en boekt deze en drukt het document vervolgens af. Geboekte projectfacturen worden geregistreerd in het grootboek, evenals de subadministraties voor klanten en projecten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]