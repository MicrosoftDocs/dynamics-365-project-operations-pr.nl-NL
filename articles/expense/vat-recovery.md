---
title: Btw-terugvordering in Onkostenbeheer
description: In dit onderwerp wordt uitgelegd hoe u terugbetalingen kunt ontvangen voor bepaalde btw-transacties.
author: suvaidya
manager: AnnBe
ms.date: 10/10/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1c7bd2cb3b200ef3be735484d4e831a7a5793d58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275937"
---
# <a name="vat-recovery-in-expense-management"></a>Btw-terugvordering in Onkostenbeheer

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Om terugbetaling te ontvangen voor in aanmerking komende btw-transacties moet een bedrijf of organisatie nauwkeurige informatie opgeven, verzamelen, verifiëren en indienen. Dit proces omvat meerdere taken en kan, afhankelijk van de grootte van uw bedrijf, betrekking hebben op meerdere medewerkers of rollen.

Als u btw wilt terugvorderen in de module **Onkostenbeheer**, moet aan de volgende voorwaarden worden voldaan:

- Belastingcodes moeten zijn gemaakt voor landen/regio's die zijn toegewezen aan onkostencategorieën.
- Voor elke belastingcode moet een btw-groep worden aangemaakt.
- Voor elke btw-groep moet een omzetbelastingscode voor het artikel worden aangemaakt.

Nadat aan de vereisten is voldaan, moeten de volgende stappen worden voltooid om teruggave van btw-transacties aan te vragen.

1. Voer op een onkostendeclaratie belastinggegevens in over de creditcardtransacties om de in aanmerking komende btw-teruggaven te identificeren.
2. Controleer of alle belastinggegevens compleet zijn en boek vervolgens de onkostendeclaratie.
3. Verwerk onkosten die in aanmerking komen voor internationale btw-teruggave.
4. Verzend de gegevens over de btw-teruggave naar de derde leverancier om de internationale terugvorderingsaangifte in te dienen.
5. Verwerk de kosten voor de binnenlandse btw-terugvordering.

De volgende secties bevatten voorbeelden die laten zien hoe Contoso-medewerkers deze stappen voltooien.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Voer belastinggegevens in over de creditcardtransacties om de in aanmerking komende btw-teruggaven te identificeren

Nancy, een verkoopvertegenwoordiger van Contoso die in de Verenigde Staten is gevestigd, is onlangs teruggekeerd van een verkoopreis naar het Verenigd Koninkrijk. Tijdens de reis maakte Nancy wat persoonlijke creditcardkosten voor maaltijden. Nancy moet nu een onkostendeclaratie maken om de onkosten af te stemmen.

Wanneer Nancy informatie invoert op de onkostendeclaratie, selecteert ze **Verenigd Koninkrijk** in het veld **Land/regio** op de pagina **Onkostendeclaratie bewerken**. De lijst met btw-groepen wordt vervolgens gefilterd, zodat alleen de groepen worden weergegeven die van toepassing zijn op het Verenigd Koninkrijk. Nancy selecteert de btw-groep **Verenigd Koninkrijk 001** en selecteert vervolgens de omzetbelastingsgroep voor het artikel **Maaltijden**. Vervolgens voegt Nancy een nieuwe transactie toe voor accommodatie. Omdat er slechts één btw-groep is en één omzetbelastingsgroep voor artikelen voor accommodatie in het Verenigd Koninkrijk, wordt deze informatie automatisch ingevuld op de onkostendeclaratie van Nancy.

Volgens het beleid van Contoso moet er voor alle onkosten een overeenkomend kwitantie zijn. Wanneer Nancy de onkostendeclaratie opslaat, ontvangt ze daarom een bericht waarin staat dat ze een kwitantie moet bijvoegen voor elke transactie die ze op haar onkostendeclaratie heeft vermeld. Nancy controleert of ze een digitale afbeelding van elke transactiebon heeft toegevoegd aan haar onkostendeclaratie en stuurt deze vervolgens ter goedkeuring in. Vervolgens stuurt ze de papieren bonnen naar het backoffice-verwerkingsteam. Dit team stuurt de gegevens voor de btw-teruggave naar de derde leverancier die internationale btw-terugvorderingsaangiften voor Contoso indient.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Belastinggegevens controleren en een onkostendeclaratie boeken

