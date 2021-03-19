---
title: Projectfactuurvoorstellen beheren
description: Dit onderwerp biedt informatie over het verwerken van klantgerichte facturen met Project Operations voor scenario's op basis van resources/niet-voorradige artikelen.
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4e663a9a0ca5b197e556d8c36233ab25affda876
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275847"
---
# <a name="manage-project-invoice-proposals"></a>Projectfactuurvoorstellen beheren

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Projectfactuurvoorstellen kunnen door uw factureringsafdeling worden verwerkt als aan de volgende twee voorwaarden is voldaan:

  - De projectmanager bevestigt de pro-formafactuur in Microsoft Dataverse.
  - Alle niet-gefactureerde verkooptransacties op tijd en materiaal die zijn opgenomen in de pro-formafactuur, worden geboekt met behulp van het **Project Operations integratie** journaal van Dynamics 365.

Gebruik de volgende stappen om een projectfactuurvoorstel in Dynamics 365 Finance te voltooien.

1. Bekijk factureringsgegevens voor tijd- en materiaaltransacties en boek het **Project Operations integratie** journaal.
2. Bekijk factureringsgegevens voor mijlpalen voor facturering met een vaste prijs.
3. Bekijk een projectfactuurvoorstel en maak dit op.
4. Projectfacturen boeken en afdrukken.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Beheer factuurgegevens in het Project Operations integratiejournaal

Werkelijke projectwaarden gemaakt in Dataverse worden beoordeeld en in Finance geplaatst door de projectaccountant. Zie voor meer informatie over het werken met het integratiejournaal [Integratiejournaal in Project Operations](../project-accounting/project-operations-integration-journal.md).

Werkelijke kosten en niet-gefactureerde werkelijke verkopen worden als afzonderlijke regels aan het integratiejournaal toegevoegd:

  - De kostprijs per eenheid en het kostenbedrag op de standaard werkelijke kosten van de transactie werkelijke kostprijs van het project in Dataverse.
  - De verkoopprijs per eenheid en het verkoopbedrag voor de niet-gefactureerde verkooptransactie komen standaard uit de werkelijke niet-gefactureerde verkooptransactie van het project in Dataverse.

### <a name="billing-sales-tax"></a>Facturering omzetbelasting

De BTW-berekening voor facturering wordt bepaald door de veldcombinatie van **BTW-groep voor facturering** en **BTW-groep voor factuuritem** op een niet-gefactureerde verkooprecord op de **Project Operations integratie** journaalregel. Het systeem stelt deze veldwaarden standaard in op basis van instellingen in het tabblad **Financiën** op de pagina **Projectbeheer en boekhoudkundige parameters**.

- **Methode BTW-groep** bepaalt de standaardlogica van de BTW-groep voor facturering:
  
  - **Project**: zal altijd standaard de BTW-groep voor facturering van het project zijn. U kunt de standaard BTW-groep voor facturering voor een project bekijken of wijzigen door **Standaard financiële administratie weergeven** op de pagina **Alle projecten** te selecteren.
  - **Projectcontract**: zal altijd standaard de BTW-groep voor facturering van het projectcontract zijn. U kunt de standaard BTW-groep voor facturering voor een projectcontract beoordelen of wijzigen door **Standaard financiële administratie weergeven** op de pagina **Projectcontracten** te selecteren.
  - **Klant**: zal altijd standaard de BTW-groep voor facturering van de klant zijn.
  - **Zoeken**: hiermee doorzoekt u alle bovenstaande entiteiten en selecteert u de eerste beschikbare waarde. Zoeken begint met de entiteit **Project**, dan de entiteit **Projectcontract** en tenslotte de entiteit **Klant**.

- **Methode BTW-groep item** bepaalt de standaardlogica van de BTW-groep van het factureringsitem:
  
  - Voor transactietypen voor tijd, onkosten en toeslagen wordt de BTW-groep van het factureringsitem altijd standaard ingesteld op de entiteit **Projectcategorie**.
  - Voor materiaaltransactietypen wordt de BTW-groep van het factureringsitem standaard ingesteld op basis van de instelling **Methode BTW-groep item** in **Parameters voor projectbeheer en boekhouding**. Het itemnummer is standaard de BTW-groep van het item uit de entiteit **Vrijgegeven product**. De categorie is standaard de BTW-groep van het item uit de entiteit **Projectcategorie**.

### <a name="financial-dimensions"></a>Financiële dimensies

De financiële dimensies voor niet-gefactureerde verkooprecords in het **Project Operations integratie** journaal zijn standaard afkomstig van de entiteit **Project**. Financiële dimensies kunnen worden beoordeeld en aangepast door het selecteren van **Bedragen verdelen**. Als u de financiële dimensies van de niet-gefactureerde verkooprecord moet wijzigen nadat het integratiejournaal is geboekt maar voordat de pro-formafactuur is bevestigd, gaat u naar **Alle projecten** > **Beheren** > **Geboekte transacties**, selecteer de transactie en selecteer vervolgens **Verwerken** > **De financiële administratie aanpassen**.

