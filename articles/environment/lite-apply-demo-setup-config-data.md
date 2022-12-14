---
title: Demogegevens voor installatie en configuratie toepassen - lite
description: Dit artikel bevat informatie over het toepassen van demogegevens voor instelling en configuratie voor Project Operations.
author: sigitac
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8ac8c910ce2d91fa47df08e8fb6efb723c0dc5fa
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/30/2022
ms.locfileid: "9811019"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demogegevens voor installatie en configuratie toepassen voor Project Operations - lite 

_**Lite-implementatie - van deal tot pro-formafacturering_



## <a name="prerequisites"></a>Vereisten

Voordat u met de configuratie begint, moet u een Dataverse-omgeving inrichten voor Dynamics 365 Project Operations.


## <a name="instructions"></a>Instructies

1. Download het [Pakket met instellingsgegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
1. Navigeer naar de map *ProjOpsSampleSetupData - CE: alleen CMT* en voer het uitvoerbare bestand *GegevensmigratieUtility* uit.
1. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

    ![Configuratiemigratie.](./media/1ConfigurationMigration.png)

1. Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.
1. Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.
1. Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.

   ![Configuratie inloggen.](./media/2ConfigurationSignin.png)

1. Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.
1. Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map *ProjOpsSampleSetupData - CE: alleen CMT*.

   ![Zipbestand.](./media/3ZipFile.png)

   ![Een bestand selecteren.](./media/4SelectAFile.png)

1. Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.

   ![Gegevens importeren.](./media/5ImportData.png)

1. Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid. Sluit de CMT-wizard nadat het importeren is voltooid. 
1. Controleer uw organisatie op gegevens in de volgende 18 entiteiten:

    -   Valuta
    -   Account
    -   Organisatie-eenheid
    -   Contact
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

    ![Import voltooien.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
