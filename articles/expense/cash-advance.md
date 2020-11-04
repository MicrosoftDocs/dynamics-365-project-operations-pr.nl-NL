---
title: Voorschot
description: Dit onderwerp biedt informatie over (kas)voorschotten.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 209fe0b8a79b2c0689c458c423664cb292da249b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074447"
---
# <a name="cash-advance"></a>Voorschot

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Met een voorschot kunnen werknemers geld van hun bedrijf lenen voordat ze onkosten maken. Wanneer een aangevraagd voorschot is goedgekeurd en betaald, kan de werknemer het geld gebruiken voor de zakelijke onkosten die hij/zij mogelijk gaat maken. 

## <a name="create-and-submit-a-cash-advance-request"></a>Een aanvraag voor een kasvoorschot maken en indienen

1. Onder **Mijn onkosten** selecteert u **Kasvoorschotten** > **Nieuw** om een nieuw kasvoorschot te creëren. 
2. Voer op de pagina **Nieuwe aanvraag kasvoorschot** het onkostendoel in en selecteer de locatie waar de onkosten worden gemaakt.
3. Voer het gevraagde bedrag en de valuta in en selecteer **Opslaan**. 
4. Wanneer u klaar bent om het verzoek om het kasvoorschot in te dienen, selecteert u op de pagina **Aanvraag kasvoorschot** de opties **Werkstroom** > **Indienen**.

## <a name="modify-a-cash-advance-request"></a>Een aanvraag voor een kasvoorschot wijzigen

U kunt een aanvraag voor een kasvoorschot als deze niet ter goedkeuring is ingediend.

1. Onder **Mijn onkosten: Kasvoorschotten** zoekt en selecteert u het kasvoorschot dat u wilt bewerken.
2. Selecteer **Bewerken** en breng de nodige wijzigingen aan in de aanvraag voor een kasvoorschot. 
3. Selecteer **Opslaan en sluiten**.


## <a name="view-cash-advance-requests"></a>Aanvragen voor kasvoorschotten weergeven
U kunt de lijst met alle aanvragen voor kasvoorschotten bekijken die de status Concept, Ingediend, In review of Betaald hebben onder **Mijn onkosten: Kasvoorschotten**. 

## <a name="approve-cash-advance-requests"></a>Aanvragen voor kasvoorschotten goedkeuren

Managers of gebruikers die in de werkstroom zijn geconfigureerd als fiatteurs, kunnen de kasvoorschotten goedkeuren die aan hen ter beoordeling zijn voorgelegd. 

1. Als u een kasvoorschot wilt goedkeuren, selecteert u onder **Kasvoorschotten verwerken** de optie **Kasvoorschotten ter beoordeling door mij**.
2. Selecteer het kasvoorschot dat u wilt bekijken en selecteer **Goedkeuren**.  

## <a name="pay-cash-advances"></a>Kasvoorschotten betalen 
De volgende procedure wordt doorgaans voltooid door een accountant of een gebruiker met boekhoudkundige machtigingen.

1. Selecteer **Goedgekeurde voorschotten** en selecteer vervolgens **Betalen en overmaken** om goedgekeurde kasvoorschotten te boeken.  
2. Geef de journaalgegevens op voor de kasvoorschotten en selecteer vervolgens **OK**. 

## <a name="submit-an-expense-report-against-a-paid-cash-advance"></a>Een onkostennota voor een betaald kasvoorschot indienen 

Wanneer u een onkostennota maakt en indient voor het kasvoorschot dat u al hebt ontvangen, worden de onkosten automatisch verrekend met dat voorschot. Als uw kasvoorschot groter is dan het afgeschreven bedrag, moet u het saldo aan het bedrijf retourneren met behulp van de onkostencategorie **Contant geld retourneren**. Als het door het bedrijf betaalde kasvoorschot lager is dan het bedrag dat u hebt afgeschreven, moet het bedrijf u het saldo terugbetalen. 

### <a name="example"></a>Voorbeeld
U wilt voor een congres van Seattle naar New York City reizen. U maakt een kasvoorschotverzoek voor USD 3000,00 omdat u de kosten van het congresticket, de vlucht, het hotel, de maaltijden en de taxi ongeveer op dit bedrag hebt geschat. U wordt pas betaald als uw manager dit verzoek heeft goedgekeurd. Nadat uw manager akkoord is gegaan, wordt het gevraagde kasvoorschot als USD 3000,00 USD op uw bankrekening gestort. Vervolgens woont u het congres bij. Na uw reis merkt u dat de totale uitgaven slechts USD 2790,00 bedroegen. Selecteer **Contant geld** in het veld **Betalingswijze** en dien uw onkosten voor USD 2790,00 in. Uw ingediende onkostenbedrag wordt automatisch verrekend met het kasvoorschot van USD 3000,00 dat aan u is uitgeleend. U bent nu een saldo van USD 210,00 (3000,00 - 2790,00) aan het bedrijf verschuldigd, dat u met de onkostencategorie **Contant geld retourneren** kunt terugbetalen aan het bedrijf. 
