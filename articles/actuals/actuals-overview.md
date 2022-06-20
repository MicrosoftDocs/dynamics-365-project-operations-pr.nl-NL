---
title: Werkelijke waarden
description: Dit artikel bevat informatie over het werken met actuele waarden in Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924792"
---
# <a name="actuals"></a>Werkelijke waarden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Werkelijke waarden vertegenwoordigen de beoordeelde en goedgekeurde financiële en geplande voortgang van een project. Ze worden gemaakt wanneer vermeldingen voor tijd, onkosten en materiaalgebruik, journaalposten en facturen worden goedgekeurd.

> [!IMPORTANT]
> Werkelijke waarden mogen niet worden bewerkt of uit het systeem worden verwijderd. Anders kan de financiële integriteit en eventuele integratie met andere financiële en boekhoudsystemen nadelig worden beïnvloed. Met Microsoft Dynamics 365 Project Operations kunt u werkelijke waarden terugboeken en vervangen om werkelijke waarden op verschillende punten in de levenscyclus van uw bedrijfsprocessen van uw projecten te bewerken.

## <a name="recording-actuals-based-on-project-events"></a>Werkelijke waarden vastleggen op basis van projectgebeurtenissen

Project Operations registreert de financiële transacties die plaatsvinden tijdens de levenscyclus van een projectopdracht als werkelijke waarden. Het maken van actuele waarden bij verschillende gebeurtenissen in de levenscyclus varieert, afhankelijk van of de projectopdracht het factureringsmodel voor tijd en materialen of het factureringsmodel met een vaste prijs gebruikt, en of het zich in de pre-salesfase bevindt of dat het een intern project is.

In de volgende artikelen wordt uitgelegd wat de impact is op de tabel Werkelijke waarden bij verschillende gebeurtenissen voor verschillende variaties:

- [Impact van werkelijke waarden in een tijd- en materiaalopdracht](ActualsonTM.md)
- [Impact van werkelijke waarden in een opdracht met een vaste prijs](ActualonFP.md)
- [Impact van werkelijke waarden tijdens de pre-salesfase van een opdracht](ActualonPreSales.md)
- [Impact van werkelijke waarden voor een intern project](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
