---
title: Een prijsdimensie uitschakelen
description: Dit artikel laat zien hoe u prijsdimensies instelt in de Project Service-oplossing.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 81c3cfaad8dc8d057985b509f20c3ba31de45e3b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913154"
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
| Systeemtechnicus|Contoso US|Hour| 100|USD|
| Hoofdsysteemtechnicus|Contoso US|Hour| 150| USD|


Wanneer u **Standaardtitel** als prijsdimensie uitschakelt en de prijsengine van Project Service naar een prijs zoekt, wordt alleen de waarde voor **Organisatie-eenheid** uit de invoercontext gebruikt. Als **Organisatie-eenheid** van de invoercontext “Contoso US” is, is het resultaat niet-deterministisch omdat beide rijen overeenkomen. Om dit scenario te voorkomen controleert Project Service bij het maken van **Rolprijs** records of de combinatie van dimensies uniek is. Als de dimensie is uitgeschakeld nadat de **Rolprijs** records zijn gemaakt, kan deze beperking worden overtreden. Daarom moet u voordat u een dimensie uitschakelt, alle rijen voor **Rolprijs** en **Opslag voor rolprijs** verwijderen waarvoor die dimensiewaarde is ingevuld.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
