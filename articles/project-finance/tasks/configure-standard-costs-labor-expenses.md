---
title: Standaardkosten voor arbeid en onkosten configureren
description: In dit onderwerp wordt uitgelegd hoe u standaardkosten voor arbeid en onkosten voor een project instelt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750846"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Standaardkosten voor arbeid en onkosten configureren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd hoe u standaardkosten voor arbeid en onkosten voor een project instelt. Deze taak maakt gebruik van de USSI-gegevensset.

1. Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Kostprijs (uur)**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Ingangsdatum** een datum in.
4. Voer een getal in het veld **Kostprijs** in. U kunt een standaardkostprijs instellen voor de projectcategorie of u kunt een kostprijs instellen op personeelsnummer, projectnummer, categorie, datum of een combinatie hiervan. De kostprijs die wordt gehanteerd is de kostprijs met het hoogste detailniveau.  
5. Selecteer **Opslaan**.
6. Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Verkoopprijs (uur)**.
7. Selecteer **Nieuw**.
8. Voer in het veld **Ingangsdatum** een datum in.
9. Selecteer een optie in het veld **Geldig voor**.
10. Voer een getal in het veld **Prijzen** in. U kunt een standaardverkoopprijs instellen voor uurtransacties of voor een projectcategorie. U kunt ook verkoopprijzen instellen op werknemersnummer, projectnummer, categorie, transactiedatum of een combinatie hiervan. De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer een transactie invoert in het urenjournaal, is de verkoopprijs met het hoogste detailniveau. Als bijvoorbeeld zowel een algemene verkoopprijs als een werknemerspecifieke verkoopprijs zijn ingesteld, wordt de werknemerspecifieke verkoopprijs gebruikt.  
11. Selecteer **Opslaan**.
12. Sluit de pagina.
13. Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Kostprijs (onkosten)**.
14. Selecteer **Nieuw**.
15. Voer in het veld **Ingangsdatum** een datum in.
16. Voer een getal in het veld **Kostprijs** in. Er kunnen meerdere velden worden ingevuld, maar dit is het minimum dat nodig is om de record op te slaan.  
17. Selecteer **Opslaan**.
18. Ga in het navigatievenster naar **Modules > Projectmanagement en financiële administratie > Instellingen > Prijzen > Verkoopprijs (onkosten)**.
19. Selecteer **Nieuw**.
20. Voer in het veld **Ingangsdatum** een datum in.
21. Selecteer een optie in het veld **Geldig voor**.
22. Voer een getal in het veld **Prijzen** in. De werkelijke verkoopprijs, die wordt toegepast wanneer een werknemer transacties invoert in een onkostenjournaal, is de verkoopprijs met het hoogste detailniveau. Als bijvoorbeeld zowel een algemene als een werknemerspecifieke verkoopprijs zijn ingesteld, wordt de werknemerspecifieke verkoopprijs gebruikt.  
23. Selecteer **Opslaan**.

