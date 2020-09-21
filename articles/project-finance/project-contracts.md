---
title: Projectcontracten
description: Dit onderwerp biedt voorbeelden van de projectcontracten die u kunt maken voor verschillende typen projecten en financieringsbronnen, terwijl bovendien wordt aangegeven hoe u contracten kunt beheren en projectklanten kunt factureren.
author: KimANelson
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 854ddfe6db93b7e93a4ee640268a9c8f254f24e7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750785"
---
# <a name="project-contracts"></a>Projectcontracten

[!include [banner](../includes/banner.md)]

Dit artikel biedt voorbeelden van de projectcontracten die u kunt maken voor verschillende typen projecten en financieringsbronnen, terwijl bovendien wordt aangegeven hoe u contracten kunt beheren en projectklanten kunt factureren.

Het type project dat u voor een projectcontract maakt, bepaalt de methode die wordt gebruikt om projectklanten te factureren. U kunt een projectcontract en het gerelateerde project wijzigen, maar niet het projecttype. 

Door gebruik te maken van een projectcontract kunt u één of meerdere projecten tegelijk factureren. Het projectcontract helpt ook om een consistente factureringsprocedure te garanderen voor elk deelproject in een projectstructuur. 

Elk project dat wordt gefactureerd, moet aan een projectcontract worden gekoppeld. De instellingen voor een projectcontract zijn van toepassing op alle projecten en deelprojecten die aan dat projectcontract zijn gekoppeld. 

Een projectcontract kan een of meer financieringsbronnen specificeren. Daarom kunt u de facturering over meerdere financiers verdelen, financieringslimieten instellen zodat aan financieringsbronnen niet meer dan een bepaald bedrag wordt gefactureerd en financieringsregels configureren voor het in rekening brengen van uitgaven.

## <a name="funding-for-project-contracts"></a>Financiering voor projectcontracten
Sommige projectcontracten specificeren dat meerdere partijen de verantwoordelijkheid delen voor de financiering van de projectkosten. Hieronder volgen een aantal voorbeelden:

-   Een grote klant met meerdere divisies vraagt om de financiering van een project op te splitsen per divisie.
-   Uw bedrijf deelt de kosten van een groot project met een externe organisatie.
-   Een wegenproject wordt medegefinancierd door twee gemeenten.
-   Een brugproject wordt gefinancierd door een overheidssubsidie en een particulier bedrijf.

In Dynamics 365 Finance kunt u de facturering voor een enkele transactie of een heel project verdelen over meerdere klanten, subsidies of organisaties. 

Bij projecten met meerdere financiers worden alle partijen die bijdragen aan de financiering van een geavanceerd financieringsproject financieringsbronnen genoemd. Nadat een klant, organisatie of subsidie is gedefinieerd als financieringsbron, kan deze worden toegewezen aan een of meer financieringsregels. Financieringsregels bevatten de criteria die bepalen hoe kosten worden toegewezen aan de verschillende financieringsbronnen voor een project. 

Omdat artikelen in voorraad, zoals artikelen die worden weergegeven in bestelopdrachten en inkooporders, niet kunnen worden opgesplitst, kan het kostenbedrag niet worden verdeeld over meerdere financieringsbronnen op het moment van distributie. Daarom blijft de financieringsbronwaarde 0 (nul) totdat de voorraadafgifte is geboekt. Wanneer de voorraadafgifte wordt geboekt, wordt het kostenbedrag verdeeld volgens de accountdistributieregels voor het project.

Hier zijn enkele stappen die u kunt nemen om het gemakkelijker te maken om de facturering over meerdere financieringsbronnen te verdelen:

-   Geef aan dat alle transacties die voor een project worden ingevoerd, dezelfde verkoopvaluta gebruiken als het projectcontract.
-   Stel financieringslimieten in, zodat een financieringsbron niet meer dan een bepaald bedrag voor een project wordt gefactureerd.
-   Configureer financieringsregels en financieringslimieten per werknemer, artikel, categorie, categoriegroep en transactietype (of voor alle transactietypen).
-   Selecteer optionele begin- en einddatums om de periode te definiëren waarin elke financieringsregel geldig is.
-   Geef het percentage op waarvoor elke financieringsbron verantwoordelijk is.
-   Specificeer welke financieringsbron verantwoordelijk is voor afrondingsverschillen die worden veroorzaakt door berekeningen van de toewijzing van middelen.
-   Stel regels op die bepalen hoe projectkosten worden gefactureerd aan externe klanten en in rekening worden gebracht bij interne organisaties.
-   Registreer transacties op een financieringsrekening in de wacht totdat aanvullende financiering kan worden verkregen of totdat u besluit de kosten intern te dragen.

