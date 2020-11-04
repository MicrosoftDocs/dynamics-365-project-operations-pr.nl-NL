---
title: Overzicht van productgebaseerde contractregels
description: Dit onderwerp bevat informatie over op producten gebaseerde contractregels.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074491"
---
# <a name="product-based-contract-lines-overview"></a>Overzicht van productgebaseerde contractregels

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

U kunt op product gebaseerde contractregels maken in Dynamics 365 Project Operations. Productgebaseerde contractregels kunnen handmatig gemaakte regels zijn of items uit de productcatalogus.

## <a name="product-catalog"></a>Productcatalogus

De producten in de productcatalogus hebben een standaardeenheid en -eenhedengroep. Als verschillende producten dezelfde set kenmerken hebben, kunt u een productfamilie maken die ook deze kenmerken heeft. Alle producten in één productfamilie nemen dezelfde set kenmerken over.

Een bedrijf verkoopt bijvoorbeeld abonnementslicenties voor verschillende soorten software. Alle abonnementssoftware heeft de volgende twee kenmerken:

- Aantal gebruikers
- Abonnementsduur (in maanden)

Als u dit type catalogus wilt onderhouden, maakt u een productreeks met een naam **Abonnementssoftware**. Voeg de kenmerken **Aantal gebruikers** en **Abonnementsduur** toe aan de productreeks. Voeg vervolgens afzonderlijke producten toe aan de productreeks **Abonnementssoftware**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Productcatalogusitems toevoegen aan een projectcontract

Projectcontracten hebben secties voor twee typen regels: op basis van project en op basis van product. Productgebaseerde regels bevatten alle producten en eenheden in de productprijslijst op het contract. Producten die geen deel uitmaken van de productprijslijst van het contract kunnen worden toegevoegd.

U kunt producten uit andere prijslijsten of rechtstreeks uit de productcatalogus selecteren. Wanneer u producten rechtstreeks uit een productcatalogus selecteert, wordt de standaardprijslijst van dat product gebruikt voor de verkoopprijs van het product. Als er geen standaardprijslijst is ingesteld, wordt de prijs ingesteld op 0 (nul).

Als een contractregel is gebaseerd op een productcatalogus, kunt u de verkoopprijs direct op de regel overschrijven. Een contractregel bevat het veld **Prijzen** met de twee waarden:

- **Prijs negeren**
- **Standaardwaarde gebruiken**

Als u het veld **Prijzen** instelt op **Prijs negeren** , wordt er geen standaardprijs ingesteld. Voer een prijs in voor het product in op de contractregel. Als u het veld instelt op **Standaardwaarde gebruiken** , wordt de standaardverkoopprijs gebruikt en kan het veld niet worden bewerkt.

Nadat u Project Operations hebt geïnstalleerd, worden standaardverkoopprijzen ingevoerd op de productgebaseerde regels van een contract. Het veld **Prijzen** wordt vervolgens ingesteld op **Prijzen negeren** , zodat u de standaardprijs op de contractregels kunt bewerken. Dit is een Project Operations-specifieke overschrijving van productgebaseerd regelgedrag in Dynamics 365 Sales.
