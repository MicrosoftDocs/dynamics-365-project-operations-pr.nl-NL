---
title: Boekbare resource gebruiken als een prijsdimensie
description: Dit onderwerp bevat informatie over het gebruik van een boekbare resource als een prijsdimensie.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a5c643745d8e10887965228da7abd8f56228006
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074663"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Boekbare resource gebruiken als een prijsdimensie
Dit onderwerp bevat informatie over het gebruik van een boekbare resource als een prijsdimensie. Voordat u begint, moet u een nieuwe oplossing voor prijsdimensies maken als u deze nog niet hebt. Als u al een oplossing voor prijsdimensies hebt, kunt u wijzigingen in die oplossing aanbrengen. Als u geen nieuwe oplossing voor prijsdimensies voor uw organisatie hebt gemaakt, voltooit u de procedures in het onderwerp [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Boekbare resource toevoegen aan formulieren en weergaven
Als u de velden zichtbaar wilt maken in de gebruikersinterface in de oplossing voor prijsdimensies, moet u alle formulieren en weergaven van de belangrijkste Project Service-entiteiten doorlopen en deze velden toevoegen aan de formulieren en weergaven van deze entiteiten.
De volgende tabel bevat een uitgebreide lijst met gebruiksklare formulieren en weergaven, weergegeven per entiteit die moeten worden bijgewerkt. Als er extra weergaven of formulieren in uw aanpassingen van deze entiteiten zijn, voegt u de nieuwe velden ook daaraan toe.
Open Oplossingenverkenner voor de oplossing voor prijsdimensies en klik op **Alle aanpassingen publiceren**.


|   Entiteit        | Formulieren   |Weergaven        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolprijs|• Informatie |• Actieve resourcecategorieprijzen<br> • Gekoppelde weergave van resourcecategorieprijzen|
|  Opslag voor rolprijs|• Informatie|• Actieve opslag voor rolprijs<br>• Gekoppelde weergave van opslag voor rolprijs|
|  Details van prijsopgaveregel|• Projectgegevens<br>• Snelle invoer van project|• Details van actieve prijsopgaveregel<br>• Gecombineerde details van prijsopgaveregels<br>• Gekoppelde weergave van details van prijsopgaveregels|
|  Details van projectcontractregel|• Projectgegevens<br>• Snelle invoer van project|• Gecombineerde contractregeldetails<br>• Actieve contractregeldetails<br>• Gekoppelde weergave voor contractregeldetails|
|  Projecttaak|• Informatie<br>• Nieuw formulier||
|  Projectteamlid|• Informatie<br>• Nieuw formulier|• Actieve projectteamleden<br>• Projectteamleden<br>• Gekoppelde weergave van projectteamleden|
|  Tijdsvermelding|• Informatie<br>• Tijdsvermelding maken|• Mijn tijdsvermeldingen op datum<br>• Mijn tijdsvermeldingen voor deze week<br>• Tijdsvermeldingen voor goedkeuring|
|  Journaalregel|• Informatie<br>• Snelle invoer|• Actieve journaalregels<br>• Gekoppelde weergave van journaalregel|
|  Factuurregeldetail|• Informatie<br>• Snelle invoer|• Actieve factuurregeldetails<br>• Factureerbare factuurtransacties<br>• Gratis factuurtransacties<br>• Gekoppelde weergave van factuurregeldetails<br>• Niet-factureerbare factuurtransacties|
|  Werkelijk|• Informatie<br>• Actieve werkelijke waarden|• Gekoppelde weergave van werkelijke waarden|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Boekbare resource instellen als een prijsdimensie

1. Ga in de webinterface naar **Project Service** > **Instellingen** > **Parameters**. Op de pagina **Parameters** op het tabblad **Op bedrag gebaseerde prijsdimensies** worden in het raster de records in de entiteit Prijsdimensies weergegeven. 
2. Voeg **Boekbare resource** toe aan deze lijst met prijsdimensies als **msdyn_bookableresource**. 
3. Geef de context aan waarin de boekbare resource werkt als een prijsdimensie en stel de waarden voor **Van toepassing op kosten** en **Van toepassing op verkoop** in.
4. Selecteer in het veld **Dimensietype** de optie **Op bedrag gebaseerd**. 
5. Selecteer de kosten- en verkoopprioriteit voor de boekbare resource. Als een boekbare resource wordt opgenomen als een prijsdimensie, heeft deze meestal de hoogste prioriteit, dus als u dit instelt op **1** (of **0** , afhankelijk van de manier waarop u de prioriteit telt), bent u verzekerd van dat gedrag.

## <a name="set-up-pricing-dimension-field-names"></a>Veldnamen voor prijsdimensies instellen

Wanneer de veldnaam van een prijsdimensie in de tabel **Rolprijs** verschilt van de veldnaam in een van de andere entiteiten waar de standaardinstelling van de prijs moet werken, moet de prijsdimensierecord op de hoogte worden gesteld van de verschillende namen.    
Voor een boekbare resource heeft de entiteit **Projectteamleden** een iets andere veldnaam ( **msdyn_bookableresourceid** ) dan in de rolentiteit **Rolprijs** ( **msdyn_ bookableresource** ). De prijsdimensierecord voor **msydn_bookableresource** moet hiervan op de hoogte worden gesteld. 
1. Dubbelklik hiervoor op de rij in het raster **Prijsdimensies** om de dimensiepagina van **msdyn_bookableresource** te openen.
2. Klik op de dimensiepagina op het tabblad **Gerelateerd** op **Veldnamen voor prijsdimensies**.

 ![Het tabblad Veldnamen voor prijsdimensies](media/PD-fieldname.png)

4. Klik in de gekoppelde weergave die wordt geopend op **Veldnaam voor nieuwe prijsdimensie toevoegen**.

 ![Veldnamen voor nieuwe prijsdimensies toevoegen](media/Add-NewPD-fieldname.png)


Hiermee opent u de pagina **Veldnaam voor nieuwe prijsdimensie** voor **msdyn_bookableresource**. 

5. Voeg **msdyn_projectteam** toe aan het veld **Logische naam van entiteit** en **msdyn_bookableresourceid** aan het veld **Veldnaam**. Sla de record op.

 ![Het formulier Veldnaam voor nieuwe prijsdimensie](media/PD-fieldname-Added.png)
