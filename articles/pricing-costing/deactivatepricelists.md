---
title: Prijslijsten deactiveren
description: In dit artikel wordt uitgelegd hoe u ongebruikte of oude prijslijsten deactiveert of verwijdert.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924378"
---
# <a name="deactivate-price-lists"></a>Prijslijsten deactiveren 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Als u oude of ongebruikte prijslijsten wilt verwijderen uit Dynamics 365 Project Operations, zijn er twee stappen die u moet doorlopen. 

1. Verwijder of wis de prijslijst van specifieke pagina's.
2. Deactiveer of verwijder de prijslijst uit de actieve prijslijsten op de pagina **Prijslijsten**.

>[!IMPORTANT]
> U moet beide stappen voltooien om een prijslijst volledig te verwijderen. Het volstaat niet om alleen stap 2, het direct verwijderen of deactiveren van de prijslijst uit de weergave Actieve prijslijsten, uit te voeren. U moet ook de koppeling van deze prijslijst verwijderen uit alle plaatsen genoemd in stap 1.

## <a name="delete-the-price-list-from-specific-pages"></a>De prijslijst van specifieke pagina's verwijderen
1. Als u een prijslijst uit Project Operations wilt verwijderen, gaat u naar de volgende pagina's:  

      - De pagina **Projectparameters** > het tabblad **Prijslijsten**
      - De pagina **Organisatie-eenheid** > het raster **Prijslijsten**
      - De pagina **Account** > het raster **Prijslijsten voor project**
      - De pagina **Projectprijsopgaven** > het raster **Prijslijsten voor project**: dit is van toepassing op alle actieve projectprijsopgaven.
      - De pagina **Projectcontracten** > het raster **Prijslijsten voor project**: dit is van toepassing op alle actieve contracten.

 2. Voor elke pagina moet u de prijslijst selecteren die u wilt verwijderen en vervolgens **Verwijderen** selecteren. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>De prijslijst uit de actieve prijslijsten op de pagina Prijslijsten verwijderen of deactiveren
 
1. Als u een prijslijst uit de actieve prijslijsten wilt verwijderen, gaat u naar **Verkoop** > **Klanten** > **Prijslijsten**. 
2. Selecteer de prijslijst die u wilt verwijderen en selecteer vervolgens **Verwijderen**. Als naar de prijslijst wordt verwezen in bestaande transacties, kunt u deze niet verwijderen. Als dit gebeurt, kunt u de prijslijst deactiveren, zodat deze in geen enkele weergave wordt weergegeven. 
3. Om de prijslijst te deactiveren, selecteert u de prijslijst opnieuw en selecteert u vervolgens **Deactiveren**.   
