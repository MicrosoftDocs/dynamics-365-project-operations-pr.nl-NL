---
title: Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen
description: Dit artikel bevat informatie over het abonneren op en implementeren van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920100"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_



In dit artikel wordt uitgelegd hoe u zich kunt abonneren op de proefversie en hoe u de Project Operations-omgeving kunt implementeren voor scenario's op basis van resources/niet-voorradige artikelen.

## <a name="prerequisites"></a>Vereisten
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant. U kunt een tenant maken tijdens de eerste inwisseling van de aanbieding. 
- Voor het implementeren van een Finance-omgeving is een geldig Azure-abonnement vereist dat per omgeving wordt gefactureerd. U kunt het bestaande abonnement van uw organisatie gebruiken of een [Azure-proefversie](https://azure.microsoft.com/free/) starten. De CDS-omgeving wordt gedurende een beperkte periode van 30 dagen gratis ter beschikking gesteld.

> [!IMPORTANT]
> Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.
> 
> Proefversies zijn voor eenmalig gebruik in de tenant. U kunt een proefversie maar één keer uitvoeren. We raden u aan een nieuwe tenant te maken voor de proefversie.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>Dynamics 365 Project Operations (CE) - preview-proefversie 

Voordat u begint, moet u ervoor zorgen dat u bent aangemeld bij een browser met de werkaccount van de gebruiker in de gewenste tenant voor de preview van Project Operations.

1. Hier kunt u de eerste aanbiedingscode voor **Dynamics 365 Project Operations** inwisselen [Project Operations-proefversie](https://aka.ms/try-po).
2. Bevestig uw order.

  U ziet dat de aanbieding voor bevestiging met succes is ingewisseld.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance preview-proefversie

Ga naar [Dynamics 365 for Finance Preview-proefversie](https://aka.ms/trypoche) en herhaal de stappen uit het vorige gedeelte met de aanbieding Aanmelden voor de cloudgehoste omgeving.  

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.

1. Ga naar het [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

3. Controleer of de **Dynamics 365 Project Operations**-licentie is geselecteerd en selecteer **Wijzigingen opslaan**.

> [!NOTE]
> De Finance-proefaanbieding hoeft niet aan een gebruiker te worden toegewezen.

## <a name="start-a-new-project-in-lcs"></a>Een nieuw project in LCS starten

Maak een nieuw LCS-project zoals beschreven in het artikel [Een nieuw project starten in LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Een Azure-abonnement toevoegen aan een LCS-project

Volg de stappen in het artikel [Een Azure-abonnement toevoegen aan een LCS-project](resource-add-azure-subscription-lcs-project.md) om deze taak te voltooien.

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementeer een Finance-demo-omgeving met Project Operations voor scenario's met resources/niet-voorradige artikelen

Volg de richtlijnen in het artikel [Een nieuwe omgeving inrichten](resource-provision-new-environment.md) om de implementatie te voltooien. Gebruik het implementatietype [demo-omgeving](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) voor preview. 

## <a name="install-cds-setup-and-configuration-data"></a>Gegevens voor CDS-installatie en configuratie installeren

Installeer CDS-instellings- en configuratiegegevens zoals beschreven in het artikel [Configuratiegegevens instellen en toepassen in de Common Data Service](resource-apply-pro-setup-config-data.md).
Voltooi deze stap pas nadat de demo-omgeving voor Finance is geïmplementeerd en de demogegevens gereed zijn.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
