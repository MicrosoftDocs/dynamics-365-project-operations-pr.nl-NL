---
title: Aanmelden voor proefversie van Project Operations
description: Dit onderwerp bevat informatie over het implementeren van een proefversie van Dynamics 365 Project Operations.
author: ruhercul
ms.date: 01/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: a0c2532370c99cfe75b54da42c329f5b244a47e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584268"
---
# <a name="sign-up-for-project-operations-trials"></a>Aanmelden voor proefversie van Project Operations 

_**Geldt voor:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering, Project Operations voor scenario's op basis van voorradige artikelen/productieorders_ 



In dit onderwerp wordt uitgelegd hoe u zich kunt abonneren op de preview-partneraanbieding en hoe u een Dynamics 365 Project Operations-omgeving implementeert.

Met de nieuwe proefversie van Project Operations kunt u automatisch een van de drie ondersteunde implementatiescenario's implementeren door een vragenlijst op basis waarvan de beste implementatieaanpak wordt aanbevolen. In dit onderwerp krijgt u informatie over hoe u het volgende doet:

- Uw proefaanbieding inwisselen.
- Inrichting starten.
- Twee keer wegschrijven configureren.
- Meer te weten komen over Project Operations. 

De volgende tabel biedt een overzicht van de details van de nieuwe proefaanbieding.

| **Aanbiedingsitem**               | **DETAILS**                                  |
|------------------------------|----------------------------------------------|
| Type aanbieding                   | Dit aanbiedingstype is Beheerder potentiële klant, dus een tenantbeheerder is vereist om in te wisselen. |
| Gebruik van aanbieding                    | Eén keer per huurder                          |
| Aanbiedingsduur               | 30 kalenderdagen                             |
| Inwisselingen per tenant       | 0                                            |
| Toestel                    | 1 verlenging, 30 kalenderdagen               |
| Aantal proefomgevingen | 3                                            |


## <a name="admin-trial-details"></a>Details proefversie beheerder
De volgende tabel bevat de details van de proefversie en hoe deze van toepassing zijn op elk implementatietype.

| **Artikel**                      | **Lite**                                     | **Niet-voorradig materiaal** | **Voorradig materiaal** |
|-------------------------------|----------------------------------------------|---------------------------|-----------------------|
| Instellingsgegevens verstrekt           | Ja                                          | Ja                       | Ja (USSI)            |
| Transactionele gegevens            | Geen                                           | Geen                        | Geen                    |
| Inrichtingstijd in minuten  | 15                                           | 90                        | 30                    |
 
## <a name="prerequisites"></a>Vereisten
Als u een proefversie van Dynamics 365 Project Operations wilt implementeren, gelden de volgende vereisten.

- Registreer u voor de [preview-proefversie van Dynamics 365 Project Operations](https://www.aka.ms/try-po).
- De gebruiker die de preview implementeert, moet algemene beheerderrechten hebben voor de Azure-tenant.

> [!IMPORTANT]
> Slechts één persoon in een organisatie, de tenantbeheerder, hoeft deze taak uit te voeren. Als u niet de abonnee van deze release bent, wacht dan tot uw organisatie is aangemeld en u uw gebruikersgegevens hebt ontvangen.

### <a name="dynamics-365-project-operations---preview-trial"></a>Dynamics 365 Project Operations - preview-proefversie 

Voordat u begint, meldt u zich aan via een browser met de gebruikerswerkaccount in de tenant waar u de preview van Project Operations wilt gebruiken.

1. Wissel de eerste aanbiedingscode **Dynamics 365 Project Operations - proefversie voor preview** in door deze in de browser-URL te plakken.

    ![Aanbieding inwisselen](./media/16RedeemFirstOfferNew.png)

2. Bevestig uw order.

    ![De order bevestigen](./media/17ConfirmOrderNew.png)

  U ziet dat de bevestigingsaanbieding is ingewisseld.

   ![Bevestiging](./media/18OrderConfirmationNew.png)

  U wordt omgeleid naar het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/projectoperationstrial).

## <a name="questionnaire-and-provisioning"></a>Vragenlijst en inrichting

