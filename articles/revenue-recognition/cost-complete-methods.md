---
title: Kosten om methoden te voltooien
description: Dit onderwerp bevat informatie over de methoden die worden gebruikt om de kosten voor het voltooien van een project te berekenen.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531400"
---
# <a name="cost-to-complete-methods"></a>Kosten om methoden te voltooien

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp bevat informatie over de methoden die worden gebruikt om de kosten voor het voltooien van een project te berekenen. Er zijn meerdere methoden die u kunt gebruiken om de kosten voor het voltooien van een project te berekenen. 

Wanneer u een schatting maakt voor een project, op de pagina **Schatting maken**, in het veld **Kosten om methoden te voltooien**, kunt u een van de volgende methoden voor het voltooien van kosten selecteren.

| Kosten om methode te voltooien    | Beschrijving                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Totale kosten - werkelijk            | Voer de geschatte kosten handmatig in de velden **Totale kosten** of **Totale hoeveelheid** in met behulp van de knop **Kostenschatting** op de pagina **Schatting**. Het systeem trekt de werkelijke kosten af van de totalen die u hebt ingevoerd. Het totaal is de kostprijs om het project te voltooien. Deze methode maakt geen gebruik van de kostenramingen en resourcetoewijzingen die zijn ingevoerd in Project Operations in Microsoft Dataverse. De totale kosten of totale hoeveelheid kunnen indien nodig handmatig worden bijgewerkt.  |
| Totale prognose - werkelijk        | Resourcetoewijzingen en kostenramingen worden gebruikt om het totale projectprognosebedrag te bepalen. De werkelijke kosten worden vergeleken met deze prognose om de kosten voor voltooien te berekenen.                                                                                                                                                                                                                                                                          |
| Zoals eerdere schatting         | Hier worden dezelfde schattingsmethoden gebruikt als in de vorige periode. Deze methode vereist een prognosemodel als de vorige periode een prognosemodel vereiste.                                                                                                                                                                                                                                                                                                                           |
| Kosten tot voltooiing instellen op nul | Deze methode wordt doorgaans gebruikt voordat het schattingsproject wordt geëlimineerd. De totale schattingen worden vergeleken met geboekte werkelijke transacties en de kolom **Kosten om te voltooien** wordt gewist. Na voltooiing is het resultaat altijd 100 procent. Voor elke kostenregel die u maakt, wordt het selectievakje **Prognoses** is uitgeschakeld en wordt de totale schatting gekopieerd uit de vorige kostenraming. Het werkelijke verbruik voor de geschatte periode wordt afgetrokken van de kosten om het project te voltooien.              |
| Vanuit kostensjabloon           | De methode voor kosten tot voltooiing die is ingesteld in de kostensjabloon die is gekoppeld aan het geselecteerde schattingsproject.                                                                                                                                                                                                                                                                                                                                                                          |