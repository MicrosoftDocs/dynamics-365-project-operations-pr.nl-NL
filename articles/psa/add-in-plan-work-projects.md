---
title: Werk plannen in Microsoft Project met de invoegtoepassing Project Service
description: Dit onderwerp bevat informatie over het gebruik van de Microsoft project-invoegtoepassing voor Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145937"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Werk plannen in Microsoft Project met de invoegtoepassing Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

Met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] is het eenvoudiger om uw projectplanning op te zetten, inclusief de schattingen. U kunt het werk definiëren zodat kosten, arbeid, en verkopenwaarde helder zijn wanneer het uiteindelijke voorstel wordt ingediend.  

U kunt de [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] installeren en al het planningswerk uitvoeren in de vertrouwde [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-omgeving. U kunt profiteren van de robuuste plannings- en beheersmogelijkheden van [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en vervolgens uw projectplan bijwerken in Project Service Automation.  

> [!IMPORTANT]
> - Als u de functie voor SharePoint-documentbeheer wilt gebruiken om uw [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestanden voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-projecten op te slaan, moet uw [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-beheerder documentbeheer inschakelen. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is alleen compatibel met [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>De invoegtoepassing downloaden en installeren  
 Houd uw aanmeldingsgegevens voor [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bij de hand. U hebt deze informatie nodig om vanuit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] verbinding te maken met [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  Download vanuit het Downloadcentrum de invoegtoepassing voor uw ondersteunde versie van Project Service, [v2.X](https://go.microsoft.com/fwlink/?linkid=828268) of [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Selecteer de downloadkoppeling.  

3.  Als de download klaar is, selecteert u **Ja** om de invoegtoepassing te installeren.  

## <a name="configure-the-add-in"></a>De invoegtoepassing configureren  

1. Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en selecteer het tabblad **Project Service**.  

2. Selecteer **Verbinding maken**.  

3. Voer uw aanmeldingsgegevens in en selecteer **Aanmelden**.  

   Nu kunt u de invoegtoepassing gebruiken.  

## <a name="read-from-a-template"></a>Lezen uit een sjabloon  
 Begin uw project te plannen door een sjabloon in te lezen die u in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] hebt gemaakt en naar [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] hebt gekopieerd. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Een projectsjabloon maken (Project Service Automation)](../psa/create-project-template.md)  

1.  Klik op het tabblad **Project Service**, selecteer **Lezen** > **Projectsjabloon van Project Service Automation**.  

2.  Kies een projectsjabloon in de lijst en selecteer **Openen**.  

    > [!NOTE]
    >  Standaard zijn de taken die uit de sjabloon naar Project gekopieerd worden, ingesteld als handmatig gepland.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Rollen in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] toewijzen aan projectresources  

1.  Open een project en selecteer het **Taak**-lint.  

2. Selecteer het menu **Gantt-diagram** en kies **Resourceblad**.  

3. Selecteer op het Resourceblad het vervolgkeuzemenu **Project Service resourcerol** en kies een Project Service Automation-rol.  

## <a name="staff-your-project-with-resources"></a>Resources toewijzen aan uw project  

1.  Selecteer op het tabblad Project Service een rij en selecteer **Resources zoeken**.  

2.  Selecteer in het scherm **Resource boeken** de resource die u wilt gebruiken voor het project.  

3.  Selecteer **Boeken** en selecteer vervolgens **OK**.  

## <a name="publish-your-project"></a>Uw project publiceren  
Wanneer de projectplanning is voltooid, moet u het project importeren in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en het publiceren.  

Het project wordt geïmporteerd in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. De processen voor het genereren van prijzen en teams worden toegepast. Open het project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] en controleer of het team, de projectschattingen en de structuur voor werkspecificatie zijn gegenereerd. In de onderstaande tabel kunt u zien waar u de resultaten kunt vinden.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gantt-diagram**   | Importbewerkingen in het [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] scherm **Structuur voor werkspecificatie**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resourceblad** |   Importbewerkingen in het [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] scherm **Projectteamleden**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Gebruik gebruiken**    |    Importbewerkingen in het scherm [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Projectschattingen**.     |

**Uw project importeren en publiceren**  
1. Ga op het tabblad **Project Service** naar **Publiceren** > **Nieuw Project Service Automation-project**.  

2. Voer in het dialoogvenster **Publiceren naar een nieuw project in Project Service** de **Projectnaam** in en selecteer de **Klant**.  

3. Selecteer eventueel de optie **Projectplan aan Project Service Automation koppelen** om het planningsbestand uit Project aan Project Service Automation te koppelen.  

4. Selecteer **Publiceren**.  

   Wanneer het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wordt gekoppeld, wordt het Project-bestand het hooftbestand en wordt de structuur voor werkspecificatie in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ingesteld op alleen-lezen.  Als u wijzigingen wilt aanbrengen in het projectplan, moet u dat doen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en deze als updates publiceren naar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Een geïmporteerd project bewerken  
 U hebt twee manieren om wijzigingen door te voeren in een projectplan dat is geïmporteerd in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]:  

- Open het hoofdbestand in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en bewerk het.  

- Het bestand ontkoppelen en het rechtstreeks in Project Service bewerken. Projecten die zijn geüpload vanuit [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] zijn standaard vergrendeld en kunnen alleen in Project worden bewerkt. Als u het bestand wilt bewerken in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], moet u het eerst ontkoppelen.  

### <a name="edit-in-pn_microsoft_project"></a>Bewerken in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Ga vanuit het hoofdmenu naar **Project Service** > **Projecten**.  

2. Open in de lijst met projecten het project dat u hebt gemaakt in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecteer in het lint **Openen in MS Project**. Hiermee wordt het gekoppelde hoofdbestand geopend in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Een bestand ontkoppelen en het in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service bewerken  

1. Ga vanuit het hoofdmenu naar **Project Service** > **Projecten**.  

2. Open in de lijst met projecten het project dat u hebt gemaakt in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Selecteer in het lint **Koppeling met MS Project verwijderen**.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Een Project-bestand uploaden naar SharePoint of Office Groepen  
 U kunt uw Project-bestand uploaden naar SharePoint. U vindt het vervolgens bij de gekoppelde documenten voor uw [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.  Uw beheerder moet het SharePoint-documentbeheer configureren en inschakelen voor de entiteit Project. 

 U kunt uw Project-bestand ook uploaden naar [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], als Office Groepen is geconfigureerd.

### <a name="upload-a-file-for-sharepoint"></a>Een bestand uploaden voor SharePoint  

1. Ga vanuit het hoofdmenu naar **Project Service** > **Uploaden**.  

2. Selecteer **Aan projectdocumenten voor Project Service Automation**.  

3. Selecteer in het dialoogvenster **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] inschakelen** **Ja** of **Nee**.  

   - Als u **Ja** selecteert, kunt u in Project Service Automation **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** selecteren, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten en het Project-bestand laden vanuit de SharePoint-documentbibliotheek.  

   - Als u **Nee** selecteert, werkt de koppeling voor **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** niet.  

4. U vindt het [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestand in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] onder **Documenten** voor het specifieke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.  

### <a name="upload-a-file-for-office-groups"></a>Een bestand uploaden naar Office Groepen  

1. Ga vanuit het hoofdmenu naar **Project Service** > **Uploaden**.  

2. Selecteer **Aan projectdocumenten voor Project Service Automation**.  

3. Selecteer in het dialoogvenster **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] inschakelen** **Ja** of **Nee**.  

   - Als u **Ja** selecteert, kunt u in Project Service Automation **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** selecteren, [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] starten en het Project-bestand laden vanuit de SharePoint-documentbibliotheek.  

   - Als u **Nee** selecteert, werkt de koppeling voor **Openen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** niet.  

4. U vindt het [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]-bestand in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] onder **Documenten** voor het specifieke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-project.  

