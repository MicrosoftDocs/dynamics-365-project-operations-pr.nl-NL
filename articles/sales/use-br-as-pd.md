---
title: Een boekbare resource gebruiken als een prijsdimensie
description: Dit onderwerp bevat informatie over het gebruik van een boekbare resource als een prijsdimensie.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dcd01d80236f0218bc6fa3a1fe1389f8314f3c9b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598621"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Een boekbare resource gebruiken als een prijsdimensie

 _**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_ 

Dit onderwerp bevat informatie over het gebruik van een boekbare resource als een prijsdimensie. Als uw prijsstrategie zo is ingesteld dat elke boekbare resource een specifieke prijs of een specifiek kostentarief moet hebben, gebruikt u een boekbare resource als prijsdimensie.

## <a name="prerequisites"></a>Vereisten
Voordat u de procedures In dit onderwerp voltooit, moet u een nieuwe prijsdimensie-oplossing voor uw organisatie hebben. Als u deze nog niet hebt gemaakt, raadpleegt u [Aangepaste velden en entiteiten maken](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Het veld Boekbare resource toevoegen aan formulieren en weergaven
Als u het veld **Boekbare resource** zichtbaar wilt maken in de oplossing voor de prijsdimensie, moet u het veld als een entiteit aan alle formulieren en weergaven toevoegen.

De volgende tabel bevat een overzicht van alle kant-en-klare formulieren en weergaven, per entiteit. U moet het nieuwe veld ook toevoegen aan eventuele aanvullende formulieren of weergaven in uw aangepaste entiteiten.

|   Entity        | Formulieren   |Weergaven        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolprijs| Gegevens | - Actieve resourcecategorieprijzen<br> - Gekoppelde resourcecategorieprijs |
|  Opslag voor rolprijs| Gegevens| - Actieve opslag voor rolprijs<br>- Gekoppelde opslag voor rolprijs |
|  Detail van prijsopgaveregel| - Projectgegevens<br>- Snelle invoer van project| - Detail van actieve prijsopgaveregel<br>- Gecombineerde details van prijsopgaveregels<br>- Gekoppelde details van prijsopgaveregels |
|  Details van projectcontractregel| - Projectgegevens<br>- Snelle invoer van project| - Gecombineerde contractregeldetails<br>- Actieve contractregeldetails<br>- Gekoppelde contractregeldetails |
|  Projecttaak| - Gegevens<br>- Nieuw formulier| &nbsp; |
|  Projectteamlid| - Gegevens<br>- Nieuw formulier| - Actieve projectteamleden<br>- Projectteamleden<br>- Gekoppelde projectteamleden |
|  Tijdsvermelding| - Gegevens<br>- Tijdsvermelding maken| - Mijn tijdsvermeldingen op datum<br>- Mijn tijdsvermeldingen voor deze week<br>- Tijdsvermeldingen voor goedkeuring|
|  Journaalregel| - Gegevens<br>- Snelle invoer| - Actieve journaalregels<br>- Gekoppelde journaalregel |
|  Factuurregeldetail| - Gegevens<br>- Snelle invoer| - Actieve factuurregeldetails<br>- Factureerbare factuurtransacties<br>- Gratis factuurtransacties<br>- Gekoppelde weergave van factuurregeldetail <br>- Niet-factureerbare factuurtransacties|
|  Actueel| - Gegevens<br>- Actieve werkelijke waarden| Gekoppelde werkelijke waarden |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Een boekbare resource instellen als een prijsdimensie
Volg deze stappen om een boekbare resource in te stellen als een prijsdimensie:

1. Ga naar **Instellingen** > **Parameters**. 
2. Controleer op de pagina **Parameter** in het tabblad **Op bedrag gebaseerde prijsdimensies** of het raster de records in de entiteit **Prijsdimensies** weergeeft. 
2. Voeg **Boekbare resource** toe aan deze lijst met prijsdimensies als **msdyn_bookableresource**. 
3. Selecteer een waarde in **Van toepassing op kosten** en **Van toepassing op verkoop**.
4. Selecteer in **Dimensietype** de optie **Op bedrag gebaseerd**. 
5. Selecteer de kosten- en verkoopprioriteit voor de boekbare resource. Een boekbare resource heeft doorgaans de hoogste prioriteit wanneer deze wordt opgenomen als prijsdimensie. Stel de prioriteit in op **1** (of **0** afhankelijk van hoe u de prioriteit telt) om dit gedrag te waarborgen.

## <a name="set-up-pricing-dimension-field-names"></a>Veldnamen voor prijsdimensies instellen

Wanneer de veldnaam van een prijsdimensie in de tabel **Rolprijs** verschilt van de veldnaam in een van de andere entiteiten waar de standaardprijs wordt gebruikt, moet de prijsdimensierecord op de hoogte worden gesteld van de verschillende namen.  

Voor een boekbare resource heeft de entiteit **Projectteamleden** een iets andere veldnaam dan in de entiteit **Rolprijs**: 

 - **Projectteamleden** entiteit = **msdyn_bookableresourceid**
 - **Rolprijs** entiteit = **msdyn_bookableresource**

De prijsdimensierecord voor **msydn_bookableresource** moet op de hoogte worden gesteld van dit verschil.

1. Dubbelklik op de rij in het raster **Prijsdimensies** om de dimensiepagina van **msdyn_bookableresource** te openen.
2. Selecteer op de dimensiepagina op het tabblad **Gerelateerd** de optie **Veldnamen voor prijsdimensies**.

  ![Het tabblad Veldnamen voor prijsdimensies.](media/PD-fieldname.png)

3. Selecteer in de gekoppelde weergave die wordt geopend **Veldnaam voor nieuwe prijsdimensie toevoegen**.

  ![Veldnamen voor nieuwe prijsdimensies toevoegen.](media/Add-NewPD-fieldname.png)

  Hiermee opent u de pagina **Veldnaam voor nieuwe prijsdimensie** voor **msdyn_bookableresource**. 

4. Op de pagina **Nieuwe veldnaam voor prijsdimensie** voegt u **msdyn_projectteam** toe aan **Logische naam van entiteit**.
5. Voeg **msdyn_bookableresourceid** toe aan **Veldnaam**.

 ![Het formulier Veldnaam voor nieuwe prijsdimensie.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]