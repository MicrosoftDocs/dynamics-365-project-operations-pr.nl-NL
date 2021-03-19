---
title: Een nieuwe omgeving inrichten
description: Dit onderwerp bevat informatie over het inrichten van een nieuwe Project Operations-omgeving.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 50e623d3716c9dd03ce34ec293ba57b5d966d39e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276882"
---
# <a name="provision-a-new-environment"></a>Een nieuwe omgeving inrichten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat informatie over het inrichten van een nieuwe Dynamics 365 Project Operations-omgeving voor scenario's op basis van resources/niet-voorradige artikelen.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>De geautomatiseerde inrichting van Project Operations in een LCS-project inschakelen

Gebruik de volgende stappen om de geautomatiseerde inrichtingsstroom van Project Operations voor uw LCS-project in te schakelen.

1. Ga naar [LCS](https://lcs.dynamics.com/v2) en selecteer de tegel **Beheer previewfunctie**.
2. Selecteer **Project Operations** in de lijst **Previewfunctie** en selecteer vervolgens **Previewfunctie ingeschakeld** om Project Operations in te schakelen.

> [!NOTE]
> Deze stap wordt slechts één keer per LCS-project uitgevoerd.

## <a name="provision-a-project-operations-environment"></a>Een Project Operations-omgeving inrichten

1. Open een nieuwe implementatie van een Dynamics 365 Finance [demo-omgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) of [sandbox-/productieomgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Volg de wizard **Omgeving inrichten**. 

> [!IMPORTANT]
> Zorg ervoor dat de geselecteerde applicatieversie 10.0.13 of hoger is.

3. Voor het inrichten van Project Operations selecteert u **Common Data Service** onder **Geavanceerde instellingen**. 
4. Schakel **Common Data Service-instelling** in door **Ja** te selecteren en voer vervolgens informatie in de vereiste velden in:

  - Meetcriterium
  - Regio
  - Taal
  - Valuta
 
5. Selecteer in het veld **Common Data Service-sjabloon** de optie **Project Operations** 

6. Selecteer het omgevingstype voor uw implementatie. Met een proefversie op basis van een abonnement kunt u een CDS-omgeving gedurende 30 dagen implementeren. 

![Instellingen voor implementatie](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Selecteer **Akkoord** om de servicevoorwaarden te erkennen en selecteer vervolgens **Gereed** om terug te keren naar de implementatie-instellingen.

![Toestemming voor implementatie](./media/2DeploymentConsent.png)

7. Optioneel - Pas demogegevens toe op de omgeving. Ga naar **Geavanceerde instellingen**, selecteer **SQL-databaseconfiguratie aanpassen** en stel **Een gegevensset opgeven voor de toepassingsdatabase** in op **Demo**.

8. Vul de overige verplichte velden in de wizard in en bevestig de implementatie. De tijd die nodig is om de omgeving in te richten, is afhankelijk van het omgevingstype. Het inrichten kan tot zes uur duren.

  Nadat de implementatie met succes is voltooid, wordt de omgeving weergegeven als **Geïmplementeerd**.

9. Selecteer om te bevestigen dat de omgeving met succes is geïmplementeerd **Aanmelden** en meld u aan bij de omgeving om te bevestigen.

![Details van -omgevingen](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Updates toepassen op de Finance-omgeving

Project Operations vereist een Finance-omgeving met toepassingsversie **10.0.13 (10.0.569.20009)** of hoger.

Mogelijk moet u kwaliteitsupdates toepassen op uw Finance-omgeving om deze versie te ontvangen.

1. Selecteer in LCS op de pagina **Omgevingsdetails** in de sectie **Beschikbare updates** de optie **Updates weergeven**.

![Updates weergeven](./media/5ViewUpdates.png)

2. Selecteer **Pakket opslaan** op de pagina **Binaire updates**.

![Pakket opslaan](./media/6SavePackage.png)

3. Klik op **Alles selecteren** en selecteer **Pakket opslaan**.

![Updates evalueren en opslaan](./media/7ReviewAndSaveUpdates.png)

4. Voer een naam en een beschrijving van het pakket in en selecteer **Opslaan**. Afhankelijk van de internetverbinding kan dit proces enige tijd duren.

![Pakket uploaden naar Activabibliotheek](./media/8UploadPackageToAssetsLibrary.png)

5. Selecteer **Gereed** nadat het pakket is opgeslagen in de Activabibliotheek in uw LCS-project.

Het opslaan en valideren van het pakket kan ongeveer 15 minuten duren.

6. Als u de update wilt toepassen, navigeert u naar de pagina **Omgevingsdetails** in LCS en selecteert u **Onderhouden** > **Updates toepassen**.

![Omgevingen onderhouden](./media/9MaintainEnvironment.png)

7. Selecteer in de lijst met updates het pakket dat u hebt gemaakt en selecteer **Toepassen**.

![Updates toepassen](./media/10ApplyUpdates.png)

Het onderhouden van de omgeving kan enige tijd duren. Nadat het is voltooid, keert de omgeving terug naar de geïmplementeerde staat.

![Omgeving geïmplementeerd](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Een verbinding voor twee keer wegschrijven tot stand brengen 

1. Ga in uw LCS-project naar de pagina **Omgevingsdetails**.
2. Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps**.
3. Selecteer nadat de koppeling is voltooid opnieuw **Koppelen met CDS voor apps**. U wordt doorgestuurd naar Twee keer wegschrijven in Finance.

![Koppeling naar CDS](./media/12LinktoCDS.png)

4. Selecteer **Oplossing toepassen** om toegang te krijgen tot de entiteiten die in de integratie worden toegewezen.

![Oplossingen toepassen](./media/13ApplySolutions.png)

5. Selecteer beide oplossingen, **Dynamics 365 Finance and Operations-entiteitstoewijzing voor twee keer wegschrijven** en **Dynamics 365 Project Operations-entiteitstoewijzingen voor twee keer wegschrijven** en selecteer vervolgens **Toepassen**.

![Oplossingen bevestigen](./media/14ConfirmSolutions.png)

Nadat de oplossingen zijn toegepast, worden de entiteiten voor twee keer wegschrijven op de omgeving toegepast.

![Oplossingen worden toegepast](./media/15ApplyingSolutions.png)

Nadat de entiteiten zijn toegepast, worden alle beschikbare toewijzingen in de omgeving weergegeven.

![Toewijzingen voor twee keer wegschrijven](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Vernieuw de gegevensentiteiten na de update

1. Ga in Finance naar de werkruimte **Gegevensbeheer**.

![Werkruimte Gegevensbeheer](./media/16DataManagement.png)

2. Selecteer de tegel **Raamwerkparameters**.

![Raamwerkparameters](./media/17FrameworkParameters.png)

3. Selecteer op de pagina **Entiteitsinstellingen** de optie **Entiteitslijst vernieuwen**.

![Entiteitslijst vernieuwen](./media/18RefreshEntityList.png)

Het vernieuwen duurt ongeveer 20 minuten. U ontvangt een melding wanneer dit is voltooid.

![Bevestiging vernieuwen](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Beveiligingsinstellingen bijwerken in Project Operations in Dataverse

1. Ga naar Project Operations in uw Dataverse-omgeving. 
2. Ga naar **Instellingen** > **Beveiliging** > **Beveiligingsrollen**. 
3. Selecteer op de pagina **Beveiligingsrollen** in de lijst met rollen **Twee keer wegschrijven app-gebruiker** en selecteer het tabblad **Aangepaste entiteiten**.  
4. Controleer of de rol de machtigingen **Lezen** en **Toevoegen aan** heeft voor:
      
      - **Type valutawisselkoers**
      - **Rekeningschema**
      - **Fiscale kalender**
      - **Grootboek**

5. Ga nadat de beveiligingsrol is bijgewerkt naar **Instellingen** > **Beveiliging** > **Teams** en selecteer het standaardteam in de teamweergave **Lokale bedrijfseigenaar**.
6. Selecteer **Rollen beheren** en controleer of de beveiligingsbevoegdheid **twee keer wegschrijven app-gebruiker** is toegepast op dit team.

## <a name="run-project-operations-dual-write-maps"></a>Toewijzingen voor twee keer wegschrijven uitvoeren in Project Operations

1. Ga in uw LCS-project naar de pagina **Omgevingsdetails**.
2. Selecteer onder **Informatie over Common Data Service-omgeving** **Koppelen met CDS voor apps.** Nadat u de koppeling hebt geselecteerd, wordt u doorgestuurd naar de lijst met entiteiten in de toewijzingen.
3. Start de toewijzingen volgens de beschrijving in de volgende tabel. Zorg ervoor dat u de volgorde volgt zoals vermeld.

| **Entiteitstoewijzing** | **Entiteit vernieuwen** | **Initiële synchronisatie** | **Model voor initiële synchronisatie** | **Vereisten voor uitvoeren** | **Vereisten voor initiële synchronisatie** |
| --- | --- | --- | --- | --- | --- |
| **Rollen voor projectresources voor alle bedrijven (bookableresourcecategories)** | Geen | Ja | Common Data Service | Geen | n.v.t. |
| **Rechtspersonen (cdm\_companies)** | Geen | Ja | Finance and Operations-apps | Geen | n.v.t. |
| **Grootboek (msdyn_ledgers)** | Geen | Ja | Finance and Operations-apps | Ja | Ja, Finance and Operations-apps |
| **Werkelijke waarden voor integratie van Project Operations (msdyn\_actuals)** | Geen | No | n.v.t. | Ja | No |
| **Projectcontractregels (salesorderdetails)** | No | No | n.v.t. | No | No |
| **Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections)** | No | No | n.v.t. | No | n.v.t. |
| **Mijlpalen voor de contractregel van Project Operations-integratie (msdyn\_contractlinesscheduleofvalues)** | No | No | n.v.t. | No | n.v.t. |
| **Entiteit voor onkostenramingen van Project Operations-integratie (msdyn\_estimateslines)** | Geen | Geen | n.v.t. | Geen | n.v.t. |
| **Entiteit voor exporteren van categorieën met projectonkosten voor Project Operations-integratie (msdyn\_expensecategories)** | Geen | Geen | n.v.t. | Geen | n.v.t. |
| **Entiteit voor exporteren van projectkosten voor Project Operations-integratie (msdyn\_expenses)** | Ja | No | n.v.t. | No | n.v.t. |
| **Entiteit voor tijdramingen van Project Operations-integratie (msdyn\_resourceassignments)** | Ja | No | n.v.t. | No | n.v.t. |


4. Als u de entiteit wilt vernieuwen, selecteert u de toewijzingsnaam en vervolgens **Entiteiten vernieuwen**. 


![Toewijzing vernieuwen](./media/20RefreshMapping.png)

5. Voer de toewijzing uit nadat het vernieuwen is voltooid. Voordat u de volgende toewijzing inschakelt, moet u controleren of de toewijzing in de tabel de status **In uitvoering** heeft. Het uitvoeren van toewijzingen met een groot aantal vereisten kan enige tijd duren.

Om een toewijzing met vereisten uit te voeren, schakelt u de wisselknop **Gerelateerde entiteitstoewijzingen weergeven** in. Als in de tabel bij **Vereisten voor initiële synchronisatie** **Nee** wordt aangegeven, controleert u of de markering **Initiële synchronisatie** op **Uit** staat voor alle vereiste toewijzingen voordat u deze uitvoert.

![Toewijzing uitvoeren](./media/21RunMap.png)

6. Controleer of alle projectgerelateerde toewijzingen de status actief hebben.

![Alle toewijzingen worden uitgevoerd](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Configuratiegegevens in CDS toepassen voor Project Operations (optioneel)

Als u demogegevens hebt toegepast op de Finance-omgeving raadpleegt u [Configuratiegegevens instellen en toepassen in Common Data Service voor Project Operations](resource-apply-pro-setup-config-data.md) om demogegevens toe te passen in de CDS-omgeving.


Uw Project Operations-omgeving is nu ingericht en geconfigureerd. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]