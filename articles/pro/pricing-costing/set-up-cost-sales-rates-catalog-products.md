---
title: Kosten- en verkooptarieven voor catalogusproducten instellen
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074631"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Kosten- en verkooptarieven voor catalogusproducten instellen

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Het instellen van prijzen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.

Omdat producten niet kunnen worden geschat of gebruikt voor projecten in Project Operations, is het niet nodig om productcatalogusprijzen in te stellen op projectprijslijsten voor offertes en contracten.

Productcatalogusprijzen moeten worden ingesteld in het veld **Productprijs** van een prijsopgave, contract of account. Stel geen productcatalogusprijzen in de projectprijslijsten voor deze entiteiten in. Projectprijslijsten zijn exclusief voor Project Operations. Er is applicatiespecifieke bedrijfslogica die de prijslijsten van een prijsopgave naar een contract kopieert. Het resultaat is een contractspecifieke prijslijst. De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt. Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken. Dit betekent dat productprijslijsten geen invloed hebben op de prestaties van het proces voor het winnen van een prijsopgave.
