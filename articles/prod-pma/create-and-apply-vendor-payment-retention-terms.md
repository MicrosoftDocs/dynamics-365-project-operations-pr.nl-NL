---
title: Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen
description: Dit onderwerp bevat informatie over het instellen en onderhouden van inhoudingstermijnen voor leveranciersbetalingen.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6f6424b983f76a96825d76e1b4b81b54dc84b84
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270942"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Inhoudingstermijnen voor leveranciersbetalingen maken en toepassen

[!include [banner](../includes/banner.md)] 

Het instellen van inhoudingstermijnen voor leveranciersbetalingen voor een project is handig wanneer uw organisatie een deel van de betalingen die voor een leverancier zijn verricht wil inhouden. Bijvoorbeeld wanneer u de betaling aan een leverancier wilt uitstellen totdat de geleverde producten aan uw verwachtingen voldoen. Inhoudingstermijnen voor leveranciersbetalingen kunnen worden opgegeven wanneer u onderhandelt over een leverancierscontract.

## <a name="create-vendor-payment-retention-terms"></a>Inhoudingstermijnen voor leveranciersbetalingen maken

U kunt het percentage van de leveranciersbetaling voor inhouding invoeren en het percentage van de eerder ingehouden bedragen die moeten worden vrijgegeven. Bedragen worden automatisch ingehouden op leveranciersfacturen totdat het contract de opgegeven status van voltooiing bereikt. Nadat u de inhoudingstermijnen hebt ingesteld, kunt u deze toepassen op elk project voor die leverancier.

Gebruik de volgende stappen om inhoudingstermijnen voor leveranciersbetalingen in te stellen en te onderhouden. 

1. Ga naar **Projectmanagement en financiële administratie** > **Inhouding** > **Inhoudingstermijnen voor leveranciersbetalingen**.
2. Selecteer **Nieuw** om een nieuwe inhoudingstermijn voor leveranciers toe te voegen. De waarde **Regel-ID** voor de nieuwe termijn wordt automatisch ingevoerd. 
3. Voer een korte beschrijving in het veld **Omschrijving** in en selecteer op het sneltabblad **Termijnen** **Regel toevoegen** om termijnwaarden in te voeren voor het volgende:

   - **Percentage geleverde eenheden**: voer een voltooiingspercentage voor de termijn in. Bedragen worden automatisch ingehouden op leveranciersfacturen totdat de projectfase van voltooiing gelijk is aan het opgegeven percentage. Als u bijvoorbeeld 50,00 invoert, worden bedragen ingehouden totdat het project voor 50 procent is voltooid.
   - **Percentage om in te houden**: voer een percentage van het leveranciersfactuurbedrag in dat moet worden ingehouden. Als u bijvoorbeeld 10,00 invoert, wordt 10 procent van het bedrag op een leveranciersfactuur ingehouden totdat het project het voltooiingspercentage bereikt dat is ingesteld in het veld **Percentage geleverde eenheden**.
   - **Percentage om vrij te geven**: selecteer **Regel toevoegen** om een percentage in te voeren van eerder ingehouden bedragen die moeten worden vrijgegeven voor het geselecteerde voltooiingsniveau van het project.

> [!NOTE]
> Als u meer dan één mijlpaal hebt voor verschillende voltooiingsniveaus van een project, voert u voor elke inhoudingsregel een afzonderlijke inhoudingstermijnregel voor leveranciers in. Met elke regel kan een ander inhoudingspercentage en een ander vrijgavepercentage worden opgegeven voor elk toegewezen voltooiingsniveau van het project.

Nadat u de inhoudingstermijnen voor een leverancier hebt ingesteld, kunt u de termijnen toepassen op een project.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Inhoudingstermijnen voor leveranciers toepassen op een project

1. Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Alle projecten** en open een project via de projectlijstpagina.
2. Selecteer **Regel toevoegen** op het sneltabblad **Leveranciersovereenkomsten**.
3. Selecteer in het veld **Rekeningcode** een van de volgende opties: 

   - **Tabel**: de inhoudingstermijnen voor leveranciers zijn van toepassing op één leverancier.
   - **Groep**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers in een leveranciersgroep.
   - **Alle**: de inhoudingstermijnen voor leveranciers zijn van toepassing op alle leveranciers.

4. Selecteer in het veld **Leverancier/Leveranciersgroep** de leverancier of leveranciersgroep waarop de inhoudingstermijnen voor leveranciers van toepassing zijn. Als u **Alle** hebt gekozen in de vorige stap, is dit veld niet beschikbaar.
5. Selecteer in het veld **Inhoudingstermijnen voor leveranciers** de inhoudingstermijnen die u in de vorige procedure hebt gemaakt.
6. Als voor het project ook PWP-voorwaarden (Pay-When-Paid) zijn ingesteld voor de leverancier, voert u het drempelpercentage voor het project in het veld **PWP-drempelpercentage** in.

De inhoudingstermijnen voor leveranciers worden ook weergegeven op inkooporders die u voor de leverancier maakt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]