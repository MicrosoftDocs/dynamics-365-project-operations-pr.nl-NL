---
title: Aanmelden voor een preview-abonnement - lite
description: Dit artikel bevat informatie over het abonneren op en implementeren van Project Operations Lite-implementatie - van deal tot pro-formafacturering.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410005"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Aanmelden voor een preview-abonnement - lite 

In dit artikel wordt uitgelegd hoe u zich kunt abonneren op de proefversie en Dynamics 365 Project Operations Lite-implementatie - van deal tot pro-formafacturering kunt implementeren.

> [!NOTE]
> Dit proces zal veranderen in komende releases van Project Operations.

## <a name="prerequisites"></a>Vereisten
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant. U kunt een tenant maken tijdens de eerste inwisseling van de aanbieding.

> [!IMPORTANT]
> Slechts één persoon, de tenantbeheerder, in een organisatie mag deze taak uitvoeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.
> 
> Proefversies zijn voor eenmalig gebruik in de tenant. U kunt een proefversie maar één keer uitvoeren. We raden u aan een nieuwe tenant te maken voor de proefversie.

### <a name="dynamics-365-project-operations-trial"></a>Dynamics 365 Project Operations-proefabonnement 

Voordat u begint, moet u ervoor zorgen dat u bent aangemeld bij een browser met de werkaccount van de gebruiker in de gewenste tenant voor de preview van Project Operations.

1. Ga naar [Proefversie van Project Operations](https://aka.ms/try-po) voor inwisseling van de eerste aanbiedingscode, **Dynamics 365 Project Operations**.
2. Bevestig uw order.

  U ziet dat de bevestigingsaanbieding succesvol is ingewisseld.

## <a name="assign-licenses"></a>Licenties toewijzen

> [!IMPORTANT]
> U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.


1. Ga naar het [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.
2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.
3. Controleer of de **Dynamics 365 Project Operations**-licentie is geselecteerd. 
4. Selecteer **Wijzigingen opslaan**.

## <a name="create-a-new-dataverse-environment"></a>Een nieuwe Dataverse-omgeving maken

1. Richt een nieuwe Project Operations Dataverse-implementatieomgeving in door de instructies in het artikel [Dataverse-implementatiemodel](lite-deployment.md) te volgen. Zorg ervoor dat u **Proefversie (op basis van abonnement)** gebruikt als u het omgevingstype selecteert.

  ![Nieuwe omgeving.](./media/19CreateEnvironment.png)

2. Selecteer de instelling **Dynamics 365-apps inschakelen** en laat **Deze apps automatisch implementeren** leeg.  
3. Selecteer **Opslaan** om de omgeving te maken.

  ![Database toevoegen.](./media/20CreateEnvironment1.png)

4. Nadat de omgeving is gemaakt, installeert u de oplossing **Microsoft Dynamics 365 Project Operations**. 

![Oplossing installeren.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Demogegevens instellen

Stel demogegevens in door de instructies in het artikel [Demo-instellingen en configuratiegegevens toepassen](lite-apply-demo-setup-config-data.md) te volgen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
