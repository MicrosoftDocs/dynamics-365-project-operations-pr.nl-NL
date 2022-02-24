---
title: Overzicht van planningsassistent
description: Dit onderwerp biedt informatie over het werken met de planningsassistent om resources te boeken.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074420"
---
# <a name="schedule-assistant-overview"></a>Overzicht van planningsassistent

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

De planningsassistent wordt gebruikt om resources te boeken op basis van de vereisten die zijn gedefinieerd door de projectmanager. De planningsassistent werkt met de parameters in de resourcevereiste om de resource te vinden. De planningsassistent beveelt resources aan die voldoen aan relevante vereisten, zoals tijdvensters of benodigde vaardigheden.

Nadat geschikte resources zijn geïdentificeerd, kan de resource- of projectmanager de resource voor het werk boeken.

## <a name="prerequisites"></a>Vereisten

De planningsassistent is onderdeel van de Universal Resource Scheduling-oplossing. Deze oplossing wordt samen met Dynamics 365 Project Operations, Dynamics 365 Field Service en Dynamics 365 Customer Service geïnstalleerd.

## <a name="matching-requirements-and-resources"></a>Afstemming van vereisten en resources

Een gegenereerde resourcevereiste wordt gebaseerd op details zoals:

-   Kenmerken
-   Functies
-   Business units
-   Resourcevoorkeuren
-   Inspanningscontouren
-   Tijdzone

De planningsassistent gebruikt deze details om resources te filteren.

## <a name="launch-the-schedule-assistant"></a>De planningsassistent starten

Er zijn twee manieren waarop de planningsassistent wordt gestart. Als u de hybride modus gebruikt, kunt u in het teamlidraster elk teamlid met een niet-vervulde resourcevereiste selecteren en vervolgens **Boeken** selecteren. Als u de centrale modus gebruikt, wordt de resource gezocht en geselecteerd door de resourcemanager.

## <a name="schedule-assistant-filters"></a>Filters voor planningsassistent

Nadat de planningsassistent is uitgevoerd, worden de details van de resourcevereiste weergegeven als gefilterde waarden in het linkerdeelvenster. De resourcemanager of de projectmanager kan de resultaten verfijnen door filters aan te passen aan de planningsbehoeften.

Het filterpaneel toont werkgerelateerde opties, waaronder:

-   Begin- en einddatum voor werk
-   Kenmerken
-   Functies
-   Organisatie-eenheden
-   Bedrijf voor resources
-   Resourcetypen
-   Geprefereerde resources