Om te bepalen welke belastinggroep aan een transactie moet worden gekoppeld, wordt het project doorzocht op een belastinggroeptoewijzing. Als er geen belastinggroeptoewijzing op projectniveau is uitgevoerd, wordt het projectcontract doorzocht.

### <a name="example-multiple-funding-sources-simple"></a>Voorbeeld: meerdere financieringsbronnen (eenvoudig)

De volgende tabel bevat scenario's voor het beheren van financieringstoewijzing over meerdere financieringsbronnen. Deze scenario's zijn gebaseerd op de volgende aannames:

-   Prioriteitsinstellingen worden meegenomen in de toewijzing van fondsen voordat andere criteria voor financieringsregels worden toegepast.
-   Er is geen datumbereik gespecificeerd om de periode d te definiëren wanneer de financieringsregel geldig is.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scenario</strong></td>
<td><strong>Financieringsbron</strong></td>
<td><strong>Toewijzingspercentage</strong></td>
<td><strong>Toewijzingsprioriteit</strong></td>
</tr>
<tr class="even">
<td>U wilt kosten toewijzen aan één financieringsbron totdat het geld op is, kosten toewijzen aan een tweede financieringsbron totdat het geld op is en tot slot de resterende kosten toewijzen aan een derde financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
<li>5</li>
</ul></td>
</tr>
<tr class="odd">
<td>U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron. Als een van deze financieringsbronnen uitgeput is, wilt u de resterende kosten betalen uit een derde financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>U wilt 75 procent van de kosten toewijzen aan één financieringsbron en 25 procent aan een tweede financieringsbron. Als een van deze financieringsbronnen uitgeput is, wilt u de resterende kosten verdelen tussen een derde financieringsbron en een vierde financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
<li>Financieringsbron 3</li>
<li>Financieringsbron 4</li>
</ul></td>
<td><ul>
<li>75%</li>
<li>25%</li>
<li>50%</li>
<li>50%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>0</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>U wilt de eerste 25 procent van de kosten toewijzen aan één financieringsbron en de rest aan een tweede financieringsbron.</td>
<td><ul>
<li>Financieringsbron 1</li>
<li>Financieringsbron 2</li>
</ul></td>
<td><ul>
<li>25%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>0</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Voorbeeld: meerdere financieringsbronnen (complex)

U hebt drie financieringsbronnen die u in de onderstaande volgorde wilt gebruiken:

1.  Gebruik financieringsbron 2 en financieringsbron 3 gelijkelijk totdat financieringsbron 2 is uitgeput.
2.  Blijf financieringsbron 3 gebruiken totdat deze is uitgeput.
3.  Gebruik financieringsbron 1 nadat financieringsbron 3 is uitgeput.

Om dit doel te bereiken, moet u het volgende doen:

-   Stel financieringslimieten in voor financieringsbron 2 en financieringsbron 3, voor hun respectievelijke bedragen.
-   Stel de volgende financieringsregel op:
    -   Regel 1 (prioriteit 1): wijs 50 procent van de transacties toe aan financieringsbron 2 en 50 procent aan financieringsbron 3.
    -   Regel 2 (prioriteit 2): wijs 100 procent van de transacties toe aan financieringsbron 3.
    -   Regel 3 (prioriteit 3): wijs 100 procent van de transacties toe aan financieringsbron 1.

Deze opzet werkt omdat transacties worden gecontroleerd aan de hand van regels en limieten om te bepalen of deze van toepassing zijn op de transactie. Als er geen specifieke regels of limieten op de transactie van toepassing zijn, is de regel Alle transacties van toepassing. De regel Alle transacties komt overeen met alle transacties. 

Als er een regel wordt gevonden die overeenkomt met een transactie, wordt het percentage dat in die regel is toegewezen eerst toegepast, maar pas nadat de overeenkomsten zijn vergeleken met eventuele limieten die zijn ingesteld. Als aan een limiet is voldaan en het geld van een financieringsbron is uitgeput, wordt de financieringsregel die aan de financieringslimiet is gekoppeld, genegeerd en controleert het programma op de volgende regel die van toepassing is. 

