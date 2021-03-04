---
title: Toerekenbare bestede uren voor resources weergeven
description: Dit onderwerp bevat informatie over de weergave met bestede uren van resources.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146387"
---
# <a name="view-chargeable-utilization-for-resources"></a>Toerekenbare bestede uren voor resources weergeven

[!include [banner](../includes/psa-now-project-operations.md)]
 
In de weergave **Bestede uren** op de pagina **Project Service - Bestede uren van resource** worden de toerekenbare bestede uren voor elke boekbare resource weergegeven. Omdat de weergave is gebaseerd op het planbord, komt u hier veel van dezelfde functies tegen.

> ![Schermafbeelding van weergave voor bestede uren van resources](media/FAQ-utilization-1.png)
 

De berekening van toerekenbare bestede uren werkt als volgt:

   Toerekenbare bestede uren = (toerekenbare werkelijke uren)/(resourcecapaciteit)

De cellen vertegenwoordigen de berekende toerekenbare bestede uren voor de geselecteerde periode (dagen, weken of maanden).

Met de kleuren in de cellen worden de toerekenbare bestede uren voor een resource ten opzichte van de beoogde toerekenbare bestede uren weergegeven. 

Het doel voor bestede uren kan worden ingesteld voor de standaardrol van de resource of voor de afzonderlijke resource zelf. Bij de berekening wordt eerst gekeken naar de afzonderlijke resource voor het doel en vervolgens naar de standaardrol van de resource.

## <a name="set-target-on-a-resource"></a>Het doel voor een resource instellen

1. Ga naar **Resources** \> **Resources**. 
2. Selecteer een resource om de record te openen. 
3. Op het tabblad **Project Service** kunt u het doel voor bestede uren voor de resource instellen.

> ![Schermafbeelding van het instellen van het doel voor bestede uren via het tabblad Project Service](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Het doel voor bestede uren voor een rol instellen

1. Ga naar **Resources** \> **Resourcerollen**. 
2. Selecteer een rol en open de record. 
3. Stel het doel voor bestede uren voor de rol in.

> ![Schermafbeelding van het instellen van het doel voor bestede uren via Resourcerollen](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>De toerekenbare bestede uren voor een resource berekenen

Als u de toerekenbare bestede uren voor een resource wilt berekenen, moet u enkele instellingen opgeven. 

### <a name="set-default-role-for-individual-resource"></a>De standaardrol voor een afzonderlijke resource instellen

Eerst moet het doel voor bestede uren worden ingesteld voor de afzonderlijke resource of voor de resourcerollen. Als u resourcerollen voor doelen gebruikt, moet elke afzonderlijke resource een standaardrol hebben. 

1. U stelt dit in door naar **Resources** \> **Resources** te gaan. 
2. Selecteer een resource, open de record en selecteer vervolgens het tabblad **Project Service**. 
3. Zorg ervoor dat er in het raster **Resourcerol** één rol is opgenomen voor de resource en dat **Is standaard** is ingesteld op **Ja**.
 
### <a name="change-billing-type-for-resource-role"></a>Het factureringstype voor de resourcerol wijzigen

Voor de resourcerollen moet het factureringstype **Toerekenbaar** zijn ingesteld. 

1. Ga naar **Resources** \> **Resourcerollen**. 
2. Open de record die u wilt bijwerken en stel vervolgens het standaardfactureringstype in op **Toerekenbaar**.

### <a name="set-working-hours-for-resource-role"></a>Werkuren voor de resourcerol instellen
 
De resource moet werkuren hebben om de capaciteit te berekenen. 

1. Ga naar **Resources** \> **Resources**. 
2. Selecteer een resource om de record te openen en selecteer vervolgens **Werkuren weergeven**. 
3. U kunt de lijst met resources bulksgewijs bijwerken door een **Werkurensjabloon** toe te passen vanuit de weergave **Resourcelijst**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Problemen met toerekenbare werkelijke uren oplossen

De toerekenbare werkelijke uren zijn afkomstig uit de entiteit **Werkelijke waarden**. Omdat werkelijke waarden met het factureringstype **Toerekenbaar** worden opgenomen in de berekening, moet u projecten hebben met toerekenbare werkelijke waarden.

U kunt het volgende controleren als u geen toerekenbare bestede uren ziet:

- Voor de resource zijn werkuren gedefinieerd voor de capaciteit.
- Voor de resource bestaat een afzonderlijk gedefinieerd doel voor bestede uren of er is een standaardrol aan toegewezen. Voor de rol is een doel voor bestede uren gedefinieerd.
- Werkelijke waarden hebben het factureringstype **Toerekenbaar** voor de periode waarvoor u een berekening van bestede uren verwacht. Controleer het volgende als u werkelijke waarden met andere factureringstypen dan Toerekenbaar tegenkomt:

  - Voor de gebruikte rol voor de werkelijke waarden is standaard geen toerekenbaar factureringstype ingesteld.
  - De projectondersteunende rol op de projectcontractregel is ingesteld op niet-toerekenbaar.
  - Aan het project is geen contractregel gekoppeld.



[!INCLUDE[footer-include](../includes/footer-banner.md)]