---
title: Leveranciersfactuurregels voor tijd
description: In dit artikel wordt uitgelegd hoe u leveranciersfactuurregels registreert voor tijdkosten die onderaannemers invoeren.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262006"
---
# <a name="vendor-invoice-lines-for-time"></a>Leveranciersfactuurregels voor tijd

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een leveranciersfactuur in Microsoft Dynamics 365 Project Operations kan leveranciersfactuurregels hebben voor tijd. Projectmanagers kunnen leveranciersfactuurregels voor tijd gebruiken om de kosten vast te leggen van tijd die onderaannemers aan projecten hebben besteed.

Leveranciersfactuurregels voor tijd kunnen al dan niet verwijzen naar een subcontractregel voor tijd. Als een leveranciersfactuurregel voor tijd naar een subcontract verwijst, kunnen projectmanagers de tijd die door de leveranciersfactuurregel wordt gefactureerd, vergelijken en verifiëren met tijd die is geregistreerd door onderaannemers en goedgekeurd door projectmanagers voor het project.

In de volgende tabel vindt u informatie over de velden op leveranciersfactuurregels voor tijd.

| Veld | Beschrijving | Functionele impact |
| --- | --- | --- |
| Name | De naam van de leveranciersfactuurregel om te helpen bij de identificatie. | Deze naam wordt weergegeven als de eerste kolom in alle zoekopdrachten die zijn gebaseerd op leveranciersfactuurregels. |
| Beschrijving | Een korte beschrijving van de services die door de leverancier worden gefactureerd op de leveranciersfactuurregel. | Geen |
| Subcontract | Het subcontract waarop de services oorspronkelijk zijn besteld. | Wanneer een subcontract wordt geselecteerd voor de leveranciersfactuur, nemen alle regels op de leveranciersfactuur die selectie over. Een leveranciersfactuur mag geen leveranciersfactuurregels hebben die verwijzen naar verschillende subcontracten. |
| Subcontractregel | De subcontractregel waarop de services zijn besteld. De lijst met uitbestedingsregels die kan worden geselecteerd is beperkt tot de regels op het geselecteerde subcontract. | Wanneer een subcontractregel wordt geselecteerd op een leveranciersfactuurregel voor tijd, worden standaardwaarden voor de velden **Project**, **Rol** en **Boekbare resource** ingevoerd vanuit de corresponderende velden op de subcontractregel. Als de geselecteerde subcontractregel waarden heeft in de velden **Project**, **Rol** en **Boekbaar**, kunnen de waarden van de corresponderende velden op de leveranciersfactuurregel niet verschillen van die waarden. |
| Transactiedatum | De datum waarop de werkelijke kosten van de leveranciersfactuurregel op het project worden vastgelegd. | Geen |
| Transactieklasse | De standaardwaarde is **Tijd**. | De waarde **Tijd** geeft aan dat de leveranciersfactuurregel wordt gebruikt om het factuurbedrag vast te leggen voor bestede tijd van onderaannemers. |
| Project | De naam van het project waarvoor de services die worden gefactureerd, zijn gebruikt. | Dit veld is vereist en kan niet leeg blijven. |
| Opdracht | De naam van de projecttaak waarvoor de services die worden gefactureerd, zijn gebruikt. Dit veld is alleen beschikbaar als een project is geselecteerd. Selectie van een projecttaak is optioneel. | Als dit veld leeg wordt gelaten, kan de projectmanager de leveranciersfactuurregel afstemmen met tijd die is vastgelegd door resources van onderaannemers voor elke taak van het project. Als de leveranciersfactuurregel niet verwijst naar een subcontractregel en dit veld leeg wordt gelaten, wordt de werkelijke kostprijs die door de leveranciersfactuurregel wordt gemaakt, niet aan niet-gefactureerde werkelijke verkoopwaarden gekoppeld. In dit geval kunnen, als facturering op basis van taken is ingesteld, de kosten mogelijk niet aan de eindklant worden gefactureerd. |
| - Rol | De rol van de subcontractresources waarvan de tijd wordt gefactureerd. | Dit veld specificeert de rol die wordt vervuld door de subcontractresources waarvan de tijd wordt gefactureerd op de leveranciersfactuur. |
| Boekbare resource | De naam van de onderaannemer wiens tijd wordt gefactureerd. Selectie van een boekbare resource is optioneel. | Als dit veld leeg wordt gelaten, kan de projectmanager de leveranciersfactuurregel afstemmen met tijd die is vastgelegd door een willekeurige resource die toebehoort aan de leverancier op de leveranciersfactuurregel. |
| Aantal | Voer het aantal uren in dat door de leverancier worden gefactureerd op de factuurregel. |Geen |
| Eenhedengroep | De standaardwaarde is **Eenhedengroep Tijd** en kan niet worden gewijzigd. | Geen |
| Eenheid | De standaardwaarde is de basiseenheid van uren van de eenhedengroep Tijd. U kunt deze waarde wijzigen om elke eenheid van de eenhedengroep Tijd te kopen, zoals dag of week. | De combinatie van waarden voor **Rol** en **Eenheid** wordt gebruikt als standaard of berekende waarde voor het veld **Eenheidsprijs** op de leveranciersfactuurregel. |
| Eenheidsprijs | De standaardeenheidsprijs gebruikt de combinatie van waarden voor **Rol** en **Eenheid** uit de projectprijslijst die van toepassing is op de transactiedatum van de leveranciersfactuurregel. | Als de prijs voor de toepasselijke projectprijslijst is ingesteld in een eenheid die afwijkt van de eenheid op de leveranciersfactuurregel, gebruikt het systeem de eenheidsconversie om de prijs per eenheid te berekenen. |
| Subtotaal | Dit is een alleen-lezen veld dat wordt berekend als *Hoeveelheid* &times; *Eenheidsprijs*, als zowel de waarde in het veld **Hoeveelheid** als de waarde in het veld **Eenheidsprijs** is ingevoerd. Als een of beide velden leeg zijn, kunt u een waarde in dit veld invoeren. | Geen |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in. | Geen |
| Totaalbedrag | Het totale bedrag van de leveranciersfactuurregel, inclusief belastingen. Dit veld wordt berekend als *Subtotaal* + *Omzetbelasting*. | Geen |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
