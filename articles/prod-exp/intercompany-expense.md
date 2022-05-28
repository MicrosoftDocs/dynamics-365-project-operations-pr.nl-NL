---
title: Intercompany-onkosten
description: Dit onderwerp biedt informatie over het gebruik van intercompany-onkosten om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk is uitgevoerd.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6788a590879bd839ebb9dedc45895dc047cc9f15
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684223"
---
# <a name="intercompany-expenses"></a>Intercompany-onkosten

Een werknemer die in dienst is van één rechtspersoon in een organisatie, kan werk verrichten voor een andere rechtspersoon in dezelfde organisatie. U kunt intercompany-onkosten gebruiken om de onkosten van een werkrol toe te wijzen aan de rechtspersoon waarvoor het werk werd uitgevoerd. De rechtspersoon die de werknemer in dienst heeft, wordt de uitlenende rechtspersoon genoemd. De rechtspersoon waarvoor de werknemer onkosten maakt, wordt de lenende rechtspersoon genoemd. 

Voordat een werkrol intercompany-onkosten kan maken en indienen, moet u intercompany-onkostenregels inschakelen. Selecteer in de uitlenende rechtspersoon op de pagina **Parameters voor onkostenbeheer** **Intercompany-onkostenregels toestaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Belastingboeking voor intercompany-onkosten

[!include [banner](../includes/banner.md)]

Voordat u in uw onkostendeclaratie belastinggroepen kunt gebruiken die aan de uitlenende rechtspersoon (bron) zijn gekoppeld in plaats van aan de lenende rechtspersoon (bestemming), moet u de functionaliteit inschakelen in de btw-instellingen van het grootboek. Wanneer de parameter **Rechtspersoon voor intercompany-belastingboeking** is ingesteld op **Bron** en **Regels voor btw-heffing toepassen** is ingesteld op **Nee** wordt de belastingcombinatie voor de uitlenende rechtspersoon gebruikt. Als dezelfde parameter is ingesteld op **Doel**, wordt de belastingcombinatie voor lenende rechtspersoon gebruikt. Voor rechtspersonen in de Verenigde Staten moet wanneer de parameter is ingesteld op **Bron**, het veld **Te ontvangen verkoopbelasting** ook worden geconfigureerd op de nieuwe pagina **Boekingsgroepen grootboek**. Het boekhoudsysteem gebruikt de informatie uit dit veld voor het invoeren van belastinggerelateerde financiële administratie.   
Het gedrag is consistent voor onkostenregels die met of zonder een project zijn geboekt.  

## <a name="new-expense-expression-builder"></a>Nieuwe opbouwfunctie voor onkostenexpressies

De nieuwe opbouwfunctie voor onkostenexpressie lost problemen op met intercompany-onkostenscenario's die gebruikmaken van projecten. Deze functie zorgt ervoor dat, wanneer u een intercompany-onkosten maakt, het onkostenbeleid correct wordt gevalideerd ten opzichte van het project dat op de onkostenregel is geselecteerd, en dat de onkostennota met succes kan worden ingediend.

Om de functie voor het maken van onkostenexpressies te laten werken, moet deze zijn ingeschakeld. Bovendien moet het onkostenbeleid met een project-id worden ingesteld.

Als u al beleidsregels hebt geconfigureerd waarmee de project-id op de onkostenregel wordt gevalideerd, moet u deze beleidsregels intrekken. U kunt de functie vervolgens inschakelen en het beleid opnieuw configureren.

Volg deze stappen om de functie in te schakelen.

1. Ga naar **Werkruimten** \> **Functiebeheer**.
2. Selecteer in de lijst **De nieuwe opbouwfunctie voor onkostenexpressie lost problemen op met intercompany-onkostenscenario's die gebruikmaken van projecten**. Selecteer vervolgens **Nu inschakelen**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
