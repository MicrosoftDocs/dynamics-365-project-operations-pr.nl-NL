---
title: Een projectcontract bevestigen
description: Dit onderwerp bevat informatie over het bevestigen van een contract in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: babce9c64098a9c87072786d914d2340251a8986
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074684"
---
# <a name="confirm-a-project-contract"></a>Een projectcontract bevestigen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Een projectcontract in Dynamics 365 Project Operations kan actief zijn met een reden van **Bevestigd** , of gesloten met een reden van **Verloren**. Wanneer u een projectcontract bevestigt, wordt de status bijgewerkt van **Concept** naar **Actief** en is de reden van de status **Bevestigd**. Een actief of gesloten contract kan niet worden bewerkt of heropend. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Financiële gevolgen van het bevestigen van een projectcontract

Nadat een projectcontract is bevestigd, worden de kosten opnieuw berekend door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te maken. De nieuwe werkelijke kosten worden vervolgens op basis van de factureringsmethode van de bijbehorende projectcontractregel verwerkt. Als de werkelijke kosten verwijzen naar een contractregel die is ingesteld op Tijd- en materiaalverbruik, worden automatisch bijbehorende niet-gefactureerde werkelijke verkoopcijfers opnieuw gemaakt. Als de werkelijke kosten verwijzen naar een contractregel die is ingesteld op Vaste prijs, wordt gestopt met de herverwerking van de werkelijke kosten.

De niet te overschrijden limieten, de toerekenbaarheidsinstelling en de instellingen voor prijzen en kosten voor de werkelijke waarden worden geëvalueerd en vervolgens bijgewerkt als onderdeel van het bevestigingsproces.

## <a name="close-a-project-contract-as-lost"></a>Een projectcontract sluiten als verloren

Wanneer u een projectcontract als verloren sluit, wordt de contractstatus bijgewerkt naar **Gesloten** en is de statusreden **Verloren**. Het projectcontract wordt alleen-lezen. Er wordt een bevestigingsvenster weergegeven voordat de wijzigingen worden doorgevoerd, omdat u een gesloten projectcontract niet opnieuw kunt openen.

Als het projectcontract dat als verloren is gesloten, verwijst naar een project op de bijbehorende regels, wordt dat project ook gemarkeerd als gesloten. Alle resourceboekingen worden vanaf die dag geannuleerd. Eventuele niet-gefactureerde werkelijke verkoopcijfers op het projectcontract die nog niet op een factuur staan, worden teruggedraaid.

> [!NOTE]
> In Dynamics 365 Project Operations heeft het sluiten van een projectcontract als verloren geen invloed op die status van de gekoppelde verkoopkans. De verkoopkans blijft open en moet handmatig worden gesloten.
