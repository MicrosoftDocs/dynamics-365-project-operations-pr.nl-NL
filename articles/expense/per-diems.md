---
title: Dagvergoedingen
description: In dit artikel vindt u informatie over per diem-regels die worden gebruikt in Onkostenbeheer.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 8fa634c23391c47c0c583647165dce2b396535e5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930174"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]