---
title: Aangepaste velden instellen als prijsdimensies
description: In dit onderwerp krijgt u informatie over het instellen van prijsdimensies met behulp van aangepaste velden.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c65d6bf64d8a81759239f2a31f3a68953181c8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599402"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Aangepaste velden instellen als prijsdimensies

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

In dit onderwerp wordt ervan uitgegaan dat u de procedures hebt voltooid in de onderwerpen [Aangepaste velden en entiteiten maken](create-custom-fields-entities-pricing-dimensions.md) en [Vereiste aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](add-custom-fields-price-setup-transactional-entities.md). Als u deze procedures niet hebt voltooid, gaat u terug, voltooit u deze en keert u terug naar Dit onderwerp. 

Dit onderwerp bevat informatie over het instellen van aangepaste prijsdimensies. Op de pagina **Parameters** op het tabblad **Op bedrag gebaseerde prijsdimensies** worden de records in de entiteiten voor prijsdimensie weergegeven. Standaard bevat het raster op dit tabblad twee rijen:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Organisatie-eenheid)

> [!IMPORTANT]
> Verwijder deze rijen niet. Als u ze echter niet nodig hebt, kunt u ze niet toepasselijk maken in een specifieke context door de velden **Van toepassing op kosten**, **Van toepassing op verkoop** en **Van toepassing op inkoop** allemaal in te stellen op **Nee**. Als u deze kenmerkwaarden instelt op **Nee**, heeft dit hetzelfde effect als wanneer het veld niet als een prijsdimensie is ingesteld.

Als u een veld wilt laten fungeren als een prijsdimensie, moet het voldoen aan de volgende voorwaarden:

- Het is gemaakt als een veld in de entiteiten **Rolprijs** en **Opslag voor rolprijs**. Meer informatie over hoe u dit doet, vindt u in [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](add-custom-fields-price-setup-transactional-entities.md).

- Het is gemaakt als een rij in de tabel **Prijsdimensie**. Voeg bijvoorbeeld prijsdimensierijen toe zoals weergegeven in de volgende afbeelding. 

![Rijen in Op bedrag gebaseerde prijsdimensies.](media/Amt-based-PD.png)

Werkuren van resource (**msdyn_resourceworkhours**) is toegevoegd als een op toeslag gebaseerde dimensie en is toegevoegd aan het raster op het tabblad **Op opslag gebaseerde prijsdimensie**.

![Rijen in Op opslag gebaseerde prijsdimensies.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Elke wijziging in de prijsdimensiegegevens in deze tabel, of dit nu bestaande of nieuwe gegevens zijn, wordt alleen doorgevoerd in de bedrijfslogica voor prijzen nadat de cache is vernieuwd. Het kan tot 10 minuten duren totdat de cache is vernieuwd. Wacht zo lang om de wijzigingen in de logica voor standaardwaarden voor prijzen te zien, die moet resulteren uit wijzigingen in de gegevens van de prijsdimensie.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Kenmerken van de tabel Prijsdimensies
De volgende secties geven informatie over de verschillende kenmerken in de tabel **Prijsdimensies**.

### <a name="pricing-dimension-name"></a>Naam van prijsdimensie
Deze waarde moet exact gelijk zijn aan de schemanaam van het veld dat wordt toegevoegd aan de tabel **Rolprijs** voor aangepaste prijsdimensies. Meer informatie over het toevoegen van velden aan de tabel **Rolprijs** vindt u in [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Type dimensie
Er zijn twee typen prijsdimensies:
  
  - **Op bedrag gebaseerde dimensies**: de dimensiewaarden van de invoercontext worden vergeleken met de dimensiewaarden op de regel **Rolprijs** en de prijs/kosten worden standaard rechtstreeks overgenomen uit de tabel **Rolprijs**.
  - **Op opslag gebaseerde dimensies**: dit zijn dimensies waarbij het volgende proces van 3 stappen wordt gebruikt om de prijs/kosten op te halen.
 
    1. De niet op opslag gebaseerde dimensiewaarden van de invoercontext worden vergeleken met de rolprijsregel om het basistarief op te halen.
    2. De dimensiewaarden van de invoercontext worden vergeleken met de regel **Opslag voor rolprijs** om een opslagpercentage op te halen.
    3. Het opslagpercentage uit de tweede stap wordt toegepast op het basistarief dat in de eerste stap uit de tabel **Rolprijs** is opgehaald om zo tot de definitieve prijs/kosten te komen.
   
   De volgende tabel illustreert de berekening van prijsopslagen.
  
| Rol        | Organisatie-eenheid    |Werklocatie      |Standaardtitel      |Werkuren van resource      |  Opslag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Op locatie            |                    |Overwerk                 |15     |
|             | Contoso India|Lokaal             |                    |Overwerk                 |10     |
|             | Contoso US   |Lokaal             |                    |Overwerk                 |20     |


Als een resource van Contoso India met een basistarief van USD 100 op locatie werkt en deze 8 uur van de reguliere werktijd en 2 uur overwerk bij de tijdsvermelding invoert, past de prijsengine het basistarief van USD 100 toe voor de 8 uur, voor een subtotaal van USD 800. Voor de 2 uur overwerk wordt een opslag van 15% toegepast op het basistarief van 100, wat een eenheidsprijs van USD 115 oplevert voor een subtotaal van USD 230.

### <a name="applicable-to-cost"></a>Van toepassing op kosten 
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de kosten- en opslagtarieven.

### <a name="applicable-to-sales"></a>Van toepassing op verkoop
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de facturerings- en opslagtarieven.

### <a name="applicable-to-purchase"></a>Van toepassing op inkoop
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de inkoopprijs. Scenario's waarin werk wordt uitbesteed, worden niet ondersteund, dus dit veld wordt niet gebruikt. 

### <a name="priority"></a>Prioriteit
Als u de dimensieprioriteit instelt, kan de prijsfunctie een prijs produceren, zelfs als geen exacte overeenkomst wordt gevonden tussen de ingevoerde dimensiewaarden en de waarden uit de tabellen **Rolprijs** en **Rolprijsopslag**. In dit scenario wordt null-waarden gebruikt voor niet-overeenkomende dimensiewaarden door de dimensies in volgorde van hun prioriteit te wegen.

- **Kostenprioriteit**: de waarde van de kostenprioriteit van een dimensie geeft de weging van die dimensie aan bij het vergelijken met de configuratie van kostprijzen. De waarde van **Kostenprioriteit** moet uniek zijn in alle dimensies die **van toepassing op kosten** zijn.
- **Verkoopprioriteit**: de waarde van de verkoopprioriteit van een dimensie geeft de weging van die dimensie aan bij het vergelijken met de configuratie van verkoopprijzen of factuurtarieven. De waarde van **Verkoopprioriteit** moet uniek zijn in alle dimensies die **van toepassing op verkoop** zijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]