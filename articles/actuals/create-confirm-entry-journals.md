---
title: Invoerdagboeken maken en bevestigen
description: Dit artikel biedt informatie over het maken en bevestigen van invoerdagboeken in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 138dccd72607d6515eeeffb066fa485f83eabbec
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912326"
---
# <a name="create-and-confirm-entry-journals"></a>Invoerdagboeken maken en bevestigen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

U gebruikt invoerdagboeken om werkelijke waarden rechtstreeks in Microsoft Dynamics 365 Project Operations vast te leggen. Wanneer u invoerdagboeken gebruikt, hoeft u geen logboeken voor tijd, onkosten en materiaalgebruik in te voeren in Project Operations.

Met een enkel invoerdagboek kunt u meerdere dagboekregels maken. Wanneer het dagboek is bevestigd, registreert een invoerdagboekregel de werkelijke waarde voor de volgende details:

- De kosten of opbrengsten, afhankelijk van het transactietype dat is geselecteerd.
- De geselecteerde transactieklasse.. De beschikbare klassen zijn **Tijd**, **Onkosten**, **Materiaal**, **Voorschot**, **Mijlpaal** en **Belasting**.
- Het project dat en/of een taak die is geselecteerd op de dagboekregel.

Volg deze stappen om een invoerdagboek te maken in Project Operations.

