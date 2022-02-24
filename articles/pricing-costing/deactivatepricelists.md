---
title: Prijslijsten deactiveren
description: In dit onderwerp wordt uitgelegd hoe u ongebruikte of oude prijslijsten kunt deactiveren of verwijderen.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701922"
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
