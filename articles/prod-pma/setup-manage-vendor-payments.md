---
title: Betalen bij betaling instellen en gebruiken voor leveranciersbetalingen
description: In dit onderwerp wordt uitgelegd hoe u Betalen bij betaling-voorwaarden kunt maken, zodat u gedeeltelijke leveranciersbetalingen kunt vrijgeven op basis van klantbetalingen.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074543"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Betalen bij betaling instellen en gebruiken voor leveranciersbetalingen

[!include [banner](../includes/banner.md)]

Wanneer u een leverancier goedkeurt om als onderaannemer te werken, wilt u misschien de betaling aan de leverancier inhouden totdat uw klant u voor het project betaalt. Ter ondersteuning van dit scenario kunt u Betalen bij betaling-voorwaarden instellen wanneer u de inkooporder bij de leverancier instelt.

Als een klant bijvoorbeeld een bedrag op een projectfactuur betaalt, kunt u het factuurbedrag geheel of gedeeltelijk vrijgeven. Stel Betalen bij betaling-voorwaarden in die specificeren dat de leverancier wordt betaald nadat u een percentage van de gerelateerde betaling van de klant hebt ontvangen. Als u een gedeeltelijke betaling van een klant ontvangt, kunt u enkele van de gerelateerde leveranciersfacturen handmatig voor betaling vrijgeven.

Het volgende voorbeeld schetst het proces van het gebruiken van Betalen bij betaling-termen.

## <a name="example"></a>Voorbeeld

Uw organisatie stemt ermee in om een klant 100 computers te leveren waarop software is geïnstalleerd, voor een prijs van 150,00 USD per computer. Vervolgens huurt u een leverancier in om u de computers te leveren waarop software is geïnstalleerd. Volgens de overeenkomst moet de klant de kwaliteit van de computers goedkeuren voordat uw organisatie wordt betaald. Het beleid van uw organisatie is om betalingen aan leveranciers in te houden totdat de klant u heeft betaald. Daarom zet u het project zo op dat er een Betalen bij betaling-percentage van 100 procent geldt.

De leverancier stuurt u de 100 computers waarop software is geïnstalleerd, samen met een factuur voor 10.000,00 USD. Omdat er Betalen bij betaling-voorwaarden zijn opgesteld voor uw project, betaalt u de verkoper niet bij ontvangst van de computers. In plaats daarvan stuurt u de computers naar de klant, samen met een factuur voor 15.000,00. De klant inspecteert de computers en keurt het volledige bedrag van de projectfactuur goed.

Nadat u de volledige betaling van de klant hebt ontvangen, betaalt u aan de leverancier USD 10.000,00, het volledige bedrag van de leveranciersfactuur.

## <a name="set-up-pwp-terms-for-a-project"></a>Betalen bij betaling-voorwaarden instellen voor een project

Wanneer u Betalen bij betaling-voorwaarden voor een project instelt, geeft u als een percentage het minimumbedrag op dat een klant u voor het project moet betalen voordat u de leverancier betaalt. Het drempelbedrag wordt automatisch berekend op de klantfacturen voor het project. Volg deze stappen om het drempelpercentage voor Betalen bij betaling-voorwaarden in te stellen.

1. Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**.
2. Zoek en open het project waarvoor u Betalen bij betaling-voorwaarden wilt instellen.
3. Selecteer **Regel toevoegen** op het sneltabblad **Leveranciersovereenkomsten**.
3. Selecteer in het veld **Rekeningcode** een van de volgende opties:

    - **Tabel** : de Betalen bij betaling-voorwaarden voor leveranciers zijn van toepassing op één leverancier.
    - **Groep** : de Betalen bij betaling-voorwaarden voor leveranciers zijn van toepassing op alle leveranciers in een leveranciersgroep.
    - **Alle** : de Betalen bij betaling-voorwaarden voor leveranciers zijn van toepassing op alle leveranciers.

