---
title: Een Azure-abonnement toevoegen aan een LCS-project
description: Dit onderwerp biedt informatie over hoe u uw Azure-abonnement kunt verbinden met een LCS-project.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e741f35f9b229d2897cec06054d91ae620397228
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175795"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Een Azure-abonnement toevoegen aan een LCS-project

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Gehoste cloudomgevingen moeten worden geïmplementeerd met een bestaand Azure-abonnement. Dit onderwerp wordt uitgelegd hoe u uw bestaande Azure-abonnement kunt verbinden met een LCS-project. 

## <a name="grant-admin-consent"></a>Beheerderstoestemming verlenen

1. Selecteer in uw LCS-project in de sectie **Omgevingen** de optie **Microsoft Azure-instellingen**.

![Instellingen voor Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. Op de pagina **Projectinstellingen** op het tabblad **Azure-connectors** selecteert u **Autoriseren**. Hierdoor kunnen omgevingen worden ingezet voor dit project.

![Azure-connectors](./media/2AzureConnectors.png)

3. Selecteer opnieuw **Autoriseren** voor toestemming van de beheerder.

![Beheerderstoestemming verlenen](./media/3GrantAdminConsent.png)

4. Accepteer het machtigingenverzoek.

![Machtigingsverzoek accepteren](./media/4AcceptPermissionRequest.png)

De autorisatie is nu voltooid. 

![Autorisatie geslaagd](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Dynamics Deployment Services toegang geven tot uw Azure-abonnement

1. Ga naar [Facturering Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) en selecteer uw abonnement. Dynamics Deployment Services heeft toegang nodig tot dit abonnement om omgevingen te kunnen implementeren.

![Details van Azure-abonnement](./media/6AzureSubscription.png)

2. Selecteer **Toegangsbeheer (IAM)** in het navigatiedeelvenster en selecteer vervolgens **Roltoewijzing toevoegen**.
3. Selecteer in de schuifregelaar aan de rechterkant **Rol van inzender** en zoek en selecteer in de weergegeven lijst **Dynamics Deployment Services**. 
4. Selecteer **Opslaan**.

![Toegang tot abonnement](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Een abonnementsconnector toevoegen aan een LCS-project

1. In uw LCS-project op de pagina **Microsoft Azure-instellingen** selecteert u **Toevoegen** om een nieuwe connector toe te voegen.
2. Voer de id van uw Azure-abonnement in. U vindt uw Azure-abonnements-id in de [Azure-portal](https://ms.portal.azure.com/), onder **Instellingen** linksonder in het scherm.
3. In het veld **Configureer om Azure Resource Manager te gebruiken** selecteert u **Ja**.
4. Zorg ervoor dat het AAD-tenantdomein van het Azure-abonnement overeenkomt met het Azure-abonnement dat eigenaar is van het gebruikte domein en selecteer **Volgende**.
5. Selecteer in het scherm **Microsoft Azure instellen** **Volgende** om te bevestigen. Als u op dit scherm een foutmelding krijgt, gaat u terug naar de sectie [Dynamics Deployment Services toegang geven tot uw Azure-abonnement](#provide) in dit onderwerp en voltooi alle stappen.
6. Download het Azure Management Certificate naar een lokale map op uw computer en upload het vervolgens naar Azure Management Portal via **Instellingen** > **Beheercertificaten**. Met dit certificaat kan LCS namens u communiceren met Azure. U kunt deze stap overslaan als uw gebruiker toegang heeft tot het abonnement.
7. Selecteer **Volgende**.
8. Selecteer de Azure-regio waarin u wilt implementeren en selecteer een datacenter bij de locatie waar u dit systeem wilt gebruiken.
9.  Selecteer **Verbinding maken**.

U hebt uw Azure-abonnement met succes verbonden. U kunt nu gehoste Dynamics 365 Finance-cloudomgevingen implementeren.


