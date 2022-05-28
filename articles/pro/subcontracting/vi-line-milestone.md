---
title: Leveranciersfactuurregels voor mijlpalen
description: In dit onderwerp wordt uitgelegd hoe u leveranciersfactuurregels maakt voor mijlpalen in een subcontract.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590616"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Leveranciersfactuurregels voor mijlpalen

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Een leveranciersfactuur in Microsoft Dynamics 365 Project Operations kan leveranciersfactuurregels hebben voor mijlpalen die zijn gedefinieerd op een subcontractregel. Projectmanagers kunnen leveranciersfactuurregels voor mijlpalen gebruiken om de kosten van ingekochte services vast te leggen als op mijlpalen gebaseerde kosten die zijn gemaakt voor services of producten die voor het project zijn ingekocht.

Leveranciersfactuurregels voor mijlpalen moeten altijd verwijzen naar een subcontractregel met Vaste prijs als factureringsmethode. Als een leveranciersfactuurregel voor mijlpalen naar een subcontractregel verwijst, kunnen projectmanagers de onderliggende kosten van tijd, onkosten of materiaal die naar die subcontractregel verwijzen afstemmen en verifiëren met de mijlpaal die wordt gefactureerd door de leverancier.

In de volgende tabel vindt u informatie over de velden op leveranciersfactuurregels voor mijlpalen.

| Veld | Beschrijving | Functionele impact |
| --- | --- | --- |
| Name | De naam van de leveranciersfactuurregel om te helpen bij de identificatie. | Deze naam wordt weergegeven als de eerste kolom in alle zoekopdrachten die zijn gebaseerd op leveranciersfactuurregels. |
| Beschrijving | Een korte beschrijving van de services die door de leverancier worden gefactureerd op de leveranciersfactuurregel. | Geen |
| Subcontract | Het subcontract waarop de services oorspronkelijk zijn besteld. | Wanneer een subcontract wordt geselecteerd voor de leveranciersfactuur, nemen alle regels op de leveranciersfactuur die selectie over. Een leveranciersfactuur mag geen leveranciersfactuurregels hebben die verwijzen naar verschillende subcontracten. |
| Subcontractregel | De subcontractregel waarop de services zijn besteld. De lijst met uitbestedingsregels die kan worden geselecteerd is beperkt tot de regels op het geselecteerde subcontract. | Wanneer een subcontractregel is geselecteerd op een leveranciersfactuurregel voor mijlpalen zijn de velden **Rol** en **Transactiecategorie** en productgerelateerde velden niet relevant en niet beschikbaar. De velden **Aantal**, **Eenheid** en **Eenheidsgroep** zijn eveneens niet relevant voor op mijlpalen gebaseerde leveranciersfactuurregels. |
| Transactiedatum | De datum waarop de werkelijke kosten van de leveranciersfactuurregel op het project worden vastgelegd. | Geen |
| Transactieklasse | Selecteer **Mijlpaal** om een leveranciersfactuur vast te leggen voor een voltooide mijlpaal die is gedefinieerd op een subcontractregel. | Geen |
| Mijlpaal | Selecteer de mijlpaal die is gedefinieerd op de gerelateerde subcontract regel die is gemarkeerd als **Gereed voor facturering**. | Mijlpalen voor subcontractregels die de status **Gereed voor facturering** hebben, kunnen worden geselecteerd op een leveranciersfactuurregel. |
| Project | De naam van het project waarvoor de services die worden gefactureerd, zijn gebruikt. | Dit veld is vereist en kan niet leeg blijven. |
| Opdracht | De naam van de projecttaak waarvoor de services die worden gefactureerd, zijn gebruikt. Dit veld is alleen beschikbaar als een project is geselecteerd. Selectie van een projecttaak is optioneel. | Als dit veld leeg wordt gelaten, kan de projectmanager de leveranciersfactuurregel afstemmen met de klasse transacties op de gerelateerde subcontractregel die is vastgelegd voor elke taak van het project. Als de leveranciersfactuurregel niet verwijst naar een subcontractregel en dit veld leeg wordt gelaten, wordt de werkelijke kostprijs die door de leveranciersfactuurregel wordt gemaakt, niet aan niet-gefactureerde werkelijke verkoopwaarden gekoppeld. In dit geval kunnen, als facturering op basis van taken is ingesteld, de kosten mogelijk niet aan de eindklant worden gefactureerd. |
| Bedrag van mijlpaal | Voer de waard in van de mijlpaal die is gedefinieerd op de subcontractregel die is gemarkeerd als Gereed voor facturering. | Geen |
| Omzetbelasting | Voer het bedrag aan omzetbelasting in. | Geen |
| Totaalbedrag | Het totale bedrag van de leveranciersfactuurregel, inclusief belastingen. Dit veld wordt berekend als *Bedrag van mijlpaal* + *Omzetbelasting*. | Geen |

> [!NOTE]
> Wanneer een leveranciersfactuurregel wordt gemaakt die verwijst naar een mijlpaal in de subcontractregel, wordt de status van de subcontractmijlpaal bijgewerkt naar **Leveranciersfactuur gemaakt**. Wanneer die leveranciersfactuur vervolgens wordt bevestigd, wordt de status van de mijlpaal van de contractregel bijgewerkt naar **Leveranciersfactuur bevestigd**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
