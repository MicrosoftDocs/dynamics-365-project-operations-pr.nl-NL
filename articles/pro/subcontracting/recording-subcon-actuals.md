---
title: Registratie van tijd, kosten en materiaalgebruik voor toeleveringscomponenten
description: In dit onderwerp wordt uitgelegd hoe tijd, onkosten en materiaalgebruik geregistreerd op projecten van toeleveringscomponenten worden bijgehouden door Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a31b4a1092cc4829cbfc789e8b8e30030b2826b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599218"
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
