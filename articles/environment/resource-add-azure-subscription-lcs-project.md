---
title: Een Azure-abonnement toevoegen aan een LCS-project
description: Dit artikel bevat informatie over het verbinden van uw Azure-abonnement met een LCS-project.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 64ee8cfa7394a08c3d588c0e8f4a73185d9496cf
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912142"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>Een Azure-abonnement toevoegen aan een LCS-project

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Gehoste cloudomgevingen moeten worden geïmplementeerd met een bestaand Azure-abonnement. In dit artikel wordt uitgelegd hoe u uw bestaande Azure-abonnement kunt verbinden met een LCS-project. 

## <a name="grant-admin-consent"></a>Beheerderstoestemming verlenen

1. Selecteer in uw LCS-project in de sectie **Omgevingen** de optie **Microsoft Azure-instellingen**.

![Instellingen voor Microsoft Azure.](./media/1MicrosoftAzureSettings.png)

2. Op de pagina **Projectinstellingen** op het tabblad **Azure-connectors** selecteert u **Autoriseren**. Hierdoor kunnen omgevingen worden ingezet voor dit project.

![Azure-connectors.](./media/2AzureConnectors.png)

3. Selecteer opnieuw **Autoriseren** voor toestemming van de beheerder.

![Beheerderstoestemming verlenen.](./media/3GrantAdminConsent.png)

4. Accepteer het machtigingenverzoek.

![Machtigingsverzoek accepteren.](./media/4AcceptPermissionRequest.png)

De autorisatie is nu voltooid. 

![Autorisatie geslaagd.](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>Dynamics Deployment Services toegang geven tot uw Azure-abonnement

1. Ga naar [Facturering Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) en selecteer uw abonnement. Dynamics Deployment Services heeft toegang nodig tot dit abonnement om omgevingen te kunnen implementeren.

![Details van Azure-abonnement.](./media/6AzureSubscription.png)

2. Selecteer **Toegangsbeheer (IAM)** in het navigatiedeelvenster en selecteer vervolgens **Roltoewijzing toevoegen**.
3. Selecteer in de schuifregelaar aan de rechterkant **Rol van inzender** en zoek en selecteer in de weergegeven lijst **Dynamics Deployment Services**. 
4. Selecteer **Opslaan**.

![Toegang tot abonnement.](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Een abonnementsconnector toevoegen aan een LCS-project

1. In uw LCS-project op de pagina **Microsoft Azure-instellingen** selecteert u **Toevoegen** om een nieuwe connector toe te voegen.
2. Voer de id van uw Azure-abonnement in. U vindt uw Azure-abonnements-id in de [Azure-portal](https://ms.portal.azure.com/), onder **Instellingen** linksonder in het scherm.
3. In het veld **Configureer om Azure Resource Manager te gebruiken** selecteert u **Ja**.
4. Zorg ervoor dat het AAD-tenantdomein van het Azure-abonnement overeenkomt met het Azure-abonnement dat eigenaar is van het gebruikte domein en selecteer **Volgende**.
5. Selecteer in het scherm **Microsoft Azure instellen** **Volgende** om te bevestigen. Als u een foutmelding krijgt op dit scherm, gaat u terug naar de sectie [Dynamics Deployment Services toegang verlenen tot Azure-abonnement](#provide) in dit artikel en zorgt u ervoor dat u alle stappen hebt voltooid.
6. Download het Azure Management Certificate naar een lokale map op uw computer. Vraag uw Azure-abonnementsbeheerder om het certificaat te uploaden naar Azure Management Portal door het abonnement te selecteren en naar **Instellingen** > **Beheercertificaten** te gaan. Met dit certificaat kan LCS namens u communiceren met Azure. U kunt deze stap overslaan als uw gebruiker toegang heeft tot het abonnement.
7. Selecteer **Volgende**.
8. Selecteer de Azure-regio waarin u wilt implementeren en selecteer een datacenter bij de locatie waar u dit systeem wilt gebruiken.
9.  Selecteer **Verbinding maken**.

U hebt uw Azure-abonnement met succes verbonden. U kunt nu door de cloud gehoste omgevingen van Dynamics 365 Finance implementeren.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
