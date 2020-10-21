---
title: Projectteamleden
description: Dit onderwerp bevat informatie over hoe u kunt werken met informatie, attributen en planning van projectteamleden.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f4941803c657fab55ee2702d9f58d6e333592889
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908031"
---
# <a name="project-team-members"></a>Projectteamleden

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Projectteamleden zijn de projectdeelnemers die het werk aan een project voltooien. Het doel van het raster met teamleden is om een lijst te bieden van benoemde resources die zich inzetten voor de opdracht, en algemene teamleden die plaatsvervangende resources zijn en later zullen worden ingevuld.

Vanuit het raster met teamleden hebben de projectmanager en de andere projectdeelnemers de mogelijkheid om te zien wie zich heeft ingezet voor het project. Ze kunnen ook een overzicht bekijken van hun boekingen, geplande inspanningen en individuele resourcetoewijzingen. Met het raster met teamleden kunnen projectmanagers resourcevereisten definiëren voor algemene teamleden en de boekingen van bestaande teamleden beheren.

De volgende tabel bevat de belangrijkste kenmerken van een projectteamlid.

| Veldnaam          | Beschrijving                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Toewijzingsmethode        | De toewijzingsmethode die wordt gebruikt om resources voor het project te boeken.                                                                         |
| Factureringstype             | Selecteer of het teamlid is geklassificeerd als factureerbaar.                                                                                                                                       |
| Boekbare resource        | De boekbare resource die is geselecteerd om de algemene resource te vervangen.                                                                                                                   |
| Verwijderingsstatus            | De verwijderingsstatus van het teamlid om bij te houden of er een verwijderingsaanvraag is verzonden naar PSS, en of PSS met succes en binnen het verwachte tijdvenster een respons terugstuurt. |
| Totale inspanning (uren)     | De totale inspanning van het teamlid voor de opdrachten.                                                                                                                         |
| Inspanning voltooid (uren) | De inspanning die door het teamlid wordt geleverd voor de opdrachten, wordt bijgehouden.                                                                                           |
| Resterende inspannen (uren) | De nog niet voltooide inspanning van het teamlid aan de opdrachten wordt bijgehouden.                                                                                    |
| Voltooien                   | De einddatum van het lidmaatschap van het resourceteam.                                                                                                                                            |
| Hard geboekte uren        | De werkelijk geboekte uren van het teamlid.                                                                                                                                                                |
| Naam van positie            | De naam die wordt gebruikt om de algemene resource aan te geven.                                                                                                                                   |
| Resource-eenheid          | De organisatie-eenheid van de resource die het werk uitvoert.                                                                                                                      |
| Projectfiatteur         | Selecteer of het teamlid tijd en onkosten kan goedkeuren.                                                                                                                     |
| Vereiste uren           | De vereiste uren van het teamlid uit vereiste voor teamleden.                                                                                                                       |
| - Rol                     | De rol die het teamlid vervult in dit team.                                                                                                                                |
| Beschrijving van positie     | Voer een beschrijving in van de rol van dit teamlid.                                                                                                                             |
| Zacht geboekte uren        | De voorlopig geboekte uren van het teamlid.                                                                                                                                                                 |
| Starten                    | De begindatum van het lidmaatschap van het resourceteam.                                                                                                                                          |

Vanuit het raster met teamledem kunnen de volgende acties worden ondernomen:

- **Boeken**: voor organisaties die gebruikmaken van de hybride boekingsmethode, stelt de boekactie gebruikers in staat een benoemde resource te boeken op basis van de vereisten die zijn gegenereerd door het algemene teamlid
- **Vereiste genereren**: deze actie genereert de vereiste.
- **Patroon specificeren**: hiermee kunnen projectmanagers de contouren van resourcevereisten op gedetailleerd niveau aanpassen. Projectmanagers kunnen zich aanpassen aan de specifieke behoeften van het project in gevallen waarin de standaarddistributie niet past.
- **Aanvraag indienen**: voor organisaties die de centrale boekingsmethode gebruiken.
- **Bewerken**: teamlidkenmerken kunnen worden bewerkt, inclusief organisatie-eenheid, rol en positienaam.
- **Boekingen bijhouden**: wanneer boekingen van resources moeten worden bijgewerkt, kan de projectmanager door het bijhouden van boekingen het volgende aanpassen:

    - Starten
    - End
    - Totale inspanningstoewijzing

- **Nieuw**: naast het rechtstreeks toevoegen van resources vanuit de planning, kunnen projectmanagers nieuwe benoemde of generieke teamleden toevoegen vanuit het teamlidraster.
- **Verwijderen**: door een of meerdere teamleden te selecteren kan de projectmanager resources verwijderen die niet langer aan het project zullen deelnemen. Als u een teamlid verwijdert, worden ook alle bijbehorende resourcetoewijzingen verwijderd en worden alle bestaande boekingen geannuleerd.
