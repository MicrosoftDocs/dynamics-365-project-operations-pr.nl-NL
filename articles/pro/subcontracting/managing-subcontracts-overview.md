---
title: Onderaannemingsbeheer in Project Operations
description: Dit onderwerp biedt een overzicht van begin tot einde van het onderaannemingsbeheerproces dat doorgaans plaatsvindt in projectgebaseerde organisaties.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 993edfd064279a970d7c42d5fcefd794e949a931
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323590"
---
# <a name="subcontract-management-in-project-operations"></a>Onderaannemingsbeheer in Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Dit onderwerp biedt een overzicht van begin tot einde van het onderaannemingsbeheerproces dat plaatsvindt in projectgebaseerde organisaties. Bij uitbesteding voor services volgt doorgaans de bedrijfsprocesstroom die wordt weergegeven in het volgende diagram.

![Processtroom voor onderaanneming](../media/SubcontractingProcessFlow.png)

Hier volgt een stapsgewijze beschrijving van het onderaannemingsproces.

1. De projectmanager stelt een subcontract op met een leverancier. Standaard worden de prijslijsten die aan de leveranciersrecord zijn gekoppeld, gebruikt voor het subcontract. De leveranciersaccount heeft het relatietype **Verkoper** of **Leverancier**.
2. De projectmanager kan alle aankopen specificeren als regelitems in het subcontract. Subcontractregels kunnen voor tijd, onkosten of producten zijn. De transactieklasse van de subcontractregel bepaalt waarvoor de regel dient.
3. De accountmanager van de leverancier en de projectmanager kunnen het subcontract herhalen. De prijzen kunnen worden aangepast in de inkoopprijslijsten die aan het subcontract zijn gekoppeld.
4. Op dit punt of verderop in het proces koppelt de accountmanager van de leverancier, als de subcontractregel voor tijd is, leverancierscontactpersonen aan elke subcontractregel. Deze koppeling biedt informatie aan de projectmanager die aan het subcontract werkt. Wanneer een leverancierscontactpersoon aan een subcontractregel is gekoppeld, maakt het systeem automatisch een boekbare resource van de contactpersoon aan, als er nog geen boekbare resource bestaat.
5. De factureringsmethode op elke subcontractregel kan **Vaste prijs** of **Tijd en materiaal** zijn. Voor subcontractregels met een vaste prijs wordt een op mijlpalen gebaseerd factuurschema ingesteld.
6.  Als het subcontract is opgesteld en de onderhandeling is voltooid, wordt het bevestigd. Bevestigde subcontracten kunnen niet worden bewerkt, maar als er wijzigingen optreden, kan een subcontract worden 'heropend voor bewerkingen', waardoor de status van **Bevestigd** weer wordt ingesteld op **Concept** en de onderhandelingen opnieuw kunnen worden geopend. 
7.  Bij het aanmaken van een generiek teamlid voor een project, kan het teamlid worden gekoppeld aan een subcontractregel. Dit geeft de noodzaak aan om het generieke teamlid te bemannen met onderaannemerscapaciteit.
8.  Benoemde teamleden kunnen rechtstreeks in een project worden gemaakt of worden gemaakt door ze te boeken met behulp van de functies voor resourceplanningen. Als een benoemd projectteamlid een contractmedewerker is, kan deze worden gekoppeld aan een subcontractregel. Hierdoor wordt de beschikbare capaciteit op een subcontractregel minder.
9.  Onderaannemersresources kunnen tijd, onkosten en materiaalgebruik voor projecten en projecttaken registreren en vervolgens ter goedkeuring indienen. Dit is vergelijkbaar voor werknemers. Bij het registreren van tijd kan een contractmedewerker een specifiek subcontract en specifieke subcontractregel selecteren.
10. Na goedkeuring worden voor tijd die is goedgekeurd door subcontracten de werkelijke projectkosten geregistreerd op basis van de aankoopprijs van de contractmedewerker of de rol die deze in het project heeft vervuld.
11. Leveranciersfacturen en leveranciersfactuurregelitems kunnen in het systeem worden vastgelegd voor het werk dat wordt uitgevoerd door leveranciersresources of producten die door de leverancier zijn geleverd. Leveranciersfactuurregels moeten specifiek zijn voor een project en voor een transactieklasse van tijd, onkosten, product/materiaal, mijlpaal of vergoeding. Leveranciersfactuurregels kunnen ook verwijzen naar een subcontractregel.
12. Het systeem koppelt automatisch alle werkelijke kosten die overeenkomen met de subcontractregel en het project aan de leveranciersfactuur. Dit vergemakkelijkt een drievoudig vergelijkings- en verificatieproces.
13. De projectmanager kan vervolgens de automatisch afgestemde werkelijke projectkosten bekijken, andere werkelijke projectkosten verwijderen of toevoegen en het verificatieproces voltooien.
14. Als u het verificatieproces op alle regels voltooit, wordt de leveranciersfactuur gemarkeerd als **Gereed voor betaling**. In dit stadium kunnen de leveranciersfactuur en -regels worden overgedragen naar een boekhoudings- of crediteurensysteem om de betaling aan de leverancier te verwerken. Eerder vastgelegde projectkosten worden teruggeboekt en werkelijke kosten van de leveranciersfactuurregel worden vastgelegd voor het project.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Op hoeveelheden en op werk gebaseerde subcontractregels

Een subcontractregel kan hoeveelheids- of werkgebaseerd zijn. 

Wanneer een subcontractregel **hoeveelheidsgebaseerd** is, kan de hoeveelheid die op de subcontractregel wordt ingekocht voor tijd, onkosten of materiaal voor elk project worden gebruikt.

Als een subcontractregel **werkgebaseerd** is, wordt de subcontractregel toegewezen aan een pakket aan werk dat wordt vertegenwoordigd door een knooppunt in het projectplan. De waarde van de subcontractregel is de som van alle componenten die nodig zijn om dat werk te leveren. Deze worden gemodelleerd als subcontractregeldetails en kunnen een verzameling tijd, onkosten of materialen zijn. Voor een op werk gebaseerde subcontractregel is de subcontractregel ook toegewezen aan één project.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

