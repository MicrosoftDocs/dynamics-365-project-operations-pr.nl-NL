---
title: Integratieparameters voor Project Service Automation
description: In dit onderwerp wordt uitgelegd hoe u kunt configureren hoe standaardgegevens worden ingevoerd wanneer u Microsoft Dynamics 365 for Project Service Automation integreert met Microsoft Dynamics 365 Finance.
author: ruhercul
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 9793b680fc2be3b300689c4aded8005470f30519
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006415"
---
# <a name="project-service-automation-integration-parameters"></a>Integratieparameters voor Project Service Automation

[!include[banner](../includes/banner.md)]

Op de pagina **Integratieparameters voor Project Service Automation** kunt u configureren hoe standaardgegevens worden ingevoerd wanneer u Dynamics 365 Project Service Automation integreert met Dynamics 365 Finance. Als u projecten met succes wilt synchroniseren van Project Service Automation naar Finance, moet u de volgende velden instellen.

Als u de pagina **Integratieparameters voor Project Service Automation** wilt openen, gaat naar **Projectmanagement en financiële administratie** \> **Instelling** \> **Dynamics 365 for Project Service Automation-integratieparameters**. 

> [!NOTE]
> - Projecttaakintegratie, onkostentransactiecategorieën, uurschattingen, onkostenschattingen en functionaliteitsvergrendeling zijn beschikbaar in versie 8.0.
> - Integratie van werkelijke waarden is beschikbaar in versie 8.0.1 of hoger.


| Tabblad                    | Veld                | Beschrijving |
|------------------------|----------------------|-------------|
| Algemeen                | Standaardprojecttype | Selecteer het standaardprojecttype. Wanneer projecten worden gesynchroniseerd vanuit Project Service Automation, wordt deze waarde gebruikt als u geen standaardwaarde hebt opgegeven in de integratiesjabloon. Tijdens synchronisatie is het veld **Projecttype** van nieuwe projecten ingesteld op deze waarde. De waarde kan echter worden bijgewerkt wanneer de projectcontractregels worden gesynchroniseerd vanuit Project Service Automation. |
|                        | Tijdcategorie        | Selecteer de standaardtijdcategorie. Deze waarde wordt gebruikt wanneer uurschattingen worden gesynchroniseerd vanuit Project Service Automation. Wanneer de uurschattingen en werkelijke uren worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** met nieuwe projectuurprognoses in Finance ingesteld op deze waarde. |
|                        | Tariefcategorie         | Selecteer de standaardtariefcategorie. Deze waarde wordt gebruikt wanneer werkelijke tariefwaarden worden gesynchroniseerd vanuit Project Service Automation. Wanneer de werkelijke tariefwaarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Categorie** met nieuwe tarieftransacties in Finance ingesteld op deze waarde. |
| Standaardwaarden voor projectgroepen | Projecttype         | Klik op **Nieuw** om een rij toe te voegen waarin u het projecttype kunt selecteren waarvoor u de standaardprojectgroep wilt instellen. Een specifiek projecttype kan slechts één keer in de configuratie worden geselecteerd. |
|                        | Projectgroep        | Selecteer de standaardprojectgroep voor het geselecteerde projecttype. Wanneer nieuwe projecten worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Projectgroep** ingesteld op de standaardwaarde voor het projecttype als u geen standaardwaarde hebt opgegeven in de integratiesjabloon. |
| Standaardwaarden voor factureringstype  | Factureringstype         | Klik op **Nieuw** om een rij toe te voegen waarin u het factureringstype kunt selecteren waarvoor u de standaardregeleigenschap wilt instellen. Een specifiek factureringstype kan slechts één keer in de configuratie worden geselecteerd. |
|                        | Regeleigenschap        | Selecteer de standaardregeleigenschap voor het geselecteerde factureringstype. Wanneer nieuwe uurschattingen, nieuwe onkostenschattingen of nieuwe werkelijke waarden worden gesynchroniseerd vanuit Project Service Automation, wordt het veld **Regeleigenschap** ingesteld op de standaardwaarde voor het factureringstype. |
| Functionaliteit vergrendelen  | Niet van toepassing       | Selecteer de functionaliteit die u wilt uitschakelen in Finance voor projecten en contracten die afkomstig zijn van Project Service Automation. U kunt bijvoorbeeld de mogelijkheid uitschakelen om contracten en projecten te bewerken, structuren voor werkspecificatie te maken en urenstaten in Finance in te voeren. Aan de financiële administratie gerelateerde velden blijven ingeschakeld, zelfs als ze niet beschikbaar zijn gemaakt door de parameterinstelling. Standaard is alle functionaliteit ingeschakeld. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]