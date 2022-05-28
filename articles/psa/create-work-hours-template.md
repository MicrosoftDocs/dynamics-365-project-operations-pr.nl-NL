---
title: Een werkurensjabloon maken
description: In dit onderwerp wordt beschreven hoe u een werkurensjabloon kunt maken in Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598942"
---
# <a name="create-a-work-hours-template-project-service"></a>Een werkurensjabloon maken (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Als u een project wilt maken en beheren, moet u een agendasjabloon op het project toepassen. De agendasjabloon definieert de volgende projectkenmerken:

- Werkuren, inclusief begin- en eindtijd
- Werkdagen
- Agenda-uitzonderingen zoals niet-werkdagen

De agendasjabloon die op een project wordt toegepast, is een kopie van de agendasjabloon die is gedefinieerd in de instellingen van uw organisatie.

> [!NOTE]
> Als u de agendasjabloon wijzigt, worden die wijzigingen niet doorgevoerd in de werktijden van het project. Als u de werktijden van het project wilt wijzigen, moet een nieuwe sjabloon worden toegepast.

Als u een agendasjabloon voor uw organisatie wilt maken, zijn er twee belangrijke vereisten:

- Definieer de gewenste werkuren van de sjabloon met behulp van een nieuwe of bestaande boekbare resource.
- Maak een nieuwe agendasjabloon en koppel de sjabloon aan de boekbare resource.

**De werkuren van de sjabloon definiëren**

1. Ga naar **Resources** \> **Resources**.
2. Maak een nieuwe resource om naar te verwijzen in de agendasjabloon of selecteer een bestaande resource.
3. Selecteer het tabblad **Werkuren** van de resource en voer de instructies uit in [Werkuren instellen voor een resource](/dynamics365/field-service/set-work-hours-resource) om de agendaregels te configureren.

**Een nieuwe agendasjabloon maken**

1. Ga naar **Instellingen** \> **Agendasjabloon**.
2. Selecteer **Nieuw** en voer een naam, beschrijving en sjabloonresource in.


> [!NOTE]
> Wanneer in een agendasjabloon naar een resource wordt verwezen, wordt een kopie van de agenda van de resource aan de agendasjabloon gekoppeld. Als de werkuren van de gekopieerde sjabloon veranderen, worden die wijzigingen niet doorgevoerd in de agendasjabloon.


### <a name="see-also"></a>Zie ook  
 [Resources instellen](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
