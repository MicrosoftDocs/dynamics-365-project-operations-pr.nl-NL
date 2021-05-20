---
title: Projectgebaseerde verkoopkansen beheren
description: Dit onderwerp bevat informatie over hoe u kunt werken met verkoopkansen die gerelateerd zijn aan projecten.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948369"
---
# <a name="manage-project-based-opportunities"></a>Projectgebaseerde verkoopkansen beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectgebaseerde bedrijven hebben hun activiteiten voor oplevering meestal verspreid over meerdere landen en regio's. De kosten van de uitvoering en oplevering van het project kunnen variëren, afhankelijk van de regio of divisie die de oplevering beheert. Dit kan weer van invloed zijn op de marges van de deal. De oplevering van projectgebaseerde diensten omvat doorgaans grote hoeveelheden personeelstijd, aanzienlijke reiskosten, materiaalkosten en andere onkosten.

Projectmatige verkoopkansen in Dynamics 365 Project Operations zijn ontworpen met uitbreidingen voor Dynamics 365 Sales. Het onderwerp bevat details over de verschillende velden en bedrijfslogica die zijn opgenomen in de aanvullende functionaliteit die projectgebaseerde bedrijven nodig hebben om projectgebaseerde verkoopkansen te beheren.

## <a name="view-all-project-based-opportunities"></a>Alle projectgebaseerde verkoopkansen weergeven

Een lijst met alle projectgebaseerde verkoopkansen is te zien op de lijstpagina **Verkoopkans**. 

1. Ga naar **Verkoop** > **Verkoopkansen**.
2. Gebruik de **Weergavewisselaar** om andere gefilterde weergaven van de verkoopkansen te selecteren. U kunt uw eigen weergaven maken met aangepaste filtercriteria om deze weergaven en navigatieopties te configureren.

Projectgebaseerde verkoopkansen kunnen worden gemaakt of verwijderd vanaf deze lijstpagina of de detailpagina.

## <a name="business-process-flow-for-project-based-deals"></a>Bedrijfsprocesstroom voor projectgebaseerde deals

De volgende bedrijfsprocesstromen worden ondersteund voor projectgebaseerde deals in Project Operations:

- Potentiële klant naar bedrijfsproces voor verkoopkans
- Verkoopproces verkoopkans

### <a name="lead-to-opportunity-business-process"></a>Het bedrijfsproces Lead naar verkoopkans 
Het bedrijfsproces Lead naar verkoopkans ondersteunt de volgende fasen:

| Fase | Toegewezen entiteit | Functionaliteit |
| --- | --- | --- |
| Kwalificeren | Lead | Kwalificeer de potentiële klant om een een account, contactpersoon en verkoopkans te maken. |
| Ontwikkelen | Kans | Ontwikkel de verkoopkans om meer informatie toe te voegen over het betrokken werk, de belanghebbenden en de concurrentie. |
| Voorstel | Kans | Ontwikkel het voorstel en verkrijg goedkeuring van het interne beoordelingsteam. |
| Afsluiten | Kans | Haal de verkoopkans binnen om de deal te sluiten. |

### <a name="opportunity-sales-process"></a>Verkoopproces verkoopkans
Het verkoopproces voor verkoopkansen in Project Operations is een uitbreiding op de bedrijfsstroom van het verkoopproces voor verkoopkansen in de Sales-toepassing. Dit bedrijfsproces is standaard ontworpen om de volgende fasen in een projectgebaseerde verkoopkans te ondersteunen.

| Fase | Toegewezen entiteit | Functionaliteit |
| --- | --- | --- |
| Kwalificeren | Kans | Kwalificeer de potentiële klant om een een account, contactpersoon en verkoopkans te maken. |
| Voorstel | Prijsopgave | Ontwikkel het voorstel met prijsopgaven voor projecten en verkrijg goedkeuring van het interne beoordelingsteam. |
| Contract | Projectcontract | Win de prijsopgave om het contract te maken en te beginnen met de uitvoering en oplevering van het project. |
| Afsluiten | Projectcontract | Rond het werk succesvol af en sluit het projectcontract. |

> [!NOTE]
> Als uw projectgebaseerde deal is begonnen met een lead, heeft het bedrijfsproces Lead naar verkoopkans voorrang.
>
> Als uw projectgebaseerde deal is begonnen met een verkoopkans, heeft het verkoopproces voor verkoopkansen voorrang.

U kunt de bedrijfsprocesstroom voor producten bewerken of uw eigen bedrijfsprocesstromen maken om uw verkoopproces indien nodig te volgen. Zie [Overzicht van bedrijfsprocesstromen](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview) voor meer informatie over de bedrijfsprocesstroom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]