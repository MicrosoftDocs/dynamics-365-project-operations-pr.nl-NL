---
title: Resources inplannen voor een project
description: Informatie over resources plannen voor een project in Project Service
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f3b7ea1a2b81b86bedc85b77689145ba5afb579d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583118"
---
# <a name="schedule-resources-for-a-project-project-service"></a>Resources plannen voor een project (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

U kunt de beschikbaarheid van de resource weergeven om een algemeen overzicht te krijgen van hoe uw resources worden geboekt, of u kunt de weergave met vaardigheden, team, de locatie, en andere opties filteren.  
  
Het planbord geeft de lijst met resources en hun beschikbaarheid weer. Selecteer een weergavemodus om beschikbaarheid weer te geven op **Uren**, **Dag**, **Week** of **Maand**.  
  
Voordat u het planbord gebruikt, moet u dit configureren. Zie [Configureer het planningsbord (Field Service, Project Service Automation)](/dynamics365/field-service/configure-schedule-board) voor meer informatie.
  
Als u een oudere versie gebruikt, raadpleegt u voor resourcebeschikbaarheid [De beschikbaarheid van resources weergeven](../psa/view-resource-availability.md).  

> [!IMPORTANT]
>  Als u de boekingsfunctionaliteit, geo-coding en locatieservices van het planbord wilt gebruiken, moet u de kaarten inschakelen.  
> 
> 1. Selecteer in het hoofdmenu **Resourceplanning** > **Beheer**.  
> 2. Klik op **Planningsparameters**.  
> 3. Open de record en schuif omlaag naar de sectie **Resource Scheduling Optimization**.  
> 4. Kies in het veld **Verbinden met Kaarten** de waarde **Ja**.  
> 5. Accepteer de voorwaarden en sla de record op.  
> 6. Selecteer in het hoofdmenu **Project Service** > **Planbord**. Vanaf dit punt zijn er verschillende manieren om een boekingsvereiste handmatig te plannen. Kies de methode die voor u het beste is.
  
## <a name="find-available-resources"></a>Beschikbare resources zoeken

1.  Klik in de lijst **Boekingsvereisten** met de rechtermuisknop op een ongeplande boeking en kies een van de volgende:  
  
- Kies **Beschikbaarheid zoeken - Huidige resources** om beschikbare resources te zoeken in de lijst met resources in het planbord.  
- Kies **Beschikbaarheid zoeken - Alle resources** om beschikbare resources te zoeken onder de resources in het systeem.  
   > [!NOTE]
   >  Wanneer u dit doet, tonen de filters de opties voor de geselecteerde boekingsvereisten.  
  
2. Als u een beschikbaar tijdvak ziet, klikt u met de rechtermuisknop op het tijdvak in het planbord en kiest u **Hier boeken**. U kunt ook de boekingsvereiste verslepen en in het beschikbare tijdvak neerzetten.  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a>Een resource boeken met de dagweergave en nog niet-volgeboekte personen vinden
  
1.  Selecteer **Weergavemodus** in het planbord en selecteer **Dagen**.  
  
    Dit opent een rasterweergave waarin is weergegeven hoeveel uur per dag een resource is geboekt en op welke dagen ze beschikbaar zijn.  
  
2.  Klik op de naam van de resource die u wilt boeken en selecteer vervolgens **Boeken**.  
  
3.  Klik in het dialoogvenster **Resourceboekingen (maken)**, kies het project waarvoor u de resource wilt boeken samen met de boekingsmethode en de start- en eindtijden.  
  
4.  Selecteer **Boeken** als u klaar bent.  
  
## <a name="view-to-the-schedule-board"></a>Weergeven op het planbord
  
1.  Selecteer een niet-geplande boekingsvereiste in de lijst onderaan de pagina.  
  
2.  Sleep de boekingsvereiste naar een beschikbare resource/tijdvak op het planbord.  
  
3.  Selecteer **Boeken** als u klaar bent.  
  
### <a name="additional-resources"></a>Aanvullende bronnen  
 [Resourcemanager-handleiding](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
