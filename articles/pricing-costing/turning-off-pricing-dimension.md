---
title: Een prijsdimensie uitschakelen
description: Dit onderwerp bevat informatie over het uitschakelen van prijsdimensies.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
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
ms.openlocfilehash: 986fae72c6b44b3f76281aefb81ffdaa96f71ae7
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650043"
---
# <a name="turning-off-a-pricing-dimension"></a>Een prijsdimensie uitschakelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U moet uw prijsstrategie mogelijk om de paar jaar controleren en bijwerken. Alle updates die u aanbrengt, vereisen mogelijk dat u een bestaande prijsdimensie uitschakelt en een nieuwe maakt. U hebt bijvoorbeeld eerder een prijs per **Rol** afgesproken, maar nu hebt u besloten om de prijs te baseren op **Werkervaring.** U moet hiervoor mogelijk **Rol** als prijsdimensie uitschakelen en **Werkervaring** als een nieuwe prijsdimensie maken. 

Het uitschakelen van een prijsdimensie, ongeacht of deze standaard of aangepast is, kan worden gedaan door de velden **Van toepassing op kosten** en **Van toepassing op verkoop** van de prijsdimensie in te stellen op **Nee**.

Als u dit echter doet, krijgt u mogelijk de foutbericht: **De prijsdimensie kan niet worden bijgewerkt of verwijderd als er gekoppelde prijsrecords zijn.**

![Fout in bedrijfsproces mogelijk bij het uitschakelen van een prijsdimensie](media/Business-Process-Error.png)

Dit foutbericht geeft aan dat er prijsrecords zijn die eerder zijn ingesteld voor de dimensie die wordt uitgeschakeld. Alle records met **Rolprijs** en **Opslag voor rolprijs** die naar een dimensie verwijzen, moeten worden verwijderd voordat de toepasbaarheid van de dimensie kan worden ingesteld op **Nee**. Deze regel is zowel van toepassing op de standaard prijsdimensies als eventuele aangepaste prijsdimensies die u hebt gemaakt. De reden voor deze validatie is dat elke **Rolprijs** record een unieke combinatie van dimensies moet hebben. Op een prijslijst met de naam **Amerikaanse kostentarieven2018**, hebt u bijvoorbeeld de volgende rijen voor **Rolprijs**. 

| Standaardtitel         | Organisatie-eenheid    |Eenheid   |Prijs  |Valuta  |
| -----------------------|-------------|-------|-------|----------|
| Systeemtechnicus|Contoso US|Hour| 100|USD|
| Hoofdsysteemtechnicus|Contoso US|Hour| 150| USD|


Wanneer u **Standaardtitel** als prijsdimensie uitschakelt en de prijsengine naar een prijs zoekt, wordt alleen de waarde voor **Organisatie-eenheid** uit de invoercontext gebruikt. Als **Organisatie-eenheid** van de invoercontext “Contoso US” is, is het resultaat niet-deterministisch omdat beide rijen overeenkomen. Om dit scenario bij het maken van **Rolprijs** records te voorkomen, controleert het systeem of de combinatie van dimensies uniek is. Als de dimensie is uitgeschakeld nadat de **Rolprijs** records zijn gemaakt, kan deze beperking worden overtreden. Daarom moet u voordat u een dimensie uitschakelt, alle rijen voor **Rolprijs** en **Opslag voor rolprijs** verwijderen waarvoor die dimensiewaarde is ingevuld.


[!INCLUDE[footer-include](../includes/footer-banner.md)]