## <a name="publish--your-project-as-a-template"></a>Uw project publiceren als een sjabloon  
 U kunt uw project opslaan en opnieuw gebruiken door het op te slaan als projectsjabloon in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projectsjablonen zijn herbruikbare projectplannen in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Zie voor meer informatie [Een projectsjabloon (Project Service Automation) maken](../psa/create-project-template.md). 

1. Ga op het tabblad **Project Service** naar **Publiceren** > **Nieuw Project Service Automation-projectsjabloon**.  

2. Voer in het dialoogvenster **Publiceren naar een nieuwe Project Service-projectsjabloon** de **Naam van de projectsjabloon** in.  

3. Selecteer eventueel de optie **Projectplan aan Project Service Automation koppelen** om het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] te koppelen.  

4. Selecteer **Publiceren**.  

Wanneer het Project-bestand aan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] wordt gekoppeld, wordt het Project-bestand het hooftbestand en wordt de structuur voor werkspecificatie in de [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]-sjabloon ingesteld op alleen-lezen.  Als u wijzigingen wilt aanbrengen in het projectplan, moet u dat doen in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] en deze als updates publiceren naar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Een schema geladen met resources lezen

Bij het lezen van een project vanuit Project Service Automation, wordt de agenda van de resource niet gesynchroniseerd met de desktopclient. Als er verschillen zijn in de duur, de inspanning of het einde van de taak, komt dat waarschijnlijk doordat de resources en de desktopclient niet dezelfde kalender voor werkuursjablonen hebben die op het project zijn toegepast.


