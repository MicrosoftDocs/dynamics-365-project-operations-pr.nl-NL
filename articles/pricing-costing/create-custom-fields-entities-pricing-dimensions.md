---
title: Aangepaste velden en entiteiten maken als prijsdimensies
description: Deze onderwerp biedt informatie over het maken van aangepaste optiesets of entiteiten.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074602"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Aangepaste velden en entiteiten maken als prijsdimensies

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit wilt maken.

> [!IMPORTANT]
> Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen. Deze belangrijke aanbevolen procedure biedt flexibiliteit in de toekomst om eventuele wijzigingen bij te werken of te verwijderen, stelt u in staat uw werk opnieuw te gebruiken en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar te publiceren. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.


## <a name="create-a-custom-solution-for-pricing-dimensions"></a>Een aangepaste oplossing maken voor prijsdimensies
1. Ga naar **Instellingen** > **Oplossingen** en selecteer vervolgens **Nieuw** om een nieuwe oplossing te maken. 
2. Noem de oplossing **\<your organization name> prijsdimensies** , voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Aangepaste velden en optiesets maken in de prijsdimensieoplossing

Een prijsdimensie kan een optieset of een entiteit zijn. Beide moeten worden gemaakt in uw prijsoplossing. In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.

### <a name="entity-based-dimensions"></a>Op entiteiten gebaseerde dimensies

1. Ga naar **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.
3. Selecteer **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken. 
4. Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.


### <a name="option-set-based-dimensions"></a>Op optieset gebaseerde dimensies 
U twee op optiesets gebaseerde dimensies maken. Gebruik **Werklocatie van resource** om de prijs van werk op de locatie **Thuis** en **Op locatie** bij te houden en gebruik **Werkuren van resource** met de waarden **Reguliere uren** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.


1. Ga naar **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**. 
3. Selecteer **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.

## <a name="create-data-for-entity-based-dimensions"></a>Gegevens maken voor op entiteiten gebaseerde dimensies

U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen. Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**. Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.

1. Selecteer **Geavanceerd zoeken** , selecteer de entiteit **Standaardtitel** en selecteer vervolgens **Resultaten**. Alle rijen in de entiteit **Standaardtitel** worden weergegeven.
2. Selecteer **Nieuw** , voer in het veld **Naam** de naam 'Systeemtechnicus' in en selecteer vervolgens **Opslaan**.
3. Sluit het formulier. 
4. Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Voeg alle vereiste entiteiten en gerelateerde onderdelen toe aan de oplossing Prijsdimensie
U moet de volgende entiteiten toevoegen aan uw prijsoplossing. Gebruik de stappen in deze procedure om een aantal belangrijke schemawijzigingen in de prijsoplossing door te voeren, zodat de entiteiten de nieuwe prijsdimensies opmerken.

1. Selecteer de opties **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Bestaande toevoegen** > **Entiteiten**.
3. Selecteer in het dialoogvenster **Onderdelen van oplossing** de volgende entiteiten:

  - Werkelijk
  - Boekbare resource
  - Schattingsregel
  - Factuurregeldetail
  - Journaalregel
  - Detail van projectcontractregels
  - Projectteamlid
  - Details van prijsopgaveregel
  - Opslag voor rolprijs
  - Rolprijs 
  - Tijdsvermelding 


> [!NOTE]
> Zorg ervoor dat alle formulieren en weergaven voor elk van de geselecteerde entiteiten worden opgenomen.

4. Wanneer u wordt gevraagd of u eventuele afhankelijke entiteiten voor de hierboven geselecteerde entiteiten wilt opnemen, selecteert u **Nee**.

