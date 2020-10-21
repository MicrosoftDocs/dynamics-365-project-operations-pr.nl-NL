---
title: Demogegevens voor installatie en configuratie toepassen
description: Dit onderwerp bevat informatie over het toepassen van demo- en configuratiegegevens voor Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948817"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Demo- en configuratiegegevens toepassen voor Project Operations Lite-implementatie, van deal tot proforma-facturering

_**Lite-implementatie - van deal tot pro-formafacturering_

1. Download het [Pakket met mastergegevens](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Navigeer naar de map *ProjOpsDemoDataSetupAndMaster - Integrated CMT* en voer het uitvoerbare bestand *DataMigrationUtility* uit.
3. Op pagina 1 van de wizard Common Data Service Configuratiemigratie (CMT) selecteert u **Gegevens importeren** en vervolgens **Doorgaan**.

![Configuratiemigratie](./media/1ConfigurationMigration.png)

4. Selecteer op pagina 2 van de CMT-wizard **Office 365** als **Implementatietype**.
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
- Factuurfrequentiedetail
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
