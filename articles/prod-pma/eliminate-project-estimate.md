---
title: Een projectschatting verwijderen
description: Dit onderwerp bevat informatie over het verwijderen van een projectschatting nadat deze is voltooid.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270672"
---
# <a name="eliminate-a-project-estimate"></a>Een projectschatting verwijderen

[!include [banner](../includes/banner.md)]

Projectschattingen bieden de financiële weergave voor werk dat voor een project wordt geschat en gepland. Als u met schattingen voor een project wilt werken, moet u het project aan een schattingsproject koppelen. Een schattingsproject wordt altijd gebaseerd op een bestaand project, maar meerdere projecten kunnen verwijzen naar één schattingsproject. Aan schattingsprojecten kunnen alleen projecten met een vaste prijs en investeringsprojecten worden gekoppeld, en die projecten moeten tot dezelfde projectgroep behoren als het schattingsproject.

Als u een schattingsproject wilt verwijderen, moet het voltooid zijn. In de volgende stappen wordt uitgelegd hoe u een schatting kunt verwijderen.

1. Ga naar **Projectmanagement en financiële administratie** > **Alle projecten** en open het project. 
2. Selecteer op het tabblad **Beheer** **Schattingen** en selecteer op de pagina **Schatting** **Verwijderen**.
3. Stel de volgende opties in op de pagina **Schatting verwijderen** op het tabblad **Algemeen**:

   - **Periodecode**: selecteer de periodecode om de juiste schattingsprojecten te kiezen. 
   - **Schattingsdatum**: selecteer de juiste schattingsdatum voor verwijdering.
   - **Verwijderen met OHW-waarschuwingen**: schakel deze optie in om een melding te geven wanneer een schatting die is gekoppeld aan werk in uitvoering (OHW), wordt verwijderd. Als deze optie niet is ingeschakeld, kan de verwijdering niet worden voortgezet als er niet-geschatte transacties bestaan. 
   > [!NOTE]
   > Deze optie is alleen beschikbaar als verwijdering wordt toegepast op een schattingsproject. De optie is niet beschikbaar als u gebruikmaakt van periodieke berichten. Deze instelling werkt met de instellingen op het tabblad **Schatting** op de pagina **Projectparameters** in de veldgroep **Verwijdering toestaan als er niet-geschatte transacties bestaan**.
   - **Fase instellen op Voltooid**: schakel deze optie in als u de fase van het schattingsproject wilt instellen op **Voltooid** nadat u de verwijdering hebt uitgevoerd.
   - **Schattingslijst afdrukken**: selecteer de informatie die moet worden opgenomen wanneer de schattingslijst wordt afgedrukt.
   - **Infolog weergeven**: schakel deze optie in om Infolog weer te geven.
   - **Boekingsdatum**: kies de boekingsdatum in het grootboek voor de schatting.

4.  Selecteer **OK**.
5. Als het verwijderingsproces is voltooid, wordt het verwijderde schattingsproject weergegeven met een negatieve waarde. 

Als u niet van plan was een schatting te verwijderen, kunt u de verwijderde schatting selecteren en **Verwijdering ongedaan maken** selecteren.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]