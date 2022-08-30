---
title: Projectstatus synchroniseren om toegang tot gesloten projecten te voorkomen
description: In dit artikel wordt uitgelegd hoe u de projectstatus kunt synchroniseren om toegang tot inactieve of gesloten projecten te voorkomen.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348003"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Projectstatus synchroniseren om toegang tot gesloten projecten te voorkomen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

## <a name="scenario"></a>Scenario

Contoso is live met Microsoft Dynamics 365 Project Operations voor scenario's op basis van resources/niet-voorradige artikelen. Als onderdeel van de normale bedrijfsactiviteiten kunnen projecten worden afgerond of on hold worden gezet. U kunt het project deactiveren om ervoor te zorgen dat er geen onkosten of facturen worden gegenereerd.

## <a name="solution"></a>Oplossing

### <a name="prerequisites"></a>Vereisten

-   Microsoft Dynamics 365 Finance 10.0.29 of hoger moet zijn geïnstalleerd.
-   De toewijzing Twee keer wegschrijven 1.0.0.3 voor projecten V2 (msdyn\_projecten) moeten worden geïnstalleerd of handmatig worden geconfigureerd zoals hieronder beschreven.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Een bijgewerkte versie maken van de toewijzing voor twee keer wegschrijven van Projecten V2 voor Project Operations-integratie

Als u de toewijzing voor twee keer wegschrijven van Projecten V2 voor Project Operations wilt bijwerken:

1. Ga naar de werkruimte **Gegevensbeheer** en selecteer **Twee keer wegschrijven**.
2. Selecteer de tegel **Twee keer wegschrijven**.
3. in de kolom T **Tabeltoewijzign**, zoek en selecteer **Project V2 (msdyn\_projecten)** en selecteer vervolgens Stoppen.
4. Selecteer de naam van de toewijzing om de toewijzing te openen en selecteer vervolgens **[Geen]**.
5. Selecteer in het dialoogvenster Kolom selecteren: **statuscode\[Projectstatus\]** en selecteer vervolgens OK. U kunt **status** in de filterwaarde typen om de lijst te verkleinen.
6.  Selecteer **Transformeren toevoegen of bewerken** in de kolom **toewijzingstype** om de transformatie te bewerken.
7.  Selecteer in het veld **Transformatietype** de optie **ValueMap**.
8.  Selecteer **Waardetoewijzing toevoegen** en voeg vervolgens het volgende toe: **Sleutels** en **Waarden**:

   Key       | Weergegeven als 
   ----------|-------
   In uitvoering | 0     
   Voltooid | 0     

![Schermopname met Twee keer wegschrijven toewijzing](media/projectstage-dw-mapping.png)

9. Selecteer **Save**.
10. Selecteer aan de bovenkant van de pagina **Twee keer wegschrijven > Projecten V2 (msdyn_projects)** de optie **Opslaan als**.
11. Selecteer vanuit **Tabel toevoegen** in het veld **Uitgever** de optie **CDS-Standaarduitgever**.
12. Stel het veld **Versie** in op 1.0.0.3.
13. Typ een **Description** en selecteer vervolgens **Opslaan**.
14. Selecteer bovenaan de pagina **Twee keer toeschrijven > Projecten V2 (msdyn_projects)** de optie **Uitvoering** om de toewijzing te starten en selecteer vervolgens **Ja** indien gevraagd om te bevestigen voorafgaand aan de uitvoering. 

### <a name="close-a-newly-completed-project"></a>Een nieuw voltooid project sluiten

Dynamics 365 Finance gebruikt het veld **projectfase** om onderscheid te maken tussen projecten **die worden uitgevoerd** of **afgerond** zijn. **Afgeronde** projecten mogen geen kosten met zich meebrengen of aan klanten worden gefactureerd.

1. Open een project om te deactiveren.
2. Selecteer **Deactiveren** in het lint.

> [!NOTE]
> U kunt een project deactiveren of sluiten, omdat ze zich beide hetzelfde gedragen in de context van Finance.

3. Open in Finance de pagina **Lijst met alle projecten**.
4. Bevestig dat het gedeactiveerde project niet in de lijst verschijnt.
5. Wijzig in de filter **projecten tonen** boven de lijst, de waarde van **Actief** in **Allemaal**.
6. U ziet nu het gedeactiveerde project.

Als u probeert om tijd of onkosten voor dit project in Finance te loggen, ziet u het project als het goed is niet meer voor selectie. Als u handmatig het projectnummer van een uitgave invoert, ziet u een bericht als "Projectfase voltooid staat geen invoer in het project toe". Facturering en andere factureringsfuncties moeten worden uitgeschakeld omdat ze in de context van een gesloten project zullen zijn.

