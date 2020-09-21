---
title: Overwegingen voor de upgrade van Microsoft Dynamics 365 Project Service Automation, versie 2.x of 1.x, naar versie 3
description: Dit onderwerp bevat informatie over de overwegingen voor het upgraden van Project Service Automation versie 2.x of 1.x naar versie 3.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x
author: JohnPBurrows
ms.assetid: e4fae2ea-9013-488e-a666-f7192dd42c0b
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: ba710eb8c07df7dac97e8b911184c00b87b14548
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750789"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Overwegingen voor de upgrade van PSA-versie 2.x of 1.x naar versie 3
[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation en Field Service
Zowel Dynamics 365 Project Service Automation als Dynamics 365 Field Service maken gebruik van de oplossing Universal Resourcing Scheduling (URS) voor resourceplanning. Als u in uw exemplaar zowel Project Service Automation als Field Service hebt, moet u beide oplossingen upgraden naar de nieuwste versie (versie 3.x voor Project Service Automation, versie 8.x voor Field Service). Bij het upgraden van Project Service Automation of Field Service wordt de nieuwste versie van URS geïnstalleerd, wat betekent dat inconsistent gedrag mogelijk is als niet zowel de Project Service Automation-oplossingen als de Field Service-oplossingen in hetzelfde exemplaar worden bijgewerkt naar de nieuwste versie.

## <a name="resource-assignments"></a>Resourcetoewijzingen
In Project Service Automation versie 2 en versie 1 zijn taaktoewijzingen opgeslagen als onderliggende taken (ook wel regeltaken genoemd) in de **entiteit Taak** en indirect gerelateerd aan de entiteit **Resourcetoewijzing**. De regeltaak is zichtbaar in het toewijzingspop-upvenster in de Structuur voor werkspecificatie (WBS).

![Regeltaken op de WBS in Project Service Automation versie 2 en versie 1](media/upgrade-line-task-01.png)

In versie 3 van Project Service Automation is het onderliggende schema voor het toewijzen van boekbare resources aan taken gewijzigd. De regeltaak is afgeschaft en er is een directe 1:1-relatie tussen de taak in de **Taakentiteit** en het teamlid in de entiteit **Resourcetoewijzing**. Taken die worden toegewezen aan een lid van het projectteam, worden nu rechtstreeks opgeslagen in de entiteit Resourcetoewijzing.  

Deze wijzigingen zijn van invloed op de upgrade van bestaande projecten met resourcetoewijzingen voor benoemde boekbare resources en algemene resources in een projectteam. Dit onderwerp bevat de overwegingen waarmee u rekening moet houden voor uw projecten wanneer u een upgrade uitvoert naar versie 3. 

### <a name="tasks-assigned-to-named-resources"></a>Taken toegewezen aan benoemde resources
Met de onderliggende taakentiteit konden teamleden in versie 2 en versie 1 voor taken een andere rol weergeven dan hun standaard gedefinieerde rol. Femke Van der Star aan wie standaard de rol van programmamanager is toegewezen, kan bijvoorbeeld worden toegewezen aan een taak met de rol van ontwikkelaar. In versie 3 is de rol van een benoemd teamlid altijd de standaardrol, dus elke taak die Femke Van der Star krijgt toegewezen, gebruikt haar standaardrol van programmamanager.

Als u een resource hebt toegewezen aan een taak buiten de standaardrol in versie 2 en versie 1, wordt bij het upgraden de benoemde resource toegewezen aan de standaardrol voor alle taaktoewijzingen, ongeacht de roltoewijzing in versie 2. Dit resulteert in verschillen in de berekende schattingen van versie 2 of versie 1 naar versie 3 omdat schattingen worden berekend op basis van de rol van de resource en niet de regeltaaktoewijzing. In versie 2 zijn bijvoorbeeld twee taken toegewezen aan Dana Plant. De rol op de regeltaak voor taak 1 is ontwikkelaar en voor taak 2 programmamanager. Dana Plant heeft de standaardfunctie van programmamanager.

![Meerdere rollen toegewezen aan één resource](media/upgrade-multiple-roles-02.png)

Omdat de rollen van ontwikkelaar en programmamanager verschillen, zijn de kosten- en verkoopschattingen als volgt:

![Kostenschattingen voor resourcerollen](media/upggrade-cost-estimates-03.png)

![Verkoopschattingen voor resourcerollen](media/upgrade-sales-estimates-04.png)

Wanneer u een upgrade uitvoert naar versie 3, worden regeltaken vervangen door resourcetoewijzingen voor de taak van het teamlid voor de boekbare resource. De toewijzing maakt gebruik van de standaardrol van de boekbare resource. In de volgende afbeelding is Dana Plant de resource die de rol van programmamanager heeft.

![Resourcetoewijzingen](media/resource-assignment-v2-05.png)

Omdat de schattingen zijn gebaseerd op de standaardrol voor de resource, kunnen de verkoop- en kostenschattingen veranderen. In de volgende afbeelding ziet u de rol van **ontwikkelaar** niet meer omdat de rol nu is overgenomen van de standaardrol van de boekbare resource.

![Kostenschattingen voor standaardrollen](media/resource-assignment-cost-estimate-06.png)
![Verkoopschatting voor standaardrollen](media/resource-assignment-sales-estimate-07.png)

Nadat de upgrade is voltooid, kunt u de rol van een teamlid bewerken in iets anders dan de toegewezen standaardwaarde. Als u echter een rol van teamleden wijzigt, wordt deze gewijzigd voor alle toegewezen taken, omdat aan teamleden niet langer meerdere rollen mogen worden toegewezen in versie 3.

![Een resourcerol bijwerken](media/resource-role-assignment-08.png)

Dit geldt ook voor regeltaken die aan benoemde resources zijn toegewezen wanneer u de organisatie-eenheid van de resource wijzigt van de standaardwaarde in een andere organisatie-eenheid. Nadat de upgrade van versie 3 is voltooid, gebruikt de toewijzing de standaardorganisatie-eenheid van de resource in plaats van de waarde die is ingesteld voor de regeltaak.

### <a name="tasks-assigned-to-generic-resources"></a>Taken toegewezen aan algemene resources
In versie 2 en versie 1 kunt u de rol en organisatie-eenheid voor een taak instellen en vervolgens de functie **Team genereren** gebruiken om algemene resources te genereren op basis van de kenmerken die voor de taak zijn ingesteld. In versie 3 maakt u de algemene teamleden met een rol en organisatie-eenheid en wijst u de teamleden vervolgens toe aan taken.

In versie 2 en versie 1 kunnen projecten met algemene resources twee statussen hebben of een combinatie van beide op taakniveau. U kunt bijvoorbeeld de volgende scenario's hebben:

- Taken waarvoor rollen en organisatie-eenheden zijn ingesteld, maar waarvoor geen gelieerde resourcetoewijzing is gegenereerd.
- Taken met resourcetoewijzingen voor algemene teamleden die zijn toegewezen door het maken van algemene resources met behulp van de functie **Team genereren**.

Voordat u begint met de upgrade, is het raadzaam dat u het team opnieuw genereert voor elk project waarvoor taken zijn toegewezen aan algemene resources of waarvoor het proces Team genereren nog moet worden uitgevoerd.

Voor taken die zijn toegewezen aan algemene teamleden die zijn gegenereerd met **Team genereren**, blijft ook na de upgrade de algemene resource bij het team en de toewijzing voor dat algemene teamlid. Het is raadzaam dat u de resourcevereiste voor het algemene teamlid genereert na de upgrade, maar voordat u een resourceaanvraag boekt of indient. Hiermee worden alle toewijzingen van organisatie-eenheden aan de algemene teamleden behouden die afwijken van de contracterende organisatie-eenheid van het project.

In het project Z is bijvoorbeeld de eenheid van de contracterende organisatie Contoso US. In het projectplan is aan testtaken binnen de implementatiefase de rol van technisch adviseur toegewezen en is de toegewezen organisatie-eenheid is Contoso India.

![Toewijzing van organisatie in implementatiefase](media/org-unit-assignment-09.png)

Na de implementatiefase wordt de integratietesttaak toegewezen aan de rol Technisch consultant, maar wordt de organisatie ingesteld op Contoso US.  

![Toewijzing van organisatie voor integratietesttaak](media/org-unit-generate-team-10.png)

Wanneer u een team voor het project genereert, worden twee algemene teamleden gemaakt vanwege de verschillende organisatie-eenheden in de taken. Aan technisch consultant 1 worden de taken van Contoso India toegewezen en technisch consultant 2 krijgt de taken van Contoso US.  

![Gegenereerde algemene teamleden](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> In Project Service Automation versie 2 en versie 1 bevat het teamlid niet de organisatie-eenheid. Deze wordt bijgehouden op de regeltaak.

![Regeltaken van versie 2 en versie 1 in Project Service Automation](media/line-tasks-12.png)

U kunt de organisatie-eenheid bekijken in de schattingenweergave. 

![Schattingen van organisatie-eenheid](media/org-unit-estimates-view-13.png)
 
Wanneer de upgrade is voltooid, wordt de organisatie-eenheid op de regeltaak die overeenkomt met het algemene teamlid toegevoegd aan het algemene teamlid en wordt de regeltaak verwijderd. Daarom is het raadzaam dat u voordat u een upgrade uitvoert, het team genereert of opnieuw genereert voor elk project dat algemene resources bevat.

Voor taken die zijn toegewezen aan een rol met een organisatie-eenheid die verschilt van de organisatie-eenheid van het contracterende project en waarvoor geen team is gegenereerd, maakt upgraden een algemeen teamlid voor de rol, maar wordt de contracterende eenheid van het project gebruikt voor de organisatie-eenheid van het teamlid. In het voorbeeld met project Z betekent dit dat aan de contracterende organisatie-eenheid Contoso US en de testtaken van het projectplan binnen de implementatiefase de rol technisch consultant is toegewezen voor de organisatie-eenheid die is toegewezen aan Contoso India. De integratietesttaak die is voltooid na de implementatiefase is toegewezen aan de rol technisch consultant. De organisatie-eenheid is Contoso US en er is geen team gegenereerd. Bij een upgrade wordt één algemeen teamlid gemaakt, een technisch adviseur met de toegewezen uren van alle drie taken en een organisatie-eenheid van Contoso US, de contracterende organisatie-eenheid van het project.   
 
Het wijzigen van de standaardwaarde van de verschillende organisatie-eenheden op niet-gegenereerde teamleden is de reden waarom we u aanraden het team te genereren of opnieuw genereren voor elk project dat vóór de upgrade algemene resources bevat, zodat de toewijzingen van de organisatie-eenheid niet verloren gaan.

