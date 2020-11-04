---
title: Een projectboeking maken vanaf het planbord
description: Dit onderwerp bevat informatie over het maken van een projectboeking via het planbord.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 57fbc71681015fca73cdda4bc7d392f6be4289f3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074581"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Een projectboeking maken vanaf het planbord

U kunt een resource rechtstreeks op van tabblad **Team** van het project boeken of door een resourcevereiste op basis van een algemene toewijzing van een teamlid te genereren en vervolgens de gegenereerde vereiste met een lid van het projectteam uit te voeren.

U kunt een resource ook rechtstreeks van het planbord naar een project boeken. Dit kunt u op drie manieren doen:

- **Boeken op basis van een gegenereerde resourcevereiste:** u kunt een resourcevereiste genereren nadat u een algemene resource hebt gemaakt en taken in een project hebt toegewezen.

- **Boeken vanuit de primaire vereiste:** de primaire vereisten worden weergegeven op het planbord op het tabblad **Project**. 

- **Boeken op basis van een nieuwe resourcevereiste:** u kunt een geheel nieuwe resourcevereiste maken en deze koppelen aan een project. In het planbord wordt de resourcevereiste weergegeven op het tabblad **Open vereisten**.

## <a name="book-from-a-generated-resource-requirement"></a>Boeken op basis van een gegenereerde resourcevereiste

U kunt een algemene resource maken en deze aan een of meer taken in een project toewijzen. Vervolgens kunt u een resourcevereiste genereren vanuit het algemene teamlid. 

1.  Op het planbord wordt deze resource op het tabblad **Vereisten openen** weergegeven. U moet mogelijk kolomfilters in het raster gebruiken als u veel open vereisten hebt. 

    ![Het tabblad Vereisten openen op het planbord](media/FAQ-Project-Booking-Schedule-Board-1.png "Schermafbeelding van tabel met boekingen en toewijzingen")

2. Selecteer de vereiste. Het tabblad **Beschikbaarheid zoeken** wordt weergegeven boven aan de geselecteerde rij.
 
3. Wanneer u het tabblad selecteert, wordt de modus Planningsassistent van het planbord geopend en worden de beschikbare resources gefilterd die aan de resourcevereiste voldoen. Daarna kunt u een resource boeken.

4. U kunt de geselecteerde rij ook van het planbord naar een resourcecel in het raster erboven slepen. Als u de vereiste hebt neergezet, wordt het deelvenster **Resourceboeking maken** rechts geopend.

    Wanneer u **Boeken** selecteert, wordt de resource voor het projectteam geboekt.

![Het deelvenster Resourceboeking maken](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Boeken vanuit de primaire vereiste

Wanneer u een project in Project Service maakt, wordt er automatisch een resourcevereiste gemaakt die de primaire vereiste wordt genoemd. Dit is een lege vereiste die wordt gebruikt om snel een resource te boeken via het planbord zonder een vereiste te genereren of een nieuwe vereiste te maken. Aangezien de vereiste leeg is, moet u datums en, indien van toepassing, de toewijzingsmethode en uren opgeven. 

1. Als u een resource met de primaire vereiste wilt boeken, selecteert u in het planbord het tabblad **Project**. Mogelijk moet u het kolomfilter voor de kolom **Project** gebruiken als u veel projecten hebt.

   ![Kolomfilters op het planbord](media/FAQ-Project-Booking-Schedule-Board-2.png "Schermafbeelding van tabel met boekingen en toewijzingen")

2. Selecteer de vereiste die de projectnaam als naam heeft en een duur van nul (0) heeft.

3. Selecteer het tabblad **Beschikbaarheid zoeken** dat wordt weergegeven in de rij. Hiermee schakelt u de modus Planningsassistent in voor het planbord en worden de beschikbare resources weergegeven die voor het project kunnen worden geboekt.

4. Aangezien een **primaire vereiste** een lege vereiste met een duur van nul (0) is, moet u de duur in het deelvenster **Resourceboeking maken** instellen wanneer u een resource selecteert en boekt.

5. U kunt de **primaire vereiste van het project** ook onder op het planbord selecteren en naar een resource slepen om deze te boeken.
 
    Aangezien de **primaire vereiste** een lege vereiste met een duur van nul (0) is, moet u de duur in het deelvenster **Resourceboeking maken** instellen wanneer u een resource selecteert en boekt.
 
    Als u een resource via de **primaire vereiste** op het planbord boekt, voegt u de resource aan het projectteam toe zonder enige toewijzingen.
 
## <a name="book-from-a-new-resource-requirement"></a>Boeken op basis van een nieuwe resourcevereiste
Voer de volgende stappen uit om te boeken via een nieuwe resourcevereiste. 

1. Ga naar **Resourcevereisten** en selecteer **Nieuw** om een nieuwe resourcevereiste te maken.

2. Selecteer op het tabblad **Project** een project om de vereiste aan het project te koppelen.
 
    Deze nieuwe vereiste wordt weergegeven op het planbord als **open vereiste** die u kunt vervullen.

3. Boek de resource om deze toe te voegen aan het projectteam.

4. Nu de resource is geboekt, moet u taken handmatig toewijzen.

