---
title: Dagvergoedingen
description: Dit onderwerp geeft informatie over de dagvergoedingsregels die worden gebruikt in Onkostenbeheer.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908036"
---
# <a name="per-diems"></a>Dagvergoedingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Een dagvergoeding is een toelage die wordt betaald aan een werknemer die voor zijn werk reist. In Onkostenbeheer kunt u dagvergoedingsregels maken voor verschillende reissituaties. Dagtarieven kunnen worden gebaseerd op de tijd van het jaar, de reislocatie of beide. Wanneer u een dagvergoeding maakt, kunt u specificeren dat een percentage van de dagvergoeding wordt ingehouden als een werknemer gratis maaltijden of diensten ontvangt. U kunt ook een minimum en maximum aantal uren instellen dat het dagtarief van toepassing kan zijn op de reis van een werknemer.

## <a name="configuration"></a>Configuratie 

1. Als u locaties voor dagvergoedingen wilt toevoegen gaat u naar **Instellen** > **Berekeningen en codes** > **Locaties voor dagvergoedingen**.
2. Selecteer voor elk van de hierboven toegevoegde locaties een dagtarief en valuta die geldig zijn tussen een specifieke begin- en einddatum voor hotel, maaltijden en andere onkosten. Dagvergoedingen en valuta's worden geconfigureerd onder **Instellen** > **Berekeningen en codes** > **Dagvergoedingen**.
3. Configureer op de pagina **Locaties voor dagvergoedingen** de tariefniveaus. Definieer met tariefniveaus de procentuele verdeling van een dagvergoeding voor hotel-, maaltijd- en andere uitgaven. 
4. Om de vergoeding voor ontbijt, lunch of diner op te geven, werkt u de velden op de pagina **Parameters voor onkostenbeheer** bij op het tabblad **Dagvergoeding**. 
    
## <a name="submit-expenses-using-per-diem"></a>Onkosten voor dagvergoedingen indienen
Als u onkosten wilt indienen met dagvergoedingen, gebruikt u de onkostencategorie **Dagvergoeding** wanneer u een onkostendeclaratie maakt. Voer **Dagvergoeding vanaf datum**, **Dagvergoeding tot datum** en **Locatie voor dagvergoeding** in. Het bedrag wordt berekend op basis van de dagtarieven voor de geselecteerde locatie en de maaltijdvergoeding wordt berekend op basis van de tariefniveaus voor dagvergoeding.
