---
title: Vereisten zacht boeken
description: Dit onderwerp legt uit hoe u resourcevereisten zacht kunt boeken.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007005"
---
# <a name="soft-book-requirements"></a>Vereisten zacht boeken

[!include [banner](../includes/psa-now-project-operations.md)]

Een resourcevereiste kan hard worden geboekt. Een harde boeking maakt een voorstel aan, waardoor de capaciteit van een resource wordt verbruikt. Het voorstel wordt vervolgens ter goedkeuring teruggestuurd naar de aanvrager. Een zachte boeking voegt een resource voorlopig toe aan een projectteam en heeft een andere status op het planbord, maar verbruikt niet de capaciteit van de resource. Als u een resource vanuit het planbord zacht wilt boeken, stelt u het veld **Boekingsstatus** in op **Zacht**.

![Boekingsstatus is ingesteld op Zacht.](media/Resource-Management-image77.png)

Wanneer het tabblad **Team** in de weergave **Benoemde teamleden** staat, wordt de resource daar weergegeven. De zacht geboekte uren worden gerapporteerd in de kolom **Zacht geboekte uren**.

![Zacht geboekte uren in de weergave met benoemde teamleden.](media/Resource-Management-image78.png)

Zacht geboekte teamleden kunnen niet aan taken worden toegewezen.

![Zacht geboekt teamlid toegewezen aan een taak.](media/Resource-Management-image79.png)

Op het tabblad **Vereffening** worden geen boekingen weergegeven voor een zacht geboekte resource, omdat het tabblad **Vereffening** alleen rekening houdt met harde boekingen.

![Zacht geboekte resource zonder boekingen op het tabblad Vereffening.](media/Resource-Management-image80.png)

> [!NOTE]
> U kunt een resource niet zacht boeken vanuit een vereiste die is gegenereerd op basis van een algemeen teamlid.

Op het planbord wordt een andere kleur gebruikt voor zachte boekingen voor een resource.

![Zachte boekingen op het planbord.](media/Resource-Management-image81.png)

Als u een zachte boeking wilt converteren naar een harde boeking, klikt u in het planbord met de rechtermuisknop op de zachte boeking en kiest u **Status wijzigen** \> **Hard boeken** \> **Hard**.

![De boekingsstatus wijzigen in hard.](media/Resource-Management-image82.png)

De boeking wordt gewijzigd en de status wordt gewijzigd op het planbord. Omdat de boekingsstatus nu **hard** is, wordt de resource weergegeven als geboekt en worden de capaciteit en beschikbaarheid aangepast.

U kunt met dezelfde methode een harde boeking of een zachte boeking annuleren op het planbord.

Als u een zacht geboekte resource wilt converteren naar hard geboekt op het tabblad **Team** van het project, selecteert u de resource en vervolgens **Bevestigen**.

![Opdracht Bevestigen.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]