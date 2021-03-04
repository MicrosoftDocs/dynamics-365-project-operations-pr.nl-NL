---
title: Intercompany-klant- en leveranciersfacturen maken
description: Dit onderwerp bevat informatie over het maken van intercompany-facturen voor klanten en leveranciers.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595452"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Intercompany-klant- en leveranciersfacturen maken

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Een projectaccountant in een uitlenende rechtspersoon maakt een intercompany-klantfactuur aan voor de projectkosten die worden overgedragen aan de lenende entiteit. Nadat de intercompany-klantfactuur is goedgekeurd en geboekt, verzendt de uitlenende rechtspersoon de intercompany-factuur naar de lenende rechtspersoon.

De projectaccountant van de uitlenende rechtspersoon kan een batchproces opzetten om periodiek intercompany-facturen te genereren. De projectaccountant specificeert de criteria, zoals specifieke projecten, om intercompany-facturen in een batch aan te maken.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Handmatig een intercompany-klantfactuur voor projecttransacties maken 

Gebruik deze procedure om handmatig een intercompany-klantfactuur voor projecttransacties te maken. Zoek naar uren die zijn geboekt door werknemers op projecten in de lenende rechtspersonen en naar onkosten die door uw rechtspersoon zijn gemaakt namens lenende rechtspersonen. U kunt zoeken op naam van de rechtspersoon, projectcontractnummer, projectnummer, datumbereik of een combinatie van deze opties. Selecteer in de zoekresultaten de transacties die u aan een intercompany-factuur wilt toevoegen.

1. Ga in Dynamics 365 Finance naar **Projectbeheer en boekhouding** > **Projectfacturen** > **Intercompany-klantfacturen**. Selecteer op de lijstpagina **Intercompany-klantfacturen** **Nieuw** in het actievenster.
2. Op de pagina **Intercompany-factuur maken** selecteert u een lenende rechtspersoon in het veld **Rechtspersoon**.
3. Optioneel: voer een specifiek projectcontract en projectnummer in.
4. Beperk de zoekopdracht door een datumbereik te selecteren. Voer specifieke datums in de velden **Startdatum** en **Einddatum** in. Alleen intercompany-transacties die binnen dit datumbereik zijn geboekt, worden in de zoekresultaten weergegeven.
5. Stel **Project geavanceerde journaalregelparameter** in op **Ja** en selecteer **Zoeken**.
6. Selecteer in de zoekresultaten de transacties die u wilt opnemen in het intercompany-factuurvoorstel en selecteer vervolgens **OK**.
7. Op de pagina **Intercompany-klantfactuur** worden de intercompany-projecttransacties weergegeven die u in de zoekresultaten hebt geselecteerd. Om de transacties te wijzigen voordat u de factuur naar de lenende rechtspersoon verzendt, doet u het volgende:
  
    1. Open de pagina **Een factuurvoorstel maken**. Selecteer aanvullende intercompany-transacties voor de huidige factuur en selecteer vervolgens **Regel toevoegen**.
    2. Als u een regel wilt verwijderen, selecteert u **Verwijderen**.
    3. Bekijk opmerkingen, redenen, financiële dimensies en andere informatie over een geselecteerde regel op het sneltabblad **Factuurregels**.
    
8. Selecteer **Boeken** in het actievenster om de intercompany-klantfactuur te boeken.

> [!NOTE]
> Als uw organisatie vereist dat intercompany-facturen worden gecontroleerd voordat ze worden geboekt, kan de systeembeheerder een werkstroom opzetten voor intercompany-facturen. Als er geen werkstroom is ingesteld voor intercompany-facturen, kunt u de intercompany-factuur boeken.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Een batchtaak maken voor intercompany-facturen

U kunt meerdere intercompany-facturen tegelijk aanmaken voor alle lenende rechtspersonen. Met de zoekfunctionaliteit kunt u bijvoorbeeld zoeken naar alle transacties die zijn geboekt door geleende werknemers en die betrekking hebben op projecten die worden beheerd door andere rechtspersonen. Vervolgens kunt u voor elke lenende rechtspersoon een intercompany-factuur aanmaken voor de transacties in de zoekresultaten.

1. Ga naar **Projectbeheer en boekhouding** > **Periodiek** > **Projectfacturen** > **Intercompany-klantfacturen**.
2. Op de pagina **Intercompany-klantfacturen maken** selecteert u een rechtspersoon in het veld **Bedrijf** om de factuur aan te richten. Als u geen bedrijf selecteert, worden alle transacties die aan de zoekcriteria voldoen weergegeven voor alle lenende rechtspersonen.
3. In **Eén factuur maken per** selecteert u of u een factuur wilt maken voor intercompany-transacties op basis van een project of op basis van een lenende rechtspersoon.
4. Optioneel: als u een specifiek project en projectcontract wilt selecteren waarvoor u intercompany-facturen wilt maken, klikt u op **Selecteer**. Selecteer op de pagina **Onderzoek** in het veld **Criteria** het projectcontract, het projectnummer of beide en selecteer vervolgens **OK**.
5. Stel op het tabblad **Batch** een batchproces in om periodiek intercompany-facturen te maken. Zie voor meer informatie [Een batchverwerkingstaak indienen vanuit een formulier](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Selecteer **Boeken** in het actievenster om de intercompany-facturen te boeken.

> [!NOTE]
> Als uw organisatie vereist dat intercompany-facturen worden gecontroleerd voordat ze worden geboekt, kan de systeembeheerder een werkstroom opzetten voor intercompany-facturen. Als er geen werkstroom is ingesteld voor intercompany-facturen, kunt u de intercompany-facturen boeken.

## <a name="post-the-intercompany-vendor-invoice"></a>De intercompany-leveranciersfactuur boeken

Een projectaccountant in de lenende rechtspersoon kan openstaande intercompany-leveranciersfacturen beoordelen wanneer de corresponderende intercompany-klantfactuur wordt geboekt. Ga in Finance in de lenende rechtspersoon naar **Leveranciers** > **Facturen** > **Leveranciersfactuur in behandeling**. Het factuurnummer in behandeling komt overeen met het factuurnummer van de intercompany-klant. Controleer of de factuur correct is en boek vervolgens de factuur. Door een intercompany-leveranciersfactuur te boeken, worden een projectsubadministratie en een grootboektransactie gemaakt die de transactiekosten in de lenende rechtspersoon weerspiegelen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]