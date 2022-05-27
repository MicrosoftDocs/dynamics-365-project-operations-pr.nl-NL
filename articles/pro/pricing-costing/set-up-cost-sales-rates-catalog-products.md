---
title: Kosten- en verkooptarieven voor catalogusproducten instellen - lite
description: Dit onderwerp bevat informatie over het instellen van kosten en verkooptarieven voor artikelen in een productcatalogus.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 12e09d99e9832c93c3aea34ec0d4488cdf6b02fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576816"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Kosten- en verkooptarieven voor catalogusproducten instellen - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Prijzen instellen voor productcatalogusartikelen in Dynamics 365 Project Operations is hetzelfde als in Dynamics 365 Sales.

In Project Operations kunnen producten niet worden geschat of gebruikt voor projecten, dus productcatalogusprijzen hoeven niet te worden ingesteld op projectprijslijsten voor prijsopgaven en contracten.

Gebruik het veld **Productprijs** van een prijsopgave, contract of account om productcatalogusprijzen in te stellen. Stel geen productcatalogusprijzen in de projectprijslijsten in. Projectprijslijsten zijn exclusief voor Project Operations. Toepassingsspecifieke bedrijfslogica kopieert de prijslijsten van een prijsopgave naar een contract. Het resultaat is een contractspecifieke prijslijst. De kopieerbewerking kan het proces voor het winnen van de prijsopgave vertragen als de projectprijslijst op de prijsopgave te groot wordt. Productprijslijsten worden niet gekopieerd om aangepaste prijslijsten voor contracten te maken. Omdat er geen sprake is van kopiëren, wordt de prestatie van het prijsopgaveproces niet beïnvloed.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]