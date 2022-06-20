---
title: Demogegevens voor installatie en configuratie toepassen - lite
description: Dit artikel bevat informatie over het toepassen van demogegevens voor instelling en configuratie voor Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 68e504dd031596b295b1383a8e81621744cae8d2
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922308"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demogegevens voor installatie en configuratie toepassen voor Project Operations - lite 

_**Lite-implementatie - van deal tot pro-formafacturering_



## <a name="prerequisites"></a>Vereisten

Voordat u met de configuratie begint, moet u een Common Data Service-omgeving (CDS) inrichten voor Dynamics 365 Project Operations.


## <a name="instructions"></a>Instructies

1. Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Navigeer naar de map *ProjOpsSampleSetupData - CE: alleen CMT* en voer het uitvoerbare bestand *GegevensmigratieUtility* uit.
3. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

    ![Configuratiemigratie.](./media/1ConfigurationMigration.png)

4. Selecteer op pagina 2 van de CMT-wizard **Microsoft 365** als **Implementatietype**.
5. Schakel de selectievakjes **Een lijst met beschikbare organisaties weergeven** en **Geavanceerd weergeven** in.
6. Selecteer de regio van uw tenant, voer uw inloggegevens in en selecteer **Login**.

   ![Configuratie inloggen.](./media/2ConfigurationSignin.png)

7. Selecteer op pagina 3 uit de lijst met organisaties op de tenant de organisatie waarin u de demogegevens wilt importeren en selecteer **Login**.
8. Selecteer op pagina 4 het zipbestand *SampleSetupAndConfigData* in de uitgepakte map *ProjOpsSampleSetupData - CE: alleen CMT*.

   ![Zipbestand.](./media/3ZipFile.png)

   ![Een bestand selecteren.](./media/4SelectAFile.png)

9. Selecteer nadat het zipbestand is geselecteerd **Gegevens importeren**.

   ![Gegevens importeren.](./media/5ImportData.png)

10. Het importeren duurt ongeveer twee tot tien minuten, afhankelijk van uw netwerksnelheid. Sluit de CMT-wizard nadat het importeren is voltooid. 
11. Controleer uw organisatie op gegevens in de volgende 18 entiteiten:

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
