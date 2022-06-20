---
title: Leveranciersfactuurregels voor producten
description: In dit artikel wordt uitgelegd hoe u leveranciersfactuurregels voor producten registreert en de verschillende velden gebruikt om productaankopen van leveranciers vast te leggen.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 206dd36a1a1e7141678da27d76a99561ac89044b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931370"
---
# <a name="vendor-invoice-lines-for-products"></a>Leveranciersfactuurregels voor producten

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een leveranciersfactuur in Microsoft Dynamics 365 Project Operations kan leveranciersfactuurregels voor producten hebben (ook wel materialen genoemd). Projectmanagers kunnen leveranciersfactuurregels voor producten gebruiken om de kosten vast te leggen van producten die voor projecten zijn ingekocht.

Leveranciersfactuurregels voor producten kunnen al dan niet verwijzen naar een subcontractregel voor materialen. Als een leveranciersfactuurregel voor producten naar een subcontract verwijst, kunnen projectmanagers de producten die door de leveranciersfactuurregel worden gefactureerd, vergelijken en verifiëren met het gebruik van producten die zijn geregistreerd en goedgekeurd door projectmanagers.

In de volgende tabel vindt u informatie over de velden op leveranciersfactuurregels voor producten.

| Veld | Beschrijving | Functionele impact |
| --- | --- | --- |
| Name | De naam van de leveranciersfactuurregel om te helpen bij de identificatie. | Deze naam wordt weergegeven als de eerste kolom in alle zoekopdrachten die zijn gebaseerd op leveranciersfactuurregels. |
| Beschrijving | Een korte beschrijving van de producten die door de leverancier worden gefactureerd op de leveranciersfactuurregel. | Geen |
| Subcontract | Het subcontract waarop de producten oorspronkelijk zijn besteld. | Wanneer een subcontract wordt geselecteerd voor de leveranciersfactuur, nemen alle regels op de leveranciersfactuur die selectie over. Een leveranciersfactuur mag geen leveranciersfactuurregels hebben die verwijzen naar verschillende subcontracten. |
| Subcontractregel | De subcontractregel waarop de producten zijn besteld. De lijst met uitbestedingsregels die kan worden geselecteerd is beperkt tot de regels op het geselecteerde subcontract. | Wanneer een subcontractregel wordt geselecteerd op een leveranciersfactuurregel voor producten, worden standaardwaarden voor de velden **Project**, **Taak** en **Product** ingevoerd vanuit de corresponderende velden op de subcontractregel. Als de geselecteerde subcontractregel waarden heeft in de velden **Project**, **Taak** en **Product**, kunnen de waarden van de corresponderende velden op de leveranciersfactuurregel niet verschillen van die waarden. |
| Transactiedatum | De datum waarop de werkelijke kosten van de leveranciersfactuurregel op het project worden vastgelegd. | Geen|
| Transactieklasse | Wanneer producten worden gefactureerd, moet dit veld worden ingesteld op **Materiaal**. | De waarde **Materiaal** geeft aan dat de leveranciersfactuurregel wordt gebruikt om het factuurbedrag vast te leggen voor materialen die zijn ingekocht. |
| Project | De naam van het project waarvoor de producten die worden gefactureerd, zijn gebruikt. | Dit veld is vereist en kan niet leeg blijven. |
| Opdracht | De naam van de projecttaak waarvoor de producten die worden gefactureerd, zijn gebruikt. Dit veld is alleen beschikbaar als een project is geselecteerd. Selectie van een projecttaak is optioneel. | Als dit veld leeg wordt gelaten, kan de projectmanager de leveranciersfactuurregel afstemmen op het aangeschafte product dat wordt gebruikt voor elke taak van het project. Als de leveranciersfactuurregel niet verwijst naar een subcontractregel en dit veld leeg wordt gelaten, wordt de werkelijke kostprijs die door de leveranciersfactuurregel wordt gemaakt, niet aan niet-gefactureerde werkelijke verkoopwaarden gekoppeld. In dit geval kunnen, als facturering op basis van taken is ingesteld, de kosten niet aan de eindklant worden gefactureerd. |
| Product selecteren | Selecteer of het product dat wordt gefactureerde een bestaand product in de catalogus is of een toe te voegen product. | De standaardwaarde wordt ingevoerd vanaf de subcontractregel wanneer een subcontractregel wordt geselecteerd. |
| Product | Selecteer het product in de catalogus. Als het product een toe te voegen product is, voert u de naam van het product in. | Dit veld wordt gebruikt om standaard inkoopprijzen voor bestaande producten in te voeren. |
| Aantal | Voer de hoeveelheid materiaal in die door de leverancier wordt gefactureerd op deze factuurregel. | Geen |
| Eenhedengroep | Selecteer de eenhedengroep van de eenheid waarin de hoeveelheid die wordt gefactureerd wordt uitgedrukt. | Geen |
| Eenheid | De standaardwaarde is de basiseenheid van de geselecteerde eenhedengroep. U kunt deze waarde wijzigen om te betalen in een willekeurige eenheid van de geselecteerde eenhedengroep. | De combinatie van waarden voor **Product** en **Eenheid** wordt gebruikt als standaard of berekende waarde voor het veld **Eenheidsprijs** op de leveranciersfactuurregel. |
| Eenheidsprijs | De standaardeenheidsprijs gebruikt de combinatie van waarden voor **Product** en **Eenheid** uit de projectprijslijst die van toepassing is op de transactiedatum van de leveranciersfactuurregel. | Geen |
| Subtotaal | Dit is een alleen-lezen veld dat wordt berekend als *Hoeveelheid* &times; *Eenheidsprijs*, als zowel de waarde in het veld **Hoeveelheid** als de waarde in het veld **Eenheidsprijs** is ingevoerd. Als een of beide velden leeg zijn, kunt u een waarde in dit veld invoeren. | Geen |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in. | Geen |
| Totaalbedrag | Het totale bedrag van de leveranciersfactuurregel, inclusief belastingen. Dit veld wordt berekend als *Subtotaal* + *Omzetbelasting*. | Geen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
