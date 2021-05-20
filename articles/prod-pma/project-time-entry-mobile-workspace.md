---
title: Mobiele werkruimte Projecttijdinvoer
description: Dit onderwerp bevat informatie over de mobiele werkruimte Projecttijdinvoer. Met deze werkruimte kunnen gebruikers een project invoeren en tijd besparen door hun mobiele apparaat te gebruiken.
author: Yowelle
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 78bb696a39a6ec126d7de01f170edbd07677a314
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950168"
---
# <a name="project-time-entry-mobile-workspace"></a>Mobiele werkruimte Projecttijdinvoer

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over de mobiele werkruimte **Projecttijdinvoer**. Met deze werkruimte kunnen gebruikers een project invoeren en tijd besparen door hun mobiele apparaat te gebruiken.

Deze mobiele werkruimte is bedoeld om te worden gebruikt met de mobiele app Dynamics 365 Unified Ops. 

## <a name="overview"></a>Samenzicht
Als onderdeel van hun dagelijkse werk zijn projectresources vaak ter plaatse of onderweg. Met de mobiele werkruimte **Projecttijdinvoer** kunnen gebruikers hun factureerbare of niet-factureerbare tijd voor een project invoeren op het mobiele apparaat van hun keuze. Daarom kunnen projectresources altijd en overal tijdregistraties uitvoeren. Ze kunnen ook tijdvermeldingen bekijken die al zijn vastgelegd. 

In de mobiele werkruimte **Projecttijdinvoer** kunnen gebruikers de volgende taken uitvoeren:

-   Voor een geselecteerde datum het aantal uren invoeren dat u aan een specifieke taak hebt besteed.
-   Op projectnaam of klant zoeken om het project te vinden waarvoor u tijd wilt invoeren.
-   De categorie en activiteit opgeven voor de tijd die u hebt besteed.
-   De tijd registreren als factureerbaar of niet-factureerbaar voor het project.
-   Optioneel externe of interne opmerkingen invoeren.

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die is geïmplementeerd voor uw organisatie.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Vereisten als u Dynamics 365 Finance gebruikt
Als Finance is geïmplementeerd voor uw organisatie, moet het systeembeheerder de mobiele werkruimte **Projecttijdinvoer** publiceren. Zie [Een mobiele werkruimte publiceren](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace) voor instructies.

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Vereisten als u versie 1611 met platformupdate 3 of hoger gebruikt
Als versie 1611 met platformupdate 3 of hoger is geïmplementeerd voor uw organisatie, moet de systeembeheerder aan de volgende vereisten voldoen. 

<table>
<thead>
<tr class="header">
<th>Vereisten</th>
<th>Rol</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>Implementeer KB 4018050.</td>
<td>Systeembeheerder</td>
<td>KB 4018050 is een X++-update of metagegevenshotfix die de mobiele werkruimte <strong>Projecttijdinvoer</strong> bevat. Als de systeembeheerder KB 4018050 wil implementeren, moeten deze stappen worden uitgevoerd.
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Download de metagegevenshotfix vanuit Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installeer de metagegevenshotfix</a>.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Maak een implementeerbaar pakket</a> dat de modellen <strong>ApplicationSuite</strong> en <strong>projectMobile</strong> bevat en upload vervolgens het implementeerbare pakket naar LCS.</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a>.</li>

</ol></td>
</tr>
<tr class="even">
<td>Publiceer de mobiele werkruimte <strong>Projecttijdinvoer</strong>.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Een mobiele werkruimte publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

De mobiele app Finance and Operations downloaden en installeren:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1.  Start de app op uw mobiele apparaat.
2.  Voer uw URL voor Dynamics 365 in.
3.  Wanneer u zich voor het eerst aanmeldt, wordt u om uw gebruikersnaam en wachtwoord gevraagd. Voer uw referenties in.
4.  Nadat u zich hebt aangemeld, worden de beschikbare werkruimten voor uw bedrijf weergegeven. Merk op dat als uw systeembeheerder later een nieuwe werkruimte publiceert, u de lijst met mobiele werkruimten moet vernieuwen.

[![Slepen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>Tijd invoeren met de mobiele werkruimte Projecttijdinvoer
1.  Selecteer op uw mobiele apparaat de werkruimte **Projecttijdinvoer**.
2.  Selecteer **Tijdinvoer**. De agendadatums voor de huidige week worden weergegeven.
3.  Selecteer voor een geselecteerde datum **Acties** &gt; **Nieuwe invoer**.
4.  Voer het aantal vast te leggen uren in.
5.  Selecteer het project voor de tijdinvoer. Een lijst toont de projecten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.
6.  Als uw project niet in de lijst staat, selecteert u **Zoeken**. Zoek op naam of schakel over naar zoeken op projectnaam of klant.
7.  Selecteer een categorie. Een lijst toont de categorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.
8.  Als uw categorie niet in de lijst staat, selecteert u **Zoeken**. Zoek op categorie of schakel over naar zoeken op categorienaam.
9.  Selecteer een activiteit. Een lijst toont de activiteiten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 items geladen, maar een ontwikkelaar kan dit aantal wijzigen. Zie [Mobiel platform](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/mobile-app-home-page) voor meer informatie.
10. Als uw activiteit niet in de lijst staat, selecteert u **Zoeken**. Zoek op activiteitnummer of schakel over naar zoeken op doel.

11. Selecteer de regeleigenschap.
12. Optioneel: voer eventuele externe en interne opmerkingen in.
13. Selecteer **Gereed**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]