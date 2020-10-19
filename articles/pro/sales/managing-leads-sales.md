---
title: Potentiële klanten beheren (Pro)
description: In dit onderwerp krijgt u informatie over beheren van potentiële klanten op basis van projecten (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 005e36811643b0b1e98a686792cf39125ae97949
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896320"
---
# <a name="manage-leads-pro"></a>Potentiële klanten beheren (Pro)

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

Projectgebaseerde potentiële klanten kunnen worden beheerd en gekwalificeerd in Project Operations. Het proces van leadbeheer omvat het maken van op werk gebaseerde potentiële klanten en het kwalificeren van die potentiële klanten. 

## <a name="list-of-project-sales-leads"></a>Lijst met potentiële klanten voor projectverkoop

Open in het gedeelte **Verkoop** in het linkernavigatievenster de lijstpagina **Potentiële klanten** om een lijst met alle records met potentiële klanten in het systeem te bekijken. De weergegeven lijst met potentiële klanten zijn werkgebaseerde en andere soorten potentiële klanten die kunnen worden gemaakt als u ook beschikt over de Dynamics 365 Sales- of Dynamics 365 Field Service-toepassingen.

U kunt een gefilterde weergave maken om alleen projectgebaseerde potentiële klanten te zien door een filter te maken op de waarde bij **Type**. U kunt er bijvoorbeeld voor kiezen om alleen werkgebaseerde potentiële klanten weer te geven.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Een nieuwe potentiële klant creëren voor een projectmatige deal

Wanneer een projectgebaseerde potentiële klant in aanmerking komt, worden een verkoopkans en een account aangemaakt. Een projectgebaseerde verkoopkans is het startpunt voor verkoopactiviteiten in de fase Verkoopkans. Projectgebaseerde verkoopkansen bieden unieke mogelijkheden die nodig zijn om projectwerk te verkopen. Het gaat om deze mogelijkheden:

- Factureringsmethoden Tijd en materiaal en Vaste prijs
- Effectieve prijslijsten met ingangsdatums voor personeelszaken, uitgaven en materiaal voor projecten.

Als u wilt dat voor een gekwalificeerde potentiële klant automatisch een verkoopkans wordt gemaakt, stelt u het kenmerk **Type** in op **Werkgebaseerd** wanneer u de potentiële klant maakt. Als u een ander type kiest, zal voor de potentiële klant geen projectgebaseerde verkoopkans worden gemaakt wanneer deze wordt gekwalificeerd. Als de projectgebaseerde mogelijkheid niet wordt gecreëerd, zijn de projectspecifieke voorzieningen niet beschikbaar in de downstream-verkoopprocessen.

De volgende tabel bevat belangrijke veldinformatie voor een potentiële klant en voor downstream-implicaties van die velden.

| **Veld** | **Locatie** | **Relevantie, doel en richtlijnen** | **Downstreamimpact** |
| --- | --- | --- | --- |
| Onderwerp | Tabblad Algemeen | Dit tekstveld moet een korte beschrijving van de deal bevatten. | Het onderwerp van de potentiële klant wordt standaard het onderwerp van de verkoopkans, en de naam van de prijsopgave en het projectcontract. |
| Type | Tabblad Algemeen | Deze optieset heeft de volgende opties:</br>- Op werk gebaseerd (alleen beschikbaar als Project Operations is geïnstalleerd)</br>- Op artikel gebaseerd (alleen beschikbaar als Project Operations en Sales zijn geïnstalleerd)</br>- Op onderhoud gebaseerd (beschikbaar wanneer Field Service is geïnstalleerd) | Als de waarde van dit veld is ingesteld op **Werkgebaseerd** voor de potentiële klant, is deze gekwalificeerd om een projectgebaseerde verkoopkans te creëren. Er is een projectgebaseerde verkoopkans vereist om alle projectspecifieke uitbreidingen en functionaliteit in het downstream-verkoopproces voor deze deal in te schakelen. |
| Voornaam | Tabblad Algemeen | Voornaam van de contactpersoon van de prospect. | Wanneer de potentiële klant in aanmerking komt, worden een account, een contactpersoon en een verkoopkans aangemaakt. De voornaam van de contactpersoon is de hier ingestelde waarde. |
| Achternaam | Tabblad Algemeen | Achternaam van de contactpersoon van de prospect. | Wanneer de potentiële klant in aanmerking komt, worden een account, een contactpersoon en een verkoopkans aangemaakt. De achternaam van de contactpersoon is de hier ingestelde waarde. |
| Bedrijf | Tabblad Algemeen | Naam van het bedrijf van de prospect | Wanneer de potentiële klant in aanmerking komt, worden een account, een contactpersoon en een verkoopkans aangemaakt. De voornaam van het gemaakte account is de hier ingestelde waarde. |
| Valuta | Tabblad Details | Valuta van prospect | Wanneer de potentiële klant in aanmerking komt, worden een account, een contactpersoon en een verkoopkans aangemaakt. De valuta van het gemaakte account is de hier ingestelde waarde. |

## <a name="qualify-a-new-project-based-lead"></a>Een nieuwe projectgebaseerde potentiële klant kwalificeren

Potentiële klanten waarvoor de waarde **Type** is ingesteld op **Werkgebaseerd** worden projectgebaseerde potentiële klanten genoemd. Wanneer een projectgebaseerde potentiële klant wordt gekwalificeerd, wordt het volgende gemaakt:

- Een account dat het veld **Bedrijf** gebruikt van de potentiële klant.
- Een contactpersoonrecord die aan het account wordt gekoppeld op basis van de waarden in de velden **Voornaam** en **Achternaam** voor de potentiële klant.
- Een projectgebaseerde verkoopkans met het veld **Type** ingesteld op &quot;**Werkgebaseerd**.

Zie [Potentiële klanten kwalificeren of converteren](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales) voor meer informatie over in aanmerking komende potentiële klanten.

## <a name="business-process-flow-for-project-based-deals"></a>Bedrijfsprocesstroom voor projectgebaseerde deals

De volgende bedrijfsprocesstromen worden ondersteund voor projectgebaseerde deals in Project Operations:

- Potentiële klant naar bedrijfsproces voor verkoopkans
- Verkoopproces verkoopkans

Het bedrijfsproces Potentiële klant naar verkoopkans ondersteunt de volgende fasen:

| Fasenaam | Toegewezen entiteit | Functionaliteit |
| --- | --- | --- |
| Kwalificeren | Lead | Kwalificeer de potentiële klant om een een account, contactpersoon en verkoopkans te maken. |
| Ontwikkelen | Kans | Ontwikkel de verkoopkans om meer informatie toe te voegen over het betrokken werk, de belanghebbenden en de concurrentie. |
| Voorstel | Kans | Ontwikkel het voorstel en verkrijg goedkeuring van het interne beoordelingsteam. |
| Afsluiten | Kans | Haal de verkoopkans binnen om de deal te sluiten. |
