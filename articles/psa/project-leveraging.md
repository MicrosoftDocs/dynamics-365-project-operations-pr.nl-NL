---
title: Verkoopschattingen en projecten
description: Dit artikel bevat informatie over hoe u kunt profiteren van de planning en schattingen in het verkoopproces.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 957c2337cce3b3bf65a0bfef7c1aee6a730971fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925390"
---
# <a name="sales-estimates-and-projects"></a>Verkoopschattingen en projecten

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tijdens het verkoopproces kunt u verkoopschattingen maken door een project aan een verkoopprijsopgave te koppelen. Op deze manier kan een deterministische schatting worden gemaakt tijdens het verkoopproces om te profiteren van de mogelijkheden voor projectplanning en -schatting. Als de verkoop doorgaat, kan de planning die is gebruikt voor verkoopschattingsdoeleinden, worden gebruikt als basis voor verdere verfijning van het projectplan.

## <a name="linking-a-project-to-a-quote-line"></a>Een project koppelen aan een prijsopgaveregel

Wanneer u een op een project gebaseerde prijsopgaveregel maakt, kunt u een nieuw project maken of een bestaand project koppelen op de pagina **Prijsopgaveregel**. 

> ![Prijsopgaveregelformulier.](media/project-8.png)
 
Wanneer u een nieuw project maakt op basis van de details van de prijsopgaveregel, kunt u gebruikmaken van projectsjablonen. Projectsjablonen zijn modelprojecten die standaardprojectplannen en financiële schattingen vertegenwoordigen die typisch zijn voor een organisatie. Ze kunnen ook kopieën van projectplannen en schattingen van eerdere projecten vertegenwoordigen.

> ![Details van prijsopgaveregel.](media/project-9.png)
  
Wanneer u het project maakt op basis van de prijsopgave, wordt het project automatisch gekoppeld aan de prijsopgaveregel.

## <a name="components-of-estimates-in-a-project"></a>Componenten van schattingen in een project

Met een planning kunt u werk verdelen in taken, een hiërarchie van taken onderhouden, bepalen welke resources nodig zijn om een taak te voltooien en een schatting toewijzen van de inspanning die nodig is om een taak te voltooien.

U kunt de werkinspanning en de planningsschattingen definiëren met behulp van de velden op het tabblad **Planning** van de pagina **Project**. Omdat er een prijslijst aan het project is gekoppeld, worden financiële schattingen berekend op basis van kost- en verkoopprijzen die zijn gedefinieerd in de prijslijst.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Schattingen importeren van een project in een prijsopgave

Nadat u projectschattingen hebt gedefinieerd, kunt u deze importeren in de prijsopgaveregel. Selecteer op de pagina **Details van prijsopgaveregel** de optie **Importeren uit schatting** op het lint om projectschattingen op het niveau van transactietype, rol of taak samen te vatten.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