### <a name="exchange-rates"></a>Wisselkoersen

Niet-gefactureerde transactievaluta in Dataverse wordt gebruikt als transactievaluta in Finance en geconverteerd naar de valuta voor boekhouding van het bedrijf met behulp van wisselkoersen die zijn gedefinieerd in Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Beheer de financiële kenmerken van factureringsmijlpalen 

Projectcontractregels die de factureringsmethode tegen een vaste prijs gebruiken, worden gefactureerd via [Mijlpalen met een vaste prijs](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). De projectaccountant kan factureringsmijlpalen in Finance bekijken door naar **Projectbeheer en boekhouding** > **Alle projecten** > **Beheren** > **Transacties op rekening** te gaan.

### <a name="billing-sales-tax"></a>Facturering omzetbelasting

De waarden voor **BTW-groep** en **BTW-groep voor item** worden standaard overgenomen uit de instellingen wanneer een nieuwe factureringsmijlpaal wordt gemaakt in Dataverse. Het systeem stelt deze veldwaarden standaard in op basis van instellingen in het tabblad **Financieel** op de pagina **Parameters voor projectbeheer en financiële administratie**.

- **Methode BTW-groep** bepaalt de standaardlogica van de **BTW-groep voor facturering**:

    - **Project** zal altijd standaard de BTW-groep voor facturering van het project zijn. U kunt de standaard BTW-groep voor een project bekijken of wijzigen door **Standaard financiële administratie weergeven** op de pagina **Alle projecten** te selecteren.
    - **Projectcontract** zal altijd standaard de BTW-groep voor facturering van het projectcontract zijn. U kunt de standaard BTW-groep voor facturering voor een projectcontract beoordelen of wijzigen door **Standaard financiële administratie weergeven** op de pagina **Projectcontracten** te selecteren.
    - **Klant** zal altijd standaard de BTW-groep voor facturering van de klant zijn.
    - Met **Zoeken** doorzoekt u alle entiteiten in deze lijst en selecteert u de eerste beschikbare waarde. Zoeken begint met de entiteit **Project**, dan de entiteit **Projectcontract** en vervolgens de entiteit **Klant**.

- **BTW-groep voor mijlpaalitem met vaste prijs** wordt gebruikt om de waarde standaard naar het veld **BTW-groep item** over te dragen.

### <a name="financial-dimensions"></a>Financiële dimensies

Standaard financiële dimensies voor de mijlpaal voor facturering met een vaste prijs worden ingesteld op projectcontractregels. Ga naar **Projectcontracten** > **Standaard financiële administratie weergeven** en selecteer op het tabblad **Contractregels** **prijs contractregel** en stel vervolgens de financiële dimensiewaarden in die u als standaard wilt gebruiken.

De projectaccountant kan de informatie over omzetbelasting en financiële dimensies op factuurmijlpalen bewerken totdat het projectfactuurvoorstel is gemaakt.


## <a name="create-project-invoice-proposals"></a>Projectfactuurvoorstellen maken

Projectfactuurvoorstellen kunnen worden bekeken in de module **Projectbeheer en boekhouding** door naar **Projectfacturen** > **Projectfactuurvoorstellen** te gaan.

De header van het projectfactuurvoorstel wordt gemaakt in Finance wanneer de pro-formafactuur wordt bevestigd in Dataverse. Voor een gemakkelijkere afstemming stelt het systeem het nummer van het projectfactuurvoorstel in Finance in op hetzelfde nummer als de pro-formafactuur-id in Dataverse. Omdat pro-formafacturen niet noodzakelijkerwijs in dezelfde volgorde worden bevestigd als waarin ze zijn gemaakt, moet de nummerreeks van het projectfactuurvoorstel in Finance ruimte laten voor wijzigingen naar lagere en hogere nummers. Configureer nummerreeksen met behulp van de volgende stappen:

1. Ga in Finance naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**.
2. Selecteer in het filter **Gebied**, **Projecten**.
3. Selecteer in het filter **Referentie**, **Factuurvoorstel**.
4. Gebruik het veld **Bedrijf** om elke rechtspersoon waarvoor de integratie van Project Operations en Dataverse is ingeschakeld te filteren.
5. Open **Details nummerreeks** en stel op het tabblad **Algemeen** het volgende in:

    - **Gebruikerswijzigingen toestaan: naar een lager nummer** = **Ja**
    - **Gebruikerswijzigingen toestaan: naar een hoger nummer** = **Ja**