In sommige gevallen kan slechts een deel van een transactie onder een regel worden toegewezen. Dit kan gebeuren omdat er een limiet is bereikt wanneer de transactie wordt toegewezen. In dit geval wordt volgens die regel slechts een bepaald bedrag toegewezen, bijvoorbeeld 50 procent aan elke financieringsbron. Dit is het geval in regel 1, die eerder in deze sectie is beschreven. De rest wordt toegewezen volgens de volgende regel in de reeks. 

In de volgende tabel wordt dit scenario's nader onderzocht.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Focus</strong></td>
<td><strong>Details</strong></td>
</tr>
<tr class="even">
<td>Financieringsregels</td>
<td><ul>
<li>Regel 1 (prioriteit 1): alle transacties. Wijs financieringsbron 2 toe aan 50% en financieringsbron 3 aan 50%.</li>
<li>Regel 2 (prioriteit 2): alle transacties. Wijs 100% toe aan financieringsbron 3.</li>
<li>Regel 3 (prioriteit 2): alle transacties. Wijs 100% toe aan financieringsbron 1.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Financieringslimieten</td>
<td><ul>
<li>Limiet financieringsbron 1 = 10.000,00</li>
<li>Limiet financieringsbron 2 = 500,00</li>
<li>Limiet financieringsbron 3 = 750,00</li>
</ul></td>
</tr>
<tr class="even">
<td>Transactie 1</td>
<td><strong>Transactiebedrag:</strong> 100,00<strong>Financiering:</strong> De transactie wordt alleen betaald volgens regel 1, omdat de transactie volledig is betaald nadat regel 1 is toegepast. De transactie wordt gelijkelijk gefinancierd tussen financieringsbron 2 en financieringsbron 3.
<ul>
<li>Financieringsbron 2: 50,00</li>
<li>Financieringsbron 3: 50,00</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transactie 2</td>
<td><strong>Transactiebedrag:</strong> 5.000,00<strong>Financiering:</strong> De transactie wordt betaald volgens alle drie de regels. <strong>Regel 1</strong>
<ul>
<li>Financieringsbron 2: 450,00</li>
<li>Financieringsbron 3: 450,00</li>
</ul>
<strong>Regel 2</strong>
<ul>
<li>Financieringsbron 3: 250,00 (= 750,00 – 50,00 – 450,00)</li>
</ul>
<strong>Regel 3</strong>
<ul>
<li>Financieringsbron 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</li>
</ul></td>
</tr>
<tr class="even">
<td>Totale bedrag dat over elke financieringsbron wordt verdeeld</td>
<td><ul>
<li>Financieringsbron 1: 3.850,00</li>
<li>Financieringsbron 2: 500,00</li>
<li>Financieringsbron 3: 750,00</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Factureringsregels
Wanneer u met een klant onderhandelt over een projectcontract, bepaalt u hoe en wanneer u de klant kunt factureren voor werkzaamheden aan een project. Nadat u het projectcontract en het project hebt opgesteld, kunt u factureringsregels voor het project instellen. Factureringsregels zijn gebaseerd op de projectvoorwaarden die zijn gespecificeerd in het projectcontract. De factureringsregels die u kunt maken, zijn afhankelijk van de voorwaarden van het projectcontract en het projecttype, zoals Tijd en materiaal of Vaste prijs, die u aan de factureringsregel koppelt. U kunt meer dan één factureringsregel maken voor een projectcontract. U kunt ook een factureringsregel toewijzen aan meerdere projecten die aan hetzelfde projectcontract zijn gekoppeld en vergelijkbare factureringsvoorwaarden hebben. 

U kunt de volgende soorten factureringsregels instellen:

-   **Leveringseenheid** - Factureer een klant wanneer u een leveringseenheid voltooit. U definieert de leveringseenheden in het contract.
-   **Voortgang** – Factureer een klant bij voltooiing van een bepaald percentage van het project. U kunt een factureringsregel instellen om automatisch het percentage voltooid werk te berekenen, of u kunt het percentage voltooid werk en het bedrag dat aan de klant moet worden gefactureerd handmatig berekenen.
-   **Mijlpaal** – Factureer een klant voor het volledige bedrag van een projectmijlpaal wanneer de mijlpaal is bereikt.
-   **Tarief** – Factureer een klant voor uw diensten plus een beheervergoeding, die doorgaans een percentage is van de kosten van de diensten.
-   **Tijd en materiaal** – Factureer een klant voor de waarde van tijd en materialen die voor een project worden gebruikt.