1.  Ga naar het [Power Platform-beheercentrum](https://admin.powerplatform.com/projectoperationstrial) en vul de vragenlijst in.  
2.  Bekijk het aanbevolen implementatietype en selecteer **Installatie starten** om de inrichting te starten.
3.  Bekijk de algemene voorwaarden en selecteer vervolgens **Starten**.

   Nadat de inrichting is gestart, wordt u omgeleid naar de omgevingslijst in het Power Platform-beheercentrum. Terwijl de inrichting wordt uitgevoerd, is de status van uw omgeving **PreparingInstance**.
 
  Wanneer de inrichting is voltooid, is de status van uw omgeving **Gereed**. Het inrichten van de omgeving omvat het implementeren van demogegevens.
 
4.  Selecteer de respectievelijke URL voor Microsoft Dataverse en de URL's voor apps voor financiën en bedrijfsactiviteiten om de implementatie te valideren.

## <a name="configuring-dual-write"></a>Twee keer wegschrijven configureren
- Zie voor het configureren van beveiligingsrollen voor twee keer wegschrijven: [Beveiligingsinstellingen bijwerken in Project Operations in Dataverse](resource-provision-new-environment.md).
- Zie [toewijzingen voor twee keer wegschrijven van Project Operations uitvoeren](resource-provision-new-environment.md#run-project-operations-dual-write-maps) om toewijzingen voor twee keer wegschrijven te configureren.

## <a name="assign-licenses"></a>Licenties toewijzen

U hebt toegang als beheerder nodig tot de Microsoft 365-portal van uw organisatie om de volgende stappen te voltooien.

1. Ga naar het [Microsoft 365-beheercentrum](https://portal.office.com/) om de licenties aan uw gebruikers toe te wijzen.

   ![Startpagina van het Beheercentrum](./media/14AdminPortal.png)

2. Selecteer op de pagina **Actieve gebruikers** de gebruikers waaraan u een licentie wilt toewijzen.

   ![Licenties toewijzen](./media/15AssignLicenses.png)

3. Controleer of de licentie voor de **Dynamics 365 Project Operations-preview** is geselecteerd en selecteer **Wijzigingen opslaan**.

## <a name="additional-resources"></a>Aanvullende bronnen

De volgende bronnen bieden nuttige begeleiding bij het begin van uw reis met Project Operations:

- [Videoserie - Overzicht van Project Operations, informatie over functies en roadmap](https://youtube.com/playlist?list=PLcakwueIHoT_LJ3Fr1tHnkPk5lioqE6uH)
- [Dynamics 365 Project Operations](/learn/modules/examine-dynamics-365-project-operations/)
- [Het type implementatie bepalen](determine-deployment-type.md)

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="what-if-i-require-alm-or-elm-for-my-finance-and-operations-apps-environment"></a>Wat moet ik doen als ik ALM of ELM nodig heb voor mijn omgeving voor apps voor financiën en bedrijfsactiviteiten?

- Zie voor partners die volledige levenscyclusbeheermogelijkheden voor de omgeving nodig hebben [Verzoek om sandbox-licentie van partner](https://experience.dynamics.com/requestlicense) om het nieuwe partneraanbod te bekijken. 
- Zie voor partners die meer informatie willen over interne gebruiksrechten [Cloud voor rechten voor intern gebruik en softwarevoordeel (microsoft.com](https://partner.microsoft.com/membership/internal-use-software).

### <a name="can-i-extend-my-trial-beyond-30-days"></a>Kan ik mijn proefperiode na 30 dagen verlengen?
Voer de volgende stappen uit om uw proefperiode te verlengen.

1. Ga in het **Microsoft 365-beheercentrum** naar **Facturering** > **Uw producten**.
2. Selecteer **Dynamics 365 Project Operations (CE) - preview-proefversie**.
3. Selecteer onder **Vervaldatum** de optie **Datum verlengen**.

### <a name="can-i-upgrade-from-the-lite-deployment-to-the-resourcenon-stocked-based-scenario-deployment"></a>Kan ik upgraden van de Lite-implementatie naar een scenario-implementatie op basis van resources/niet-voorradige artikelen?
Momenteel is er geen ondersteuning voor het upgraden van een omgeving van een Lite-implementatie naar een implementatie zonder voorraad.

### <a name="can-i-access-lifecycle-services-lcs-for-my-finance-environments"></a>Kan ik toegang krijgen tot Lifecycle Services (LCS) voor mijn Finance-omgevingen?  
Nee Voor deze proefversies wordt de implementatie afgehandeld via het Power Platform-beheercentrum. De toegang tot de Finance-omgeving is beperkt.

### <a name="can-i-install-my-trial-on-an-existing-environment"></a>Kan ik mijn proefversie installeren in een bestaande omgeving?
Als u een bestaande omgeving hebt, mag u de Lite-implementatie installeren in een bestaande Dataverse-verkoopomgeving vanuit het Power Platform-beheercentrum.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
