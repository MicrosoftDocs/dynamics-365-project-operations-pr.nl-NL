---
title: Toewijzingsversies van twee keer wegschrijven voor Project Operations
description: Dit onderwerp biedt de lijst met kaarten voor twee keer wegschrijven die zijn vereist voor Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 385893e8ecdb29f4dc411c233b9ae19bb2448dfd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612744"
---
# <a name="project-operations-dual-write-map-versions"></a>Toewijzingsversies van twee keer wegschrijven voor Project Operations

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Het gebruik van Dynamics 365 Project Operations voor op resources/niet-voorraad gebaseerde scenario's is een set kaarten voor twee keer wegschrijven vereist om in de omgeving te worden uitgevoerd. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Vereiste kaarten: indelingsoplossing voor twee keer wegschrijven

De volgende kaarten zijn vereisten voor de Project Operations-oplossing. Zorg ervoor dat u de kaarten in de volgende tabel en alle gerelateerde tabeltoewijzingen in uw omgeving uitvoert.

| Tabeltoewijzing | Initiële synchronisatie |
| --- | --- |
| Grootboek (msdyn_ledgers) | Vereist initiële synchronisatie voor de tabeltoewijzing en alle vereisten. Master voor initiële synchronisatie is apps voor financiën en bedrijfsactiviteiten. |
| Rechtspersonen (cdm_companies) | Niet vereist. Het systeem vult deze entiteit automatisch in wanneer omgevingen worden gekoppeld met behulp van twee keer wegschrijven. |
| Klanten V3 (accounts) | Niet vereist voor inrichting. |
| Leveranciers V2 (msdyn_vendors) | Niet vereist voor inrichting. |

1. Selecteer in de lijst met toewijzingen de toewijzing **(msdyn\_ledgers)** met alle vereisten en schakel het selectievakje **Initiële synchronisatie** in. Selecteer in het veld **Master voor initiële synchronisatie** de optie **Finance and Operations-apps** voor zowel de grootboekkaart als alle vereiste kaarten. Selecteer **Uitvoeren**.

![Synchronisatie van grootboektoewijzing.](media/DW6.png)

2. Volg dezelfde stappen voor alle resterende tabeltoewijzingen die in de bovenstaande tabel worden vermeld. Schakel het selectievakje **Initiële synchronisatie** niet in bij het uitvoeren van die kaarten.

## <a name="project-operations-dual-write-maps"></a>Kaarten voor twee keer wegschrijven in Project Operations

De volgende kaarten zijn vereist voor een Project Operations-oplossing. Toewijzingsversies van twee keer wegschrijven met Project Operations mei 2021-update, versie 4.10.0.186.

| Entiteitstoewijzing | Nieuwste versie | Initiële synchronisatie | Vereiste versie van Dynamics 365 Finance |
| --- | --- | --- | --- |
| Integratie-entiteit voor projecttransactierelaties (msdyn\_transactionconnections) | 1.0.0.0 | Niet vereist voor inrichting. ||
| Projectcontractkoppen (verkooporders) | 1.0.0.1 | Niet vereist voor inrichting. ||
| Projectcontractregels (salesorderdetails) | 1.0.0.0 | Niet vereist voor inrichting. ||
| Bron voor projectfinanciering (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Niet vereist voor inrichting. ||
| Project Operations-integratietabel voor materiaalschattingen (msdyn\_estimatelines) | 1.0.0.0 | Niet vereist voor inrichting. ||
| Projectfactuurvoorstellen V2 (facturen) | 1.0.0.3 | Niet vereist voor inrichting. ||
| Werkelijke waarden voor integratie van Project Operations (msdyn_actuals) | 1.0.0.14 | Niet vereist voor inrichting. ||
| Mijlpalen voor projectcontractregels voor Project Operations-integratie (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Niet vereist voor inrichting. ||
| Project Operations-integratie-entiteit voor onkostenschattingen (msdyn_estimatelines) | 1.0.0.2 | Niet vereist voor inrichting. ||
| Entiteit voor tijdramingen van Project Operations-integratie (msdyn_resourceassignments) | 1.0.0.5 | Niet vereist voor inrichting. ||
| Entiteit voor exporteren van categorieën met projectonkosten voor Project Operations-integratie (msdyn_expensecategories) | 1.0.0.1 | Niet vereist voor inrichting. ||
| Entiteit voor exporteren van projectkosten voor Project Operations-integratie (msdyn_expenses) | 1.0.0.3 | Niet vereist voor inrichting. ||
| Entiteit voor exporteren van leverancierfacturen in Project Operations-integratieprojecten (msdyn_projectvendorinvoices) | 1.0.0.0 | Niet vereist voor inrichting. ||
| Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten (msdyn_projectvendorinvoicelines) | 1.0.0.4 | Niet vereist voor inrichting. | 10.0.26 of hoger |
| Rollen voor projectresources voor alle bedrijven (bookableresourcecategories) | 1.0.0.1 | Vereist een initiële synchronisatie voor de tabeltoewijzing om de resourcerollen van Projectmanager en Teamlid te synchroniseren die zijn ingevuld in de Dynamics 365 Dataverse omgeving tijdens het inrichten. Dataverse is de belangrijkste bron voor de initiële synchronisatie. ||
| Projecttaken (msdyn_projecttasks) | 1.0.0.4 | Niet vereist voor inrichting. ||
| Projecttransactiecategorieën (msdyn_transactioncategories) | 1.0.0.0 | Niet vereist voor inrichting. ||
| Projecten V2 (msdyn_projects) | 1.0.0.2 | Niet vereist voor inrichting. ||

Voer de volgende stappen uit om de weergegeven kaarten uit te voeren.

1. Schakel de Project-resourcerollen in voor de tabeltoewijzing **alle bedrijven (bookableresourcecategories)** aangezien deze map de initiële synchronisatie vereist. Selecteer in het veld **Model voor initiële synchronisatie** het veld **Common Data Service**. 

 ![Synchronisatie van de tabeltoewijzing voor resourcerollen.](media/6ResourceInitialSync.jpg)

 Wacht tot de status van de kaart **Actief** is voordat u naar de volgende stap gaat.

2. Selecteer alle resterende vereiste kaarten. U kunt ze filteren in de lijst met kaarten voor twee keer wegschrijven met behulp van het trefwoord **Project** bij zoeken in de rechterbovenhoek. U kunt alle kaarten meerdere keren selecteren en vervolgens uitvoeren. Zie [Meerdere tabeltoewijzingen beheren](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps) voor meer informatie. Zorg ervoor dat u ook gerelateerde entiteitstoewijzingen inschakelt en uitvoert.

### <a name="project-operations-dual-write-map-versions"></a>Toewijzingsversies van twee keer wegschrijven voor Project Operations

Voer altijd de meest recente versie van de kaart uit in uw omgeving. Bepaalde functies en mogelijkheden werken mogelijk niet correct als een van de volgende omstandigheden zich voordoet:

- Een kaart is niet geactiveerd.
- De meest recente versie van de kaart is niet geactiveerd. 
- Gerelateerde tabeltoewijzingen zijn niet geactiveerd.

U kunt de actieve versie van de kaart weergeven in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de kaart activeren door **Versies van tabeltoewijzing** te selecteren, de meest recente versie te kiezen en vervolgens de geselecteerde versie op te slaan. Als u een kant-en-klare tabeltoewijzing hebt aangepast, moet u de wijzigingen opnieuw toepassen. Zie [Beheer van de toepassingslevenscyclus](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management) voor meer informatie.