Voor alle typen factureringsregels kunt u een retentiepercentage specificeren dat van de klantfacturen wordt afgetrokken totdat een project een afgesproken fase bereikt. Het retentiepercentage van de betaling wordt gespecificeerd in het projectcontract. Het bedrag wordt berekend op basis van en afgetrokken van de totale waarde van de regels op een klantfactuur. 

Voor factureringsregels **Tijd en materiaal** en **Voortgang** kunt u toerekenbare categorieën toewijzen. Toerekenbare categorieën geven de transacties aan die op de facturen van klanten moeten worden opgenomen. 

Wanneer u klaar bent om de klant te factureren, wordt het te factureren bedrag voor het project berekend op basis van de factureringsregels en wordt een projectfactuurvoorstel gegenereerd. 

In de volgende secties worden voorbeelden gegeven die laten zien hoe u factureringsregels voor een project instelt en beheert.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Voorbeeld: maak een factureringsregel die is gebaseerd op het aantal geleverde eenheden

Uw organisatie gaat een overeenkomst aan om in totaal vijf trainingen te geven aan de medewerkers van een klant voor 10.000 per training. U factureert de klant na elke trainingssessie. 

Wanneer u de factureringsregels voor het contract instelt, gebruikt u de volgende waarden:

-   De leveringseenheid is één trainingssessie.
-   De eenheidsprijs is 10.000 per trainingssessie.
-   Het totale aantal eenheden is vijf trainingssessies.

Als u één trainingssessie hebt afgerond, kunt u een factuur van 10.000, voor de eerste geleverde eenheid, aanmaken en de factuur naar de klant sturen.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Voorbeeld: maak een factureringsregel die is gebaseerd op een bepaald percentage van de voltooiing van het project (handmatige berekening)

Uw organisatie, een softwareadviesbureau, gaat een overeenkomst aan met een klant om een deel van een product te ontwikkelen dat de klant aan het ontwikkelen is. Uw organisatie stemt ermee in om de softwarecode gedurende een periode van zes maanden te leveren. De klant gaat ermee akkoord om uw organisatie in totaal 100.000 te betalen voor het werk. U stelt een factureringsregel op om de klant te factureren op basis van het percentage werk dat aan het project is voltooid, zoals gespecificeerd in het contract.

-   Aan het einde van de eerste maand overlegt u met de klant om het percentage voltooid werk te bepalen. Nadat u en de klant het project hebben beoordeeld, besluit u dat het project voor 15 procent is voltooid.
-   U maakt een factuur voor 15.000 (15 procent van 100.000) en stuurt deze naar de klant.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Voorbeeld: maak een factureringsregel die is gebaseerd op een bepaald percentage van de voltooiing van het project (automatische berekening)

Uw organisatie, een softwareontwikkelingsbedrijf, stemt ermee in om een salarisadministratiepakket voor een klant te ontwikkelen voor 30.000. De klant gaat ermee akkoord om uw organisatie te betalen op basis van het percentage voltooid werk. U schat dat de projectkosten 20.000 bedragen. Het projectcontract specificeert de werkcategorieën die u in het factureringsproces gebruikt. U stelt factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooid werk voor elke categorie. U stelt voor elke categorie een budget in:

-   **Ontwikkeling** – Kosten van 15.000 en opbrengsten van 20.000
-   **Installatie** – Kosten van 5.000 en opbrengsten van 10.000

Wanneer u voor het eerst een klantfactuur aanmaakt, wordt het factuurbedrag automatisch berekend op basis van de volgende informatie:

-   Na een maand dient de projectmedewerker een urenstaat in voor het project. De kosten van de arbeidsuren zijn 5.000 voor ontwikkeling en 1.000 voor installatie. Het ontwikkelingswerk is voor 33 procent voltooid (5.000 werkelijke kosten/15.000 budgetkosten) en het installatiewerk is voor 20 procent voltooid (1.000 werkelijke kosten/5.000 budgetkosten).
-   Het factuurbedrag van 8.667 wordt automatisch berekend (33 procent van 20.000 + 20 procent van 10.000).
-   U maakt een factuur voor 8.667 en stuurt deze naar de klant.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Voorbeeld: maak een factureringsregel die is gebaseerd op overeengekomen mijlpalen

