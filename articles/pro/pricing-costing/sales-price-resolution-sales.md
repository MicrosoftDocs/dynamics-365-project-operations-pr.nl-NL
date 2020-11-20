---
title: Verkoopprijzen voor schattingen en werkelijke waarden omzetten - lite
description: Dit onderwerp bevat informatie over het omzetten van verkoopprijzen voor schattingen en werkelijke waarden.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176740"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Verkoopprijzen voor schattingen en werkelijke waarden omzetten - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Wanneer verkoopprijzen op schattingen en werkelijke waarden worden omgezet in Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta van de gerelateerde projectprijsopgave of het projectcontract om de verkoopprijslijst om te zetten. Nadat de verkoopprijslijst is omgezet, wordt het verkoop- of factuurtarief omgezet.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Verkooptarieven omzetten voor regels met werkelijke waarden en schattingen voor tijd

In Project Operations worden schattingsregels voor tijd gebruikt om de prijsopgaveregel- en contractregeldetails voor tijd en resourcetoewijzingen aan het project aan te geven.

Nadat een prijslijst voor verkopen is omgezet, voert het systeem de volgende stappen uit om het factuurtarief te standaardiseren.

1. De velden **Rol** en **Resource-eenheid** op de schattingsregel voor tijd worden gebruikt voor afstemming met de rolprijsregels in de omgezette prijslijst. Bij deze afstemming wordt ervan uitgegaan dat u standaardprijsdimensies voor factureringstarieven gebruikt. Als u de prijzen hebt geconfigureerd op basis van andere velden in plaats van of naast **Rol** en **Resource-eenheid**, dan wordt die combinatie gebruikt om een overeenkomende rolprijsregel op te halen.
2. Als een rolprijsregel wordt gevonden met een factureringstarief voor de combinatie van de velden **Rol** en **Resource-eenheid**, is dat het standaardfactuurtarief.
3. Als de waarden voor de velden **Rol** en **Resource-eenheid** niet kunnen worden afgestemd, worden rolprijsregels opgehaald met een overeenkomende rol, maar lege waarden van de **Resource-eenheid**. Nadat het systeem een overeenkomende rolprijsrecord heeft gevonden, wordt het factuurtarief uit die record standaard ingesteld. Deze afstemming veronderstelt een standaardconfiguratie voor de relatieve prioriteit van **Rol** versus **Resource-eenheid** als een verkoopprijsdimensie.

> [!NOTE]
> Als u een andere prioriteitstelling van **Rol** en **Resource-eenheid** hebt geconfigureerd, of als u andere dimensies heeft die een hogere prioriteit hebben, zal dit gedrag dienovereenkomstig veranderen. Rolprijsrecords worden opgehaald met waarden die overeenkomen met elk van de prijsdimensiewaarden in de volgorde van prioriteit, waarbij rijen met null-waarden voor die dimensies als laatste komen.

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
    | &nbsp; | Toeslag op kosten | Pas een toeslag toe zoals gedefinieerd door de categorieprijsregel op het eenheidskostentarief van de gerelateerde werkelijke kosten |

4. Als het systeem de veldwaarden **Categorie** en **Eenheid** niet kan afstemmen, wordt het verkooptarief standaard op nul (0) ingesteld.
