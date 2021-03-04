---
title: Tijdzones beheren
description: Wanneer een project wordt gemaakt, is de tijdzone ervan gebaseerd op de tijdzone die is gedefinieerd in de toegepaste werkurensjabloon.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119817"
---
# <a name="manage-time-zones"></a>Tijdzones beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_


## <a name="projects"></a>Projecten

Wanneer een project wordt gemaakt, is de tijdzone gebaseerd op de tijdzone die is gedefinieerd in de toegepaste werkurensjabloon. In het **Project** zijn de datums altijd relatief ten opzichte van de tijdzone van de gebruiker die is aangemeld op elk tabblad, behalve het tabblad **Taak**. Wanneer u de structuur voor werkspecificatie bekijkt, worden de datums altijd weergegeven in de tijdzone van het project.

## <a name="tasks"></a>Opdrachten

Wanneer een taak wordt gemaakt, worden de starttijd, eindtijd en uren/dag bepaald door de werkuren van het project. Als een taak bijvoorbeeld is gemaakt met een project met tijdzone -8 PST en de volgende werkuren: 9:00 uur tot 17:00 uur van maandag tot vrijdag, zal elke taak die zonder toewijzing wordt gemaakt, de starttijd en eindtijd van de projectkalender respecteren.

## <a name="manage-resources-with-time-zones"></a>Resources beheren met tijdzones

Voor nauwkeurige en voorspelbare resultaten bij gebruik van **Boeking uitbreiden**, zijn er twee belangrijke voorwaarden waaraan moet worden voldaan:  

- De gebruiker moet de tijdzone van zijn apparaat configureren zodat deze overeenkomt met de tijdzone die is gedefinieerd in **Persoonlijke instellingen** van het systeem.
 
  ![Tijdzone-instellingen in Windows 10](media/reconcile-assignments-03.png)

  ![Tijdzone-instellingen in Persoonlijke instellingen](media/reconcile-assignments-04.png)
 
- De boekbare resource moet ten minste één minuut werktijd hebben die overlapt met de contouren waarmee de aangevraagde uitbreiding wordt gedefinieerd. Bijvoorbeeld de volgende resources met werktijden die vallen tussen 9.00 en 19.00 uur. 

  ![Vergelijking van resourcecontouren](media/reconcile-assignments-05.png)

In de onderstaande tabel ziet u het volgende:

- Een sjabloon van een projectagenda
- Resource A: Deze resource heeft dezelfde agenda en bevindt zich in dezelfde tijdzone als het project. De starttijd van de boekingen is 09.00 uur.
- Resource B: deze resource bevindt zich in een andere tijdzone dan het project en begint om 7:00 uur in zijn tijdzone. De boekingen beginnen echter om 09:00 uur, omdat dit de vroegste starttijd van de toewijzingscontour is.
- Resources C en D: de resources bevinden zich in verschillende tijdzones, beide verschillend van elkaar en van het project, en hun boekingen beginnen niet eerder dan hun respectievelijke beschikbare starttijden.

|Entiteit  |Agenda  |
|-|-|
|Sjabloon van projectagenda   | ![projectagenda](media/reconcile-assignments-06.png) |
|Resource A  | ![Agenda van resource A](media/reconcile-assignments-06.png) |
|Resource B  |  ![Agenda van resource B](media/reconcile-assignments-07.png) |
|Resource C  |  ![Agenda van resource C](media/reconcile-assignments-08.png) |
|Resource D  | ![Agenda van resource D](media/reconcile-assignments-09.png)  |
 
In de weergave **Afstemming** worden de resourcetoewijzingen en de bijbehorende boekingstekorten weergegeven.

![Afstemmingsweergave vóór uitbreiding](media/reconcile-assignments-10.png)

Nadat de functie voor het uitbreiden van boekingen is gebruikt voor elke resource, worden boekingen verlengd voor elke resource omdat de werkuren van elke resource de contouren van het tekort overlappen.

![Afstemmingsweergave na uitbreiding van de boeking](media/reconcile-assignments-11.png) 

Merk op dat de details van de boekingen verschillen laten zien in de starttijd van de boekingen. De boekingen starten niet eerder dan de starttijd van de toewijzingscontour en niet eerder dan de beschikbare starttijd van de resource.

![Nieuwe boekingen van de resources in het planbord](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]