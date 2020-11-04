---
title: Algemene boekbare resources toewijzen aan een taak en projectteam
description: Dit onderwerp bevat informatie over het boeken van algemene resources aan taken en projectteams.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074579"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Algemene, boekbare resources toewijzen aan een taak en resourcevereisten genereren 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U kunt niet alleen benoemde of echte resources boeken en toewijzen aan uw project, maar u kunt ook algemene resources toewijzen aan projecttaken. Deze resources kunnen fungeren als tijdelijke aanduidingen voor benoemde resources totdat u klaar bent om benoemde resources voor uw project te kiezen. 

1. Open in Project Service Automation (PSA) de pagina **Project** en voer op het tabblad **Planning** de positienaam van de algemene resource in de cel **Resource** van de planning in. Of klik op het pictogram **Resource** in de cel en voer vervolgens in de resourcekiezer de naam in van de algemene resource die u wilt maken.

![Een algemeen teamlid maken en toewijzen](media/RM-how-to-9.png)

Het deelvenster **Snelle invoer: Projectteamlid** wordt geopend. 

2. Voer de rol en organisatie-eenheid van het algemene resourceteamlid in en klik vervolgens op **Opslaan**.

![Algemeen teamlid snel maken](media/RM-how-to-10.png)

3. Nadat u het nieuwe algemene resourceteamlid hebt gemaakt, wordt dit lid toegewezen aan de taak. U kunt deze algemene resource blijven toewijzen aan andere taken in de taakplanning.

![Bestaand algemeen teamlid toewijzen aan taken](media/RM-how-to-11.png)

4. Nadat u de algemene resource hebt toegewezen, kunt u een resourcevereiste genereren en hieraan voldoen door direct een resourceaanvraag te boeken of in te dienen bij een resourcemanager.

![Een vereiste voor een algemeen teamlid genereren](media/RM-how-to-12.png)

In het raster van teamleden kunt u de resourcekiezer niet alleen gebruiken op de hierboven beschreven wijze, maar ook direct algemene resources toevoegen. De resources worden toegevoegd met een resourcevereiste die is gebaseerd op de begin- en einddatums en toewijzingsmethode die is opgegeven in het deelvenster **Snelle invoer: Projectteamlid**.

U ziet een verschil als u het algemene teamlid rechtstreeks toevoegt en vervolgens meer taken toewijst aan de algemene resource dan er vereiste uren om te dekken zijn. Klik op **Vereiste genereren** om de vereiste opnieuw te genereren om de vereiste uren af te stemmen met toewijzingen.

U kunt ook op de koppeling **Resourcevereiste** in het teamraster klikken om de vereiste te openen en vaardigheden, voorkeursresources en dergelijke toe te voegen.

![Resourcevereiste](media/RM-how-to-13.png)
