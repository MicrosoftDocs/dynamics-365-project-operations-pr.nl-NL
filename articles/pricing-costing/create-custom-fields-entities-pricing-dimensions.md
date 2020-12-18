---
title: Aangepaste velden en entiteiten maken als prijsdimensies
description: Deze onderwerp biedt informatie over het maken van aangepaste optiesets of entiteiten.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: fc5917856b8f28d36dc55593a68eba7823a00b36
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642807"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a>Aangepaste velden en entiteiten maken als prijsdimensies

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voer de volgende stappen uit wanneer u een aangepaste optieset of entiteit wilt maken en gebruiken als een prijsdimensie. Zie [Overzicht van prijsdimensies](pricing-dimensions-overview.md) voor meer informatie.  

> [!IMPORTANT]
> Het is raadzaam om alle wijzigingen in aangepaste prijsdimensies in een afzonderlijke oplossing aan te brengen. Deze belangrijke methode biedt flexibiliteit voor de toekomst om wijzigingen indien nodig bij te werken of te verwijderen. Dit helpt ook bij het hergebruik van uw werk en maakt het gemakkelijker om deze wijzigingen naar een ander exemplaar over te dragen. Nadat u alle vereiste wijzigingen hebt aangebracht, exporteert u deze oplossing als een **Beheerde oplossing** en importeert u deze in andere exemplaren om uw prijsinstellingen opnieuw te gebruiken.

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a>Aangepaste velden en optiesets maken in de prijsdimensieoplossing

Een prijsdimensie kan een optieset of een entiteit zijn. Beide moeten worden gemaakt in uw prijsoplossing. In de stappen in deze procedure wordt uitgelegd hoe u op entiteiten gebaseerde dimensies en op optieset gebaseerde dimensies maakt.

### <a name="entity-based-dimensions"></a>Op entiteiten gebaseerde dimensies
Volg deze stappen om op entiteiten gebaseerde dimensies te maken:

1. Ga naar **Instellingen** > **Oplossingen** en dubbelklik vervolgens op **\<your organization name> prijsdimensies**.
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster **Entiteiten**.
3. Selecteer **Nieuw** om een nieuwe entiteit met de naam **Standaardtitel** te maken. 
4. Geef de overige vereiste gegevens op en selecteer vervolgens **Opslaan**.

> ![Definitie van entiteit Standaardtitel](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a>Op optieset gebaseerde dimensies 
U twee op optiesets gebaseerde dimensies maken. 

- Gebruik **Werklocatie van resource** om de prijs van locatiewerk **Thuis** en **Op locatie** bij te houden. 
- Gebruik **Werkuren van resource** met waarden **Regelmatig** en **Overuren** om een opslag toe te passen wanneer het werk is voltooid.

De volgende afbeelding geeft een weergave van de dimensie **Werklocatie van resource**. 

> ![Op optieset gebaseerde prijsdimensie met de naam Werklocatie van resource](media/Option-set-PD-called-Resource-Work-Location.png)

De volgende afbeelding geeft een weergave van de dimensie **Werkuren van resource**. 

> ![Op optieset gebaseerde prijsdimensie met de naam Werkuren van resource](media/Option-set-PD-called-Resource-Work-Hours.png)

1. Ga naar **Instellingen** > **Oplossingen** en dubbelklik op **\<your organization name> prijsdimensies**. 
2. Selecteer in Oplossingenverkenner in het linkernavigatiedeelvenster de optie **Optiesets**. 
3. Selecteer **Nieuw** om een nieuwe optieset te maken, voer de resterende vereiste informatie in en selecteer vervolgens **Opslaan**.

## <a name="create-data-for-entity-based-dimensions"></a>Gegevens maken voor op entiteiten gebaseerde dimensies

U kunt gegevens voor op entiteiten gebaseerde dimensies handmatig maken of met behulp van Microsoft Excel-imports of serviceaanroepen. Gebruik de stappen in deze procedure om de twee standaardtitels **Systeemtechnicus** en **Hoofdsysteemtechnicus** te maken op basis van de op entiteiten gebaseerde dimensie **Standaardtitel**. Als u een beperkte hoeveelheid gegevens wilt maken, zoals in het volgende voorbeeld, kunt u een standaardformulier gebruiken.

1. Selecteer **Geavanceerd zoeken**.
2. Selecteer de entiteit **Standaardtitel** en selecteer **Resultaten**. Alle rijen in de entiteit **Standaardtitel** worden weergegeven.
3. Selecteer **Nieuw**, voer in het veld **Naam** de naam 'Systeemtechnicus' in en selecteer vervolgens **Opslaan**.
4. Sluit de pagina. 
5. Herhaal stap 1-3 om een andere standaardtitel te maken voor Hoofdsysteemtechnicus.

> ![Voorbeeldgegevens voor de entiteit Standaardtitel](media/ST-data.png)
