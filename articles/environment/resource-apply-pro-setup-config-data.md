---
title: Configuratiegegevens in Common Data Service instellen en toepassen
description: Dit onderwerp bevat informatie over het instellen en toepassen van configuratiegegevens in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642222"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configuratiegegevens in Common Data Service instellen en toepassen 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u begint met het configureren van gegevens in Common Data Service (CDS), moet aan de volgende voorwaarden worden voldaan:

1.  Richt een CDS-omgeving en een Dynamics 365 Finance-omgeving in voor Project Operations.
2.  Informatie over rechtspersoon van Dynamics 365 Finance wordt gedeeld met de CDS-omgeving. Dit betekent dat de entiteit **Bedrijf** in CDS de volgende bedrijfsrecords heeft:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Gegevens voor installatie en configuratie installeren

1. Download, deblokkeer en extraheer het [Installatie- en configuratiegegevenspakket](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Navigeer naar de uitgepakte map en voer het uitvoerbare bestand *DataMigrationUtility* uit.
3. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.
5. Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.
6. Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.
8. Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map.

![Selectie zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.

![Gegevens importeren](./media/5ImportData.png)

10. Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid. Sluit de CMT-wizard nadat het importeren is voltooid. 
11. Controleer uw organisatie op gegevens in de volgende 19 entiteiten:

  - Valuta
  - Organisatie-eenheid
  - Contact
  - Belastinggroep
  - Klantengroep
  - Eenheid
  - Eenhedengroep
  - Prijslijst
  - Prijslijst voor projectparameters
  - Factuurfrequentie
  - Categorie van boekbare resources
  - Transactiecategorie
  - Onkostencategorie
  - Rolprijs
  - Prijs voor transactiecategorie
  - Kenmerk
  - Boekbare resource
  - Toewijzing van categorie met boekbare resources
  - Kenmerk van boekbare resources

![Import voltooid](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations-configuraties bijwerken

1. Navigeer naar de CE-omgeving. U kunt dit vinden door het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) te openen, de omgeving te selecteren en vervolgens **Omgeving openen** te selecteren. 

![Omgeving openen](./media/7OpenEnvironment.png)

2. Ga naar **Projecten** > **Resources** en selecteer **Nieuw** om een boekbare resource voor uw gebruiker te maken.

![Boekbare resources](./media/8BookableResources.png)

3. Selecteer op het tabblad **Algemeen** uw gebruiker met beheerdersrechten. Controleer of de tijdzone overeenkomt met de zone waarin u zich bevindt. 

![Nieuwe boekbare resource](./media/9NewBookableResource.png)

4. Op het tabblad **Planning**, in het veld **Bedrijf** kiest u het bedrijf **USPM** en selecteert u **Opslaan**. 

![Tabblad Planning](./media/10SchedulingTab.png)

5. Selecteer het tabblad **Werkuren**.  

![Werkuren](./media/11WorkHours.png)

6. Dubbelklik op een waarde in de kalender en selecteer **Bewerken** > **Alle gebeurtenissen in de reeks**. 

![Werkagenda](./media/12WorkCalendar.png)

7. Verander werkuren in een werkdag van acht (8) uur, markeer weekends als vrije dagen en zorg ervoor dat de tijdzone overeenkomt met de uwe. 
8. Selecteer **Opslaan en sluiten**.

![Agenda bijwerken](./media/13UpdateCalendar.png)

9. Ga naar **Instellingen** > **Agendasjablonen** en selecteer **Nieuw**.
 
 ![Agendasjablonen](./media/14CalendarTemplates.png)
 
 10. Voer een naam in, selecteer de sjabloonresource die u hebt gemaakt en selecteer vervolgens **Opslaan**. 
 
 ![Agendasjabloon opslaan](./media/15SaveCalendarTemplate.png)
 
 11. Ga naar **Parameters** en dubbelklik op de record. 
 
 ![Projectparameters](./media/16ProjectParameters.png)
 
12. Werk de volgende velden bij:

 - **Standaardbedrijf**: USPM
 - **Standaard organisatie-eenheid**: Contoso Robotics Global
 - **Factuurfrequentie**: zevende en laatste dag
 - **Werkuursjabloon**: ga naar de sjabloon die u hebt gemaakt.

13. Selecteer **Opslaan**. 

![Bijgewerkte projectparameters](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]