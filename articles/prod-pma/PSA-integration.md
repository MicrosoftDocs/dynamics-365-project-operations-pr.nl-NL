---
title: Overzicht van Project Service Automation
description: Dit artikel bevat informatie over de oplossing voor integratie van Dynamics 365 Project Service Automation en Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 96fdb31b7b1d4f33cb565cf902039f72a3f90fd7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929576"
---
# <a name="project-service-automation-overview"></a>Overzicht van Project Service Automation

[!include[banner](../includes/banner.md)]


De oplossing voor integratie van Project Service Automation met Finance gebruikt de functie Gegevensintegratie om gegevens te synchroniseren tussen exemplaren van Dynamics 365 Finance en Dynamics 365 Project Service Automation via Common Data Service. De integratiesjablonen die beschikbaar zijn met de functie Gegevensintegratie maken de stroom van projecten, projectcontracten, projectcontractregels en mijlpalen voor projectcontractregels, projecttaken, onkostentransactiecategorieën, uurschattingen en onkostenschattingen vanuit Project Service Automation naar Finance mogelijk.

> [!NOTE]
> - Als u versie 7.3.0 gebruikt, moet u KB 4074835 installeren. U kunt dan projecten met een vaste prijs integreren.
> - Als u versie 7.3.0 gebruikt en u transactiekosten overbrengt vanuit Project Service Automation, moet u KB 4345320 installeren om deze kosten in de projectfactuur op te nemen.
> - Als u versie 8.0 gebruikt, kunt u projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling gebruiken.
> - Als u versie 8.0.1 of hoger gebruikt, kunt u werkelijke waarden synchroniseren.

Voordat u Project Service Automation Finance kunt integreren, moet u de integratieparameters van Project Service Automation configureren. Zie [Integratieparameters voor Project Service Automation](PSA-parameters.md) voor meer informatie.

Deze integratieoplossing maakt directe synchronisatie mogelijk in de volgende scenario's:

- Onderhoud projectcontracten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Maak projecten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Onderhoud projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Onderhoud mijlpalen voor projectcontractregels in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Onderhoud projecttaken in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Onderhoud onkostentransactiecategorieën in Finance en synchroniseer ze rechtstreeks vanuit Finance naar Project Service Automation.
- Maak schattingen van projecturen in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Maak schattingen van projectonkosten in Project Service Automation en synchroniseer ze rechtstreeks vanuit Project Service Automation naar Finance.
- Maak werkelijke waarden voor projecttijd, onkosten en tarieven in Project Service Automation en maak projecttransacties in het integratiejournaal van Project Service Automation, zodat ze in Finance kunnen worden geboekt.

## <a name="data-synchronization"></a>Gegevenssynchronisatie

De volgende afbeelding laat zien hoe de gegevens worden gesynchroniseerd als onderdeel van de integratie tussen Project Service Automation en Finance.

> [!NOTE]
> Niet alle sjablonen zijn momenteel beschikbaar. Sjablonen worden vrijgegeven zodra ze zijn voltooid.

[![Integratie van Project Service Automation met Finance.](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systeemvereisten voor Finance

Als u de integratieoplossing Project Service Automation naar Finance wilt gebruiken, moet u Enterprise-editie 7.3 met platformupdate 12 of hoger installeren.

## <a name="system-requirements-for-project-service-automation"></a>Systeemvereisten voor Project Service Automation

Als u de integratieoplossing Project Service Automation naar Finance wilt gebruiken, moet u de volgende onderdelen installeren:

- Dynamics 365 Project Service Automation versie 9.0.0.0 of later
- Oplossing Van prospect tot contanten voor Dynamics 365 Sales, versie 1.14.0.0 (v14) of hoger
- Project Service Automation naar Finance-oplossing voor Dynamics 365 Project Service Automation versie 1.0.0.0 of hoger

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installeer de integratieoplossing Project Service Automation naar Finance in uw Project Service Automation-exemplaar

Download de integratieoplossing Project Service Automation naar Finance vanuit het [Microsoft-downloadcentrum](https://www.microsoft.com/download/details.aspx?id=57016) en volg de instructies die bij de oplossing zijn geleverd.


[!INCLUDE[footer-include](../includes/footer-banner.md)]