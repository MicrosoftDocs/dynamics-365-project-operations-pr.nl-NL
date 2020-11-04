---
title: Verkoopprijslijst instellen
description: Dit onderwerp bevat informatie over verkoopprijslijsten voor projectprijzen.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074619"
---
# <a name="sales-price-list-setup"></a>Verkoopprijslijst instellen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voor projectprijsopgaven en -contracten bevat een projectprijslijst een ander patroon voor prijsoverschrijving dan een productprijslijst. Op een op een productcatalogus gebaseerde prijsopgaveregel kunt u de prijs voor rollen en categorieën rechtstreeks op de prijsopgaveregel overschrijven, omdat elke prijsopgaveregel naar exact één catalogusitem verwijst. Op een projectgebaseerde prijsopgaveregel kunt u de prijs echter niet rechtstreeks op de prijsopgaveregel overschrijven voor rollen en categorieën. U kunt de projectprijslijst gebruiken om met de twee verschillende overschrijvingspatronen te werken.

> [!NOTE]
> Het is raadzaam om een aparte prijslijst voor uw projectresources en uw catalogusitems te hanteren vanwege de verschillen in gedrag tussen de twee wanneer u prijzen overschrijft.

Aan elk van de volgende entiteiten kunnen een of meer verkoopprijslijsten worden gekoppeld voor projectprijzen:

- Klant (account) 
- Verkoopkans 
- Prijsopgave 
- Projectcontract

De koppeling van deze entiteiten aan een prijslijst wordt aangegeven door de projectprijslijsten. U kunt een of meer prijslijsten koppelen aan de verkoopentiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract.

Een standaardprojectprijslijst wordt niet automatisch ingevoerd in een klantrecord. U kunt een projectprijslijst echter handmatig aan de klantrecord koppelen. Koppel een projectprijslijst echter alleen handmatig als u een aangepaste prijsafspraak met de klant hebt. 

Wanneer een projectprijslijst aan een verkoopentiteit wordt gekoppeld, wordt de volgende informatie gevalideerd:

- De prijslijst heeft als context **Verkoop**. 
- De prijslijstvaluta komt overeen met de klantvaluta. 

Voor een projectcontract wordt de volgende prioriteitsvolgorde gebruikt om automatisch gerelateerde projectprijslijsten in te stellen:

1. Prijsopgave
2. Kans
3. Klant 
4. Algemene instellingen 

Wanneer een projectprijslijst standaard wordt ingevoerd, controleert het systeem of de valuta overeenkomt met de valuta van de klant en of de standaardprijslijsten die zijn ingevoerd, de context **Verkoop** hebben.

U kunt meerdere projectprijslijsten koppelen aan de entiteiten Klant, Verkoopkans, Prijsopgave en Projectcontract. Deze mogelijkheid ondersteunt datumspecifieke standaardprijzen voor een langlopend projectcontract, waarbij u mogelijk meer dan één prijslijst nodig hebt voor prijsupdates die worden veroorzaakt door inflatie. Als de prijslijsten die u aan de entiteit Klant, Verkoopkans, Prijsopgave of Projectcontract koppelt echter overlappende geldigheidsdatums hebben, zijn de standaardprijzen mogelijk onjuist. Daarom moet u ervoor zorgen dat projectprijslijsten met overlappende geldigheidsdatums niet zijn gekoppeld aan deze entiteiten.
