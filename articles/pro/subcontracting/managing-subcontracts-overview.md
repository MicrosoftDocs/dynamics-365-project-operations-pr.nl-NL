---
title: Onderaannemingsbeheer in Project Operations
description: Dit onderwerp biedt een overzicht van begin tot einde van het onderaannemingsbeheerproces in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994225"
---
# <a name="subcontract-management-in-project-operations"></a>Onderaannemingsbeheer in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Onderaanneming in Microsoft Dynamics 365 Project Operations ondersteunt de volgende bedrijfsprocesstroom.

![Processtroom voor onderaanneming](../media/SubcontractingProcessFlow.png)

Hier is een stapsgewijze beschrijving van het onderaannemingsproces.

1. De projectmanager stelt een subcontract op met een leverancier. Standaard worden de prijslijsten die aan de leveranciersrecord zijn gekoppeld, gebruikt voor het subcontract. De leveranciersaccount heeft het relatietype **Verkoper** of **Leverancier**.
2. De projectmanager kan alle aankopen specificeren als regelitems in het subcontract. Subcontractregels kunnen voor tijd, onkosten of producten zijn. De transactieklasse die voor elke subcontractregel wordt geselecteerd, bepaalt waarvoor de regel dient.
3. De accountmanager van de leverancier en de projectmanager kunnen het subcontract herhalen. De prijzen kunnen worden aangepast in de inkoopprijslijsten die aan het subcontract zijn gekoppeld.
4. Op dit punt of verderop in het proces, koppelt de accountmanager van de leverancier, als de subcontractregel voor tijd is, contactpersonen aan elke subcontractregel. Deze koppeling biedt informatie aan de projectmanager die aan het subcontract werkt. Wanneer een contactpersoon aan een subcontractregel is gekoppeld, maakt het systeem automatisch een boekbare resource van de contactpersoon aan, als er nog geen boekbare resource bestaat.
5. De factureringsmethode op elke subcontractregel kan **Vaste prijs** of **Tijd en materiaal** zijn. Voor subcontractregels met een vaste prijs kunt u een op mijlpalen gebaseerd factuurschema instellen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
