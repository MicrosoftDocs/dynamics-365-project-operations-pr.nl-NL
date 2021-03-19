---
title: Projectinstellingen
description: In dit onderwerp krijgt u informatie over instellingen voor projectbeheer.
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c55d0f4c8f8db231a995d91a46a582bca2e1e6e3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283722"
---
# <a name="project-settings"></a>Projectinstellingen

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Gebruik de volgende instellingen voor toegang tot de functies voor projectplanning.

## <a name="work-template"></a>Werksjabloon

Als u een projectplanning wilt maken, maakt u een sjabloon voor een projectagenda waarin het aantal werkuren per dag en eventuele sluitingsdagen van het bedrijf worden aangegeven. Als u een sjabloon voor een projectagenda wilt maken, koppelt u een werksjabloon aan het veld **Agendasjabloon** voor het project. Voer deze stappen uit om een werksjabloon te maken.

1. Klik in PSA in het linkernavigatiedeelvenster op **Resources**. 
2. Open op de lijstpagina **Resources** een gebruikersrecord en selecteer vervolgens **Werkuren weergeven**.

  > [!NOTE]
  > Zorg ervoor dat u pop-ups op de browserpagina toestaat. Op deze manier kunt u de werkuren zien die voor de resource zijn ingesteld.
  
3. Klik op het tabblad **Maandweergave** op **Instellen**. Er wordt een lijst met drie opties weergegeven: 

  - Nieuwe weekplanning
  - Werkplanning voor één dag
  - Vrije tijd

> ![Instellingsopties](media/project-13.png)

4. Selecteer **Nieuwe weekplanning** en stel vervolgens de opties voor deze resourceplanning in. U kunt een terugkerende weekplanning, parameters voor dagelijkse uren, sluitingsdagen van het bedrijf en meer instellen.
5. Stel het datumbereik in, selecteer **Opslaan** en klik vervolgens op **Sluiten**. 
6. Ga terug naar de lijstpagina **Resources** en selecteer de resource waarvoor u de werkuren wilt instellen. 
7. Selecteer **Agenda instellen als** om de werksjabloon in te stellen. 
8. Voer in het dialoogvenster **Werksjabloon** een naam voor de werksjabloon in en selecteer **Toepassen**. 

U kunt nu de werksjabloon aan een sjabloon voor een projectagenda koppelen.

## <a name="resource-roles"></a>Resourcerollen

De term *resourerol* verwijst naar de reeks vaardigheden, competenties en certificeringen die een persoon moet hebben om een specifieke reeks taken voor een project te kunnen uitvoeren. In PSA kunt u de kosten en factuurtarieven van de tijd van een resource bepalen op basis van de rol waaraan de resource is gekoppeld. Elke organisatie moet deze rollen instellen met behulp van de linkernavigatiebalk in het menu **Project Service**.

Elke organisatie moet deze rollen instellen op de pagina **Actieve resourcecategorieën**. Als u deze pagina wilt openen, selecteert u in het linkernavigatiedeelvenster de optie **Resourcerollen**.

## <a name="price-lists"></a>Prijslijsten

Met prijslijsten kunt u kosten en verkoopprijzen voor resourcerollen, onkostencategorieën, producten en andere elementen in een organisatie instellen. Voordat u financiële schattingen instelt voor het werk dat voor een project moet worden geleverd, moet u een achterliggende lijst met kosten en een verkoopprijzen maken. In de parametersectie moet u ook een standaardlijst met kosten en verkoopprijzen instellen die van toepassing is op alle projecten die in de organisatie worden gemaakt. Zorg ervoor dat u op de pagina **Actieve projectparameters** een standaardlijst met kosten en verkoopprijzen instelt.


[!INCLUDE[footer-include](../includes/footer-banner.md)]