Uw organisatie, een managementadviesbureau, stemt ermee in om marktonderzoek uit te voeren voor een consumentenproduct dat de klant wil gaan verkopen. De klant stemt ermee in om uw diensten gedurende drie maanden te gebruiken, beginnend in maart, en stemt ermee in om uw organisatie 50.000 te betalen. Het project kent drie mijlpalen:

-   Mijlpaal 1: consumentengegevens verzamelen – 31 maart
-   Mijlpaal 2: consumentengegevens analyseren – 30 april
-   Mijlpaal 3: een voorstel voor de levensvatbaarheid van het product presenteren – 31 mei

De klant stemt ermee in om uw organisatie 10.000 te betalen voor de eerste mijlpaal, 20.000 voor de tweede mijlpaal en 20.000 voor de derde mijlpaal. 

Wanneer u het projectcontract opstelt, gaat u ermee akkoord de klant te factureren op basis van de mijlpaal die is bereikt. Het instellen van de factureringsregel omvat de volgende stappen:

-   Definieer de projectmijlpalen.
-   Definieer het bedrag dat de klant moet factureren wanneer elke mijlpaal is voltooid.

Wanneer de eerste mijlpaal op 31 maart is voltooid, markeert u de mijlpaal als voltooid, stelt u een factuur op voor 10.000 en stuurt u deze naar de klant. U kunt pas een factuur voor een mijlpaal opstellen als u de mijlpaal als voltooid hebt gemarkeerd.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Voorbeeld: maak een factureringsregel die is gebaseerd op services plus beheerkosten

Uw organisatie, een managementadviesbureau, stemt ermee in om marktonderzoek uit te voeren om de levensvatbaarheid te evalueren van een product dat de klant, een retailbedrijf, ontwikkelt. De voorwaarden van de overeenkomst specificeren dat u de diensten van uw drie beste managementconsultants zult leveren, die het onderzoek op basis van tijd en materiaal zullen uitvoeren. De klant gaat ermee akkoord 100 euro per uur te betalen, plus 10 procent managementvergoeding voor de adviesuren die aan het project in rekening worden gebracht. 

Wanneer u het projectcontract opstelt, maakt u een factureringsregel om een beheervergoeding van 10 procent toe te voegen aan de adviesuren die aan het project in rekening worden gebracht. 

Wanneer u een factuur voor de klant opstelt, krijgt de klant 10 procent beheerkosten plus de kosten van de adviesuren in rekening gebracht. Als de drie consultants bijvoorbeeld in totaal 200 uur aan het project hebben gewerkt, wordt er een factuur voor 22.000 uur opgesteld op basis van de volgende berekening:

-   200 uur à 100 per uur = 20.000
-   10 procent beheervergoeding = 2.000
-   Totaal factuurbedrag = 22.000

Als tarieven voor een klant belastbaar zijn en u een omzetbelastinggroep in het projectcontract selecteert, wordt de omzetbelastinggroep automatisch ingevoerd in een factureringsregel voor tarieven.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Voorbeeld: stel een factureringsregel op voor de waarde van tijd en materialen

Uw organisatie, een softwareadviesbureau, stemt ermee in om de komende zes maanden vijf technisch consultants ter beschikking te stellen voor een softwareontwikkelingsproject voor een klant. De klant stemt ermee in om 150 euro per adviesuur te betalen, plus de kosten van kantoorbenodigdheden. Aan het einde van elke maand stuurt uw organisatie een factuur naar de klant. 

Wanneer u het projectcontract opstelt, gaat u ermee akkoord om de klant elke maand de tijd en materialen voor het project in rekening te brengen. U stelt een factureringsregel op die de volgende informatie bevat:

-   De contractduur bedraagt zes maanden.
-   De adviestijd wordt berekend tegen een tarief van 150 per uur.
-   Kantoorbenodigdheden worden tegen kostprijs gefactureerd en de totale kosten voor het project mogen niet hoger zijn dan 10.000.
-   U maakt tijdens het project aan het einde van elke kalendermaand een klantfactuur aan.

Gedurende de eerste maand worden in totaal 800 uur geregistreerd door de adviseurs van het project. De kosten van kantoorbenodigdheden die ten laste van het project worden gebracht, bedragen 2.000. Daarom maakt u aan het einde van de maand een factuur aan voor 122.000, die wordt berekend als 800 uur à 150 per uur, plus 2.000 voor kantoorbenodigdheden.



