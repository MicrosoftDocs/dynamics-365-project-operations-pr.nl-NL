---
title: Voldoen aan algemene resourcevereisten
description: Dit onderwerp bevat informatie over het boeken van benoemde resources voor een algemene resourcevereiste.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074509"
---
# <a name="generic-resource-requirement-fulfillment"></a>Voldoen aan algemene resourcevereisten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U een kunt benoemde resource boeken om een algemene resource met een resourcevereiste te vervangen.

1. Selecteer op de pagina **Projecten** het tabblad **Team**.
2. Selecteer in de lijst de algemene resource met een resourcevereiste en selecteer vervolgens **Boeken**. Of open de resourcevereiste en selecteer vervolgens **Boeken**.
3. Selecteer op de pagina **Planningsassistent** een benoemde resource die u wilt boeken voor uw projectteam, en selecteer vervolgens **Boeken**.

Wanneer de boeking is voltooid door een benoemde resource, wordt de algemene resource vervangen door de benoemde resource.

De toewijzingen in de planning worden ook bijgewerkt met de benoemde resource.

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Een algemene resource vervullen met meerdere benoemde resources
Het voldoen aan een vereiste voor een algemene resource met meerdere benoemde resources is vergelijkbaar met het toewijzen van een één benoemde resource. Er is bijvoorbeeld een taak met een duur van vijf dagen en 120 uur werk. Deze taak kan niet worden voltooid door één resource met een normale 40-urige werkweek. 

De vereiste heeft betrekking op 120 uur aan robotica-engineering gedurende vijf dagen, wat neerkomt op 24 uur per dag.

Dit is een voorbeeld van wanneer er meerdere benoemde resources nodig zijn om te voldoen aan een algemene resourceaanvraag. U moet meerdere resources boeken om aan de vereiste te voldoen.

Het belangrijkste verschil in dit scenario is dat de algemene resource in het team blijft dat is toegewezen aan de taak terwijl de geboekte benoemde resourceteamleden niet worden toegewezen als onderdeel van de positie. De projectmanager kan het werk naar behoefte toewijzen aan de benoemde resources. De weergave **Afstemming** biedt een projectmanager overzicht van de boekingen voor meerdere resources naar taaktoewijzingen. Dit gebeurt niet automatisch omdat in elk scenario's dat complexer is dan het eenvoudige bovenstaande scenario, bijvoorbeeld als de vereiste bestaat uit een reeks taken, door het systeem moet worden verondersteld wat de intentie van de projectmanager is als het gaat om het toewijzen van resources. Omdat het systeem de intentie niet begrijpt, is de kans groot dat de veronderstellingen van het systeem verschillen van de intentie van de projectmanager wat leidt tot een onjuist of onvoorspelbaar resultaat. Het voorspelbare resultaat is dat de algemene resource toegewezen blijft totdat de projectmanager opzettelijk toewijzingen maakt, st met behulp van de weergave **Afstemming**.


