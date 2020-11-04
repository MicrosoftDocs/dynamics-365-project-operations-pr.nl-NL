---
title: Intercompany-onkosten
description: Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie. In dit geval kunt u de functie voor intercompany-onkosten gebruiken om de onkosten van de werknemer toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074715"
---
# <a name="intercompany-expenses"></a>Intercompany-onkosten

[!include [banner](../includes/banner.md)]

Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie. In dit geval kunt u de functie voor intercompany-onkosten gebruiken om de onkosten van de werknemer toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd. De rechtspersoon die de werknemer in dienst heeft, wordt de uitlenende rechtspersoon genoemd. De rechtspersoon waarvoor de werknemer onkosten maakt, wordt de lenende rechtspersoon genoemd. 

Voordat een werknemer onkosten kan aanmaken en indienen voor werk dat wordt uitgevoerd voor een andere rechtspersoon, in de uitlenende rechtspersoon, selecteert u op de pagina **Parameters onkostenbeheer** de optie **Intercompany-onkostenregels toestaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Belastingboeking voor intercompany-onkosten

[!include [banner](../includes/banner.md)]

Als u in uw onkostendeclaratie belastinggroepen wilt gebruiken die aan de uitlenende (bron) rechtspersoon zijn gekoppeld in plaats van aan de lenende (doel) rechtspersoon, moet u dit configureren in de instelling voor verkoopbelasting in het grootboek. Als de grootboekparameter **Rechtspersoon voor intercompany-belastingboeking** is ingesteld op **Bron** en **Belastingregels verkoopbelasting toepassen** is ingesteld op **Nee** , wordt de belastingcombinatie voor de uitlenende rechtspersoon gebruikt. Als dezelfde parameter is ingesteld op **Doel** , wordt de belastingcombinatie voor lenende rechtspersoon gebruikt. Voor rechtspersonen in de Verenigde Staten moet wanneer de parameter is ingesteld op **Bron** , het veld **Te ontvangen verkoopbelasting** ook worden geconfigureerd op de nieuwe pagina **Boekingsgroepen grootboek**. Het boekhoudsysteem gebruikt de informatie uit dit veld voor het invoeren van belastinggerelateerde boekhouding.   
Het gedrag is consistent voor onkostenregels die met of zonder een project zijn geboekt.  
