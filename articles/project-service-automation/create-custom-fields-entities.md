---
title: Aangepaste velden en entiteiten maken
description: In dit onderwerp wordt uitgelegd hoe u optiesets en entiteiten maakt in uw eigen oplossing in het Power Apps-platform.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750820"
---
# <a name="create-custom-fields-and-entities"></a>Aangepaste velden en entiteiten maken 

Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit op het Power Apps-platform wilt maken.  
De procedures in dit onderwerp moeten worden voltooid met behulp van de webinterface van Project Service Automation (PSA).

> [!IMPORTANT]
> Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen. Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Een aangepaste oplossing maken voor prijsdimensies
1. Klik in PSA op **Instellingen** > **Oplossingen** en klik vervolgens op **Nieuw** om een nieuwe oplossing te maken. 
2. Noem de oplossing **\<uw organisatienaam> prijsdimensies**, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.

> ![Een aangepaste oplossing maken voor prijsdimensies](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Aangepaste velden en optiesets maken in de prijsdimensieoplossing

Een prijsdimensie kan een optieset of een entiteit zijn. Beide moeten worden gemaakt in uw prijsoplossing. In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.

### <a name="entity-based-dimensions"></a>Op entiteiten gebaseerde dimensies

1. Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<naam van uw organisatie > prijsdimensies**.
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.
3. Klik op **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken. Geef de overige vereiste gegevens op en klik vervolgens op **Opslaan**.

> ![Definitie van entiteit Standaardtitel](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a>Op optieset gebaseerde dimensies 
U twee op optiesets gebaseerde dimensies maken. Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.


1. Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<de naam van uw organisatie > prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**. 
3. Klik op **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en klik vervolgens op **Opslaan**.

> ![Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a>Gegevens maken voor op entiteiten gebaseerde dimensies

U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen. Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**. Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.

1. Klik in PSA op **Geavanceerd zoeken**. Selecteer de entiteit **Standaardtitel** en klik op **Resultaten**. Alle rijen in de entiteit **Standaardtitel** worden weergegeven.
2. Klik op **Nieuw**. Voer in het veld **Naam** de tekst Systeemtechnicus in en klik vervolgens op **Opslaan**.
3. Sluit het formulier. 
4. Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.

> ![Voorbeeldgegevens voor de entiteit Standaardtitel ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a>Voeg alle vereiste PSA-entiteiten en gerelateerde onderdelen toe aan de oplossing Prijsdimensie
U moet de volgende Project Service-entiteiten toevoegen aan uw prijsoplossing. Gebruik de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.

1. Klik in PSA op **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<naam van uw organisatie > prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.
3. Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:

- Werkelijk
- Boekbare resource
- Schattingsregel
- Factuurregeldetail
- Journaalregel
- Detail van projectcontractregels
- Projectteamlid
- Details prijsopgaveregel
- Opslag voor rolprijs
- Rolprijs 
- Tijdsvermelding 

> ![Bestaande entiteiten toevoegen aan de oplossing voor prijsdimensies](media/Existing-entities-to-PD-solution.png)

> ![Oplossingsonderdelen selecteren](media/Dimension-Components.png)

> [!NOTE]
> Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.

4. Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, klikt u op **Nee**.

> ![Niet alle gerelateerde onderdelen opnemen](media/Do-not-include-required.png)


