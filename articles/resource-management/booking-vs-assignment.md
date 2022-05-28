---
title: Boekingen versus toewijzingen
description: Dit onderwerp biedt informatie over de verschillen tussen resourceboekingen en resourcetoewijzingen.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b06555ec48e50f88c11872336539ca88c5cef34a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591260"
---
# <a name="bookings-vs-assignments"></a>Boekingen versus toewijzingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Boekingen zijn de harde of zachte toewijzing van resources aan een project. Een harde boeking verbruikt de capaciteit van een resource. Boekingen vertegenwoordigen organisatieconcepten voor teams, zodat ze kunnen begrijpen hoe resources bij verschillende projecten worden ingezet. Dynamics 365 Project Operations beschouwt boekingen als een concept op projectniveau. 

In tegenstelling tot boekingen zijn toewijzingen de toezegging van resources voor projecttaken in de projectplanning. De resources kunnen een naam hebben of generiek zijn.  Wanneer een resourcevereiste wordt afgeleid uit de projecttaaktoewijzingen, gebruikt Project Operations de inspanningscontouren van de resourcetoewijzing om de contouren van de details van resourcevereisten op te bouwen. Een verwijzing naar de resourcetoewijzingen wordt echter niet gehandhaafd. Updates van de boekingen die zijn afgeleid van de resourcevereiste werken geen resourcetoewijzingen bij.

Meestal is de som van de boekingen voor een resource gelijk aan de som van de toewijzingen van de resource voor een of meerdere taken. In Project Operations is deze overeenkomst echter niet verplicht. In de weergave **Afstemming** wordt aan een projectmanager getoond waar boekingen en toewijzingen van een resource niet overeenkomen.




[!INCLUDE[footer-include](../includes/footer-banner.md)]