---
title: Een prijsdimensie uitschakelen
description: Dit onderwerp laat zien hoe u prijsdimensies instelt in de Project Service-oplossing.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9f690dfdb40e962ef329f323716f3f755493805d764dbfaa2d4f9d042231cee7
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006780"
---
# <a name="turn-off-a-pricing-dimension"></a>Een prijsdimensie uitschakelen

[!include [banner](../includes/psa-now-project-operations.md)]

U moet uw prijsstrategie mogelijk om de paar jaar controleren en bijwerken. Alle updates die u aanbrengt, vereisen mogelijk dat u een bestaande prijsdimensie uitschakelt en een nieuwe maakt. U hebt bijvoorbeeld eerder een prijs per **Rol** afgesproken, maar nu hebt u besloten om de prijs te baseren op **Werkervaring.** Dit kan vereisen dat u **Rol** uitschakelt als prijsdimensie en van **Werkervaring** een nieuwe prijsdimensie maakt. 

Het uitschakelen van een prijsdimensie, ongeacht of deze standaard of aangepast is, kan worden gedaan door de velden **Van toepassing op kosten** en **Van toepassing op verkoop** van de prijsdimensie in te stellen op **Nee**.

Als u dit doet, kunt u echter de volgende foutmelding ontvangen.

![Fout in bedrijfsproces mogelijk bij het uitschakelen van een prijsdimensie.](media/Business-Process-Error.png)


Dit foutbericht geeft aan dat er prijsrecords zijn die eerder zijn ingesteld voor de dimensie die wordt uitgeschakeld. Alle records met **Rolprijs** en **Opslag voor rolprijs** die naar een dimensie verwijzen, moeten worden verwijderd voordat de toepasbaarheid van de dimensie kan worden ingesteld op **Nee**. Deze regel is zowel van toepassing op de standaard prijsdimensies als eventuele aangepaste prijsdimensies die u hebt gemaakt. De reden voor deze validatie is dat Project Service een beperking heeft dat elke **rolprijsrecord** een unieke combinatie van dimensies moet hebben. Op een prijslijst met de naam **Amerikaanse kostentarieven2018**, hebt u bijvoorbeeld de volgende rijen voor **Rolprijs**. 

| Standaardtitel         | Organisatie-eenheid    |Eenheid   |Prijs  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systeemtechnicus|Contoso VS|Uur| 100|USD|
| Hoofdsysteemtechnicus|Contoso VS|Uur| 150| USD|


Wanneer u **Standaardtitel** als prijsdimensie uitschakelt en de prijsengine van Project Service naar een prijs zoekt, wordt alleen de waarde voor **Organisatie-eenheid** uit de invoercontext gebruikt. Als **Organisatie-eenheid** van de invoercontext “Contoso US” is, is het resultaat niet-deterministisch omdat beide rijen overeenkomen. Om dit scenario te voorkomen controleert Project Service bij het maken van **Rolprijs** records of de combinatie van dimensies uniek is. Als de dimensie is uitgeschakeld nadat de **Rolprijs** records zijn gemaakt, kan deze beperking worden overtreden. Daarom moet u voordat u een dimensie uitschakelt, alle rijen voor **Rolprijs** en **Opslag voor rolprijs** verwijderen waarvoor die dimensiewaarde is ingevuld.



[!INCLUDE[footer-include](../includes/footer-banner.md)]