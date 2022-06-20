---
title: Verwijderde of afgeschafte functies in Dynamics 365 Project Operations
description: In dit artikel worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921480"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Verwijderde of afgeschafte functies in Dynamics 365 Project Operations

_**Geldt voor:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering, en Project Operations voor scenario's op basis van voorradige artikelen/productieorders_

In dit artikel worden de functies beschreven die zijn verwijderd of die zijn gepland voor verwijdering uit Dynamics 365 Project Operations.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *verouderde* functie wordt niet actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Deze lijst is bedoeld als hulpmiddel bij overwegingen over verwijderde en verouderde functies voor uw eigen planning.

> [!NOTE]
> Gedetailleerde informatie over objecten in apps voor financiën en bedrijfsactiviteiten is te vinden in de [**Rapporten met technische naslaginformatie**](/dynamics/s-e/global/axtechrefrep_61). U kunt de verschillende versies van deze rapporten vergelijken voor meer informatie over objecten die zijn gewijzigd of verwijderd in elke versie van apps voor financiën en bedrijfsactiviteiten.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Verwijderde of afgeschafte functies in de versie van Project Operations van maart 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projectbeheer- en boekhoudingsarameter "Altijd aanpassingstransactie maken"

| &nbsp; | &nbsp; |
|--------|--------|
| **Reden voor uitfasering/verwijdering** | Aanpassingstransacties zijn vereist voor controledoeleinden. Na afschaffing wordt deze parameter verborgen. Het systeem zal altijd aanpassingstransacties maken, net zoals op dit moment gebeurt wanneer de parameter is ingesteld op **Ja**. |
| **Vervangen door een andere functie?** | No |
| **Productgebieden waarop dit van invloed is** | Aanvraag |
| **Implementatieoptie** | Project Operations voor scenario's op basis van productie/voorradige artikelen |
| **-Status** | Afgeschaft: tegen 1 maart 2023 zullen we de parameter verbergen en het systeemgedrag wijzigen, zodat er altijd aanpassingstransacties worden gemaakt. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projectbeheer- en boekhoudingsparameter "Aanpassingsdatum gebruiken als nieuwe projectdatum"

| &nbsp; | &nbsp; |
|--------|--------|
| **Reden voor uitfasering/verwijdering** | Deze parameter werd oorspronkelijk gebruikt om aanpassingen mogelijk te maken wanneer een boekingsperiode was gesloten. Het is echter niet langer vereist, omdat de boekhouddatum van de transactie kan worden gewijzigd in de eerste datum van de open periode, als deze is geconfigureerd. De projectdatum mag niet worden gewijzigd, omdat deze de datum vertegenwoordigt waarop de transactie heeft plaatsgevonden. |
| **Vervangen door een andere functie?** | No |
| **Productgebieden waarop dit van invloed is** | Aanvraag |
| **Implementatieoptie** | Project Operations voor scenario's op basis van productie/voorradige artikelen |
| **-Status** | Afgeschaft: tegen 1 maart 2023 zullen we de parameter verbergen en het systeemgedrag wijzigen, zodat de projectdatum nooit wordt gewijzigd bij aanpassingen. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Werkstoorm voo resourceaanvraag in Project Operations voor scenario's op basis van voorradige artikelen/productieorders

| &nbsp; | &nbsp; |
|--------|--------|
| **Reden voor uitfasering/verwijdering** | Afgeschaft vanwege gering gebruik en beperkte transactievolumes. |
| **Vervangen door een andere functie?** | No |
| **Productgebieden waarop dit van invloed is** | Aanvraag |
| **Implementatieoptie** | Project Operations voor scenario's op basis van productie/voorradige artikelen |
| **-Status** | Afgeschaft: voor 1 maart 2023 zullen we de optie uitschakelen om resources voor het project aan te vragen via de werkstroom. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projectfactuurvoorstelpagina zonder weergaven Koptekst en Regels

| &nbsp; | &nbsp; |
|--------|--------|
| **Reden voor uitfasering/verwijdering** | Afgeschaft vanwege verbeteringen aan de pagina die samen met de functietoets **Formulieren voor projectfactuurvoorstel en factuurjournaal gebruiken met de weergave Koptekst en Regels** is geïntroduceerd. |
| **Vervangen door een andere functie?** | Ja |
| **Productgebieden waarop dit van invloed is** | Aanvraag |
| **Implementatieoptie** | Project Operations vvoor scenario's op basis van productie/voorradige artikelen; Project Operations voor scenario's op basis van resources/niet-voorradige artikelen |
| **-Status** | Afgeschaft: voor 1 maart 2023 zullen we de eerdere (verouderde) pagina uitschakelen en de functietoets **Formulieren voor projectfactuurvoorstel en factuurjournaal gebruiken met de weergave Koptekst en Regels** standaard inschakelen. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Verwijderde of afgeschafte functies in de versie van Project Operations van december 2021

### <a name="collaboration-workspaces"></a>Samenwerkingswerkruimten

[Een samenwerkingswerkruimte maken of er een koppeling naar maken (project)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Reden voor uitfasering/verwijdering** | Afgeschaft omdat het te weinig werd gebruikt. Klanten die Project Operations gebruiken voor scenario's op basis van resources/niet-voorradige artikelen kunnen gebruikmaken van [Samenwerking met Office-groepen](../project-management/collaboration-groups.md). |
| **Vervangen door een andere functie?** | No |
| **Productgebieden waarop dit van invloed is** | Aanvraag  |
| **Implementatieoptie** | Project Operations voor scenario's op basis van productie/voorradige artikelen |
| **-Status** | Afgeschaft: we zijn van plan om vanaf 1 december 2022 geen samenwerkingswerkruimten meer te ondersteunen. |
