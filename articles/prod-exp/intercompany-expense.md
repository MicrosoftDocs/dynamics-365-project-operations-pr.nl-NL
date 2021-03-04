---
title: Intercompany-onkosten
description: Dit onderwerp biedt informatie over het gebruik van intercompany-onkosten om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960826"
---
# <a name="intercompany-expenses"></a>Intercompany-onkosten

Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie. U kunt intercompany-onkosten gebruiken om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk werd uitgevoerd. De rechtspersoon die de werknemer in dienst heeft, wordt de uitlenende rechtspersoon genoemd. De rechtspersoon waarvoor de werknemer onkosten maakt, wordt de lenende rechtspersoon genoemd. 

Voordat een werkrol intercompany-onkosten kan maken en indienen, moet u intercompany-onkostenregels inschakelen. Selecteer in de uitlenende rechtspersoon op de pagina **Parameters voor onkostenbeheer** **Intercompany-onkostenregels toestaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Belastingboeking voor intercompany-onkosten

[!include [banner](../includes/banner.md)]

Voordat u in uw onkostendeclaratie belastinggroepen kunt gebruiken die aan de uitlenende rechtspersoon (bron) zijn gekoppeld in plaats van aan de lenende rechtspersoon (bestemming), moet u de functionaliteit inschakelen in de btw-instellingen van het grootboek. Wanneer de parameter **Rechtspersoon voor intercompany-belastingboeking** is ingesteld op **Bron** en **Regels voor btw-heffing toepassen** is ingesteld op **Nee** wordt de belastingcombinatie voor de uitlenende rechtspersoon gebruikt. Als dezelfde parameter is ingesteld op **Doel**, wordt de belastingcombinatie voor lenende rechtspersoon gebruikt. Voor rechtspersonen in de Verenigde Staten moet wanneer de parameter is ingesteld op **Bron**, het veld **Te ontvangen verkoopbelasting** ook worden geconfigureerd op de nieuwe pagina **Boekingsgroepen grootboek**. Het boekhoudsysteem gebruikt de informatie uit dit veld voor het invoeren van belastinggerelateerde financiële administratie.   
Het gedrag is consistent voor onkostenregels die met of zonder een project zijn geboekt.  
