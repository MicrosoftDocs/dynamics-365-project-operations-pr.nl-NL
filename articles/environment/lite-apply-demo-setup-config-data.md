---
title: Demogegevens voor installatie en configuratie toepassen - lite
description: Dit onderwerp bevat informatie over het toepassen van demo- en configuratiegegevens voor Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642087"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demogegevens voor installatie en configuratie toepassen voor Project Operations - lite 

_**Lite-implementatie - van deal tot pro-formafacturering_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Vereisten

Voordat u met de configuratie begint, moet u een Common Data Service-omgeving (CDS) inrichten voor Dynamics 365 Project Operations.


## <a name="instructions"></a>Instructies

1. Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigeer naar de map *ProjOpsDemoDataSetupAndMaster - Integrated CMT* en voer het uitvoerbare bestand *DataMigrationUtility* uit.
3. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.
5. Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.
6. Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.

![Configuratie inloggen](./media/2ConfigurationSignin.png)

7. Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.
8. Selecteer op pagina 4 het zipbestand *MasterAndSetupData* in de uitgepakte map, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Zipbestand](./media/3ZipFile.png)

![Selecteer een bestand](./media/4SelectAFile.png)

9. Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.

![Gegevens importeren](./media/5ImportData.png)

10. Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid. Sluit de CMT-wizard nadat het importeren is voltooid. 
11. Controleer uw organisatie op gegevens in de volgende 20 entiteiten:

-   Valuta
-   Account
-   Organisatie-eenheid
-   Contact
-   Belastinggroep
-   Klantengroep
-   Eenheid
-   Eenhedengroep
-   Prijslijst
-   Prijslijst voor projectparameters 
-   Factuurfrequentie
-   Categorie van boekbare resources
-   Transactiecategorie
-   Onkostencategorie
-   Rolprijs
-   Prijs voor transactiecategorie
-   Kenmerk
-   Boekbare resource
-   Toewijzing van categorie met boekbare resources
-   Kenmerk van boekbare resources

![Import voltooid](./media/6CompleteImport.png)
