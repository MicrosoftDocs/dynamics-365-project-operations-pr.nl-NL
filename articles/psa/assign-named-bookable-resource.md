---
title: Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen
description: Dit onderwerp bevat informatie over hoe u benoemde resources voor projectteams kunt boeken en hen aan taken kunt toewijzen.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 8568921dd16472f10a7043c5fe3f58b9f5cd3989ad39e3a3bdf269b0c7203ae2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998635"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a>Benoemde, boekbare resources boeken voor een projectteam en taken toewijzen 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U kunt een benoemde resource toevoegen aan uw projectteam door ze rechtstreeks voor het team te boeken. U doet dit via de volgende stappen:

1. Ga in Project Service Automation naar **Projecten** en open het project waarvoor u boekt.
2. Klik op de pagina **Project** op het tabblad **Team** op **Nieuw**. 

![Een teamlid toevoegen via het tabblad Team.](media/RM-how-to-1.png)

3. Selecteer de boekbare resource in het dialoogvenster **Snelle invoer: Projectteamlid**. Het veld **Rol** wordt gevuld met de standaardrol van de resource, indien toegewezen. Indien nodig kunt u de rol wijzigen. 
4. Selecteer de begin- en einddatums voor de periode waarvoor de resource nodig is en selecteer de toewijzingsmethode van de capaciteit van de resource. 
5. Als u wilt dat het teamlid een projectfiatteur is, selecteert u **Ja** in het veld **Projectfiatteur**. Dit betekent dat het teamlid ingediende tijd- en onkostenposten voor dit project kan goedkeuren. 
6. Klik op **Opslaan**.

![Een teamlid toevoegen in het formulier voor snelle invoer.](media/RM-how-to-2.png)


U kunt de geboekte resource nu toewijzen aan taken in het project. Klik op de pagina **Project** op het tabblad **Planning** om taken aan de nieuwe resource toe te wijzen. De resourcekiezer die wordt gestart vanuit het veld **Resources** in het taakraster bevat de teamleden die u kunt selecteren.

![Een teamlid toewijzen aan een taak op het tabblad Planning.](media/RM-how-to-3.png)

In versie 3 voor Project Service Automation (PSA) zijn resourceboekingen en taaktoewijzingen niet nauw gekoppeld. Dit betekent dat u taken aan teamleden kunt toewijzen voor meer uren dan hun boekingen dekken in het project wanneer u de resourcekiezer in de planning gebruikt.
U kunt de verschillen tussen boekingen en toewijzingen voor teamleden op het tabblad **Team** of op het tabblad **Resourceafstemming** bekijken. U kunt ook de verschillen tussen boekingen en toewijzingen voor resources op een meer gedetailleerd niveau afstemmen.

![Het tabblad Afstemming van resources.](media/RM-how-to-4.png)

U ook de resourcekiezer op het tabblad **Planning** gebruiken om boekbare resources te zoeken en te selecteren die nog geen deel uitmaken van het projectteam. Deze worden weergegeven in de resourcekiezer als **Andere resources**.

![Een niet-teamlidresource toewijzen aan een taak.](media/RM-how-to-5.png)

Wanneer u dit doet, wordt de resource toegevoegd aan het projectteam en toegewezen aan de taak, maar er worden geen boekingen gegenereerd.

![Teamlid met toewijzingen en geen boekingen.](media/RM-how-to-6.png)

U kunt de functie voor uitgebreid boeken van het tabblad **Afstemming** of het **planbord** gebruiken om de capaciteit van de resource voor het project te boeken.

![Boekingen voor een teamlid uitbreiden op het tabblad Afstemming van resources.](media/RM-how-to-7.png)

Nadat een teamlid is geboekt voor uw project, kunt u Boekingen bijhouden of het planbord rechtstreeks gebruiken om hun boekingen te beheren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]