1. Ga naar **Verkoop** \> **Transacties** \> **Dagboeken**.
2. Selecteer op de lijstpagina **Invoerdagboeken** in het actievenster de optie **Nieuw** om een dagboek te maken.
3. Voer op de pagina **Nieuw dagboek** in het veld **Beschrijving** een beschrijving van het dagboek in.
4. Zorg ervoor dat het veld **Dagboektype** is ingesteld op **Vermelding** en selecteer vervolgens **Opslaan**. Nadat het nieuwe invoerdagboek is opgeslagen, zou een tabblad **Dagboekregels** moeten verschijnen op de dagboekpagina moeten verschijnen.
5. Selecteer op het tabblad **Dagboekregels** op de werkbalk boven het raster de optie **Nieuw** om een invoerdagboekregel te maken.
6. Stel in het dialoogvenster **Snelle invoer** voor het maken van een invoerdagboekregel de velden in zoals beschreven in de volgende tabel.

    | Veld | Beschrijving | Functionele impact |
    | --- | --- | --- |
    | Transactieklasse | De dagboekregel kan worden ingedeeld in een van de zes transactieklassen: **Tijd**, **Onkosten**, **Materiaal**, **Voorschot**, **Mijlpaal** of **Belasting**. | De transactieklasse **Belasting** is afgeschaft in Project Operations. <br> Als u een transactieklasse **Belasting** maakt, wordt deze niet verwerkt door facturering of in kosten- of opbrengstberekeningen. **Mijlpaal** is een transactieklasse voor alleen opbrengsten. <br>De transactieklasse **Voorschot** vertegenwoordigt een voorschot dat is ontvangen van een klant. Het moet altijd worden gemaakt als een paar gefactureerde verkoop- en niet-gefactureerde verkoopdagboekregels. |
    | Transactietype | De transactietypen **Onkosten**, **Interorganisatorische verkopen** en **Kosten van resource-eenheid** moeten worden gebruikt om de kosten vast te leggen.<br> De transactietypen **Niet-gefactureerde verkoop** en **Gefactureerde verkoop** moeten worden gebruikt om opbrengsten te registreren. | De transactieklasse **Voorschot** werkt alleen met de transactietypen **Niet-gefactureerde verkoop** en **Gefactureerde verkoop**.<br> De transactieklasse **Mijlpaal** werkt alleen met het transactietype **Gefactureerde verkoop**. <br>De transactietypen **Interorganisatorische verkopen** en **Kosten van resource-eenheid** zijn alleen van toepassing op de transactieklasse **Tijd** en deze zijn alleen beschikbaar in invoerdagboeken in het Lite-implementatiescenario en niet bij het implementeren van Project Operations in de scenario's op basis van resources/niet-voorradige artikelen. |
    | Product selecteren | Wanneer de transactieklasse **Materiaal** is geselecteerd, kunt u in dit veld opgeven of de materiaaltransactie waarvoor u de dagboekregel maakt een bestaand product of een toe te voegen product is. | Als u **Toe te voegen product** selecteert, kunt u een naam voor het product invoeren. |
    | Product | Een verwijzing naar het product uit de catalogus. | |
    | Beschrijving | Een beschrijving van de dagboekregel om deze gemakkelijk te kunnen identificeren. | Voor niet-gefactureerde verkoopdagboekregels wordt de waarde gebruikt als de beschrijving wanneer de factuurregeldetails worden gemaakt. |
    | Externe beschrijving | Een beschrijving van de dagboekregel die kan worden gebruikt om te delen met externe belanghebbenden. | Voor niet-gefactureerde verkoopdagboekregels wordt de waarde gebruikt als de externe beschrijving wanneer de factuurregeldetails worden gemaakt. Het kan ook voorkomen op de factuur die naar de klant wordt gestuurd. |
    | Factureringstype | Een waarde die aangeeft of de dagboekregel wordt geteld als een belastbaar, gratis of niet-belastbaar onderdeel van het project. | In een typische stroom wordt het factureringstype afgeleid van de overeengekomen voorwaarden die in het contract zijn vastgelegd. Wanneer u echter een dagboekregel vastlegt, kunt u in dit veld een waarde invoeren. |
    | Documentdatum | Gebruik een datum wanneer de transactie heeft plaatsgevonden. | |
    | Begindatum | Gebruik de datum wanneer de transactie heeft plaatsgevonden. | Dit veld wordt gebruikt voor vergelijking met de aanmaakdatum van de factuur voor transacties van het type **Niet-gefactureerde verkoop**. Deze vergelijking zal u helpen beslissen of de transactie in de toekomst of in het verleden is gedateerd. Alleen verouderde transacties worden aan de factuur toegevoegd. |
    | Einddatum | Gebruik de datum wanneer de transactie heeft plaatsgevonden. | |
    | Boekhouddatum | Gebruik de datum waarop de boekhoudkundige impact wordt geregistreerd. | |
    | Contractregelklant | Als de contractregel slechts één klant heeft, wordt dit veld standaard ingesteld op de klant op de contractregel wanneer de dagboekregel wordt opgeslagen. Als de contractregel meerdere klanten heeft, selecteert u de juiste klant op de contractregel. | Als het systeem de klant van de contractregel op de dagboekregel niet kan bepalen, en als de werkelijke waarde van het type **Niet-gefactureerde verkoop** dat is gemaakt op basis van de dagboekregel leeg is, wordt de werkelijke waarde niet gefactureerd. |
    | Project | Selecteer het project waarvoor u de werkelijke waarde wilt vastleggen. | Op basis van het geselecteerde project, de transactieklasse en de taak probeert het systeem het contract, de contractregel en de contractregelklant te bepalen. |
    | Taak | Selecteer de taak waarvoor u de werkelijke waarde wilt vastleggen. | Als u tijdens de contractconfiguratie taken aan contractregels hebt gekoppeld, gebruikt het systeem de geselecteerde taak, samen met een project- en transactieklasse, om het contract, de contractregel en de contractregelklant te bepalen. |
    | Transactiecategorie | Selecteer de transactiecategorie waarvoor u de werkelijke waarde wilt vastleggen. | Voor onkosten bepaalt de geselecteerde transactiecategorie de standaardprijs die op de dagboekregel wordt ingevoerd wanneer deze wordt opgeslagen. |
    | - Rol | Dit veld is relevant voor tijddagboekregels. Selecteer de rol van de resource die tijd heeft besteed aan het project en/of de taak. | Als u voor tijddagboekregels de kant-en-klare configuratie gebruikt voor het invoeren van standaard resourcekosten en factuurtarieven, wordt de geselecteerde rol samen met de resource-eenheid gebruikt om de standaardprijs te bepalen die op de dagboekregel wordt ingevoerd wanneer deze wordt opgeslagen. Als u een aangepaste configuratie gebruikt voor het invoeren van standaardprijzen, moet u die configuratie bekijken om te bepalen of het veld **Rol** wordt gebruikt om standaardprijswaarden in te voeren. |
    | Subcontract | Als de dagboekregel uitbestede capaciteit of uitbestede onkosten of materialen vertegenwoordigt, selecteert u het relevante subcontract. | Wanneer onkostendagboekregels worden geregistreerd, bepaalt het geselecteerde subcontract de prijslijst die wordt gebruikt om de standaardeenheidskosten in te voeren. |
    | Subcontractregel | Als de dagboekregel uitbestede capaciteit of uitbestede onkosten of materialen vertegenwoordigt, selecteert u de relevante subcontractregel. | Wanneer onkostendagboekregels worden geregistreerd, zorgt de geselecteerde subcontractregel ervoor dat de beschikbare capaciteitsberekeningen op de subcontractregel correct worden berekend. |
    | Bedragmethode | Dit veld is standaard ingesteld op **Hoeveelheid vermenigvuldigen met prijs**. Wanneer deze methode wordt gebruikt, wordt het bedrag berekend als *Aantal* × *Prijs*. De andere ondersteunde methode is **Vaste prijs**. Wanneer deze methode wordt gebruikt, wordt de prijs ingesteld op het bedrag en wordt de hoeveelheid niet gebruikt in de berekening. | |
    | Eenheidsplanning en eenheid | Samen identificeren de eenheidsplanning en de eenheid de eenheid van de hoeveelheid. | De combinatie van de eenheid en de transactiecategorie wordt gebruikt om standaardprijzen voor onkosten in te voeren. In de standaardconfiguratie van Project Operations wordt de combinatie van eenheid, rol en resource-eenheid gebruikt om standaardprijzen voor tijd in te voeren. Als u een aangepaste configuratie hebt voor het invoeren van standaardprijzen, wordt deze samen met de eenheid gebruikt. De combinatie van product en eenheid wordt gebruikt om standaardprijzen voor materialen in te voeren. |
    | Aantal | Voer de hoeveelheid in. | |
    | Prijs | Als de prijs leeg wordt gelaten wanneer de dagboekregel wordt gemaakt, worden de relevante waarden gebruikt om de standaardprijzen in te voeren, afhankelijk van de transactieklasse. Als een prijs wordt ingevoerd wanneer de dagboekregel wordt gemaakt, wordt die prijs gebruikt. | |
    | Belastingen | Vul een willekeurig belastingbedrag in. | Afhankelijk van het belastingbedrag dat wordt ingevoerd, wordt het berekende bedrag berekend als *Bedrag* + *Belasting*. |

