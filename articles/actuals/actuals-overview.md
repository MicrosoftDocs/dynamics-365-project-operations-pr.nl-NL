---
title: Werkelijke waarden
description: Dit onderwerp biedt informatie over hoe u met werkelijke waarden kunt werken in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581278"
---
# <a name="actuals"></a>Werkelijke waarden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Werkelijke waarden vertegenwoordigen de beoordeelde en goedgekeurde financiële en geplande voortgang van een project. Ze worden gemaakt wanneer vermeldingen voor tijd, onkosten en materiaalgebruik, journaalposten en facturen worden goedgekeurd.

> [!IMPORTANT]
> Werkelijke waarden mogen niet worden bewerkt of uit het systeem worden verwijderd. Anders kan de financiële integriteit en eventuele integratie met andere financiële en boekhoudsystemen nadelig worden beïnvloed. Met Microsoft Dynamics 365 Project Operations kunt u werkelijke waarden terugboeken en vervangen om werkelijke waarden op verschillende punten in de levenscyclus van uw bedrijfsprocessen van uw projecten te bewerken.

## <a name="recording-actuals-based-on-project-events"></a>Werkelijke waarden vastleggen op basis van projectgebeurtenissen

Project Operations registreert de financiële transacties die plaatsvinden tijdens de levenscyclus van een projectopdracht als werkelijke waarden. Het maken van actuele waarden bij verschillende gebeurtenissen in de levenscyclus varieert, afhankelijk van of de projectopdracht het factureringsmodel voor tijd en materialen of het factureringsmodel met een vaste prijs gebruikt, en of het zich in de pre-salesfase bevindt of dat het een intern project is.

In de volgende onderwerpen wordt uitgelegd wat de impact is op de tabel Werkelijke waarden bij verschillende gebeurtenissen voor verschillende variaties:

- [Impact van werkelijke waarden in een tijd- en materiaalopdracht](ActualsonTM.md)
- [Impact van werkelijke waarden in een opdracht met een vaste prijs](ActualonFP.md)
- [Impact van werkelijke waarden tijdens de pre-salesfase van een opdracht](ActualonPreSales.md)
- [Impact van werkelijke waarden voor een intern project](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
