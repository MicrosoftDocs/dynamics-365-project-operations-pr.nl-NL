---
title: Leveranciersfactuurregels voor onkostencategorieën
description: In dit onderwerp wordt uitgelegd hoe u leveranciersfactuurregels registreert voor onkostencategorieën.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579530"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Leveranciersfactuurregels voor onkostencategorieën

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een leveranciersfactuur in Microsoft Dynamics 365 Project Operations kan leveranciersfactuurregels hebben voor onkostencategorieën. Projectmanagers kunnen leveranciersfactuurregels voor onkostencategorieën gebruiken om de kosten van services die worden ingekocht als onkostencategorieën vast te leggen.

Leveranciersfactuurregels voor onkostencategorieën kunnen al dan niet verwijzen naar een subcontractregel voor onkostencategorieën. Als een leveranciersfactuurregel voor onkostencategorieën naar een subcontract verwijst, kunnen projectmanagers de onkosten die door de leveranciersfactuurregel worden gefactureerd, vergelijken en verifiëren met onkosten die zijn geregistreerd voor deze onkostencategorieën en zijn goedgekeurd door projectmanagers voor het project.

In de volgende tabel vindt u informatie over de velden op leveranciersfactuurregels voor onkostencategorieën.

| Veld | Beschrijving | Functionele impact |
| --- | --- | --- |
| Name | De naam van de leveranciersfactuurregel om te helpen bij de identificatie. | Deze naam wordt weergegeven als de eerste kolom in alle zoekopdrachten die zijn gebaseerd op leveranciersfactuurregels. |
| Beschrijving | Een korte beschrijving van de services die door de leverancier worden gefactureerd op de leveranciersfactuurregel. | Geen |
| Subcontract | Het subcontract waarop de services oorspronkelijk zijn besteld. | Wanneer een subcontract wordt geselecteerd voor de leveranciersfactuur, nemen alle regels op de leveranciersfactuur die selectie over. Een leveranciersfactuur mag geen leveranciersfactuurregels hebben die verwijzen naar verschillende subcontracten. |
| Subcontractregel | De subcontractregel waarop de services zijn besteld. De lijst met uitbestedingsregels die kan worden geselecteerd is beperkt tot de regels op het geselecteerde subcontract. | Wanneer een subcontractregel wordt geselecteerd op een leveranciersfactuurregel voor onkostencategorieën, worden standaardwaarden voor de velden **Project**, **Taak** en **Transactiecategorie** ingevoerd vanuit de corresponderende velden op de subcontractregel. Als de geselecteerde subcontractregel waarden heeft in de velden **Project**, **Projecttaak** en **Transactiecategorie**, kunnen de waarden van de corresponderende velden op de leveranciersfactuurregel niet verschillen van die waarden. |
| Transactiedatum | De datum waarop de werkelijke kosten van de leveranciersfactuurregel op het project worden vastgelegd. |Geen |
| Transactieklasse | Selecteer **Onkosten** om een leveranciersfactuur voor een onkostencategorie vast te leggen. | De waarde **Onkosten** geeft aan dat de leveranciersfactuurregel wordt gebruikt om het factuurbedrag vast te leggen voor services die zijn ingekocht als onkostencategorieën. |
| Project | De naam van het project waarvoor de services die worden gefactureerd, zijn gebruikt. | Dit veld is vereist en kan niet leeg blijven. |
| Taak | De naam van de projecttaak waarvoor de services die worden gefactureerd, zijn gebruikt. Dit veld is alleen beschikbaar als een project is geselecteerd. Selectie van een projecttaak is optioneel. | Als dit veld leeg wordt gelaten, kan de projectmanager de leveranciersfactuurregel afstemmen met onkosten die zijn vastgelegd voor elke taak van het project. Als de leveranciersfactuurregel niet verwijst naar een subcontractregel en dit veld leeg wordt gelaten, wordt de werkelijke kostprijs die door de leveranciersfactuurregel wordt gemaakt, niet aan niet-gefactureerde werkelijke verkoopwaarden gekoppeld. In dit geval kunnen, als facturering op basis van taken is ingesteld, de kosten mogelijk niet aan de eindklant worden gefactureerd. |
| Transactiecategorie | De transactiecategorie die wordt gefactureerd. Voor de geselecteerde transactiecategorie moet een bijbehorende onkostencategorie worden gemaakt. | De combinatie van waarden voor **Transactiecategorie** en **Eenheid** wordt gebruikt als standaard of berekende waarde voor het veld **Eenheidsprijs** op de leveranciersfactuurregel. |
| Aantal | Voer de hoeveelheid in die door de leverancier wordt gefactureerd op de factuurregel. |Geen|
| Eenhedengroep | Er wordt een standaardwaarde ingevoerd op basis van de eenhedengroep van de geselecteerde transactiecategorie. | Geen |
| Eenheid | De standaardwaarde is de basiseenheid van de geselecteerde eenhedengroep. U kunt deze waarde wijzigen om een willekeurige eenheid van de eenhedengroep te kopen. | De combinatie van waarden voor **Transactiecategorie** en **Eenheid** wordt gebruikt als standaard of berekende waarde voor het veld **Eenheidsprijs** op de leveranciersfactuurregel. |
| Eenheidsprijs | De standaardeenheidsprijs gebruikt de combinatie van waarden voor **Transactiecategorie** en **Eenheid** uit de projectprijslijst die van toepassing is op de transactiedatum van de leveranciersfactuurregel. | Als de prijs voor de toepasselijke projectprijslijst is ingesteld in een eenheid die afwijkt van de eenheid op de leveranciersfactuurregel, gebruikt het systeem de eenheidsconversie om de prijs per eenheid te berekenen. |
| Subtotaal | Dit is een alleen-lezen veld dat wordt berekend als *Hoeveelheid* &times; *Eenheidsprijs*, als zowel de waarde in het veld **Hoeveelheid** als de waarde in het veld **Eenheidsprijs** is ingevoerd. Als een of beide velden leeg zijn, kunt u een waarde in dit veld invoeren.| Geen |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in. | Geen |
| Totaalbedrag | Het totale bedrag van de leveranciersfactuurregel, inclusief belastingen. Dit veld wordt berekend als *Subtotaal* + *Omzetbelasting*. | Geen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
