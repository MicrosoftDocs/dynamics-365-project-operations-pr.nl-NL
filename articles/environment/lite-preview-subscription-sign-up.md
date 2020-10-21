---
title: Aanmelden voor een preview-abonnement
description: In dit onderwerp vindt u informatie over hoe u zich kunt abonneren op Project Operations Lite en hoe u dit kunt implementeren, van deal tot pro-formafacturering.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a9c1432e8971eeb7918e23e00be9989294335f49
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948819"
---
# <a name="sign-up-for-a-preview-subscription-for-lite-deployment--deal-to-proforma-invoicing"></a>Aanmelden voor een preview-abonnement voor lite-implementatie, van deal tot proforma-facturering

In dit onderwerp wordt beschreven hoe u zich kunt abonneren op het partneraanbod voor een preview, en hoe u Dynamics 365 Project Operations Lite kunt implementeren, van deal tot pro-formafacturering.

> [!NOTE]
> Dit proces zal veranderen in komende releases van Project Operations.

## <a name="prerequisites"></a>Vereisten

- U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview. U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.
- De gebruiker die de preview implementeert, heeft een telefoonnummer en een geldige creditcard nodig. Tijdens het aanmelden worden er zes maanden geen kosten in rekening gebracht op de kaart. Na zes maanden moet u het abonnement opzeggen. 
- Bekijk alle voorwaarden.

## <a name="subscribe"></a>Abonneren

Wanneer uw [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) wordt goedgekeurd, ontvangt u twee aanbiedingen van Microsoft per e-mail. Met deze aanbiedingen kunt u de preview van Project Operations implementeren:

- Proefversie voor Dynamics 365 Customer Service-preview: code voor eenmalig gebruik
- Dynamics 365 Project Operations, proefversie voor preview

### <a name="dynamics-365-customer-service-paid-offer"></a>Betaalde aanbieding voor Dynamics 365 Customer Service

1. Gebruik een InPrivate/Incognito-browservenster en wissel de eerste aanbiedingscode in voor Dynamics 365 Customer Service. Voor de registratie voor Customer Service hebt u het volgende nodig:

- Een telefoonnummer
- Een creditcard. Wanneer u zich aanmeldt, worden er zes maanden geen kosten in rekening gebracht op de kaart. Na zes maanden moet u het abonnement opzeggen.
- Bekijk alle voorwaarden.

2. Geef uw contactgegevens op.

![Contactpersoongegevens](./media/1ContactInformation.png)

3. Geef de nieuwe tenantgegevens op.

![Gebruikers-id maken](./media/2CreateUserID.png)

4. Verifieer uw identiteit, sla uw nieuwe gebruikers-id op en selecteer **Instellen**.

![Info opslaan](./media/3SaveInfo.png)

5. Voltooi de registratie van de creditcard en bekijk alle voorwaarden. 

![Creditcard voltooien](./media/4CompleteCreditCard.png)

![Creditcard uitchecken](./media/5CreditCardCheckout.png)

![Order opslaan](./media/6SaveOrder.png)

![Bevestiging van creditcard](./media/7Confirmation.png)

## <a name="cancel-the-dynamics-365-customer-service-enterprise-offer"></a>De aanbieding voor Dynamics 365 Customer Service Enterprise annuleren

De aanbieding voor Dynamics 365 Customer Service Enterprise is zes maanden gratis beschikbaar. Het aanbod wordt aan het einde van de periode van zes maanden tegen het volledige tarief verlengd. Voer de volgende instructies uit om te annuleren vóór de verlengingsdatum. 

> [!NOTE]
> Nadat u deze stappen hebt voltooid, kunt u de openbare preview-omgeving van Project Operations niet meer gebruiken.

1. Ga naar de [Beheerportal](https://admin.microsoft.com/) en selecteer onder **Facturering** **Uw producten**.

![Beheerportal, uw productenpagina](./media/8AdminPortal.png)

2. Selecteer **Aanbieding voor Dynamics 365 Customer Service Enterprise**.

![Abonnement annuleren](./media/9CancelSubscription.png)

3. Selecteer **Instellingen** > **Acties** > **Abonnement annuleren**.
4. Voer in het formulier **Abonnement opzeggen** de vereiste velden in.
5. Selecteer **Annuleren** > **Abonnement.**

### <a name="dynamics-365-project-operations--preview-trial"></a>Dynamics 365 Project Operations, proefversie voor preview

1. Wissel de tweede aanbieding voor de proefversie van Dynamics 365 Project Operations in via de URL in uw welkomste-mail.

![Aanbieding 2 inwisselen](./media/10RedeemOffer2.png)

2. Controleer of u bent aangemeld als de gebruiker die tot de organisatie behoort die met de eerste aanbiedingscode een abonnement heeft genomen, en ga vervolgens verder met het inwisselen van de aanbieding. 
3. Selecteer **Ja, voeg het toe aan mijn account**.

![Toevoegen aan account](./media/11AddToAccount.png)

![Scherm Probeer nu](./media/12TryNow.png)

![Orderdetails](./media/13Confirmation.png)

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Office 365-portal van uw organisatie om de volgende stappen te voltooien.

1. Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.

![Startpagina van het Beheercentrum](./media/14AdminPortal.png)

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

![Licenties toewijzen](./media/15AssignLicenses.png)

3. Controleer of licentie voor **Customer Service Enterprise** en **Project Operations** zijn geselecteerd en selecteer **Wijzigingen opslaan**.

## <a name="create-a-new-cds-environment"></a>Een nieuwe CDS-omgeving maken

Richt een nieuwe CDS-implementatieomgeving voor Project Operations in aan de hand van de instructies in het onderwerp [CDS-implementatiemodel](lite-deployment.md).

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-configuratie installeren en demogegevens instellen

Installeer de CDS-configuratie en stel demogegevens in aan de hand van de instructies in het onderwerp [Demogegevens voor installatie en configuratie toepassen](lite-apply-demo-setup-config-data.md).