## <a name="data-synchronization"></a>Gegevenssynchronisatie
De tabellen in deze sectie bieden informatie over de synchronisatie van entiteitsgegevens tussen Project Service Automation en de Microsoft Project-desktopinvoegtoepassing.

### <a name="project-task-entity-table"></a>Entiteitstabel projecttaak
In de volgende tabel wordt beschreven hoe entiteitsgegevens voor een projecttaak worden gesynchroniseerd tussen Project Service Automation en de Microsoft Project-desktopinvoegtoepassing.

| **Entiteit** | **Veld** | **Microsoft Project met Project Service Automation** | **Project Service Automation met Microsoft Project** |
| --- | --- | --- | --- |
| Projecttaak | Vervaldatum | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Geschatte inspanning | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Id van MS Project Client | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Bovenliggende taak | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Project | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Projecttaak | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Naam van projecttaak | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Resource-eenheid (Afgeschaft in v3.0) | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Geplande duur | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Begindatum | Gesynchroniseerd | Niet gesynchroniseerd |
| Projecttaak | Id van structuur van werkspecificatie | Gesynchroniseerd | Niet gesynchroniseerd |

### <a name="team-member-entity-table"></a>Entiteitstabel teamlid
In de volgende tabel wordt beschreven hoe teamlid-entiteitsgegevens worden gesynchroniseerd tussen Project Service Automation en de Micros

| **Entiteit** | **Veld** | **Microsoft Project met Project Service Automation** | **Project Service Automation met Microsoft Project** |
| --- | --- | --- | --- |
| Teamlid | Id van MS Project Client | Gesynchroniseerd | Niet gesynchroniseerd |
| Teamlid | Naam van positie | Gesynchroniseerd | Niet gesynchroniseerd |
| Teamlid | project | Gesynchroniseerd | Gesynchroniseerd |
| Teamlid | Projectteam | Gesynchroniseerd | Gesynchroniseerd |
| Teamlid | Resource-eenheid | Niet gesynchroniseerd | Gesynchroniseerd |
| Teamlid | - Rol | Niet gesynchroniseerd | Gesynchroniseerd |
| Teamlid | Werkuren | Niet gesynchroniseerd | Niet gesynchroniseerd |

### <a name="resource-assignment-entity-table"></a>Entiteitstabel resourcetoewijzing
In de volgende tabel wordt beschreven hoe entiteitsgegevens voor resourcetoewijzing worden gesynchroniseerd tussen Project Service Automation en de Micros

| **Entiteit** | **Veld** | **Microsoft Project met Project Service Automation** | **Project Service Automation met Microsoft Project** |
| --- | --- | --- | --- |
| Resourcetoewijzing | Begindatum | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Uur | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Id van MS Project Client | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Gepland werk | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Project | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Projectteam | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Resourcetoewijzing | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Opdracht | Gesynchroniseerd | Niet gesynchroniseerd |
| Resourcetoewijzing | Datum tot | Gesynchroniseerd | Niet gesynchroniseerd |

### <a name="project-task-dependencies-entity-table"></a>Entiteitstabel projecttaakafhankelijkheden
In de volgende tabel wordt beschreven hoe entiteitsgegevens voor projecttaakafhankelijkheden worden gesynchroniseerd tussen Project Service Automation en de Micros

| **Entiteit** | **Veld** | **Microsoft Project met Project Service Automation** | **Project Service Automation met Microsoft Project** |
| --- | --- | --- | --- |
| Afhankelijkheden van projecttaken | Afhankelijkheid van projecttaken | Gesynchroniseerd | Niet gesynchroniseerd |
| Afhankelijkheden van projecttaken | Type koppeling | Gesynchroniseerd | Niet gesynchroniseerd |
| Afhankelijkheden van projecttaken | Voorgaande taak | Gesynchroniseerd | Niet gesynchroniseerd |
| Afhankelijkheden van projecttaken | Project | Gesynchroniseerd | Niet gesynchroniseerd |
| Afhankelijkheden van projecttaken | Volgende taak | Gesynchroniseerd | Niet gesynchroniseerd |

### <a name="additional-resources"></a>Aanvullende bronnen
 [Projectmanager-handleiding](../psa/project-manager-guide.md)
