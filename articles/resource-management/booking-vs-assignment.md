---
title: Boekingen versus toewijzingen
description: Dit onderwerp biedt informatie over de verschillen tussen resourceboekingen en resourcetoewijzingen.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841166"
---
# <a name="bookings-vs-assignments"></a>Boekingen versus toewijzingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Boekingen zijn de harde of zachte toewijzing van resources aan een project. Een harde boeking verbruikt de capaciteit van een resource. Boekingen vertegenwoordigen organisatieconcepten voor teams, zodat ze kunnen begrijpen hoe resources bij verschillende projecten worden ingezet. Dynamics 365 Project Operations beschouwt boekingen als een concept op projectniveau. 

In tegenstelling tot boekingen zijn toewijzingen de toezegging van resources voor projecttaken in de projectplanning. De resources kunnen een naam hebben of generiek zijn.  Wanneer een resourcevereiste wordt afgeleid uit de projecttaaktoewijzingen, gebruikt Project Operations de inspanningscontouren van de resourcetoewijzing om de contouren van de details van resourcevereisten op te bouwen. Een verwijzing naar de resourcetoewijzingen wordt echter niet gehandhaafd. Updates van de boekingen die zijn afgeleid van de resourcevereiste werken geen resourcetoewijzingen bij.

Meestal is de som van de boekingen voor een resource gelijk aan de som van de toewijzingen van de resource voor een of meerdere taken. In Project Operations is deze overeenkomst echter niet verplicht. In de weergave **Afstemming** wordt aan een projectmanager getoond waar boekingen en toewijzingen van een resource niet overeenkomen.


