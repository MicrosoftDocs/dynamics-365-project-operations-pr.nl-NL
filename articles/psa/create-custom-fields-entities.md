---
title: Aangepaste velden en entiteiten maken
description: In dit onderwerp wordt uitgelegd hoe u optiesets en entiteiten maakt in uw eigen oplossing in het Power Apps-platform.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: d2fbe6a4061a93ac3186bbc8624bf5d16209cdf9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574378"
---
# <a name="create-custom-fields-and-entities"></a>Aangepaste velden en entiteiten maken 

[!include [banner](../includes/psa-now-project-operations.md)]

Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit op het Power Apps-platform wilt maken.  
De procedures In dit onderwerp moeten worden voltooid met behulp van de webinterface van Project Service Automation (PSA).

> [!IMPORTANT]
> Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen. Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Aangepaste velden en optiesets maken in de prijsdimensieoplossing

Een prijsdimensie kan een optieset of een entiteit zijn. Beide moeten worden gemaakt in uw prijsoplossing. In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.

### <a name="entity-based-dimensions"></a>Op entiteiten gebaseerde dimensies

1. Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.
3. Klik op **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken. Geef de overige vereiste gegevens op en klik vervolgens op **Opslaan**.

> ![Definitie van entiteit Standaardtitel.](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Op optieset gebaseerde dimensies 
U twee op optiesets gebaseerde dimensies maken. Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.


1. Selecteer in PSA de opties **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**. 
3. Klik op **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.

> ![Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource.](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource.](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Gegevens maken voor op entiteiten gebaseerde dimensies

U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen. Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**. Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.

1. Klik in PSA op **Geavanceerd zoeken**. Selecteer de entiteit **Standaardtitel** en klik op **Resultaten**. Alle rijen in de entiteit **Standaardtitel** worden weergegeven.
2. Klik op **Nieuw**. Voer in het veld **Naam** de tekst Systeemtechnicus in en klik vervolgens op **Opslaan**.
3. Sluit het formulier. 
4. Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.

> ![Voorbeeldgegevens voor de entiteit Standaardtitel.](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
