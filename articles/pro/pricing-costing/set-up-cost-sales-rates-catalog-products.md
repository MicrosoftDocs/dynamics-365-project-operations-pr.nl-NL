---
title: Kosten- en verkooptarieven voor catalogusproducten instellen - lite
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176695"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kosten- en verkooptarieven voor catalogusproducten instellen - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Het instellen van prijzen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.

Omdat producten niet kunnen worden geschat of gebruikt voor projecten in Project Operations, is het niet nodig om productcatalogusprijzen in te stellen op projectprijslijsten voor offertes en contracten.

Productcatalogusprijzen moeten worden ingesteld in het veld **Productprijs** van een prijsopgave, contract of account. Stel geen productcatalogusprijzen in de projectprijslijsten voor deze entiteiten in. Projectprijslijsten zijn exclusief voor Project Operations. Er is applicatiespecifieke bedrijfslogica die de prijslijsten van een prijsopgave naar een contract kopieert. Het resultaat is een contractspecifieke prijslijst. De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt. Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken. Dit betekent dat productprijslijsten geen invloed hebben op de prestaties van het proces voor het winnen van een prijsopgave.
