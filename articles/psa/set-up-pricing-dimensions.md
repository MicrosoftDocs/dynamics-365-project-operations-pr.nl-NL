---
title: Aangepaste velden instellen als prijsdimensies
description: Dit onderwerp bevat informatie over het instellen van aangepaste prijsdimensies.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
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
ms.openlocfilehash: 81f926e0aa209dd83f9b850c2342bd35a4f236c3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282462"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Aangepaste velden instellen als prijsdimensies 

[!include [banner](../includes/psa-now-project-operations.md)]

Voordat u begint, wordt er in dit onderwerp vanuit gegaan dat u de procedures hebt voltooid in de onderwerpen [Aangepaste velden en entiteiten maken](create-custom-fields-entities.md) en [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md). Als u deze procedures niet hebt voltooid, gaat u terug, voltooit u deze en keert u terug naar dit onderwerp. 

Dit onderwerp bevat informatie over het instellen van aangepaste prijsdimensies. In de webinterface van Project Service ziet u op de pagina **Parameters** in het tabblad **Op bedrag gebaseerde prijsdimensies** de records in de dimensie-entiteiten voor prijs. Standaard worden bij de installatie van Project Service twee rijen aangemaakt in het raster op dit tabblad:

- **msdyn_resourcecategory** (Rol)
- **msdyn_OrganizationalUnit** (Organisatie-eenheid)

> [!IMPORTANT]
> Verwijder deze rijen niet. Als u ze echter niet nodig hebt, kunt u ze niet toepasselijk maken in een specifieke context door de velden **Van toepassing op kosten**, **Van toepassing op verkoop** en **Van toepassing op inkoop** allemaal in te stellen op **Nee**. Als u deze kenmerkwaarden instelt op **Nee**, heeft dit hetzelfde effect als wanneer het veld niet als een prijsdimensie is ingesteld.

Als u een veld wilt laten fungeren als een prijsdimensie, moet het voldoen aan de volgende voorwaarden:

- Het is gemaakt als een veld in de entiteiten **Rolprijs** en **Opslag voor rolprijs**. Meer informatie over hoe u dit doet, vindt u in [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md).
- Het is gemaakt als een rij in de tabel **Prijsdimensie**. Voeg bijvoorbeeld prijsdimensierijen toe zoals weergegeven in de volgende afbeelding. 

![Rijen in Op bedrag gebaseerde prijsdimensies](media/Amt-based-PD.png)

U ziet dat Werkuren van resource (**msdyn_resourceworkhours**) is toegevoegd als een op toeslag gebaseerde dimensie en is toegevoegd aan het raster op het tabblad **Op opslag gebaseerde prijsdimensie**.

![Rijen in Op opslag gebaseerde prijsdimensies](media/Markup-based-PD.png)

> [!IMPORTANT]
> Elke wijziging in de prijsdimensiegegevens in deze tabel, of dit nu bestaande of nieuwe gegevens zijn, wordt alleen doorgevoerd in de bedrijfslogica voor prijzen van Project Service nadat de cache is vernieuwd. Het kan tot 10 minuten duren totdat de cache is vernieuwd. Wacht zo lang om de wijzigingen in de logica voor standaardwaarden voor prijzen te zien, die moet resulteren uit wijzigingen in de gegevens van de prijsdimensie.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Kenmerken van de tabel Prijsdimensies
De volgende secties geven informatie over de verschillende kenmerken in de tabel **Prijsdimensies**.

### <a name="pricing-dimension-name"></a>Naam van prijsdimensie
Deze waarde moet exact gelijk zijn aan de schemanaam van het veld dat wordt toegevoegd aan de tabel **Rolprijs** voor aangepaste prijsdimensies. Meer informatie over het toevoegen van velden aan de tabel **Rolprijs** vindt u in [Aangepaste velden toevoegen aan prijsinstellingen en transactie-entiteiten](field-references.md).

### <a name="type-of-dimension"></a>Type dimensie
Er zijn twee typen prijsdimensies:
  
  - **Op bedrag gebaseerde dimensies**: de dimensiewaarden van de invoercontext worden vergeleken met de dimensiewaarden op de regel **Rolprijs** en de prijs/kosten worden standaard rechtstreeks overgenomen uit de tabel **Rolprijs**.
  - **Op opslag gebaseerde dimensies**: dit zijn dimensies waarbij Project Service het volgende proces met 3 stappen doorloopt om de prijs/kosten op te halen.
 
    1. Project Service vergelijkt de niet op opslag gebaseerde dimensiewaarden van de invoercontext met de rolprijsregel om het basistarief op te halen.
    2. Project Service vergelijkt alle dimensiewaarden van de invoercontext met de regel **Opslag voor rolprijs** om een opslagpercentage op te halen.
    3. Project Service past het opslagpercentage uit de tweede stap toe op het basistarief dat is verkregen uit de tabel **Rolprijs** in de eerste stap, en komt zo tot de definitieve prijs/kosten.
   
   De volgende tabel illustreert de berekening van prijsopslagen.
  
| Rol        | Organisatie-eenheid    |Werklocatie      |Standaardtitel      |Werkuren van resource      |  Opslag|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Op locatie            |                    |Overwerk                 |15     |
|             | Contoso India|Lokaal             |                    |Overwerk                 |10     |
|             | Contoso US   |Lokaal             |                    |Overwerk                 |20     |


Als een resource van Contoso India met een basistarief van USD 100 op locatie werkt en deze 8 uur van de reguliere werktijd en 2 uur overwerk op de tijdsvermelding registreert, past de prijsengine van Project Service het basistarief van 100 toe voor de 8 uur, voor een subtotaal van USD 800. Voor de 2 uur overwerk wordt een opslag van 15% toegepast op het basistarief van 100, wat een eenheidsprijs van USD 115 oplevert voor een subtotaal van USD 230.

### <a name="applicable-to-cost"></a>Van toepassing op kosten 
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de kosten- en opslagtarieven.

### <a name="applicable-to-sales"></a>Van toepassing op verkoop
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de facturerings- en opslagtarieven.

### <a name="applicable-to-purchase"></a>Van toepassing op inkoop
Als dit is ingesteld op **Ja**, geeft dit aan dat de dimensiewaarde van de invoercontext moet worden gebruikt om de **Rolprijs** en de **Rolprijsopslag** te vergelijken bij het ophalen van de inkoopprijs. Momenteel biedt Project Service geen ondersteuning voor scenario's met uitbesteding, zodat dit veld niet wordt gebruikt. 

### <a name="priority"></a>Prioriteit
Als u de dimensieprioriteit instelt, kan de prijsfunctie van Project Service een prijs produceren, zelfs als geen exacte overeenkomst wordt gevonden tussen de ingevoerde dimensiewaarden en de waarden uit de tabellen **Rolprijs** en **Rolprijsopslag**. In dit scenario gebruikt Project Service null-waarden voor niet-overeenkomende dimensiewaarden door de dimensies in volgorde van hun prioriteit te wegen.

- **Kostenprioriteit**: de waarde van de kostenprioriteit van een dimensie geeft de weging van die dimensie aan bij het vergelijken met de configuratie van kostprijzen. De waarde van **Kostenprioriteit** moet uniek zijn in alle dimensies die **van toepassing op kosten** zijn.
- **Verkoopprioriteit**: de waarde van de verkoopprioriteit van een dimensie geeft de weging van die dimensie aan bij het vergelijken met de configuratie van verkoopprijzen of factuurtarieven. De waarde van **Verkoopprioriteit** moet uniek zijn in alle dimensies die **van toepassing op verkoop** zijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]