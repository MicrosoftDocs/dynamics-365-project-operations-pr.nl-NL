---
title: Transactiecategorie gebruiken als prijsdimensie
description: Dit onderwerp bevat informatie over het gebruik van een transactiecategorie als een prijsdimensie.
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
ms.openlocfilehash: 0019571a1d37d3b6a503e7221db3c3b51365c236
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4074648"
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
|  Projecttaak|• Informatie<br>• Nieuw formulier||
|  Projectteamlid|• Informatie<br>• Nieuw formulier|• Actieve projectteamleden<br>• Projectteamleden<br>• Gekoppelde weergave van projectteamleden|
|  Tijdsvermelding|• Informatie<br>• Tijdsvermelding maken|• Mijn tijdsvermeldingen op datum<br>• Mijn tijdsvermeldingen voor deze week<br>• Tijdsvermeldingen voor goedkeuring|
|  Journaalregel|• Informatie<br>• Snelle invoer|• Actieve journaalregels<br>• Gekoppelde weergave van journaalregel|
|  Factuurregeldetail|• Informatie<br>• Snelle invoer|• Actieve factuurregeldetails<br>• Factureerbare factuurtransacties<br>• Gratis factuurtransacties<br>• Gekoppelde weergave van factuurregeldetails<br>• Niet-factureerbare factuurtransacties|
|  Werkelijk|• Informatie<br>• Actieve werkelijke waarden|• Gekoppelde weergave van werkelijke waarden|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Transactiecategorie gebruiken als prijsdimensie instellen

1. Ga in de webinterface naar **Project Service** > **Instellingen** > **Parameters**. 
2. Kijk op de pagina **Parameters** in het tabblad **Op bedrag gebaseerde prijsdimensies** naar het raster in het tabblad met de records in de entiteit **Prijsdimensies**.
3. Voeg **Transactiecategorie** toe aan deze lijst en stel de velden **Van toepassing op kosten** en **Van toepassing op verkoop** in op **Ja**.
4. Selecteer in het veld **Dimensietype** de optie **Op bedrag gebaseerd** en selecteer vervolgens de prioriteit voor **Transactiecategorie** met betrekking tot kosten en verkopen.
