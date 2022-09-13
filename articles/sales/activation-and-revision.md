---
title: Een projectprijsopgave activeren en reviseren
description: Dit artikel bevat informatie over het activeren en reviseren van prijsprijsopgaven in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410315"
---
# <a name="activate-and-revise-a-project-quote"></a>Een projectprijsopgave activeren en reviseren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Met activerings- en revisiemogelijkheden kunt u versiebeheer bijhouden voor projectgebaseerde prijsopgaves tijdens de schattings- en onderhandelingsfasen. Wanneer een concept van een prijsopgave wordt geactiveerd, wordt deze alleen-lezen.

Met de activerings- en revisiemogelijkheden kunt u de volgende taken uitvoeren:

- Win of verlies prijsopgaven pas na activering.
- Reviseer een prijsopgave om wijzigingen aan te brengen in de bestaande prijsopgave of om een nieuwe versie te maken.

> [!NOTE]
> Nadat de functie voor de activering en revisie van prijsopgaven is ingeschakeld, kan deze niet worden uitgeschakeld.

Volg deze stappen om de mogelijkheid in te schakelen om projectgebaseerde prijsopgaven te activeren en te reviseren.

1. Ga naar **Instellingen** \> **Parameters**.
1. Open de record **Parameters**.
1. Selecteer in het actievenster op het tabblad **Besturingselement voor functie** de optie **Activering en revisies van prijsopgaven inschakelen**.
1. Selecteer in het bevestigingsvenster de optie **OK**.
1. Vernieuw na enkele ogenblikken uw browser. Activerings- en revisiemogelijkheden zouden nu beschikbaar moeten zijn. U weet dat deze mogelijkheden zijn ingeschakeld als de knop **Activering en revisies van prijsopgaven inschakelen** niet meer wordt weergegeven in het actievenster.

## <a name="activating-a-quote"></a>Een prijsopgave activeren

Als de functie voor activering en revisie van prijsopgaven is ingeschakeld, zijn de knoppen **Prijsopgave sluiten als gewonnen** en **Prijsopgave sluiten als verloren** in het actievenster niet beschikbaar voor concepten van projectprijsopgaven. Ze zijn pas beschikbaar nadat een prijsopgave is geactiveerd.

Activering is de fase in het prijsopgaveproces waarin u meer wijzigingen in de prijsopgave wilt voorkomen. In dit stadium wordt de prijsopgave verzonden voor interne beoordeling of naar de klant.

De knoppen **Prijsopgave sluiten als gewonnen** en **Prijsopgave sluiten als verloren** in het actievenster zijn beschikbaar voor geactiveerde prijsopgaven. Afhankelijk van de uitkomst van de interne of klantbeoordeling kunt u één van deze knoppen gebruiken om een geactiveerde prijsopgave te sluiten. U kunt onderhandelingen voeren en wijzigingen aanbrengen in geactiveerde prijsopgaven door **Prijsopgave reviseren** te selecteren.

## <a name="revising-a-quote"></a>Een prijsopgave reviseren

Als u wijzigingen moet aanbrengen in een geactiveerde prijsopgave, selecteert u **Prijsopgave reviseren**. De prijsopgave wordt gesloten en de **gereviseerde** redencode wordt gebruikt. Vervolgens wordt een nieuwe prijsopgave gemaakt met dezelfde id en een verhoogd revisienummer. Alle details uit de oorspronkelijke prijsopgave worden gekopieerd naar de nieuwe prijsopgave. De nieuwe prijsopgave heeft de conceptstatus en kan naar wens worden bewerkt.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
