---
title: Niet-voorradig materiaal en in behandeling zijnde leveranciersfacturen configureren
description: In dit onderwerp wordt uitgelegd hoe u niet-voorradig materiaal en in behandeling zijnde leveranciersfacturen kunt inschakelen.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a84245a246f49ab69466aba0fec332f0489eec6c
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880635"
---
# <a name="configure-non-stocked-materials-and-pending-vendor-invoices"></a>Niet-voorradig materiaal en in behandeling zijnde leveranciersfacturen configureren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

## <a name="minimum-version-requirement"></a>Minimaal vereiste versie

Voor gebruik van niet-voorradig materiaal en in behandeling zijnde leveranciersfacturen voor scenario's voor niet-voorradig materiaal of op resources gebaseerde scenario's in Dynamics 365 Project Operations zijn de volgende versies vereist:

Dynamics 365 Dataverse-oplossingen:

- Project Operations – 4.9.0.221 of hoger
- Indelingsoplossing voor twee keer wegschrijven - 2.2.2.23 of hoger

Dynamics 365 Finance:
- 10.0.18 (10.0.793.52) of hoger. Zorg ervoor dat uw Finance-omgeving actueel is en dat alle kwaliteitsupdates worden toegepast om aan de minimale versievereisten te voldoen.

## <a name="run-dual-write-maps-for-non-stocked-materials-and-vendor-invoice-integration"></a>Kaarten voor Twee keer wegschrijven uitvoeren voor niet-voorradig materiaal en integratie van leveranciersfacturen

