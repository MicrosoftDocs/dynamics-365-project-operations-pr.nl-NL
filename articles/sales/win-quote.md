---
title: Een prijsopgave sluiten
description: Dit onderwerp biedt informatie over het sluiten van prijsopgaven in Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 25f5a515769b97e963b2a2ac8738884b3f0db2fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598574"
---
# <a name="close-a-quote"></a>Een prijsopgave sluiten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een projectprijsopgave kan worden afgesloten als Gewonnen of Verloren. Omdat de functies Activeren en Herzien van prijsopgaven niet worden ondersteund in Microsoft Dynamics 365 Project Operations, kunt u een conceptprijsopgave sluiten.

## <a name="close-a-quote-as-won"></a>Een prijsopgave sluiten als gewonnen

Als u een projectprijsopgave afsluit als gewonnen, wordt de status van de prijsopgave ingesteld op **Gesloten** en de statusreden op **Gewonnen**. Als de prijsopgave wordt afgesloten, wordt deze alleen-lezen en wordt een concept-projectcontract gecreëerd met alle informatie. Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.

Het projectcontract dat wordt gecreëerd op basis van een projectprijsopgave, wordt ook beschikbaar gesteld in de module Projectbeheer en financiële administratie van Project Operations. Als een projectcontract op geen van de regels aan een project is toegewezen, wordt dit projectcontract beschikbaar gemaakt als een inactief projectcontract en wordt het actief zodra een project is toegewezen aan ten minste één van zijn contractregels.

Als de prijsopgave is gekoppeld aan een verkoopkans, worden alle andere projectprijsopgaven voor de verkoopkans automatisch gesloten als Verloren.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Financiële gevolgen van het sluiten van een prijsopgave als Gewonnen

Als er voor een project werkelijke tijd is geregistreerd terwijl dit nog aan een conceptprijsopgave is gehecht, worden alleen de kosten van de tijd of uitgaven geregistreerd. Nadat een prijsopgave is gesloten als Gewonnen, zal de toepassing de kosten herfactureren door de oudere werkelijke kosten om te keren en nieuwe werkelijke kosten opnieuw te creëren. De applicatie verwerkt deze werkelijke kosten op basis van de factureringsmethode van de bijbehorende projectcontractregel. Als de werkelijke kosten verwijzen naar een contractregel voor tijd en materiaal, zal het systeem automatisch overeenkomstige niet-gefactureerde werkelijke verkoopcijfers creëren voor wanneer de offerte wordt gesloten en het projectcontract wordt gecreëerd. Als de werkelijke kosten verwijzen naar een contractregel met een vaste prijs, stopt de applicatie met het opnieuw verwerken van de werkelijke kosten op basis van de regels voor gesplitste facturering voor de projectcontractklanten.

Alle opnieuw verwerkte werkelijke waarden beschikbaar zijn in de module Projectmanagement en financiële administratie zodat de projectaccountant deze kan beoordelen, bijwerken en naar het grootboek kan boeken. 

## <a name="close-a-quote-as-lost"></a>Een prijsopgave sluiten als verloren

Als u een projectprijsopgave afsluit als verloren, wordt de status van de prijsopgave ingesteld op **Gesloten** en de statusreden op **Verloren**. Als u de prijsopgave sluit, wordt deze alleen-lezen. Omdat een gesloten prijsopgave niet opnieuw kan worden geopend, zal een bevestigingsvenster uw wijzigingen bevestigen voordat u een prijsopgave sluit.

Als de projectprijsopgave is gesloten als Verloren een project heeft waarnaar wordt verwezen op een van de regels, wordt dat project ook gemarkeerd als Gesloten en worden alle resourceboekingen vanaf die dag geannuleerd.

> [!NOTE]
> In Project Operations heeft het sluiten van een prijsopgave als Gewonnen of Verloren geen invloed op de status van de verkoopkans. Deze blijft open totdat deze handmatig wordt gesloten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]