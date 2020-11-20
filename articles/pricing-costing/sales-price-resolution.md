---
title: Verkoopprijzen voor schattingen en werkelijke waarden omzetten
description: Dit onderwerp bevat informatie over hoe verkooptarieven voor schattingen en werkelijke waarden worden omgezet.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119547"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Verkoopprijzen voor schattingen en werkelijke waarden omzetten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Wanneer verkoopprijzen op schattingen en werkelijke waarden worden omgezet in Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta van de gerelateerde projectprijsopgave of het projectcontract om de verkoopprijslijst om te zetten. Nadat de verkoopprijslijst is omgezet, wordt het verkoop- of factuurtarief omgezet.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Verkooptarieven omzetten voor regels met werkelijke waarden en schattingen voor tijd

In Project Operations worden schattingsregels voor tijd gebruikt om de prijsopgaveregel- en contractregeldetails voor tijd en resourcetoewijzingen aan het project aan te geven.

Nadat een prijslijst voor verkopen is omgezet, voert het systeem de volgende stappen uit om het factuurtarief te standaardiseren.

1. De velden **Rol** en **Resourcebedrijf** en **Resource-eenheid** op de schattingsregel voor tijd worden gebruikt voor afstemming met de rolprijsregels in de omgezette prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u standaardprijsdimensies voor factureringstarieven gebruikt. Als u de prijzen hebt geconfigureerd op basis van andere velden in plaats van of naast **Rol**, **Resourcebedrijf** en **Resource-eenheid**, dan wordt die combinatie gebruikt om een overeenkomende rolprijsregel op te halen.
2. Als een rolprijsregel wordt gevonden met een factureringstarief voor de combinatie van de velden **Rol**, **Resourcebedrijf** en **Resource-eenheid**, is dat het standaardfactuurtarief.
3. Als de waarden voor de velden **Rol**, **Resourcebedrijf** en **Resource-eenheid** niet kunnen worden afgestemd, worden rolprijsregels opgehaald met een overeenkomende rol, maar lege waarden van de **Resource-eenheid**. Nadat het systeem een overeenkomende rolprijsrecord heeft gevonden, wordt het factuurtarief uit die record standaard ingesteld. Deze afstemming veronderstelt een standaardconfiguratie voor de relatieve prioriteit van **Rol** versus **Resource-eenheid** als een verkoopprijsdimensie.

> [!NOTE]
> Als u een andere prioriteitstelling van **Rol**, **Bedrijf voor resources** en **Resource-eenheid** hebt geconfigureerd, of als u andere dimensies heeft die een hogere prioriteit hebben, zal dit gedrag dienovereenkomstig veranderen. Rolprijsrecords worden opgehaald met waarden die overeenkomen met elk van de prijsdimensiewaarden in de volgorde van prioriteit, waarbij rijen met null-waarden voor die dimensies als laatste komen.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Verkooptarieven omzetten voor regels met werkelijke waarden en schattingen voor onkosten

In Project Operations worden schattingsregels voor onkosten gebruikt om de prijsopgaveregel- en contractregeldetails voor onkosten en de schattingsregels voor onkosten in het project aan te geven.

Nadat een prijslijst voor verkopen is omgezet, voert het systeem de volgende stappen uit om de verkoopprijs per eenheid te standaardiseren.

1. Een combinatie van de velden **Categorie** en **Eenheid** op de schattingsregel voor onkosten wordt gebruikt voor afstemming met de categorieprijsregels in de omgezette prijslijst.
2. Als een categorieprijsregel wordt gevonden met een verkooptarief voor de combinatie van **Categorie** en **Eenheid**, wordt het verkooptarief standaard ingesteld.
3. Als het systeem een overeenkomende categorieprijsregel vindt, kan de prijsmethode worden gebruikt om de standaardverkoopprijs te bepalen. In de onderstaande tabel ziet u het standaardgedrag van de onkosten in Project Operations.

    | Context | Prijsmethode | Standaardprijs |
    | --- | --- | --- |
    | Schatting | Prijs per eenheid | Gebaseerd op de categorieprijslijn |
    | &nbsp; | Tegen kosten | 0.00 |
    | &nbsp; | Toeslag op kosten | 0.00 |
    | Actueel | Prijs per eenheid | Gebaseerd op de categorieprijslijn |
    | &nbsp; | Tegen kosten | Gebaseerd op de gerelateerde werkelijke kosten |
    | &nbsp; | Toeslag op kosten | Door een toeslag toe te passen zoals gedefinieerd door de categorieprijsregel op het eenheidskostentarief van de gerelateerde werkelijke kosten |

4. Als het systeem de veldwaarden **Categorie** en **Eenheid** niet kan afstemmen, wordt het verkooptarief standaard op nul (0) ingesteld.
