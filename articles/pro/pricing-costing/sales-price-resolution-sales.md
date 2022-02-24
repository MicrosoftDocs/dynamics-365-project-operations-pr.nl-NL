---
title: Verkoopprijzen voor projectschattingen en werkelijke waarden omzetten
description: Dit onderwerp geeft informatie over hoe verkoopprijzen in projectschattingen en werkelijke waarden worden omgezet.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3bf4686b414300370e6b364834b33edad98b7f39
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877350"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Verkoopprijzen voor projectschattingen en werkelijke waarden omzetten

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Wanneer verkoopprijzen voor schattingen en werkelijke waarden worden opgelost in Dynamics 365 Project Operations, gebruikt het systeem eerst de datum en valuta van de gerelateerde projectprijsopgave of contract om de verkoopprijslijst op te lossen. Nadat de verkoopprijslijst is omgezet, wordt het verkoop- of factuurtarief omgezet.

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

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Verkooptarieven voor werkelijke en schattingsregels voor materiaal omzetten

In Project Operations worden schattingsregels voor materiaal gebruikt ter aanduiding van de prijsopgave- en contractregeldetails voor materialen en de materiaalschattingsregels voor het project.

Nadat een prijslijst voor verkopen is omgezet, voert het systeem de volgende stappen uit om de verkoopprijs per eenheid te standaardiseren.

1. Het systeem gebruikt de combinatie van de velden **Product** en **Eenheid** op de schattingsregel voor materiaal dat moet worden vergeleken met de prijslijstartikelregels in de prijslijst die is omgezet.
2. Als een prijslijstartikelregel met een verkooptarief voor de combinatie van **Product** en **Eenheid** wordt gevonden en de prijsmethode is **Valutabedrag**, dan wordt de verkoopprijs gebruikt die is opgegeven op de prijslijstregel.
3. Als de waarden voor **Product** en **Eenheid** niet overeenkomen, wordt het verkooptarief standaard ingesteld op nul.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
