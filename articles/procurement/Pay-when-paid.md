---
title: Leveranciersbetalingen op basis van Betalen bij betaling
description: In deze onderwerp wordt uitgelegd hoe u het Betalen bij betaling-scenario kunt gebruiken.
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525332"
---
# <a name="pay-when-paid-vendor-payments"></a>Leveranciersbetalingen op basis van Betalen bij betaling

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In deze onderwerp wordt uitgelegd hoe u het Betalen bij betaling-scenario kunt gebruiken.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Een inkooporder maken met Betalen bij betaling-voorwaarden

Wanneer u een factuur van een leverancier boekt en voor de leverancier Betalen bij betaling-voorwaarden gelden, worden die voorwaarden weergegeven op de inkooporderregels. Volg deze stappen om een inkooporder te maken met Betalen bij betaling-voorwaarden.

1. Voer een of meer van deze stappen uit in Microsoft Dynamics 365 Finance:

    - Ga naar **Inkoop en sourcing** \> **Inkooporders** \> **Alle inkooporders**. Selecteer **Nieuw** in het actievenster. Selecteer in het dialoogvenster **Inkooporder maken** de leverancier waarvoor Betalen bij betaling-voorwaarden zijn ingesteld voor het project, voer andere vereiste informatie in en selecteer vervolgens **OK**.
    - Ga naar **Projectmanagement en financiële administratie** \> **Projecten** \> **Alle projecten**. Selecteer in het actievenster op het tabblad **Beheren** de optie **Artikeltaak**. Selecteer de inkooporder. Selecteer de leverancier waarvoor Betalen bij betaling-voorwaarden zijn ingesteld voor het project en selecteer vervolgens **OK**.

2. Selecteer op de pagina **Inkooporder** op het sneltabblad **Inkooporderregels** de optie **Regel toevoegen** om een inkooporderregel te maken.
3. Selecteer het artikelnummer of de aanschafcategorie en voer de overige vereiste gegevens in. Bekijk de details van de inkooporderregel voor de leverancier.

    De optie **Betalen bij betaling** wordt automatisch geselecteerd en de waarde in het veld **Betalen bij betaling-drempelpercentage** wordt automatisch gekopieerd uit het veld **Betalen bij betaling-drempelpercentage** op de pagina **Projecten**.

4. Als u geen Betalen bij betaling-voorwaarden wilt toepassen op de leverancier voor een inkooporderregel, schakelt u de optie **Betalen bij betaling** uit. In dit geval wordt het veld **Betalen bij betaling-drempelpercentage** voor de inkooporderregel teruggezet op **0** (nul).
5. Selecteer op de pagina **Inkooporder** in het actievenster op het tabblad **Inkoop** de optie **Bevestigen** om de inkooporder te bevestigen.
6. Selecteer vervolgens in het actievenster op het tabblad **Factuur** de optie **Factuur** om de factuur voor de inkooporder te genereren.

## <a name="create-a-project-invoice-proposal"></a>Een projectfactuurvoorstel maken

Projectfactuurvoorstellen worden gebruikt om projectfacturen voor de klant te maken. In het Betalen bij betaling-scenario zijn leveranciersbetalingen afhankelijk van klantbetalingen volgens de Betalen bij betaling-instellingen. Er zijn echter opties waarmee u de betalingen naar wens kunt vrijgeven zonder klantbetalingen. Volg deze stappen om een projectfactuur voor de klant te maken.

1. Ga in apps voor klantbetrokkenheid naar **Projecten** \> **Projecten** en selecteer het project.
2. Selecteer op het tabblad **Werkelijke waarden** de werkelijke regel die wordt gegenereerd door de inkooporder met het transactietype **Niet-gefactureerde verkopen**. Selecteer vervolgens **Gereed voor facturering**.
3. Ga naar **Verkoop** \> **Verkoop** \> **Projectcontract** en selecteer het projectcontract.
4. Selecteer **Factuur** in het actievenster om de klantfactuur te genereren.
5. Ga in Finance naar **Projectmanagement en boekhouding** \> **Periodiek** \> **Importeren uit opslagtabel** en selecteer **OK** om het Project Operations-integratiejournaal te genereren.
6. Ga naar **Projectmanagement en boekhouding**\>**Projectfacturen**\>**Projectfactuurvoorstel** en selecteer **Boeken** om het factuurvoorstel te boeken dat voor het project is gegenereerd.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Een klantbetaling bijwerken en de leverancier betalen

Wanneer een leverancier zijn werk aan een project voltooit en u een factuur stuurt, moet u de projectstatus en klantfacturen bekijken om te bepalen of aan de Betalen bij betaling-voorwaarden voor het project is voldaan. Als aan de Betalen bij betaling-voorwaarden voor de leverancier is voldaan, kunt u bepalen welke regels op de leveranciersfactuur u wilt betalen, op basis van de klantbetalingen voor het project. Als u besluit om de leverancier te betalen, ook al werd niet aan de Betalen bij betaling-voorwaarden voldaan, kunt u de Betalen bij betaling-voorwaarden op de pagina **Leveranciersfactuur met betaling bij betaling** negeren.

1. Ga in Finance naar **Projectmanagement en boekhouding** \> **Projecten** \> **Alle projecten** en selecteer het project.
2. Selecteer in het actievenster **Besturingselement** en selecteer vervolgens **Leveranciersfacturen** om alle leveranciersfacturen weer te geven die voor het project zijn gegenereerd.
3. Op de pagina **Leveranciersfactuur met betaling bij betaling** voert u in het zoekveld waarden in om de leveranciersfactuur te zoeken die u wilt bekijken, en selecteert u vervolgens **Zoeken**.
4. Selecteer de optie **Betalen bij betaling** om alleen Betalen bij betaling-facturen te bekijken.
5. Op het sneltabblad **Leveranciersfactuurregels** selecteert u de regels die u wilt vrijgeven voor betaling.
6. Selecteer **Leveranciersbetaling vrijgeven**. De optie **Betalen bij betaling** wordt uitgeschakeld en de waarde van het veld **Klaar voor betaling** wordt gewijzigd in **Ja**.
