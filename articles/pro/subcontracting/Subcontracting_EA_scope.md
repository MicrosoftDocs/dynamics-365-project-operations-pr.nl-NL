---
title: Onderaanneming in versie voor vroege toegang oktober 2021
description: Dit onderwerp biedt een overzicht van de mogelijkheden voor onderaanneming in Project Operations die deel uitmaken van de release voor vroege toegang van oktober 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383689"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Onderaanneming in versie voor vroege toegang oktober 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp biedt een overzicht van de mogelijkheden voor onderaanneming in Dynamics 365 Project Operations die deel uitmaken van de release voor vroege toegang van oktober 2021. Deze functieset is niet klaar voor productie- of live-omgevingen, dus deze functies blijven beschikbaar in de versie voor vroege toegang totdat de volledige functieset wordt vrijgegeven. We raden u ten zeerste aan om de functieset voor onderaanneming niet te gebruiken voor live productiescenario's totdat de preview-banner is verwijderd. 

De volgende lijst biedt een overzicht van wat momenteel beschikbaar is in de versie voor vroege toegang van oktober 2021:

1. De projectmanager stelt een subcontract op met een leverancier. Standaard worden de prijslijsten die aan de leveranciersrecord zijn gekoppeld, gebruikt voor het subcontract. De leveranciersaccount heeft het relatietype **Verkoper** of **Leverancier**.

2. De projectmanager kan alle aankopen specificeren als regelitems in het subcontract. Subcontractregels kunnen voor tijd, onkosten of producten zijn. De transactieklasse van de subcontractregel bepaalt waarvoor de regel dient.

3. De accountmanager van de leverancier en de projectmanager kunnen het subcontract herhalen. De prijzen kunnen worden aangepast in de inkoopprijslijsten die aan het subcontract zijn gekoppeld.

4. Op dit punt of verderop in het proces koppelt de accountmanager van de leverancier, als de subcontractregel voor tijd is, leverancierscontactpersonen aan elke subcontractregel. Deze koppeling biedt informatie aan de projectmanager die aan het subcontract werkt. Wanneer een leverancierscontactpersoon aan een subcontractregel is gekoppeld, maakt het systeem automatisch een boekbare resource van de contactpersoon aan, als er nog geen boekbare resource bestaat.

5. De factureringsmethode op elke subcontractregel kan **Vaste prijs** of **Tijd en materiaal** zijn. Voor subcontractregels met een vaste prijs wordt een op mijlpalen gebaseerd factuurschema ingesteld.

De resterende stappen in de bedrijfsprocesstroom voor onderaanneming die in Overzicht worden beschreven, zijn momenteel niet beschikbaar. Zodra er nieuwe functionaliteit wordt toegevoegd, wordt dit onderwerp bijgewerkt. 

In de volgende afbeelding wordt de versie voor vroege toegang van Onderaanneming weergegeven in contrast met het end-to-end bedrijfsproces.

![Processtroom voor onderaanneming](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Op hoeveelheden en op werk gebaseerde subcontractregels in versie voor vroege toegang
In de versie van oktober 2021 worden alleen op hoeveelheid gebaseerde subcontractregels ondersteund. Dit betekent dat een subcontractregel kan worden gebruikt om tijd, onkosten of materialen van een leverancier in te kopen, maar niet een heel pakket. Dit betekent ook dat de hoeveelheid die wordt ingekocht (tijdseenheden, onkosten of hoeveelheid materialen) op een subcontractregel voor elk project in het systeem kan worden gebruikt.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