Dit gedeelte bevat informatie over de specifieke kaarten die nodig zijn voor niet-voorradig materiaal en leveranciersfacturen. Controleer of de vereiste kaarten in het onderwerp [Een nieuwe omgeving inrichten](../environment/resource-provision-new-environment.md#run-project-operations-dual-write-maps) worden uitgevoerd op uw omgeving.

1. Ga naar Lifecycle Services (LCS), navigeer naar uw LCS-project en ga naar de pagina **Omgevingsdetails**.
2. Selecteer in het gedeelte **Common Data Service-omgevingsinformatie** de optie **Koppelen aan CDS for Apps**. Nadat u de koppeling hebt geselecteerd, wordt u doorgestuurd naar de lijst met entiteiten in de toewijzingen.
3. Controleer of de volgende kaarten actief zijn. Als ze niet actief zijn, start u deze en zorgt u ervoor dat u alle gerelateerde tabeltoewijzingen opneemt.

    - CDS heeft verschillende producten (producten) uitgebracht
    - Leveranciers v2 (msdyn_vendors)
    - Project Operations-tabel voor materiaalschattingen (msdyn_estimatelines)
    - Entiteit voor exporteren van leverancierfacturen in Project Operations-integratieprojecten (msdyn_projectvendorinvoices)
    - Entiteit voor exporteren van leverancierfactuurregels in Project Operations-integratieprojecten (msdyn_projectvendorinvoicelines)
    - Werkelijke waarden voor integratie van Project Operations (msdyn_actuals). Zorg ervoor dat u kaartversie 1.0.0.14 of hoger gebruikt. U kunt de actieve versie van de kaart zien in de kolom **Versie** op de pagina **Twee keer wegschrijven**. U kunt een nieuwe versie van de kaart activeren door **Versie van tabeltoewijzing** te selecteren en vervolgens de geselecteerde versie op te slaan.

Als u standaarddemogegevens gebruikt, moet u mogelijk ook de volgende entiteitstoewijzingen stoppen en opnieuw starten bij de initiële synchronisatie:
  - Betaaldagen CDS V2 (msdyn_paymentdays)
  - Betalingsschema (msdyn_paymentschedules)
  - Betalingsvoorwaarden (msdyn_paymentterms)
  - Leveranciersgroepen (msdyn_vendorgroups)
  - Eenheden (uom)

> [!NOTE]
> De initiële synchronisatie voor leveranciersgroepen en -eenheden kan mislukken voor enkele records in de bestaande demogegevensset. U kunt de fouten negeren, aangezien ze u er niet van weerhouden om demogegevens te gebruiken met Project Operations.

## <a name="configure-prerequisites-in-dataverse"></a>Vereisten configureren in Dataverse

### <a name="activate-workflow-to-create-accounts-based-on-vendor-entity"></a>Werkstroom activeren om accounts te maken op basis van leveranciersentiteit

De indelingsoplossing voor twee keer wegschrijven biedt [hoofdintegratie voor leveranciers](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-mapping). Als voorwaarde voor deze functie moeten leveranciersgegevens worden gemaakt in de entiteit **Accounts**. Activeer een sjabloonwerkstroomproces om leveranciers te maken in de tabel **Accounts** zoals beschreven in [Schakelen tussen leveranciersontwerpen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/vendor-switch#use-the-extended-vendor-design-for-vendors-of-the-organization-type).

### <a name="set-products-to-be-created-as-active"></a>Te maken producten instellen als actief

Niet-voorradig materiaal moet worden geconfigureerd als **Vrijgegeven producten** in Finance. De indelingsoplossing voor twee keer wegschrijven biedt een kant-en-klare [integratie van vrijgegeven producten naar Dataverse-productcatalogus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/product-mapping). Standaard worden producten van Finance gesynchroniseerd met Dataverse in een conceptstatus. U kunt het product met een actieve status synchroniseren, zodat het direct kan worden gebruikt in materiaalgebruiksdocumenten of in behandeling zijnde leveranciersfacturen, gaat u naar **Systeem** > **Beheer** > **Systeembeheer** > **Systeeminstellingen** en stelt u op het tabblad **Verkoop** de optie **Producten maken met status actief** in op **Ja**.

## <a name="configure-prerequisites-in-finance"></a>Vereisten configureren in Finance

### <a name="enable-the-feature-key-for-pending-vendor-invoices"></a>De functiesleutel in voor in behandeling zijnde leveranciersfacturen

Voltooi de volgende stappen uit om functionaliteit in te schakelen om projectdetails toe te voegen aan in behandeling zijnde leveranciersfactuurregels.

1. Ga in Finance naar de werkruimte **Functiebeheer**.
2. Zoek in de lijst met functies de functie **In behandeling zijnde leveranciersfacturen inschakelen in Project Operations voor scenario's op basis van resources/scenario's zonder voorraad** en selecteer **Inschakelen**.

### <a name="define-category-groups-and-project-categories-for-items"></a>Categoriegroepen en projectcategorieën definiëren voor artikelen

Configureer ten minste één categoriegroep voor het transactietype **Artikel** en ten minste één projectcategorie die deze groep gebruikt. Zie [Projectcategorieën configureren](../project-accounting/configure-project-categories.md#category-groups) voor meer informatie.

Bekijk de projectkosten- en opbrengstprofielen en configureer de instellingen voor grootboekboekingen voor artikeltransacties. Zie [Boekhouding voor factureerbare projecten configureren](../project-accounting/configure-accounting-billable-projects.md) voor meer informatie.

### <a name="set-up-a-write-in-product"></a>Een toe te voegen product instellen

In Project Operations kunt u materiaalschattingen en gebruik vastleggen voor catalogusproducten die zijn geconfigureerd in de vrijgegeven productcatalogus en voor toe te voegen producten. Het gebruik van toe te voegen producten vereist een enkel vrijgegeven product dat voor dit doel in Finance is geconfigureerd. Voer de volgende stappen uit om een toe te voegen product te configureren. Herhaal deze stappen in elke rechtspersoon die Project Operations gebruikt voor scenario's voor resources/niet-voorraad.

1. Ga in Finance naar **Productinformatiebeheer** > **Producten** > **Vrijgegeven producten** en selecteer **Nieuw**.
2. Selecteer in het veld **Producttype** de optie **Artikel** en in het veld **Productsubtype** de optie **Product**.
3. Voer het productnummer (WRITEIN) en de productnaam (toe te voegen product) in.
4. Selecteer de artikelmodelgroep. Zorg ervoor dat voor de artikelmodelgroep die u selecteert het veld **Voorraadbeleid Voorradig product** is ingesteld op **Onwaar**.
5. Selecteer waarden in de velde **Artikelgroep**, **Opslagdimensiegroep** en **Traceringsdimensiegroep**. Gebruik **Opslagdimensie** uitsluitend voor **Site** en stel geen traceringsdimensies in.
6. Selecteer waarden in de velden **Voorraadeenheid**, **Aankoopeenheid** en **Verkoopeenheid** en sla uw wijzigingen op.
7. Stel op het tabblad **Plan** de instellingen voor de standaardvolgorde in en stel op het tabblad **Voorraad** de standaardsite en het magazijn in.
8. Ga naar **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters** en open **Project Operations in Dynamics 365 Dataverse**. 
9. Selecteer op het tabblad **Materialen** in veld **Toe te voegen product** het product dat u hebt gemaakt.
10. Open in uw Dataverse-omgeving, in het siteoverzicht, de entiteit **Producten** en zoek de record voor het toe te voegen product. 
11. Open de recorddetails en stel de productstatus in op **Buiten gebruik gesteld**. Deze productstatus voorkomt dat iemand deze record per ongeluk rechtstreeks in materiaalschattingen en gebruiksdocumenten gebruikt.

### <a name="set-up-a-procurement-integration-account"></a>Een inkoopintegratieaccount instellen

Het inkoopintegratieaccount wordt gebruikt als verrekeningsaccount bij het boeken van een openstaande leveranciersfactuur met regels die aan een project zijn toegewezen.

Wanneer het systeem een in behandeling zijnde leveranciersfactuur boekt, wordt dit account gebruikt voor het bedrag van de projectkosten. De leveranciersfactuurgegevens worden verwerkt in Dataverse en er wordt een corresponderende werkelijke projectwaarde gemaakt. De informatie van de werkelijke projectwaarde wordt toegevoegd aan het Project Operations-integratiejournaal. Wanneer u het integratiejournaal boekt, wordt het bedrag verrekend vanuit de inkoopintegratieaccount en geregistreerd bij de projectkosten.

1. Als u het inkoopintegratieaccount wilt instellen, gaat u naar **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters** en opent u **Project Operations in Dynamics 365 Dataverse**. 
2. Selecteer het tabblad **Materialen** en selecteer een waarde in het veld **Inkoopintegratieaccount**.

#### <a name="set-up-project-category-defaults-for-an-item"></a>Standaardinstellingen voor projectcategorieën instellen voor een artikel

1. Ga in Finance naar **Projectmanagement en boekhouding** > **Instellingen** > **Projectbeheer en boekhoudkundige parameters** en open **Project Operations in Dynamics 365 Dataverse**. 
2. Ga naar het tabblad **Standaardinstellingen voor projectcategorieën** en selecteer een waarde in het veld **Artikel**. Deze projectcategorie wordt gebruikt voor materiaaltransacties als de projectcategorie niet is ingesteld op de record van de werkelijke waarden van het project.