## <a name="confirm-an-entry-journal"></a>Een invoerdagboek bevestigen

Nadat u alle dagboekregels in een invoerdagboek hebt ingevoerd, kunt u het dagboek bevestigen. Bij dit proces wordt elke dagboekregel als werkelijke waarde voor de juiste projecten geregistreerd.

Nadat een dagboek is bevestigd, kunt u dit dagboek of de regels ervan niet langer bewerken.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Werkelijke waarden die worden gemaakt door bevestiging van het invoerdagboek

Er zijn een paar belangrijke verschillen tussen werkelijke waarden die worden gemaakt door bevestiging van het invoerdagboek en werkelijke waarden die worden gemaakt tijdens de goedkeuring van logboeken voor tijd, onkosten en materiaalgebruik en factuurbevestiging in Project Operations:

- Invoerdagboeken gebruiken geen transactiekoppelingen om de werkelijke kosten te koppelen aan de werkelijke niet-gefactureerde verkopen. De werkelijke waarden die worden gemaakt wanneer logboeken voor tijd, onkosten en materiaalgebruik worden goedgekeurd, gebruiken altijd transactieverbindingen om de kosten en niet-gefactureerde werkelijke verkoopwaarden te koppelen.
- Invoerdagboeken gebruiken geen transactieoorsprongen om de werkelijke kosten en de werkelijke waarden voor ongefactureerde verkopen te koppelen aan een oorspronkelijke record. De werkelijke waarden die worden gemaakt wanneer logboeken voor tijd, onkosten en materiaalgebruik worden goedgekeurd, gebruiken altijd transactieoorsprongen om de kosten en niet-gefactureerde werkelijke verkoopwaarden aan de oorspronkelijke tijdsvermelding te koppelen.
- Wanneer niet-gefactureerde werkelijke verkoopwaarden die zijn gemaakt door bevestiging van het invoerdagboek worden gefactureerd, worden de gefactureerde werkelijke verkoopwaarden die tijdens de factuurbevestiging worden gemaakt op dezelfde manier gekoppeld aan de niet-gefactureerde werkelijke verkoopwaarden die worden gemaakt wanneer logboeken voor tijd, onkosten en materiaalgebruik zijn goedgekeurd.
- Invoerdagboekregels die zijn gemaakt voor tijd die is ingevoerd door interorganisatorische resources veroorzaken geen werkelijke waarden van de typen **Kosten van resource-eenheid** en **Interorganisatorische verkopen** die automatisch worden gemaakt. Deze werkelijke waarden moeten handmatig worden gemaakt. Dit gedrag verschilt van het gedrag voor tijdsvermeldingen die worden vastgelegd door interorganisatorische resources. Wanneer in dat geval de tijd wordt goedgekeurd, maakt de toepassing automatisch werkelijke waarden van het type **Onkosten** voor het project en de werkelijke waarden van de typen **Kosten van resource-eenheid** en **Interorganisatorische verkopen** in de divisie van de werknemer die eigenaar is. Vervolgens worden transactieverbindingen gebruikt om die werkelijke waarden aan elkaar te koppelen en transactieoorsprongen om aan de oorspronkelijke tijdsvermelding te koppelen.
- Wanneer invoerdagboeken worden bevestigd, maken zij werkelijke waarden. Correctiedagboeken kunnen echter niet worden gebruikt om die werkelijke waarden te corrigeren. Dit gedrag verschilt van het gedrag voor werkelijke waarden die worden gemaakt wanneer logboeken voor tijd, onkosten en materiaalgebruik worden goedgekeurd. In dat geval kunt u in de toepassing correctiedagboeken gebruiken om de werkelijke waarden te corrigeren om eventuele fouten te corrigeren, op voorwaarde dat die werkelijke waarden nog niet zijn gefactureerd. Als ze al zijn gefactureerd, kunt u een werkelijke waarde nog steeds corrigeren als u een volledige creditering van die werkelijke waarde aan de klant verwerkt.

> [!NOTE]
> Invoerdagboeken dwingen geen strikte standaardregels af. Gebruik deze invoerdagboeken daarom zo weinig mogelijk en wees voorzichtig en zorg ervoor dat u geen beschadigde financiële gegevens in uw systeem maakt. Gebruik waar mogelijk logboeken voor tijd, onkosten- en materiaalgebruik, de mijlpaal- en voorschotinstellingen voor projectcontracten en het proces voor bevestiging van projectfacturen in plaats van invoerdagboeken om werkelijke waarden te maken.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
