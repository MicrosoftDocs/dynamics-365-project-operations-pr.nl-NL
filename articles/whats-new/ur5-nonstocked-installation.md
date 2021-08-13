---
title: Project Operations updaten in uw Finance-omgeving
description: Dit onderwerp bevat informatie over hoe u Project Operations updatet in uw Dynamics 365 Finance-omgeving.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3665bccfa25c759c0f2351c691d24901867c178f7c339f4a524856842666aec5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986755"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Project Operations updaten in uw Finance-omgeving

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_


Dit onderwerp bevat informatie over hoe u Dynamics 365 Project Operations updatet in uw Dynamics 365 Finance-omgeving. Er zijn drie procedures nodig om Project Operations te updaten naar Update 5 (UR5):

- [Het pakket importeren in uw preview-project](#import)
- [De update toepassen](#apply)
- [Uw Dataverse-omgeving updaten](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Het pakket importeren in uw LCS-project

1. Meld u aan bij [Lifecycle Services (LCS)](https://lcs.dynamics.com/) als projecteigenaar of omgevingsmanager.
2. Selecteer in de lijst met projecten uw LCS-project.
3. Open op de pagina **Project** in de groep **Omgevingen** de omgeving die u wilt updaten.
4. Controleer of de omgeving wordt uitgevoerd. Start de omgeving als deze niet is gestart.
5. Selecteer in de sectie **Nieuwe versie** onder **Beschikbare updates**, **Update weergeven** voor 10.0.15.

![Knop Update weergeven.](media/view-update.png)

6. Selecteer op de pagina **Binaire updates** **Pakket opslaan**.
7. Selecteer op de pagina **Updates beoordelen en opslaan** **Pakket opslaan**.
8. Voer in het deelvenster **Pakket opslaan in de assetbibliotheek** dat wordt geopend, de pakketnaam in en selecteer vervolgens **Pakket opslaan**.
9. Wanneer LCS het pakket heeft opgeslagen, wordt de knop **Gereed** ingeschakeld. Selecteer **Gereed**. LCS controleert het pakket. Verificatie kan enkele minuten of maximaal een uur duren.


## <a name="apply-the-package-update"></a><a name="apply"></a>De pakketupdate toepassen

1. Selecteer in LCS, op de pagina **Omgevingsgegevens** **Onderhouden** > **Updates toepassen**.
2. Selecteer in de lijst het pakket dat u eerder hebt opgeslagen en selecteer vervolgens **Toepassen**.
3. Selecteer **Ja** om te bevestigen dat u het pakket wilt implementeren.

![Dialoogvenster voor bevestigen van pakketimplementatie.](media/confirm-package-deployment.png)

4. Selecteer **Ja** om te bevestigen dat u de toepassing wilt updaten.

![Dialoogvenster voor bevestigen van toepassingsupdate.](media/confirm-application-update.png)

De implementatie en toepassingsupdate worden gestart. 

Op de pagina **Omgevingsgegevens** wordt in de rechterbovenhoek de omgevingsstatus bijgewerkt naar **Onderhoud**. Over ongeveer twee uur is de update voltooid. De versie-informatie van de toepassing wordt bijgewerkt naar **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** en de omgevingsstatus wordt bijgewerkt naar **Geïmplementeerd**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Uw Dataverse-omgeving updaten

1. Meld u aan bij het [Power Platform-beheercentrum](https://admin.powerplatform.com/).
2. Zoek en open in de lijst de omgeving die u hebt gebruikt om Project Operations te installeren.
3. Selecteer op de pagina **Omgevingen** **Resource** > **Dynamics 365-apps**.
4. Zoek in de lijst **Microsoft Dynamics 365 Project Operations** en selecteer in de kolom **Status** **Update beschikbaar**.
5. Schakel het selectievakje **Ik ga akkoord met de servicevoorwaarden** in en selecteer vervolgens **Bijwerken**. De nieuwste versie van de oplossing wordt geïnstalleerd.

Nadat de installatie is voltooid, hebt u versie 4.5.0.134 geïnstalleerd.

## <a name="configure-new-features"></a>Nieuwe functies configureren

### <a name="enable-dual-write-mapping"></a>Toewijzing van twee keer wegschrijven inschakelen

Nadat u de update in de Finance en Dataverse-omgevingen hebt afgerond, kunt u de vereiste toewijzingen voor twee keer wegschrijven inschakelen. Doorloop de volgend procedures om toewijzingen voor twee keer wegschrijven in te schakelen.

- [De beveiligingsinstellingen in de Customer Engagement-omgeving bijwerken](#security)
- [Gegevenseenheden vernieuwen](#refresh)
- [De toewijzingen voor twee keer wegschrijven bijwerken en uitvoeren](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>De beveiligingsinstellingen in de Dataverse-omgeving bijwerken

De volgende updates van de beveiligingsbevoegdheden voor entiteiten zijn vereist als onderdeel van de update naar UR5.

1. Ga in uw Dataverse-omgeving naar **Instellingen** en selecteer in de groep **Systeem** **Beveiliging**.

![Dataverse-omgevingsinstellingen.](media/Picture21.png)

2. Selecteer **Beveiligingsrollen**.
3. Selecteer uit de lijst met rollen **Twee keer wegschrijven app-gebruiker** en selecteer het tabblad **Aangepaste entiteiten**. 
4. Controleer of de rol de machtigingen **Lezen** en **Toevoegen aan** heeft voor:

      - **Type valutawisselkoers**
      - **Rekeningschema** 
      - **Fiscale kalender** 
      - **Grootboek**

5. Ga nadat de beveiligingsrol is bijgewerkt naar **Instellingen** > **Beveiliging** > **Teams**. Controleer of de rol **twee keer wegschrijven app-gebruiker** is toegepast op het team. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Gegevensentiteiten uit de update vernieuwen

1. Open in uw Finance-omgeving de werkruimte **Gegevensbeheer** en vervolgens de pagina **Framework-parameters**.
2. Selecteer op het tabblad **Entiteitsinstellingen** **Entiteitenlijst vernieuwen**.
3. Selecteer **Sluiten** om het vernieuwen van de entiteit te bevestigen.

 > [!NOTE]
 > Dit proces neemt ongeveer 20 minuten in beslag. U krijgt een melding wanneer het vernieuwen is voltooid.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Toewijzingen voor twee keer wegschrijven bijwerken

1. Selecteer in de werkruimte **Gegevensbeheer** **Twee keer wegschrijven**.
2. Selecteer **Oplossingen toepassen**, selecteer beide oplossingen in de lijst en selecteer vervolgens **Toepassen**.
3. Selecteer op de pagina **Twee keer wegschrijven** de volgende tabeltoewijzingen en selecteer vervolgens **Stoppen**.

    - **Werkelijke waarden voor integratie van Project Operations (msdyn_actuals)**
    - **Projectonkostencategorieën voor integratie van Project Operations (msdyn_expensecategories)**
    - **Werkelijke waarden voor projectonkosten exportentiteit voor integratie van Project Operations (msdyn_expensecategories)**

4. Pas op de pagina **Versie tabeltoewijzing** een nieuwe versie van de toewijzing toe op elk van de drie entiteiten.
5. Selecteer uitvoeren op de pagina **Twee keer wegschrijven** om de toewijzingen opnieuw op te starten.
6. Selecteer in de lijst met toewijzingen de toewijzing **Grootboek (msdyn_ledgers)** met alle vereisten en schakel het selectievakje **Eerste synchronisatie** in. 
7. Selecteer in het veld **Master voor eerste synchronisatie** **Finance and Operations-apps** en selecteer vervolgens **Uitvoeren**.
 
 ![Synchronisatie van grootboektoewijzing.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]