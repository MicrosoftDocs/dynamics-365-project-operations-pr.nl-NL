---
title: Een prijsopgave sluiten - lite
description: Dit onderwerp biedt informatie over het sluiten van een prijsopgave in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764858"
---
# <a name="close-a-quote---lite"></a>Een prijsopgave sluiten - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een projectprijsopgave kan worden afgesloten als Gewonnen of Verloren. Een conceptprijsopgave kan worden gesloten omdat de bewerkingen Activeren en Herzien van prijsopgaven niet worden ondersteund in Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Een prijsopgave sluiten als gewonnen

Wanneer u een projectprijsopgave als Binnengehaald sluit, wordt de status ingesteld op Gesloten en de reden van status is Binnengehaald. Als de prijsopgave wordt afgesloten, wordt deze alleen-lezen en wordt een concept-projectcontract gecreëerd dat de informatie bevat. Omdat een gesloten prijsopgave niet heropend kan worden, zal een bevestigingsvenster uw wijzigingen bevestigen.

Als de prijsopgave is gekoppeld aan een verkoopkans, worden alle andere projectprijsopgaven voor de verkoopkans automatisch gesloten als Verloren.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financiële gevolgen van het sluiten van een prijsopgave als Gewonnen

Als er werkelijke waarden zijn voor tijd van een project terwijl dit nog aan een conceptprijsopgave is gekoppeld, worden alleen de kosten van de tijd of de onkosten geregistreerd. Nadat een prijsopgave is gesloten als Gewonnen, zal de toepassing de kosten herfactureren door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te creëren. De applicatie verwerkt deze werkelijke kosten op basis van de factureringsmethode van de bijbehorende projectcontractregel. Als de werkelijke kosten verwijzen naar een tijd- en materiaalcontractregel, worden overeenkomstige niet-gefactureerde werkelijke verkoopcijfers gemaakt voor het moment waarop de prijsopgave wordt gesloten en het projectcontract wordt gecreëerd. Als de werkelijke kosten verwijzen naar een contractregel met een vaste prijs, stopt de toepassing met het opnieuw verwerken van de werkelijke kosten die zijn gebaseerd op de regels voor gesplitste facturering voor de projectcontractklanten.

## <a name="closing-a-quote-as-lost"></a>Een prijsopgave sluiten als verloren:

Wanneer u een projectprijsopgave sluit als Gemist, wordt de status ingesteld op Gesloten en de reden van status is Gemist. Als u de prijsopgave sluit, wordt de prijsopgave van het project alleen-lezen. Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.

Als de projectprijsopgave die wordt gesloten als Gemist verwijst naar een project op een van de regels, wordt dat project ook gemarkeerd als Gemist. Alle resourceboekingen worden vanaf die dag geannuleerd.

> [!NOTE]
> In Project Operations heeft het sluiten van een prijsopgave als Gewonnen of Verloren geen invloed op de status van de verkoopkans. Deze blijft open totdat deze handmatig wordt gesloten.
