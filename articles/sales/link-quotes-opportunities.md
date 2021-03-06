---
title: Prijsopgaven voor projecten maken op basis van verkoopkansen
description: In dit onderwerp krijgt u informatie over het maken van een projectprijsopgave op basis van een verkoopkans.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898526"
---
# <a name="create-project-quotes-from-opportunities"></a>Prijsopgaven voor projecten maken op basis van verkoopkansen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Prijsopgaven kunnen op de volgende manieren worden gemaakt van projectkansen:

- Via het tabblad **Prijsopgaven** op de pagina **Projectverkoopkans**
- Via de stroom Verkoopproces verkoopkans
- Door de verkoopkansreferentie op een bestaande offerte bij te werken

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a>Via het tabblad Prijsopgaven van de pagina Projectverkoopkans

Voer de volgende stappen uit om een projectprijsopgave te maken op basis van een verkoopkans.

1. Open de pagina **Projectverkoopkans** en selecteer het tabblad **Prijsopgaven**. 
2. Selecteer in het subraster **Prijsopgaven** de **+** om een nieuwe projectprijsopgave te maken op basis van de verkoopkans. Alle verkoopkansregels en gerelateerde projectprijslijsten worden vanuit de verkoopkans naar de nieuwe prijsopgave gekopieerd.

## <a name="from-the-opportunity-sales-process-flow"></a>Via de stroom Verkoopproces verkoopkans

Voer de volgende stappen uit om een prijsopgave te maken op basis van een verkoopprocesstroom voor een verkoopkans.

1. Open de Verkoopkans vanuit de verkoopprocesstroom Verkoopkans.
2. Selecteer de fase **Kwalificeren**. 
3. Selecteer **Volgende** en vervolgens **+ Maken** om een nieuwe prijsopgave aan te maken. De meeste informatie op het tabblad **Samenvatting** voor deze nieuwe prijsopgave komt standaard uit de verkoopkans. 
4. Voer alle vereiste ontbrekende informatie in of werk indien nodig standaardwaarden bij op het tabblad **Samenvatting**.
5. Selecteer **Opslaan**. De nieuwe prijsopgave wordt gemaakt en aan de verkoopkans gekoppeld. U kunt nu de prijsopgave-informatie bekijken op het tabblad **Prijsopgaven** van de pagina **verkoopkans**. 

   Het verkoopproces Verkoopkans gaat naar de volgende fase, **Voorstellen**.


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a>Door de verkoopkansreferentie op een bestaande offerte bij te werken

Een bestaande prijsopgave kan worden gekoppeld aan een verkoopkans. Voer de volgende stappen uit om de verkoopkansinformatie op een bestaande prijsopgave bij te werken.

1. Open de pagina **Prijsopgave** en selecteer het tabblad **Samenvatting**.
2. Selecteer in het veld **Verkoopkans** de verkoopkans die u aan de prijsopgave wilt koppelen. U kunt de prijsopgave zien in het raster **prijsopgaven** van de verkoopkans. 
3. Met behulp van het verkoopproces kan de verkoopkans worden verplaatst naar de volgende fase, **Voorstellen**. 

   Wanneer u een verkoopkans naar deze fase verplaatst, kunt u deze prijsopgave selecteren uit een lijst met prijsopgaven die aan deze verkoopkans zijn gekoppeld. Als u deze prijsopgave selecteert, geeft u aan dat u ermee verder gaat.

   Alle andere prijsopgaven die aan de verkoopkans zijn gekoppeld, blijven beschikbaar en actief totdat een van deze wordt geaccepteerd. U kunt het verkoopproces terug verplaatsen naar de vorige fase **Kwalificeren** en een andere prijsopgave kiezen om mee verder te gaan.
