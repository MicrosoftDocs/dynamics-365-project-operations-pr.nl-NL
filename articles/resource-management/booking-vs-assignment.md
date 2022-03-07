---
title: Boekingen versus toewijzingen
description: Dit onderwerp biedt informatie over de verschillen tussen resourceboekingen en resourcetoewijzingen.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1906ebd76f5fc66215aa5963242de13206a81668cb4973cccaf5b153514672d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008445"
---
# <a name="bookings-vs-assignments"></a>Boekingen versus toewijzingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Boekingen zijn de harde of zachte toewijzing van resources aan een project. Een harde boeking verbruikt de capaciteit van een resource. Boekingen vertegenwoordigen organisatieconcepten voor teams, zodat ze kunnen begrijpen hoe resources bij verschillende projecten worden ingezet. Dynamics 365 Project Operations beschouwt boekingen als een concept op projectniveau. 

In tegenstelling tot boekingen zijn toewijzingen de toezegging van resources voor projecttaken in de projectplanning. De resources kunnen een naam hebben of generiek zijn.  Wanneer een resourcevereiste wordt afgeleid uit de projecttaaktoewijzingen, gebruikt Project Operations de inspanningscontouren van de resourcetoewijzing om de contouren van de details van resourcevereisten op te bouwen. Een verwijzing naar de resourcetoewijzingen wordt echter niet gehandhaafd. Updates van de boekingen die zijn afgeleid van de resourcevereiste werken geen resourcetoewijzingen bij.

Meestal is de som van de boekingen voor een resource gelijk aan de som van de toewijzingen van de resource voor een of meerdere taken. In Project Operations is deze overeenkomst echter niet verplicht. In de weergave **Afstemming** wordt aan een projectmanager getoond waar boekingen en toewijzingen van een resource niet overeenkomen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]