Voordat April, de coördinator bij de crediteurenadministratie voor Contoso, een onkostendeclaratie kan boeken, zij moet alle ontbrekende belastinggegevens invoeren. Ze opent de pagina **Details van onkostendeclaratie** en ziet Nancy's goedgekeurde onkostendeclaratie. April opent vervolgens de onkostendeclaratie om de details van de transacties te bekijken. Ze ziet dat Nancy geen btw-groep voor een van de transacties heeft ingevoerd. Omdat deze informatie niet wordt verstrekt, kan April de onkostendeclaratie niet boeken. Daarom kijkt ze op de pagina **Belastingconfiguraties** in Onkostenbeheer en zoekt ze de juiste omzetbelastingsgroep van het artikel voor land/regio en het transactietype. April kan nu de onkostendeclaratie naar het grootboek boeken.

Wanneer April de onkostendeclaratie boekt, wordt een werkitem voor de btw-teruggave aangemaakt. Dit werkitem wordt toegewezen aan een lid van het backoffice-verwerkingsteam. April ontvangt een bericht met de bevestiging dat de boeking is gelukt. Dit bericht vermeldt ook het aantal btw-transacties dat is geïdentificeerd voor terugvordering.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Onkosten verwerken die in aanmerking komen voor internationale btw-teruggave

Arnie, een lid van het backoffice-verwerkingsteam van Contoso, is verantwoordelijk voor het controleren of alle vereiste informatie voor btw-terugvordering is opgenomen in onkostendeclaraties. Hij opent de pagina **Terugvordering van belasting op onkosten** en selecteert de onkostendeclaratie die Nancy heeft ingediend. Arnie controleert vervolgens of alle vereiste kwitanties zijn bijgevoegd en of de juiste btw-groep en btw-codes voor artikelen zijn ingevoerd.

Wanneer Arnie de papieren kwitanties van Nancy ontvangt, verifieert hij ze met de digitale ontvangstbewijzen en verandert vervolgens de status van de onkostendeclaratie in **Klaar voor terugvordering**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Btw-terugvorderingsgegevens naar derde leverancier verzenden

Wanneer Arnie klaar is om de onkostendeclaratiegegevens naar de derde leverancier te sturen die de btw-terugvordering zal indienen, opent hij de pagina **Terugvordering van belasting op onkosten**. Hij filtert de pagina zodat deze alleen de onkostendeclaraties toont die zijn gemarkeerd als **Klaar voor terugvordering**. Arnie selecteert vervolgens **Bestand** &gt; **Exporteren naar Excel**. De btw-gegevens uit de onkostendeclaraties worden geëxporteerd naar een Microsoft Excel-werkblad. Arnie stuurt dit werkblad door naar de derde leverancier en voegt een bericht toe waarin staat dat de papieren kwitanties per post zijn verzonden.

## <a name="process-expenses-for-domestic-vat-recovery"></a>De onkosten voor de binnenlandse btw-terugvordering verwerken

Arnie moet controleren of de onkostendeclaratietransacties in aanmerking komen voor btw-terugvordering, en dat de digitale kwitanties bij de rapportages worden gevoegd. Om te beginnen met het verwerken van in aanmerking komende uitgaven voor binnenlandse terugvordering, opent Arnie de pagina **Terugvordering van belasting op onkosten** en selecteert hij de onkostendeclaratie die moet worden geverifieerd. Hij controleert of de bonnen op naam van het bedrijf staan in plaats van op de werknemer. (Voor btw-terugvordering moeten de kwitanties op naam van het bedrijf staan.) Arnie controleert vervolgens of alle vereiste kwitanties zijn bijgevoegd en of de juiste btw-groep en btw-codes voor artikelen zijn ingevoerd.

Wanneer Arnie de papieren ontvangstbewijzen ontvangt, verandert hij de status van de onkostendeclaratie in **Klaar voor terugvordering**. Hij kan dan de aangifte indienen bij de betreffende belastingdienst. In dit geval gaat het in de Verenigde Staten om de Internal Revenue Service (IRS).


[!INCLUDE[footer-include](../includes/footer-banner.md)]