---
title: Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over het abonneren op en inrichten van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a6dfa51f59119834230b7c9f8859a9d85eaae999
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642946"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp geeft aan hoe u zich abonneert op de preview-/partneraanbieding en hoe u de Project Operations-omgeving implementeert voor scenario's op basis van resources/niet-voorradige artikelen.

## <a name="prerequisites"></a>Vereisten

- U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview. U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.
- Voor het implementeren van een Finance-omgeving is een geldig Azure-abonnement vereist dat per omgeving wordt gefactureerd. U kunt het bestaande abonnement van uw organisatie gebruiken of een [Azure-proefversie](https://azure.microsoft.com/en-us/free/) starten. De CDS-omgeving wordt gedurende een beperkte periode van 30 dagen gratis ter beschikking gesteld.

## <a name="subscribe"></a>Abonneren

Wanneer uw [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) wordt goedgekeurd, ontvangt u drie aanbiedingen van Microsoft per e-mail. Met deze aanbiedingen kunt u de preview van Project Operations implementeren:

- Dynamics 365 Project Operations (CRM) - proefversie voor preview
- Office 365 Project Operations - proefversie voor preview
- Dynamics 365 Finance - proefversie voor preview

> [!IMPORTANT]
> Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - proefversie voor preview 

Voordat u begint, moet u ervoor zorgen dat u bent aangemeld bij een browser met de werkaccount van de gebruiker in de gewenste tenant voor de preview van Project Operations.

1. Wissel de eerste aanbiedingscode **Dynamics 365 Project Operations (CRM) - proefversie voor preview** in door de in de browser-URL te plakken.

![Aanbieding inwisselen](./media/16RedeemFirstOfferNew.png)

2. Bevestig uw order.

![De order bevestigen](./media/17ConfirmOrderNew.png)

U ziet dat de aanbieding voor bevestiging met succes is ingewisseld.

![Bevestiging](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - proefversie voor preview

Herhaal dezelfde stappen als bij de eerste aanbiedingscode. Zorg ervoor dat u de tweede aanbiedingscode toevoegt met dezelfde gebruikersaccount die is gebruikt bij de eerste aanbiedingscode.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-proefversie voor preview

Herhaal dezelfde stappen met de laatste aanbieding uit de welkomstmail.

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.

1. Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.

![Startpagina van het Beheercentrum](./media/14AdminPortal.png)

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

![Licenties toewijzen](./media/15AssignLicenses.png)

3. Controleer of de licentie voor **Dynamics 365 Project Operations (CRM) Preview** en **Office 365 Project Operations - Preview** is geselecteerd en selecteer **Wijzigingen opslaan**.

> [!NOTE]
> De Finance-proefaanbieding hoeft niet aan een gebruiker te worden toegewezen.

## <a name="start-a-new-project-in-lcs"></a>Een nieuw project in LCS starten

Maak een nieuw LCS-project zoals beschreven in het onderwerp [Een nieuw project starten in LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>Een Azure-abonnement toevoegen aan een LCS-project

Om deze taak te voltooien volgt u de stappen in het onderwerp [Een Azure-abonnement toevoegen aan het LCS-project](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>Implementeer een Finance-demo-omgeving met Project Operations voor scenario's met resources/niet-voorradige artikelen

Volg de richtlijnen in het onderwerp [Een nieuwe omgeving inrichten](resource-provision-new-environment.md) om de implementatie te voltooien. Gebruik het implementatietype [demo-omgeving](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) voor preview. 

## <a name="install-cds-setup-and-configuration-data"></a>Gegevens voor CDS-installatie en configuratie installeren

Installeer CDS-installatie- en configuratiegegevens zoals beschreven in het onderwerp [Configuratiegegevens instellen en toepassen in Common Data Service](resource-apply-pro-setup-config-data.md).
Voltooi deze stap pas nadat de demo-omgeving van Finance is geïmplementeerd en de demogegevens in FO gereed zijn.
