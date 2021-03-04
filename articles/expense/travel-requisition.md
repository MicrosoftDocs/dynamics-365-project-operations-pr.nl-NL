---
title: Reisaanvragen
description: Dit onderwerp biedt informatie over reisaanvragen.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 46a678ac4486c99f11d74dbac07dedd08364cb2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123732"
---
# <a name="travel-requisitions"></a>Reisaanvragen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Op een reisaanvraag staan de onkosten vermeld die worden gemaakt om te reizen. Een reisaanvraag wordt ter beoordeling ingediend en kan worden gebruikt om onkosten te autoriseren.

Mogelijk moet u een reisaanvraag indienen voordat u kosten maakt die aan de organisatie in rekening worden gebracht. Deze vereiste is van toepassing, ongeacht of u kosten in rekening brengt op een bedrijfscreditcard, contant geld uitgeeft dat u van een contant voorschot hebt ontvangen of contante uitgaven doet die door de organisatie worden vergoed.

Reisaanvragen en beleid kunnen worden gebruikt om de uitgaven van de organisatie te beheren. Als uw organisatie bijvoorbeeld werkt aan een project met vaste prijs waarvoor reizen nodig is, moeten de reiskosten van de teamleden van het project passen binnen het projectbudget. Door te eisen dat reiskosten worden goedgekeurd voordat ze worden gemaakt, kan de organisatie ervoor zorgen dat het project binnen het budget blijft.

## <a name="configuration"></a>Configuratie 

Reisaanvragen kunnen worden geconfigureerd als "verplicht" door het inschakelen van de parameter "Pre-autorisatie van reizen is verplicht" in Parameters voor onkostenbeheer. 

## <a name="create-and-submit-a-travel-requisition"></a>Een reisaanvraag maken en indienen

1. Ga naar **Mijn onkosten: reisaanvraag** en selecteer **Nieuwe reisaanvraag**.
2. Voer een doel en bestemming in voor de aanvraag.
3. Voer in het veld **Reisbeschrijving** eventuele aanvullende informatie in. 
4. Maak voor elk van de verwachte uitgaven, zoals vlucht, maaltijden of autoverhuur, een onkostenpost. Vermeld de geschatte datum, het geschatte bedrag en de valuta voor elke uitgave. 
5. Als u klaar bent met het toevoegen van de verwachte uitgaven, selecteert u **Opslaan**.
6. Als u klaar bent om de reisaanvraag in te dienen, selecteert u **Workflow** > **Verzenden**.

U kunt uw goedgekeurde reisaanvragen bekijken onder **Mijn onkosten: reisaanvraag**. 

## <a name="view-available-travel-requisitions"></a>Beschikbare reisaanvragen weergeven

U kunt al uw reisaanvragen bekijken onder **Mijn onkosten: reisaanvragen**.

## <a name="approve-travel-requisitions"></a>Reisaanvragen goedkeuren

Selecteer de reisaanvraag die u wilt goedkeuren en selecteer vervolgens **Workflow** > **Goedkeuren**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Een onkostendeclaratie indienen met uw goedgekeurde reisaanvraag

1. Maak een nieuwe onkostendeclaratie en selecteer in de kop van de onkostendeclaratie en in de lijst met goedgekeurde reisaanvragen **Toewijzen aan reisaanvraag**.
2. Het veld **Bedrag reisaanvraag** wordt automatisch bijgewerkt in de kop van de onkostendeclaratie.
3. Voeg alle kosten toe die voor de reis zijn gemaakt. Als het veld **Pre-geautoriseerd** is ingeschakeld, worden het afgestemde bedrag en het geautoriseerde bedrag voor de specifieke onkostencategorie bijgewerkt.

> [!NOTE]
> Wanneer u een onkostendeclaratie toewijst aan een goedgekeurde reisaanvraag, kan het transactiebedrag niet hoger zijn dan het geautoriseerde bedrag. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]