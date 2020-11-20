---
title: Een prijsopgave sluiten - lite
description: Dit onderwerp biedt informatie over het sluiten van een prijsopgave in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175705"
---
# <a name="close-a-quote---lite"></a>Een prijsopgave sluiten - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een projectprijsopgave kan worden afgesloten als Gewonnen of Verloren. Omdat de functies Activeren en Herzien niet worden ondersteund voor prijsopgaven in Microsoft Dynamics 365 Project Operations kunt u een conceptofferte sluiten.

## <a name="close-a-quote-as-won"></a>Een prijsopgave sluiten als gewonnen

Als u een projectprijsopgave afsluit als gewonnen, wordt de status van de prijsopgave ingesteld op Gesloten en de statusreden op Gewonnen. Als de prijsopgave wordt afgesloten, wordt deze alleen-lezen en wordt een concept-projectcontract gecreëerd dat de informatie bevat. Omdat een gesloten prijsopgave niet heropend kan worden, een bevestigingsvenster. Er is een bevestigingsvenster voordat de wijzigingen worden doorgevoerd, aangezien een gesloten prijsopgave niet opnieuw kan worden geopend en de wijzigingen onomkeerbaar zijn.

Als de prijsopgave is gekoppeld aan een verkoopkans, worden alle andere projectprijsopgaven voor de verkoopkans automatisch gesloten als Verloren.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financiële gevolgen van het sluiten van een prijsopgave als Gewonnen

Als er voor een project werkelijke tijd is geregistreerd terwijl dit nog aan een conceptprijsopgave is gehecht, worden alleen de kosten van de tijd of uitgaven geregistreerd. Nadat een prijsopgave is gesloten als Gewonnen, zal de toepassing de kosten herfactureren door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te creëren. De applicatie verwerkt deze werkelijke kosten op basis van de factureringsmethode van de bijbehorende projectcontractregel. Als de werkelijke kosten verwijzen naar een contractregel voor tijd en materiaal, zal het systeem automatisch overeenkomstige niet-gefactureerde werkelijke verkoopcijfers creëren voor wanneer de offerte wordt gesloten en het projectcontract wordt gecreëerd. Als de werkelijke kosten verwijzen naar een contractregel met een vaste prijs, stopt de applicatie met het opnieuw verwerken van de werkelijke kosten op basis van de regels voor gesplitste facturering voor de projectcontractklanten.

## <a name="closing-a-quote-as-lost"></a>Een prijsopgave sluiten als verloren:

Als u een projectprijsopgave afsluit als verloren, wordt de status van de prijsopgave ingesteld op Gesloten en de statusreden op Verloren. Als u de prijsopgave sluit, wordt de prijsopgave van het project alleen-lezen. Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.

Als de projectprijsopgave is gesloten als Verloren een project heeft waarnaar wordt verwezen op een van de regels, wordt dat project ook gemarkeerd als Gesloten en worden alle resourceboekingen vanaf die dag geannuleerd.

> [!NOTE]
> In Project Operations heeft het sluiten van een prijsopgave als Gewonnen of Verloren geen invloed op de status van de verkoopkans. Deze blijft open totdat deze handmatig wordt gesloten.
