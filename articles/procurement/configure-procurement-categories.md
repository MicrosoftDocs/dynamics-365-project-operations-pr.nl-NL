---
title: Inkoopcategorieën gebruiken met projectinkooporders en openstaande leveranciersfacturen
description: In dit artikel wordt beschreven hoe u inkoopcategorieën configureert die kunnen worden gebruikt met projectinkooporders en openstaande leveranciersfacturen.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7d774631a4712de9b29ddedfee2ea3fc4a2d436f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927414"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Inkoopcategorieën gebruiken met projectinkooporders en openstaande leveranciersfacturen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Inkoopprofessionals kunnen catalogi van artikelen en services maken en onderhouden die kunnen worden gebruikt in projectinkooporders en in behandeling zijnde leveranciersfacturen. [Inkoopcatalogi](/dynamics365/supply-chain/procurement/procurement-catalogs) bieden u een gemakkelijke manier om aankopen te categoriseren zonder dat u een vrijgegeven productcatalogus hoeft te configureren en te gebruiken. Elke inkoopcategorie kan worden toegewezen aan een projectcategorie voor tijd-, onkosten- of artikeltransacties. Nadat een openstaande leveranciersfactuur die een inkoopcategorie gebruikt, is geboekt, maakt het systeem werkelijke projectwaarden voor tijd, onkosten of materiaal, projecttransacties en posten in de subadministratie aan.

## <a name="minimum-version-requirements"></a>Minimaal vereiste versie

De volgende versies zijn vereist om inkoopcategorieën te kunnen gebruiken met projectinkooporders voor Microsoft Dynamics 365 Project Operations-scenario's op basis van resources/niet-voorradige artikelen:

- Project Operations Dataverse-oplossingsversie 4.41.0.45 of hoger
- Omgeving voor financiën en bedrijfsactiviteiten versie 10.0.26 of hoger

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Toewijzingen voor twee keer wegschrijven uitvoeren voor ondersteuning van inkoopcategorieën

Zorg ervoor dat de toewijzing voor **Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten msdyn\_projectvendorinvoicelines** gebruikmaakt van versie 1.0.0.4 of hoger.

## <a name="enable-the-feature-key-for-procurement-categories"></a>De functiesleutel voor inkoopcategorieën inschakelen

Volg deze stappen om de functionaliteit voor het gebruik van inkoopcategorieën met projectinkooporders in te schakelen.

1. Open in Dynamics 365 Finance de werkruimte **Functiebeheer**.
1. Zoek en selecteer in de functielijst de functie **Inkoopcategorieën gebruiken in Project Operations voor op resources gebaseerde/niet-voorraadscenario's** en selecteer vervolgens **Inschakelen**.

> [!IMPORTANT]
> Als voorwaarde moet u ook de functie **In behandeling zijnde leveranciersfacturen inschakelen in Project Operations voor op resources gebaseerde/niet-voorraadscenario's** inschakelen.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Projectcategorieën toewijzingen in de hiërarchie van inkoopcategorieën

Volg deze stappen om projectcategorieën toe te wijzen aan inkoopcategorieën in de de hiërarchie **Inkoopcategorie**:

1. Ga naar **Inkoop en sourcing \> Inkoopcategorieën**.
1. Selecteer **Categoriehiërarchie bewerken**.
1. Selecteer het gewenste categoriehiërarchieknooppunt en koppel vervolgens, op het tabblad **Projectcategorieën toewijzen** het knooppunt aan de projectcategorie uit de categorie **Tijd**, **Onkosten** of **Artikelproject** (dat wil zeggen de categorie **Standaardtijd** of **Standaardkosten**).
1. Selecteer **Save**.
1. Sluit de pagina.

> [!NOTE]
> Het toewijzen van een inkoopcategorie aan een projectcategorie is optioneel. Als een inkoopcategorie niet is toegewezen, gebruikt het systeem de waarde die is ingesteld in het veld **Artikel** veld in de sectie **Standaardinstellingen projectcategorie** op het tabblad **Project Operations in Dynamics 365 Customer Engagement** van de pagina **Projectbeheer- en boekhoudingsparameters**.
