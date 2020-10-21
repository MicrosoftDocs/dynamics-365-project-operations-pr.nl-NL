---
title: Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen
description: Dit onderwerp bevat informatie over het abonneren op en inrichten van Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948822"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Aanmelden voor preview-abonnementen op Project Operations voor scenario's voor resources/niet-voorradige artikelen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Dit onderwerp geeft aan hoe u zich abonneert op de preview-/partneraanbieding en hoe u de Project Operations-omgeving implementeert voor scenario's op basis van resources/niet-voorradige artikelen.

## <a name="prerequisites"></a>Vereisten

- U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview. U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.
- Voor het implementeren van een Finance-omgeving is een geldig Azure-abonnement vereist dat per omgeving wordt gefactureerd. U kunt het bestaande abonnement van uw organisatie gebruiken of een [Azure-proefversie](https://azure.microsoft.com/en-us/free/) starten. De CDS-omgeving wordt gedurende een beperkte periode van 30 dagen gratis ter beschikking gesteld.

## <a name="subscribe"></a>Abonneren

Wanneer uw [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) wordt goedgekeurd, ontvangt u twee aanbiedingen van Microsoft per e-mail. Met deze aanbiedingen kunt u de preview van Project Operations implementeren:

- Dynamics 365 Project Operations, proefversie voor preview
- Dynamics 365 for Finance and Operations-proefversie voor preview.

> [!IMPORTANT]
> Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations, proefversie voor preview

1. Wissel de eerste aanbieding voor de **proefversie van Dynamics 365 Project Operations** in via de URL in uw welkomste-mail.

![Eerste aanbieding](./media/1FirstOffer.png)

2. Controleer of u bent aangemeld als de gebruiker die tot de organisatie behoort die zich op de service zal abonneren.
3. Ga verder met het inwisselen van de aanbieding. 
4. Selecteer **Ja, voeg het toe aan mijn account**.

![Aanbieding inwisselen](./media/2RedeemFirstOffer.png)

![Aanbieding bevestigen](./media/3ConfirmFirstOffer.png)

![Aanbieding ingewisseld](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance-proefversie voor preview

Herhaal dezelfde stappen met de tweede aanbieding uit de welkomstmail.

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Office 365-portal van uw organisatie om de volgende stappen te voltooien.

1. Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om licenties aan uw gebruikers toe te wijzen.

![Office-beheerportal](./media/5OfficeAdminPortal.png)

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

![Licenties toewijzen](./media/6AssignLicenses.png)

3. Controleer of de Project Operations-licentie is geselecteerd en selecteer **Wijzigingen opslaan**. 

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

