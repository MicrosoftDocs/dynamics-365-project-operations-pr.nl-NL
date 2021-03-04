---
title: Aanmelden voor een preview-abonnement - lite
description: In dit onderwerp vindt u informatie over hoe u zich kunt abonneren op Project Operations Lite en hoe u dit kunt implementeren, van deal tot pro-formafacturering.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6f4360b7febab57b97df0776ef9148d2a38f16a7
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175885"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Aanmelden voor een preview-abonnement - lite 

In dit onderwerp wordt beschreven hoe u zich kunt abonneren op het partneraanbod voor een preview, en hoe u Dynamics 365 Project Operations Lite kunt implementeren, van deal tot pro-formafacturering.

> [!NOTE]
> Dit proces zal veranderen in komende releases van Project Operations.

## <a name="prerequisites"></a>Vereisten

- U ontvangt een e-mail waarin u wordt uitgenodigd om deel te nemen aan de preview. U kunt een preview aanvragen op de [website van Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.
- Bekijk alle voorwaarden.

## <a name="subscribe"></a>Abonneren

Wanneer u een goedkeuring voor een [preview-aanvraag](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) ontvangt, krijgt u twee aanbiedingen van Microsoft per e-mail. Met deze aanbiedingen kunt u de preview van Project Operations implementeren:

- Dynamics 365 Project Operations (CRM) - proefversie voor preview
- Office 365 Project Operations - proefversie voor preview

> [!IMPORTANT]
> Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>Dynamics 365 Project Operations (CRM) - proefversie voor preview 

Voordat u begint, moet u ervoor zorgen dat u bent aangemeld bij een browser met de werkaccount van de gebruiker in de gewenste tenant voor de preview van Project Operations.

1. Wissel de eerste aanbiedingscode in, **Dynamics 365 Project Operations (CRM) - proefversie van preview** door deze in de browser-URL te plakken.

![Aanbieding inwisselen](./media/16RedeemFirstOfferNew.png)

2. Bevestig uw order.
![De order bevestigen](./media/17ConfirmOrderNew.png)

U ziet dat de aanbieding voor bevestiging met succes is ingewisseld.

![Bevestiging](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>Office 365 Project Operations - proefversie voor preview

Herhaal dezelfde stappen als bij de eerste aanbiedingscode. Zorg ervoor dat u de tweede aanbiedingscode toevoegt met dezelfde gebruikersaccount die is gebruikt bij de eerste aanbiedingscode.

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.


1. Ga naar [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.

![Startpagina van het Beheercentrum](./media/14AdminPortal.png)

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

![Licenties toewijzen](./media/15AssignLicenses.png)

3. Controleer of de licenties **Dynamics 365 Project Operations (CRM) - preview** en **Office 365 Project Operations - preview** zijn geselecteerd. 
4. Selecteer **Wijzigingen opslaan**.

## <a name="create-a-new-cds-environment"></a>Een nieuwe CDS-omgeving maken

1. Richt een nieuwe CDS-implementatieomgeving voor Project Operations in aan de hand van de instructies in het onderwerp [CDS-implementatiemodel](lite-deployment.md). Zorg ervoor dat u **Proefversie (op basis van abonnement)** gebruikt als u het omgevingstype selecteert.
![Nieuwe omgeving](./media/19CreateEnvironment.png)

2. Selecteer de instelling **Dynamics 365-apps inschakelen** en laat **Deze apps automatisch implementeren** leeg.  
3. Selecteer **Opslaan** om de omgeving te maken.

![Database toevoegen](./media/20CreateEnvironment1.png)

4. Nadat de omgeving is gemaakt, installeert u de oplossing **Microsoft Dynamics 365 Project Operations**. 

![Oplossing installeren](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS-configuratie installeren en demogegevens instellen

Installeer de CDS-configuratie en stel demogegevens in aan de hand van de instructies in het onderwerp [Demogegevens voor installatie en configuratie toepassen](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]