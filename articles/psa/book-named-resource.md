---
title: Benoemde resources boeken op basis van resourcevereisten
description: Dit onderwerp bevat informatie over het boeken van benoemde resources voor een algemene resourcevereiste.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: e929a5fb4c307d3b64d0f7f70203fe20bc6dd4f99e89e039fae0ce8276c69c52
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000480"
---
# <a name="book-named-resources-from-resource-requirements"></a>Benoemde resources boeken op basis van resourcevereisten

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

U een kunt benoemde resource boeken om een algemene resource met een resourcevereiste te vervangen.

1. Klik in Project Service Automation (PSA) op de pagina **Projecten** op het tabblad **Team**.
2. Selecteer de algemene resource met een resourcevereiste in de lijst en klik vervolgens op **Boeken**. Of open de resourcevereiste en klik op **Boeken**.


![Een algemeen teamlid boeken.](media/RM-how-to-14.png)


3. Selecteer op de pagina **Planningsassistent** een benoemde resource die u wilt boeken naar uw projectteam en klik vervolgens op **Boeken**.

![Een algemeen teamlid boeken via de planningsassistent.](media/RM-how-to-15.png)

Wanneer de boeking is voltooid door een benoemde resource, wordt de algemene resource vervangen door de benoemde resource.

![Benoemd teamlid dat een algemeen teamlid vervangt.](media/RM-how-to-16.png)

De toewijzingen in de planning worden ook bijgewerkt met de benoemde resource.

![Benoemd teamlid dat is toegewezen aan projecttaken.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Een algemene resource vervullen met meerdere benoemde resources
Het voldoen aan een vereiste voor een algemene resource met meerdere benoemde resources is vergelijkbaar met het toewijzen van een één benoemde resource. Er is bijvoorbeeld een taak met een duur van vijf dagen en 120 uur werk. Deze taak kan niet worden voltooid door één resource met een normale 40-urige werkweek. 

![Een taak van 120 uur werk in vijf dagen.](media/RM-how-to-21.png)

De vereiste heeft betrekking op 120 uur aan robotica-engineering gedurende vijf dagen, wat neerkomt op 24 uur per dag.

![Vereiste per dag.](media/RM-how-to-22.png)

Dit is een voorbeeld van wanneer er meerdere benoemde resources nodig zijn om te voldoen aan een algemene resourceaanvraag. U moet meerdere resources boeken om aan de vereiste te voldoen.

![Meerdere resources boeken om aan de vereiste te voldoen.](media/RM-how-to-23.png)

Het belangrijkste verschil in dit scenario is dat de algemene resource in het team blijft dat is toegewezen aan de taak terwijl de geboekte benoemde resourceteamleden niet worden toegewezen als onderdeel van de positie. De projectmanager kan het werk naar behoefte toewijzen aan de benoemde resources. De weergave **Afstemming** biedt een projectmanager overzicht van de boekingen voor meerdere resources naar taaktoewijzingen. Dit gebeurt niet automatisch omdat in complexere scenario's dan het bovenstaande voorbeeld, bijvoorbeeld waar de vereiste bestaat uit een bundel taken, moet worden aangenomen wat de intentie van de projectmanager is voor het toewijzen. Omdat het systeem de intentie niet begrijpt, kunnen de veronderstellingen waarschijnlijk anders zijn dan bedoeld en zal er een onjuist of onvoorspelbaar resultaat optreden. Het voorspelbare resultaat is dat de algemene resource toegewezen blijft totdat de projectmanager opzettelijk toewijzingen maakt, st met behulp van de weergave **Afstemming**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]