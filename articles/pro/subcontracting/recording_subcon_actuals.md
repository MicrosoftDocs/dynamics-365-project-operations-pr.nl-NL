---
title: Registratie van tijd, kosten en materiaalgebruik voor toeleveringscomponenten
description: In dit onderwerp wordt uitgelegd hoe tijd, onkosten en materiaalgebruik geregistreerd op projecten van toeleveringscomponenten worden bijgehouden door Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: 04c78dd48367c3720b8f5ad5d924ed106da6a128
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902843"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Registratie van tijd, kosten en materiaalgebruik op projecten voor toeleveringscomponenten

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In dit onderwerp wordt uitgelegd hoe tijd, onkosten en materiaalgebruik geregistreerd op projecten van toeleveringscomponenten worden bijgehouden door Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Kostenberekening van de tijd van toeleveranciers op projecten
In Project Operations kunnen contractwerknemers op dezelfde manier als medewerkers tijd op projecten vastleggen. Bij het invoeren van tijd op projecten en/of projecttaken kan een contractwerknemer een specifiek toeleveringscontract en toeleveringscontractregel selecteren.

Wanneer de door contractwerknemers ingediende tijd is goedgekeurd, worden de projectkosten geregistreerd op basis van het eenheidskostentarief dat is ingesteld voor de contractwerknemer-resource in het gedeelte **Rolprijzen** van de inkoopprijslijst op het toeleveringscontract.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Kostenberekening van de onkosten van toeleveranciers op projecten
Bij het boeken van onkosten gemaakt voor projecten, kunt u een toeleveringscontract en toeleveringscontractregel selecteren op de onkostenpost. 

Wanneer deze onkostenpost is ingediend en goedgekeurd, worden de kosten van onkosten geregistreerd op basis van het eenheidskostentarief dat is ingesteld voor de transactiecategorie in het gedeelte **Categorieprijzen** van de inkoopprijslijst op het toeleveringscontract.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Kostenberekening van de materialen van toeleveranciers op projecten
Bij het boeken van het materiaalgebruik voor projecten, kunt u een toeleveringscontract en toeleveringscontractregel selecteren in het logboek voor materiaalgebruik. Wanneer het materiaalgebruiklog is ingediend en goedgekeurd, worden de materiaalkosten geregistreerd op basis van het eenheidskostentarief dat is ingesteld voor dat product in het gedeelte **Prijslijstitems** van de prijslijst van het toeleveringscontract.

Materiaalgebruik kan ook worden geregistreerd voor toe te voegen producten op projecten. Dit type materiaalgebruik kan ook worden gekoppeld aan een toeleveringscontract en toeleveringscontractregel. Wanneer u het materiaalgebruik voor toe te voegen producten registreert, moet u de kosten per eenheid van het toe te voegen product invoeren. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
