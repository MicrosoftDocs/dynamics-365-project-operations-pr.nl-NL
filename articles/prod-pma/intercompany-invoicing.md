---
title: Intercompany-facturering
description: Dit artikel bevat informatie over en voorbeelden van intercompany-facturering voor projecten.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f66af9b7e2cb0e18a5464b23216ff03b63a0a3
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685372"
---
# <a name="intercompany-invoicing"></a>Intercompany-facturering

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over en voorbeelden van intercompany-facturering voor projecten.

Uw organisatie heeft mogelijk meerdere divisies, dochterondernemingen en andere rechtspersonen die producten en diensten aan elkaar leveren voor projecten. De rechtspersoon die de dienst of het product levert, wordt de *uitlenende rechtspersoon* genoemd en de rechtspersoon die de dienst of het product ontvangt, de *lenende rechtspersoon*. 

De volgende afbeelding toont een typisch scenario waarin twee rechtspersonen, SI FR (de lenende rechtspersoon) en SI USA (de uitlenende rechtspersoon) resoources delen om een project voor klant A te leveren. Voor dit scenario is SI FR gecontracteerd om het werk aan klant A te leveren. 

[![Voorbeeld van intercompany-facturering.](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg) 

Het doel is om kostenbeheersing, omzetverantwoording, belastingen en verrekenprijs voor intercompany-projecttransacties flexibeler en krachtiger te maken. Daarnaast worden de volgende mogelijkheden geboden:

-   Het opstellen van klantfacturen voor een project in een lenende rechtspersoon met behulp van intercompany-urenstaten, onkosten en leveranciersfacturen in een uitlenende rechtspersoon.
-   Het ondersteunen van belastingberekeningen en indirecte kosten.
-   Het uitstellen van omzetverantwoording in een uitlenende rechtspersoon en het erkennen van de kosten door een lenende rechtspersoon.
-   Het genereren van OHW-inkomsten (onderhanden werk) in de uitlenende rechtspersoon.
-   Het instellen van verrekenprijzen in die kunnen worden gebaseerd op verschillende prijsmodellen. Hieronder volgen een aantal voorbeelden:
    -   **Hoeveelheid** - Het bedrag dat u invoert in het veld **Prijsstelling** is de werkelijke kosten per hoeveelheid of eenheid.
    -   **Kostenbedrag** - De prijs/kosten per transactie plus het kostenbedrag dat u invoert in het veld **Prijsstelling**.
    -   **Kostenpercentage** - De verrekenprijs is de prijs/kosten per transactie vermenigvuldigd met het kostenpercentage dat u invoert in het veld **Prijsstelling**.
    -   **Percentage van verkoopprijs** - Het percentage van de verkoopprijs dat wordt overgedragen aan de uitlenende rechtspersoon.
    -   **Bedrag onder verkoopprijs** - Het bedrag dat de lenende rechtspersoon achterhoudt van de verkoopprijzen vóór overdracht aan de uitlenende rechtspersoon.
    -   **Bijdrageratio** - Het getal dat u invoert in het veld **Prijsstelling** is de bijdrageratio, die wordt uitgedrukt als een percentage van de verkoopprijs.

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a>Voorbeeld 1: parameters voor intercompany-facturering instellen
In dit voorbeeld is USSI een uitlenende rechtspersoon en rapporteren zijn resources tijd aan de lenende rechtspersoon, FRSI, die eigenaar is van het contract met de eindklant. Uren en onkosten die USSI-medewerkers rapporteren, kunnen worden opgenomen in de projectfactuur die FRSI genereert. Daarnaast is er een derde bron van transacties die afkomstig kan zijn van de uitlenende rechtspersoon (USSI in dit voorbeeld) wanneer deze gedeelde leveranciersdiensten levert aan dochterondernemingen (zoals FRSI) en die kosten vervolgens doorberekent aan projecten binnen die dochterondernemingen. Alle overeenkomende factuurdocumenten en belastingberekeningen worden door Finance ingevuld. 

Voor dit voorbeeld moet FRSI een klant zijn in de rechtspersoon USSI en moet USSI een leverancier zijn in de rechtspersoon FRSI. U kunt vervolgens een intercompany-relatie opzetten tussen de twee rechtspersonen. De volgende procedure laat zien hoe u de parameters instelt zodat beide rechtspersonen kunnen deelnemen aan intercompany-facturering.

1. Stel FRSI in als klant in de rechtspersoon USSI en stel USSI in als leverancier in de rechtspersoon FRSI. Er zijn drie toegangspunten voor de stappen die nodig zijn voor deze taak.

   | Stap |                                                       Toegangspunt                                                        |                                                                                                                                                                                               Beschrijving                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  A   | Klik in USSI op <strong>Klanten</strong> &gt; <strong>Klanten</strong> &gt; <strong>Alle klanten</strong>. |                                                                                                                                                                  Maak een nieuwe klantrecord voor FRSI en selecteer de klantengroep.                                                                                                                                                                  |
   |  B   |    Klik in FRSI op <strong>Leveranciers</strong> &gt; <strong>Leveranciers</strong> &gt; <strong>Alle leveranciers</strong>.     |                                                                                                                                                                    Maak een nieuwe leveranciersrecord voor USSI en selecteer de leveranciersgroep.                                                                                                                                                                    |
   |  C   |                                  Open in FRSI de leveranciersrecord die u zojuist hebt gemaakt.                                  | Ga naar het actievenster op het tabblad <strong>Algemeen</strong> en klik in de groep <strong>Instellen</strong> op <strong>Intercompany</strong>. Stel op de pagina <strong>Intercompany</strong>, op het tabblad <strong>Handelsrelatie</strong>, de schuifregelaar <strong>Actief</strong> in op <strong>Ja</strong>. Selecteer in het veld <strong>Klantbedrijf</strong> de klantrecord die u in stap A hebt gemaakt. |


2. Klik op **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Parameters voor Projectmanagement en financiële administratie** en klik vervolgens op het tabblad **Intercompany**. De manier waarop u de parameters instelt, is afhankelijk van of u de lenende rechtspersoon of de uitlenende rechtspersoon bent.
   -   Als u de lenende rechtspersoon bent, selecteert u de aanschaffingscategorie die moet worden gebruikt voor afstemming met de leveranciersfacturen, die automatisch worden gegenereerd.
   -   Als u de uitlenende rechtspersoon bent, selecteert u per lenende entiteit een standaardprojectcategorie voor elk transactietype. Projectcategorieën worden gebruikt voor belastingconfiguratie wanneer de gefactureerde categorie in intercompany-transacties alleen bestaat in de lenende rechtspersoon. U kunt ervoor kiezen om inkomsten toe te rekenen voor intercompany-transacties. Deze toerekening vindt plaats wanneer de transacties worden geboekt en wordt vervolgens teruggeboekt wanneer de intercompany-factuur wordt geboekt.

3. Klik op **Projectmanagement en financiële administratie** &gt; **Instelling** &gt; **Prijzen** &gt; **Verrekenprijs**.
4. Selecteer een valuta, transactietype en verrekenprijsmodel. De valuta die op de factuur wordt gebruikt, is de valuta die is geconfigureerd in de klantrecord voor de lenende rechtspersoon in de uitlenende rechtspersoon. De valuta wordt gebruikt om de posten in de verrekenprijstabel te matchen.
5. Klik op **Grootboek** &gt; **Boeking instellen** &gt; **Intercompany-boekhouding** en stel een relatie in voor USSI en FRSI.

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a>Voorbeeld 2: een intercompany-urenstaat maken en boeken
USSI, de uitlenende rechtspersoon, moet de urenstaat maken en boeken voor een project van FRSI, de lenende rechtspersoon. Er zijn twee toegangspunten voor de stappen die nodig zijn voor deze taak.

| Stap | Toegangspunt                                                                       | Beschrijving                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projectmanagement en financië;e administratie** &gt; **Urenstaten** &gt; **Alle urenstaten** | Maak een nieuwe urenstaat. Selecteer op urenstaatregel, in het veld **Rechtspersoon** de optie **FRSI**. Selecteer in het veld **Project-id** het project in FRSI. Voer de uren in voor elke dag van de week. |
| B    | Pagina **Urenstaat**                                                                | Nadat de werkstroom is uitgevoerd, boekt u de urenstaat en noteert u het boekstuknummer.                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a>Voorbeeld 3: een intercompany-leveranciersfactuur maken en boeken
USSI, de uitlenende rechtspersoon, moet de intercompany-leveranciersfactuur maken en boeken voor een project van FRSI, de lenende rechtspersoon. Deze leveranciersfactuur vertegenwoordigt de uitbestede arbeid en onkosten die zijn gemaakt door leveranciers die door USSI worden betaald. Er zijn twee toegangspunten voor de stappen die nodig zijn voor deze taak.

| Stap | Toegangspunt                                                                                      | Beschrijving                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Leveranciers** &gt; **Facturen** &gt; **Open leveranciersfacturen** &gt; **Nieuwe leveranciersfactuur** | Maak een nieuwe leveranciersfactuur en voer de diensten in die namens het project van FRSI zijn aangeschaft.                                                                                                                                                                                  |
| B    | De pagina **Leveranciersfactuur**                                                                      | Voer regels in die de uitbestede diensten namens FRSI vertegenwoordigen. Voer op het sneltabblad **Regeldetails** op het tabblad **Project** voor de factuurregel in het veld **Projectbedrijf** de waarde **FRSI** in. Voer het project en de bijbehorende informatie in. Boek vervolgens de leveranciersfactuur. |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a>Voorbeeld 4: de intercompany-factuur maken en boeken
USSI, de uitlenende rechtspersoon, moet de intercompany-factuur maken en boeken. Er zijn twee toegangspunten voor de stappen die nodig zijn voor deze taak.

| Stap | Toegangspunt                                                                                             | Beschrijving                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| A    | **Projectmanagement en financiële administratie** &gt; **Projectfacturen** &gt; **Intercompany-klantfactuur**  | Klik op **Nieuw** om de pagina **Intercompany-factuur maken** te openen.                                                                                  |
| B    | **Projectmanagement en financiële administratie** &gt; **Projectfacturen** &gt; **Intercompany-klantfacturen** | Voer op de pagina **Intercompany-factuur maken** de rechtspersoon in, specificeer de transactie die moet worden opgenomen en klik vervolgens op **Zoeken**. |
| C    | **Projectmanagement en financiële administratie** &gt; **Projectfacturen** &gt; **Intercompany-klantfacturen** | Selecteer de transacties die u wilt factureren of klik op **Alles selecteren** om alle transacties in de lijst te factureren en klik vervolgens op **OK**.                  |
| D    | De pagina **Intercompany-factuur**                                                                       | Het voorstel voor een intercompany-klantfactuur wordt weergegeven.                                                                                             |
| E    | De pagina **Intercompany-factuur**                                                                       | Klik op **Bericht**.                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a>Voorbeeld 5: de leveranciersfactuur boeken en de klant factureren
Wanneer de uitlenende rechtspersoon, USSI, de intercompany-klantfactuur boekt, wordt een overeenkomende openstaande leveranciersfactuur gemaakt in de lenende rechtspersoon, FRSI. Nadat deze leveranciersfactuur is geboekt, factureert FRSI ook de projectklant voor de uren die USSI heeft ingevoerd. Er zijn drie toegangspunten voor de stappen die nodig zijn voor deze taak.

| Stap | Toegangspunt                                                                                        | Beschrijving                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| A    | **Leveranciers** &gt; **Facturen** &gt; **Leveranciersfacturen in behandeling**                            | Bekijk de factuur om te controleren of de urenstaatwaarden zijn opgenomen en boek vervolgens de leveranciersfactuur.                  |
| B    | **Projectmanagement en financiële administratie** &gt; **Projectfacturen** &gt; **Projectfactuurvoorstellen** | Maak een nieuwe projectfactuur voor het project en controleer of de geboekte uurtransacties verschijnen.            |
| C    | De pagina **Projectfactuur**                                                                       | Selecteer de projectfactuur en klik op **Details weergeven** om de kosten en het verkoopbedrag te bekijken. Boek vervolgens de factuur. |


Zie [Intercompany-projectfacturering configureren](tasks/configure-intercompany-project-invoicing.md) voor meer informatie.




[!INCLUDE[footer-include](../includes/footer-banner.md)]