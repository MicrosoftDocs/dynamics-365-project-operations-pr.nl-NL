---
title: Transactiecategorie gebruiken als prijsdimensie
description: Dit onderwerp bevat informatie over het gebruik van een transactiecategorie als een prijsdimensie.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 64b81ca7-e2db-4e4a-a202-aae0eb235ffd
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: a36e0578b8d77a0ed1ea61134453aa064771760f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750825"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Transactiecategorie gebruiken als prijsdimensie
Dit onderwerp laat zien hoe u een transactiecategorie gebruikt als een prijsdimensie. Voordat u begint, moet u een nieuwe oplossing voor prijsdimensies maken als u deze nog niet hebt. Als u al een oplossing voor prijsdimensies hebt, kunt u wijzigingen in die oplossing aanbrengen. Als u geen nieuwe oplossing voor prijsdimensies voor uw organisatie hebt gemaakt, voltooit u de procedures in het onderwerp [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Transactiecategorie toevoegen aan formulieren en weergaven
Als u de transactiecategorie zichtbaar wilt maken in de gebruikersinterface in de oplossing voor prijsdimensies, moet u alle formulieren en weergaven van de belangrijkste entiteiten doorlopen en deze velden toevoegen aan de formulieren en weergaven van deze entiteiten.
De volgende tabel bevat een uitgebreide lijst met gebruiksklare formulieren en weergaven per entiteit die moeten worden bijgewerkt met de nieuwe velden. Als er extra weergaven of formulieren in uw aanpassingen van deze entiteiten zijn, voegt u de nieuwe velden ook daar aan toe.

|  Entiteit        | Formulieren     |Weergaven        |
| ------------------------------|---------------------------------|----------------------------------|
|  Rolprijs|• Informatie |• Actieve resourcecategorieprijzen<br> • Gekoppelde weergave van resourcecategorieprijzen|
|  Opslag voor rolprijs|• Informatie|• Actieve opslag voor rolprijs<br>• Gekoppelde weergave van opslag voor rolprijs|
|  Details van prijsopgaveregel|• Projectgegevens<br>• Snelle invoer van project|• Details van actieve prijsopgaveregel<br>• Gecombineerde details van prijsopgaveregels<br>• Gekoppelde weergave van details van prijsopgaveregels|
|  Details van projectcontractregel|• Projectgegevens<br>• Snelle invoer van project|• Gecombineerde contractregeldetails<br>• Actieve contractregeldetails<br>• Gekoppelde weergave voor contractregeldetails|
|  Projectteamlid|• Informatie<br>• Nieuw formulier|• Actieve projectteamleden<br>• Projectteamleden<br>• Gekoppelde weergave van projectteamleden|
|  Tijdsvermelding|• Informatie<br>• Tijdsvermelding maken|• Mijn tijdsvermeldingen op datum<br>• Mijn tijdsvermeldingen voor deze week<br>• Tijdsvermeldingen voor goedkeuring|
|  Journaalregel|• Informatie<br>• Snelle invoer|• Actieve journaalregels<br>• Gekoppelde weergave van journaalregel|
|  Factuurregeldetail|• Informatie<br>• Snelle invoer|• Actieve factuurregeldetails<br>• Toerekenbare factuurtransacties<br>• Gratis factuurtransacties<br>• Gekoppelde weergave van factuurregeldetails<br>• Niet-toerekenbare factuurtransacties|
|  Werkelijk|• Informatie<br>• Actieve werkelijke waarden|• Gekoppelde weergave van werkelijke waarden|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Transactiecategorie gebruiken als prijsdimensie instellen

1. Ga in de webinterface naar **Project Service** > **Instellingen** > **Parameters**. 
2. Kijk op de pagina **Parameters** in het tabblad **Op bedrag gebaseerde prijsdimensies** naar het raster in het tabblad met de records in de entiteit **Prijsdimensies**.
3. Voeg **Transactiecategorie** toe aan deze lijst en stel de velden **Van toepassing op kosten** en **Van toepassing op verkoop** in op **Ja**.
4. Selecteer in het veld **Dimensietype** de optie **Op bedrag gebaseerd** en selecteer vervolgens de prioriteit voor **Transactiecategorie** met betrekking tot kosten en verkopen.
