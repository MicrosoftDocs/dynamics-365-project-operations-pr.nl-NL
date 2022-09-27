---
title: Onkostennota's boeken
description: In dit artikel wordt uitgelegd hoe u onkostennota's boekt.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524863"
---
# <a name="post-expense-reports"></a>Onkostennota's boeken

Nadat een onkostendeclaratie is goedgekeurd en naar het journaal is overgeboekt, kan deze worden geboekt. Wanneer u een onkostendeclaratie boekt, worden uitgaven geïdentificeerd die in aanmerking komen voor terugvordering van belasting over de omzetbelasting. De taak om btw-betalingen te verifiëren en terug te vorderen, wordt toegewezen aan de werknemer die verantwoordelijk is voor het verifiëren van de onkostendeclaratie.

Als kosten op een onkostendeclaratie in rekening worden gebracht bij een ander bedrijf dan het bedrijf dat de werknemer in dienst heeft, moet u zowel het bedrijf verifiëren waaraan die kosten verschuldigd zijn aan als het bedrijf waaraan ze verschuldigd zijn. De werknemer die een onkostendeclaratie heeft ingediend, werkt bijvoorbeeld voor het DAT-bedrijf, maar heeft kosten in rekening gebracht bij het DIR-bedrijf. In dit geval is DAT het bedrijf waaraan de kosten verschuldigd zijn en DIR het bedrijf waarvan de kosten verschuldigd zijn. Nadat u deze journaalregels hebt gecontroleerd, kunt u de onkostenregels naar het grootboek boeken.

Om een onkostendeclaratie te boeken selecteert u op de pagina **Goedgekeurde onkostendeclaraties** de onkostendeclaratie en vervolgens in het actievenster **Boeken**.

U kunt ook alle onkostendeclaraties in de lijst tegelijk boeken. Selecteer alle onkostendeclaraties en vervolgens **Boeken**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>De functie Mogelijkheid om onkostenverplichtingen in leveranciersvaluta te boeken voor contante betalingsmethode inschakelen

Met de functie  **Mogelijkheid om onkostenverplichtingen in leveranciersvaluta te boeken voor contante betalingsmethode** kunnen onkostennota's worden geboekt in een leveranciersvaluta voor de contante betalingsmethode.

Wanneer u momenteel contante uitgaven indient, worden onkostennota's geboekt in de boekhoudvaluta. Vanwege de omrekening van bedragen tussen de transactievaluta, boekhoudvaluta en leveranciersvaluta wordt een onjuist bedrag betaald aan leveranciers als de transactiedatum van de onkosten en de werkelijke betalingsdatum verschillende wisselkoersen hebben.

Deze functie zorgt ervoor dat het leverancierssaldo wordt vastgelegd in de leveranciersvaluta wanneer de onkostennota wordt geboekt.

1. Ga naar **Werkruimten** \> **Functiebeheer**.
2. Zoek in de lijst de optie **Mogelijkheid om onkostenverplichtingen in leveranciersvaluta te boeken voor contante betalingsmethode**, selecteer deze en selecteer vervolgens **Nu inschakelen**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
