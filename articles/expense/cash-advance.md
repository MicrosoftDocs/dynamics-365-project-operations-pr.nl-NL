---
title: Voorschot
description: Dit artikel biedt informatie over kasvoorschotten.
author: suvaidya
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: bc270944faa7c16d2e97a988495a2a16380ba879
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931508"
---
# <a name="cash-advance"></a>Voorschot

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Met een voorschot kunnen werknemers geld van hun bedrijf lenen voordat ze onkosten maken. Wanneer een aangevraagd voorschot is goedgekeurd en betaald, kan de werknemer het geld gebruiken voor de zakelijke onkosten die hij/zij mogelijk gaat maken. 

## <a name="create-and-submit-a-cash-advance-request"></a>Een aanvraag voor een kasvoorschot maken en indienen
Om een nieuw kasvoorschot aan te maken en een verzoek om een kasvoorschot in te dienen, doet u het volgende: 

1. Selecteer onder **Mijn onkosten**, **Kasvoorschotten** > **Nieuw**. 
2. Voer op de pagina **Nieuwe aanvraag kasvoorschot** het onkostendoel in en selecteer de locatie waar de onkosten worden gemaakt.
3. Voer het gevraagde bedrag en de valuta in en selecteer **Opslaan**. 
4. Wanneer u klaar bent om het verzoek om het kasvoorschot in te dienen, selecteert u op de pagina **Aanvraag kasvoorschot** de opties **Werkstroom** > **Indienen**.

## <a name="modify-a-cash-advance-request"></a>Een aanvraag voor een kasvoorschot wijzigen

U kunt een aanvraag voor een kasvoorschot als deze niet ter goedkeuring is ingediend.

1. Zoek en selecteer onder **Mijn onkosten: kasvoorschotten** het kasvoorschot dat u wilt bewerken.
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

Wanneer u een onkostendeclaratie maakt en indient voor het kasvoorschot dat u al hebt ontvangen, worden de onkosten automatisch verrekend met dat voorschot. Als uw kasvoorschot groter is dan het afgeschreven bedrag, moet u het saldo aan het bedrijf retourneren met behulp van de onkostencategorie **Contant geld retourneren**. Als het door het bedrijf betaalde kasvoorschot lager is dan het bedrag dat u hebt uitgegeven, moet het bedrijf u het saldo terugbetalen. 

### <a name="select-cash-advances-that-apply-to-your-expenses"></a>Voorschotten selecteren die van toepassing zijn op uw uitgaven
Voordat u een onkostennota indient, kunt u het voorschot selecteren dat overeenkomt met de onkostentransacties in het rapport. Als u deze functionaliteit wilt gebruiken, moeten de volgende twee functies zijn ingeschakeld via de werkruimte **Functiebeheer**:

  - Opnieuw ontworpen onkostennota's
  - Mogelijkheid om voorschotten toe te wijzen aan onkostenregels
 
 Als deze functies zijn ingeschakeld:
 
  - U kunt voor elke onkostenregel een of meer kasvoorschotten toevoegen.
  - Het beschikbare saldo van een voorschot is in realtime zichtbaar wanneer een onkostennota wordt opgeslagen. Zo kunt u onkostentransacties verwerken en tegelijkertijd contante transacties retourneren.
  - U kunt voor één onkostentransactie meerdere voorschotten selecteren.
  - Afstemmingsgegevens voor voorschotten zijn beschikbaar met behulp van een query. 
 
Als u deze functies niet gebruikt, blijft de functionaliteit hetzelfde, waarbij bestaande voorschotten automatisch worden verlaagd als er onkosten worden ingediend.

### <a name="example"></a>Voorbeeld 
U bent van plan om van Seattle naar New York City te reizen voor een conferentie. U maakt een aanvraag voor een kasvoorschot aan voor 3000,00 USD op basis van de geschatte kosten van het conferentieticket, vluchten, hotel, maaltijden en taxi. Dit wordt niet betaald, tenzij uw manager deze aanvraag goedkeurt. Nadat uw manager akkoord is gegaan, wordt het gevraagde kasvoorschot als USD 3000,00 USD op uw bankrekening gestort. Vervolgens woont u het congres bij. Na uw reis merkt u dat de totale uitgaven slechts USD 2790,00 bedroegen. Selecteer **Contant geld** in het veld **Betalingswijze** en dien uw onkosten voor 2790,00 USD in. Uw ingediende onkostenbedrag wordt automatisch verrekend met het kasvoorschot van USD 3000,00 dat aan u is uitgeleend. U bent nu een saldo van 210,00 USD (3000,00 - 2790,00) verschuldigd, dat u aan het bedrijf kunt retourneren met de onkostencategorie **Retouren kas**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