Projectfactuurvoorstelregels worden door het systeem toegevoegd via het periodieke proces **Importeren uit opslagtabel** (**Projectbeheer en boekhouding** > **Periodiek** > **Project Operations integratie** > **Importeren uit opslagtabel**). Dit proces kan handmatig worden uitgevoerd of via een periodieke planning. Het systeem voegt geen regels toe aan het factuurvoorsteldocument totdat alle regels klaar zijn om te worden gefactureerd. Tijd- en materiaaltransacties zijn alleen gereed om te worden gefactureerd wanneer ze zijn geboekt met het **Project Operations integratie** journaal.

## <a name="format-and-print-invoice-proposals"></a>Projectfactuurvoorstellen opmaken en afdrukken

De projectaccountant kan een afgedrukte projectfactuur aanpassen met behulp van de pagina **Factuurvoorstel opmaken** en afdrukbeheermogelijkheden.

### <a name="format-invoice-proposals"></a>Factuurvoorstellen opmaken

De pagina **Factuurvoorstellen opmaken** maakt het mogelijk om aangepaste groeperingstransacties weer te geven in de projectfactuur van de klant.

1. Selecteer op de pagina **Projectfactuurvoorstel**, **Afdrukken** > **Factuurvoorstel opmaken**.
2. Selecteer **Nieuw** om een nieuwe groepering te maken voor de afdruk van de projectfactuur.
3. Selecteer in het veld **Detail/samenvatting** opties voor deze groepering:

    - Selecteer **Detail** om de transactiegegevens van de klantfactuur af te drukken.
    - Selecteer **Samenvatting** om het transactieoverzicht van de klantfactuur af te drukken.

> [!NOTE]
> De selectie in het veld **Detail/samenvatting** op de pagina **Factuurvoorstel opmaken** overschrijft de optie die is geselecteerd in het veld **Factuuropmaak** op de pagina **Factuurvoorstellen** om een gedetailleerde factuur of een factuuroverzicht af te drukken.

- Selecteer de transactieregels die u in deze sectie op het tabblad **Beschikbare transacties** wilt opnemen en selecteer **Transacties opnemen** om ze naar het tabblad **Geselecteerde transacties** te verplaatsen.
- Selecteer **Omhoog** en **Omlaag** om de volgorde van de secties te wijzigen.
- Selecteer **Afdrukvoorbeeld** om een voorbeeld van de opgemaakte factuur te bekijken.

### <a name="print-management"></a>Afdrukbeheer

Afdrukbeheer gebruikt verschillende rapportbestanden voor afdrukken, opgeven van bestemmingen en het aanpassen van de voettekst voor de factuur. Afdrukbeheer kan worden ingesteld op moduleniveau, maar deze instellingen kunnen worden overschreven voor een specifiek klant-, contract- of factuurvoorstel. Om toegang te krijgen tot deze functie op de pagina **Projectfactuurvoorstel** selecteert u **Afdrukken** > **Afdrukbeheer**.

De instellingen voor afdrukbeheer worden weergegeven als een boomstructuur, waarbij op elk knooppuntniveau de beschikbare documenten worden weergegeven die kunnen worden aangepast. U kunt aangepaste afdrukken toewijzen op module-, klant-, contract- of factuurvoorsteldocumentniveau. Om de originele documentafdruk te wijzigen, vouwt u het gewenste knooppunt uit en selecteert u **Origineel item**. Selecteer in het veld **Rapportindeling** de rapportindeling die voor het afdrukken moet worden gebruikt. U kunt aangepaste rapportindelingen gebruiken met [Raamwerk voor zakelijk documentbeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Factuurvoorstellen boeken

Nadat de factuur is gecontroleerd en bewerkt, en de factuurvoorstelregels naar wens zijn, controleert u de factuurtotalen en omzetbelasting. Selecteer in de groep **Details** **Totalen** en selecteer vervolgens **Boeken** om de factuur te boeken.

Schakel om de factuur te bekijken voordat u deze boekt het selectievakje **Boeken** uit. **Pro-forma** wordt op de factuur afgedrukt om aan te geven dat het een voorbeeldfactuur is. Schakel het selectievakje **Factuur afdrukken** in om de factuur af te drukken.

Naast via de pagina **Factuurvoorstel** kunnen factuurvoorstellen ook worden geboekt door de periodieke taak uit te voeren, **Factuurvoorstellen boeken**. Ga voor deze taak naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectfacturen** > **Factuurvoorstellen boeken**.

Deze pagina toont alle factuurvoorstellen die klaar zijn om geboekt te worden. U kunt het boeken van factuurvoorstellen plannen door **Batch** te selecteren. Stel de **Batchverwerkingsparameter** in op **Ja** en stel de herhaling van batchverwerking in door **Herhaling** te selecteren.


[!INCLUDE[footer-include](../includes/footer-banner.md)]