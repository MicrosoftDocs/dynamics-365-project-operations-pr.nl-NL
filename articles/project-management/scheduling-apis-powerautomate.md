---
title: API's voor projectplanning gebruiken met Power Automate
description: Dit artikel biedt een voorbeeldstroom die gebruikmaakt van de API's (Application Programming Interfaces) voor projectplanning.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404395"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>API's voor projectplanning gebruiken met Power Automate

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Dit artikel bevat een beschrijving van een voorbeeldstroom die laat zien hoe u een compleet projectplan kunt maken met behulp van Microsoft Power Automate, hoe u een bewerkingsset maakt en hoe u een entiteit bijwerkt. Het voorbeeld laat zien hoe u een project, projectteamlid, bewerkingssets, projecttaken en resourcetoewijzingen maakt. In dit artikel wordt ook uitgelegd hoe u een entiteit bijwerkt en een bewerkingsset uitvoert.

Het volgende is een volledige lijst van de stappen die zijn gedocumenteerd in de voorbeeldstroom in dit artikel:

1. [Een PowerApps-trigger maken](#1)
2. [Een project maken](#2)
3. [Een variabele initialiseren voor het teamlid](#3)
4. [Een algemeen teamlid maken](#4)
5. [Een bewerkingsset maken](#5)
6. [Een projectbucket maken](#6)
7. [Een variabele initialiseren voor de koppelingsstatus](#7)
8. [Een variabele initialiseren voor het aantal taken](#8)
9. [Een variabele initialiseren voor de projecttaak-id](#9)
10. [Doen tot](#10)
11. [Een projecttaak instellen](#11)
12. [Een projecttaak maken](#12)
13. [Een resourcetoewijzing maken](#13)
14. [Een variabele verlagen](#14)
15. [Naam van een projecttaak wijzigen](#15)
16. [Een bewerkingsset uitvoeren](#16)

## <a name="assumptions"></a>Aannames

In dit artikel wordt ervan uitgegaan dat u over basiskennis van het Dataverse-platform, cloudstromen en de Application Programming Interface (API) voor projectplanning beschikt. Zie de sectie [Verwijzingen](#references) verderop in dit artikel voor meer informatie.

## <a name="create-a-flow"></a>Stroom maken

### <a name="select-an-environment"></a>Selecteer een omgeving

U kunt de Power Automate-stroom maken in uw omgeving.

1. Ga naar <https://flow.microsoft.com> en gebruik uw beheerdersreferenties om zich aan te melden.
2. Selecteer **Omgevingen** in de rechterbovenhoek.
3. Selecteer in de lijst de omgeving waarin Dynamics 365 Project Operations is geinstalleerd.

### <a name="create-a-solution"></a>Een oplossing maken

Volg deze stappen om een [oplossingsbewuste stroom](/power-automate/overview-solution-flows) te maken. Door een oplossingsbewuste stroom te maken, kunt u de stroom gemakkelijker exporteren voor later gebruik.

1. Selecteer in het navigatiedeelvenster de optie **Oplossingen**.
2. Selecteer **Nieuwe oplossing** op de pagina **Oplossingen**.
3. Stel in het dialoogvenster **Nieuwe oplossing** de vereiste velden in en selecteer vervolgens **Maken**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Stap 1: Een PowerApps-trigger maken

1. Selecteer op de pagina **Oplossingen** de oplossing die u hebt gemaakt en selecteer vervolgens **Nieuw**.
2. Selecteer in het linkerdeelvenster de optie **Cloudstromen** \> **Automatisering** \> **Cloudstroom** \> **Direct**.
3. Voer in het veld **Stroomnaam** de waarde **API-demostroom plannen** in.
4. Selecteer in de lijst **Kiezen hoe deze stroom wordt geactiveerd** de optie **Power Apps**. Wanneer u een Power Apps-trigger maakt, bepaalt u als auteur de logica. Laat in dit artikel de invoerparameters leeg voor testdoeleinden.
5. Selecteer **Maken**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Stap 2: Een project maken

Voer deze stappen uit om een voorbeeldproject te maken.

1. Selecteer in de stroom die u hebt gemaakt de optie **Nieuwe stap**.

    ![Een nieuwe stap toevoegen.](media/newstep.png)

2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.

    ![Een bewerking selecteren.](media/chooseactiontab.png)

3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.

![Een stap een andere naam geven.](media/renamestep.png)

4. Geef de stap **Project maken** een nieuwe naam.
5. Selecteer in het veld **Actienaam** de waarde **msdyn\_CreateProjectV1**.
6. Selecteer in het veld **msdyn\_subject** de waarde **Dynamische inhoud toevoegen**.
7. Voer op het tabblad **Expressie** in het functieveld de waarde **Projectnaam - utcNow()** in.
8. Selecteer **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Stap 3: Een variabele initialiseren voor het teamlid

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele initialiseren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Init teamlid**.
5. Voer in het veld **Naam** de tekst **TeamMemberAction** in.
6. Selecteer in het veld **Type** de optie **Tekenreeks**.
7. Voer **msdyn\_CreateTeamMemberV1** in het veld **Waarde** in.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Stap 4: Een algemeen teamlid maken

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. De naam van de stap **Teamlid maken** wijzigen.
5. Selecteer in het veld **Actienaam** de waarde **TeamMemberAction** in het dialoogvenster **Dynamische inhoud**.
6. Voer in het veld **Actieparameters** de volgende parameterinformatie in.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Hier volgt een uitleg van de parameters:

    - **\@\@odata.type**: de naam van de entiteit. Voer bijvoorbeeld **"Microsoft.Dynamics.CRM.msdyn\_projectteam"** in.
    - **msdyn\_projectteamid**: de primaire sleutel van de projectteam-id. De waarde is een GUID-expressie (Globally Unique Identifier).   De id wordt gegenereerd op het tabblad Expressie.

    - **msdyn\_project\@odata.bind**: de project-id van het project dat eigenaar is. De waarde is dynamische inhoud die afkomstig is van de respons op de stap "Project maken". Zorg ervoor dat u het volledige pad invoert en voeg dynamische inhoud toe tussen de haakjes. Aanhalingstekens zijn verplicht. Voer bijvoorbeeld **"/msdyn\_projects(VOEG DYNAMISCHE INHOUD TOE)"** in.
    - **msdyn\_name**: de naam van het teamlid. Voer bijvoorbeeld **"ScheduleAPIDemoTM1"** in.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Stap 5: Een bewerkingsset maken

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Bewerkingsset maken**.
5. Selecteer in het veld **Actienaam** de aangepaste Dataverse-actie **msdyn\_CreateOperationSetV1**.
6. Voer **ScheduleAPIDemoOperationSet** in het veld **Beschrijving** in.
7. Voer in het veld **Project** de waarde **/msdyn\_projects(** in.
8. Selecteer in het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateProjectV1Response ProjectId**.
9. Voer in het veld **Project** de waarde **)** in.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Stap 6: Een projectbucket maken

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **nieuwe rij toevoegen** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Geef de stap **Bucket maken** een nieuwe naam.
5. Selecteer in het veld **Tabelnaam** de waarde **Projectbuckets**.
6. Voer in het veld **Naam** de tekst **ScheduleAPIDemoBucket1** in.
7. Selecteer in het veld **Project** van het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateProjectV1Response ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Stap 7: Een variabele initialiseren voor de koppelingsstatus

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele initialiseren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Init linkstatus**.
5. Voer in het veld **Naam** de tekst **linkstatus** in.
6. Selecteer in het veld **Type** de optie **Geheel getal**.
7. Voer in het veld **Waarde** de waarde **192350000** in.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Stap 8: Een variabele initialiseren voor het aantal taken

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele initialiseren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Init Aantal taken**.
5. Voer in het veld **Naam** de tekst **aantal taken** in.
6. Selecteer in het veld **Type** de optie **Geheel getal**.
7. Voer in het veld **Waarde** de waarde **5** in.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Stap 9: Een variabele initialiseren voor de projecttaak-id

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele initialiseren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Init ProjectTaskID**.
5. Voer in het veld **Naam** de tekst **aantal taken** in.
6. Selecteer in het veld **Type** de optie **Tekenreeks**.
7. Voer in het veld **Waarde** de waarde **guid()** in de opbouwfunctie voor expressies in.

## <a name="step-10-do-until"></a><a id="10"></a>Stap 10: Doen tot

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **doen tot** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Stel de eerste waarde in de voorwaardelijke instructie in op de variabele **aantal taken** in het dialoogvenster **Dynamische inhoud**.
4. Stel de voorwaarde in op **kleiner dan of gelijk aan**.
5. Stel de tweede waarde in de voorwaardelijke instructie in op **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Stap 11: Een projecttaak instellen

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele instellen** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de nieuwe stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Projecttaak instellen**.
5. Selecteer **msdyn\_projecttaskid** in het veld **Naam**.
6. Voer in het veld **Waarde** de waarde **guid()** in de opbouwfunctie voor expressies in.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Stap 12: Een projecttaak maken

Volg deze stappen om een projecttaak te maken met een unieke id die hoort bij het huidige project en de projectbucket die u hebt gemaakt.

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Projecttaak maken**.
5. Selecteer in het veld **Actienaam** de waarde **msdyn\_PssCreateV1**.
6. Voer in het veld **Entiteit** de volgende parameterinformatie in.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Hier volgt een uitleg van de parameters:

    - **\@\@odata.type**: de naam van de entiteit. Voer bijvoorbeeld **"Microsoft.Dynamics.CRM.msdyn\_projecttask"** in.
    - **msdyn\_projecttaskid**: de unieke id van de taak. De waarde moet worden ingesteld op een dynamische variabele vanuit **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind**: de project-id van het project dat eigenaar is. De waarde is dynamische inhoud die afkomstig is van de respons op de stap "Project maken". Zorg ervoor dat u het volledige pad invoert en voeg dynamische inhoud toe tussen de haakjes. Aanhalingstekens zijn verplicht. Voer bijvoorbeeld **"/msdyn\_projects(VOEG DYNAMISCHE INHOUD TOE)"** in.
    - **msdyn\_subject**: willekeurige taaknaam.
    - **msdyn\_projectbucket\@odata.bind**: de projectbucket die de taken bevat. De waarde is dynamische inhoud die afkomstig is van de respons op de stap "Bucket maken". Zorg ervoor dat u het volledige pad invoert en voeg dynamische inhoud toe tussen de haakjes. Aanhalingstekens zijn verplicht. Voer bijvoorbeeld **"/msdyn\_projectbuckets(VOEG DYNAMISCHE INHOUD TOE)"** in.
    - **msdyn\_start**: dynamische inhoud voor de begindatum. Morgen wordt bijvoorbeeld weergegeven als **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart**: de geplande begindatum. Morgen wordt bijvoorbeeld weergegeven als **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend**: de geplande einddatum. Selecteer een datum in de toekomst. Geef bijvoorbeeld **"addDays(utcNow(), 5)"** op.
    - **msdyn\_LinkStatus**: de koppelingsstatus. Voer bijvoorbeeld **"192350000"** in.

7. Selecteer in het veld **OperationSetId** van het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateOperationSetV1Response**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Stap 13: Een resourcetoewijzing maken

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Geef de stap **Toewijzing maken** een nieuwe naam.
5. Selecteer in het veld **Actienaam** de waarde **msdyn\_PssCreateV1**.
6. Voer in het veld **Entiteit** de volgende parameterinformatie in.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Selecteer in het veld **OperationSetId** van het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateOperationSetV1Response**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Stap 14: Een variabele verlagen

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **variabele verlagen** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in het veld **Naam** de tekst **aantal taken**.
4. Voer in het veld **Waarde** de waarde **1** in.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Stap 15: De naam van een projecttaak wijzigen

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Naam van projecttaak wijzigen**.
5. Selecteer in het veld **Actienaam** de waarde **msdyn\_PssUpdateV1**.
6. Voer in het veld **Entiteit** de volgende parameterinformatie in.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Selecteer in het veld **OperationSetId** van het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateOperationSetV1Response**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Stap 16: Een bewerkingsset uitvoeren

1. Selecteer in de stroom de optie **Nieuwe stap**.
2. Voer in het dialoogvenster **Een bewerking kiezen** de waarde **niet-gebonden actie uitvoeren** in. Selecteer daarna op het tabblad **Acties** de bewerking in de lijst met resultaten.
3. Selecteer in de stap het beletselteken (**...**) en selecteer vervolgens **Naam wijzigen**.
4. Wijzig de naam van de stap **Bewerkingsset uitvoeren**.
5. Selecteer in het veld **Actienaam** de waarde **msdyn\_ExecuteOperationSetV1**.
6. Selecteer in het veld **OperationSetId** van het dialoogvenster **Dynamische inhoud** de waarde **msdyn\_CreateOperationSetV1Response OperationSetId**.

## <a name="references"></a>Verwijzingen

- [Overzicht van het integreren van stromen met Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [API's voor projectplanning gebruiken om bewerkingen uit te voeren met planningsentiteiten](schedule-api-preview.md)
- [Overzicht van de cloudstromen - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Overzicht van oplossingsbewuste stromen - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
