---
title: Planbord configureren om contractwerknemers en capaciteit van resources op contractbasis weer te geven
description: Dit onderwerp beschrijft hoe u het planbord in Microsoft Dynamics 365 Project Operations kunt configureren om capaciteit van resources op contractbasis te tonen bij het bemannen voor projectresource-vereisten.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587811"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Planbord configureren om contractwerknemers en capaciteit van resources op contractbasis weer te geven 

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Planbord in Microsoft Dynamics 365 Project Operations kan op twee manieren worden gebruikt voor het zoeken naar resources:

- Algemeen zoeken naar resources zonder de context van een specifieke projectgebaseerde resourcevereiste.
- Vereiste-specifiek zoeken naar bronnen waarbij de projectvereiste de context zal bieden voor de voorgestelde resources.

Om het planbord te informeren over capaciteit van resources op contractbasis en contractwerknemers, moet u de instellingen van het planbord bijwerken. Deze updates omvatten: 
- Werk de instellingen van het planbord bij voor het algemene zoeken naar resources.
- Werk de instellingen van het planbord bij voor het vereiste-gebaseerde zoeken naar resources.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Instellingen van planbord bijwerken voor algemeen zoeken naar resources
### <a name="update-filters-for-general-resource-search"></a>Filters bijwerken voor algemeen zoeken naar resources
Wanneer u naar een resource zoekt, moeten de filters die beschikbaar zijn op het planbord worden bijgewerkt, zodat u ook naar externe resources kunt zoeken door een of meer van de volgende zaken op te geven:
  - Werknemertype of de getoonde resources contractwerknemers of werknemers moeten zijn.
  - Het leverende bedrijf waartoe de resource moet behoren.
  - Resources die bij een specifiek toeleveringscontract of specifieke toeleveringscontractregel horen.
    
### <a name="update-retrieve-resource-query"></a>Resourcequery voor ophalen bijwerken
De query die voor het zoeken wordt gebruikt, moet ook worden bijgewerkt om deze aanvullende filterkenmerken te gebruiken. Gebruik de volgende stappen om de configuratie van het planbord bij te werken voor algemeen zoeken naar resources:  
1. Open **Instellingen planningsbord** voor een specifiek planbord.
2. Open het tabblad **Algemene instellingen** en blader naar **Overige instellingen**.
3. Werk in de lijst met instellingen in deze sectie de **Filterlay-out** bij naar **Standaardfilterindeling voor Project Operations Lite**.
4. Werk **Query Resources ophalen** bij naar **Standaardquery Resources ophalen voor Project Operations Lite**.

![Instellingen van planbord bijwerken voor algemeen zoeken naar resources](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Instellingen van planbord bijwerken voor vereiste-gebaseerde zoeken naar resources
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filters bijwerken voor vereiste-specifieke zoeken naar resources 
Wanneer u naar een resource zoekt, moeten de filters die beschikbaar zijn op het planbord worden bijgewerkt, zodat u ook naar externe resources kunt zoeken door een of meer van de volgende zaken op te geven:
 - Werknemertype of de getoonde resources contractwerknemers of werknemers moeten zijn.
 - Het leverende bedrijf waartoe de resource moet behoren.
 - Resources die bij een specifiek toeleveringscontract of specifieke toeleveringscontractregel horen.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Query Resources ophalen bijwerken voor vereiste-specifieke resource zoeken 
De query die voor het zoeken wordt gebruikt, moet ook worden bijgewerkt om deze aanvullende filterkenmerken te gebruiken. Gebruik de volgende stappen om de configuratie van het planbord bij te werken voor vereiste-gebaseerd zoeken naar resources:

1. Open **Instellingen planningsbord** voor een specifiek planbord en selecteer vervolgens **Standaardinstellingen openen** om de instellingen voor vereiste-specifiek zoeken te openen.
2. Open het tabblad **Algemene instellingen** en blader naar **Overige instellingen**.
3. Werk in de lijst met instellingen in deze sectie de **Filterlay-out** bij naar **Standaardfilterindeling voor Project Operations Lite**.
4. Werk **Query Resources ophalen** bij naar **Standaardquery Resources ophalen voor Project Operations Lite**.
5. Open het tabblad **Planningstypen** en ga naar **Project**.
6. Onder de instellingen voor **Project**, werk **Query Resources ophalen voor planningsassistent** bij naar **Standaardquery Resources ophalen voor Project Operations Lite** en werk **Query Beperkingen ophalen voor planningsassistent** bij naar **Standaardquery Beperkingen ophalen voor Project Operations**.

![Instellingen van planbord bijwerken voor vereiste-gebaseerde zoeken naar resources](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
