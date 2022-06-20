---
title: Configuratiegegevens in Common Data Service instellen en toepassen
description: Dit artikel bevat informatie over het instellen en toepassen van configuratiegegevens in Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2c918425e9a6c5fe8888ed8a4258ca59f0464828
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928012"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configuratiegegevens in Common Data Service instellen en toepassen 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_



## <a name="prerequisites"></a>Vereisten

Voordat u begint met het configureren van gegevens in Common Data Service (CDS), moet aan de volgende voorwaarden worden voldaan:

1.  Een CDS-omgeving en een Dynamics 365 Finance-omgeving inrichten voor Project Operations.
2.  Informatie over rechtspersonen uit Dynamics 365 Finance wordt gedeeld met de CDS-omgeving. Dit betekent dat de entiteit **Bedrijf** in CDS de volgende bedrijfsrecords heeft:
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Gegevens voor installatie en configuratie installeren

1. Download, deblokkeer en extraheer het [Installatie- en configuratiegegevenspakket](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).
2. Navigeer naar de uitgepakte map en voer het uitvoerbare bestand *DataMigrationUtility* uit.
3. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

![Configuratiemigratie.](./media/1ConfigurationMigration.png)

4. Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.
5. Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.
6. Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.

![Configuratie inloggen.](./media/2ConfigurationSignin.png)

7. Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.
8. Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map.

![Selectie zipbestand.](./media/3ZipFile.png)

![Een bestand selecteren.](./media/4SelectAFile.png)

9. Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.

![Gegevens importeren.](./media/5ImportData.png)

10. Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid. Sluit de CMT-wizard nadat het importeren is voltooid. 
11. Controleer uw organisatie op gegevens in de volgende 26 entiteiten:

  - Valuta
  - Rekeningschema
  - Fiscale kalender
  - Typen valutawisselkoers
  - Betalingsdag
  - Betalingsschema
  - Betalingsvoorwaarde
  - Organisatie-eenheid
  - Contact
  - Belastinggroep
  - Klantengroep
  - Leveranciersgroep
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

![Import voltooien.](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Project Operations-configuraties bijwerken

1. Navigeer naar de CE-omgeving. U kunt dit vinden door het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) te openen, de omgeving te selecteren en vervolgens **Omgeving openen** te selecteren. 

![Omgeving openen.](./media/7OpenEnvironment.png)

2. Ga naar **Projecten** > **Resources** en selecteer **Nieuw** om een boekbare resource voor uw gebruiker te maken.

![Boekbare resources.](./media/8BookableResources.png)

3. Selecteer op het tabblad **Algemeen** uw gebruiker met beheerdersrechten. Controleer of de tijdzone overeenkomt met de zone waarin u zich bevindt. 

![Nieuwe boekbare resource.](./media/9NewBookableResource.png)

4. Op het tabblad **Planning**, in het veld **Bedrijf** kiest u het bedrijf **USPM** en selecteert u **Opslaan**. 

![Tabblad Planning.](./media/10SchedulingTab.png)

5. Selecteer het tabblad **Werkuren**.  

![Werkuren.](./media/11WorkHours.png)

6. Dubbelklik op een waarde in de kalender en selecteer **Bewerken** > **Alle gebeurtenissen in de reeks**. 

![Werkagenda.](./media/12WorkCalendar.png)

7. Verander werkuren in een werkdag van acht (8) uur, markeer weekends als vrije dagen en zorg ervoor dat de tijdzone overeenkomt met de uwe. 
8. Selecteer **Opslaan en sluiten**.

![Agenda bijwerken.](./media/13UpdateCalendar.png)

9. Ga naar **Instellingen** > **Agendasjablonen** en selecteer **Nieuw**.
 
 ![Agendasjablonen.](./media/14CalendarTemplates.png)
 
 10. Voer een naam in, selecteer de sjabloonresource die u hebt gemaakt en selecteer vervolgens **Opslaan**. 
 
 ![Agendasjabloon opslaan.](./media/15SaveCalendarTemplate.png)
 
 11. Ga naar **Parameters** en dubbelklik op de record. 
 
 ![Projectparameters.](./media/16ProjectParameters.png)
 
12. Werk de volgende velden bij:

 - **Standaardbedrijf**: USPM
 - **Standaard organisatie-eenheid**: Contoso Robotics Global
 - **Factuurfrequentie**: zevende en laatste dag
 - **Werkuursjabloon**: ga naar de sjabloon die u hebt gemaakt.

13. Selecteer **Opslaan**. 

![Bijgewerkte projectparameters.](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