4. Als u **Tabel** of **Groep** hebt gekozen in de vorige stap, selecteert u in het veld **Leverancier/leveranciersgroep** de leverancier of leveranciersgroep waarop de Betalen bij betaling-voorwaarden van toepassing zijn. Als u **Alle** hebt gekozen in de vorige stap, kan het veld **Leverancier/leveranciersgroep** niet worden bewerkt.
5. Als er inhoudingsvoorwaarden voor leveranciers zijn ingesteld voor de leverancier in het project, selecteert u in het veld **Inhoudingsvoorwaarden voor leveranciers** de regel-id voor de inhoudingsvoorwaarden.
6. In het veld **Betalen bij betaling-drempelpercentage** voert u het drempelpercentage voor het project in. Het percentage dat u voor het project invoert, bepaalt het minimumbedrag dat de klant u moet betalen voordat u de leverancier betaalt.

## <a name="create-a-po-that-has-pwp-terms"></a>Een inkooporder maken met Betalen bij betaling-voorwaarden

Wanneer u een factuur van een leverancier boekt en voor de leverancier Betalen bij betaling-voorwaarden gelden, worden die voorwaarden weergegeven op de inkooporderregels. Volg deze stappen om een inkooporder te maken met Betalen bij betaling-voorwaarden.

1. Ga naar **Inkoop en sourcing** \> **Inkooporders** \> **Alle inkooporders**.
2. Selecteer **Nieuw** in het actievenster. Voer vervolgens in het dialoogvenster **Inkooporder maken** de vereiste informatie in en selecteer **OK**.

    U kunt ook een bestaande inkooporder openen op de lijstpagina **Alle inkooporders**.

4. Bekijk op de pagina **Inkooporder** op het sneltabblad **Inkooporderregels** de details van de inkooporderregel voor de leverancier. De optie **Betalen bij betaling** wordt automatisch geselecteerd en de waarde in het veld **Betalen bij betaling-drempelpercentage** wordt automatisch gekopieerd uit het veld **Betalen bij betaling-drempelpercentage** op de pagina **Projecten**.
6. Als u geen Betalen bij betaling-voorwaarden wilt toepassen op de leverancier voor een inkooporderregel, schakelt u de optie **Betalen bij betaling** uit. In dit geval wordt het veld **Betalen bij betaling-drempelpercentage** voor de inkooporder-regel teruggezet op 0 (nul).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Een klantbetaling bijwerken en de leverancier betalen

Wanneer een leverancier zijn werk aan een project voltooit en u een factuur stuurt, moet u de projectstatus en klantfacturen bekijken om te bepalen of aan de Betalen bij betaling-voorwaarden voor het project is voldaan. Als aan de Betalen bij betaling-voorwaarden voor de leverancier is voldaan, kunt u bepalen welke regels op de leveranciersfactuur u wilt betalen, op basis van de klantbetalingen voor het project. Als u besluit om de leverancier te betalen, ook al werd niet aan de Betalen bij betaling-voorwaarden voldaan, kunt u de Betalen bij betaling-voorwaarden op de pagina **Leveranciersfactuur met betaling bij betaling** negeren.

1. Ga naar **Projectmanagement en financiële administratie** \> **Rapporten en informatieverzoeken** \> **Verzoeken voor inhouding** \> **Leveranciersfactuur met betaling bij betaling**.
2. Op de pagina **Leveranciersfactuur met betaling bij betaling** voert u in het zoekveld waarden in om de leveranciersfactuur te zoeken die u wilt bekijken, en selecteert u vervolgens **Zoeken**.
3. Op het sneltabblad **Leveranciersfactuurregels** selecteert u de regels die u wilt wijzigen.
4. Als aan de voorwaarden voor **Betalen bij betaling** is voldaan voor de factuurregel, selecteert u **Leveranciersbetaling vrijgeven**. De optie **Betalen bij betaling** wordt uitgeschakeld en de waarde van het veld **Klaar voor betaling** wordt gewijzigd in **Ja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]