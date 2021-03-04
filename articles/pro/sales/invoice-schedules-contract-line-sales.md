---
title: Factuurschema's maken voor een projectgebaseerde contractregel - lite
description: Dit onderwerp bevat informatie over het maken van factuurschema's en mijlpalen.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 728a35b2b69fb63a2b20f218c250365c5068370f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180321"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a>Factuurschema's maken voor een projectgebaseerde contractregel - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

U kunt een factuurschema koppelen aan een projectgebaseerde contractregel. Facturering is alleen toegestaan nadat het contract is gewonnen om een projectcontract te creëren. Met factuurschema's kunnen conceptfacturen voor een projectgebaseerde contractregel automatisch worden aangemaakt. Als u van plan bent om altijd handmatig facturen aan te maken, kunt u het maken van factuurschema's op een projectgebaseerde contractregel of een contractregel overslaan.

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a>Een factuurschema voor tijd en materiaal maken voor een projectgebaseerde contractregel

Wanneer voor een projectgebaseerde contractregel de factureringsmethode Tijd en materiaal wordt gebruikt, kunt u een datumgebaseerd factuurschema maken. Voer de volgende stappen uit om automatisch een op datum gebaseerd factuurschema te genereren.

1. Ga naar **Instellingen** > **Factuurfrequenties** om de factuurfrequentie in te stellen.
2. Open het projectcontract en stel op het tabblad **Samenvatting** de gewenste leverdatum in.
3. Open de tijd- en materiaalcontractregel waarvoor u een op datum gebaseerd factuurschema wilt maken. 
4. Selecteer op het tabblad **Factuurschema** een begindatum voor facturering en de frequentie van de facturering. 
5. Selecteer in het subraster **Factuurschema genereren**.

    Het systeem genereert het factuurschema met de volgende veldinformatie:

    - **Uitvoeringsdatum van factuur** wordt ingesteld op de datum op basis van de factuurfrequentie.
    - **Uiterste datum voor transactie** wordt ingesteld op de dag vóór **Uitvoeringsdatum van factuur**.
    - **Uitvoeringsstatus** wordt automatisch ingesteld op **Niet uitvoeren**. Wanneer de taak voor het automatisch maken van facturen wordt uitgevoerd voor **Uitvoeringsdatum van factuur**, wordt dit veld bijgewerkt naar **Uitvoering geslaagd** of **Uitvoering mislukt**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a>Een factuurschema met een vaste prijs maken voor een projectgebaseerde contractregel

Wanneer een projectgebaseerde contractregel een factureringsmethode met een vaste prijs heeft, kunt u een op mijlpalen gebaseerd factuurschema maken. Voer de volgende stappen uit om automatisch een factuurschema op basis van mijlpalen te genereren voor een vaste set mijlpalen die gelijkelijk over de kalenderperiode worden verdeeld.

1. Ga naar **Instellingen** > **Factuurfrequenties** om de factuurfrequentie in te stellen.
2. Open het projectcontract en stel op het tabblad **Samenvatting** de gewenste leverdatum in.
3. Open de contractregel met een vaste prijs waarvoor u een mijlpaalschema wilt maken. 
4. Selecteer op het tabblad **Factuurschema (Factureringsmijlpalen)** een begindatum voor facturering en de frequentie van de facturering. 
5. Selecteer in het subraster **Periodieke mijlpalen genereren**.

    Het systeem genereert het factuurschema met de volgende informatie voor mijlpalen.

    - **Mijlpaalnaam** is ingesteld op de datum die wordt bepaald op basis van de factuurfrequentie.
    - **Mijlpaaldatum** is ingesteld op de datum die wordt bepaald op basis van de factuurfrequentie.
    - **Mijlpaalbedrag** wordt berekend door het contractbedrag op de projectgebaseerde contractregel te delen door het aantal mijlpalen zoals bepaald door de frequentie, het begin van de facturering en de gewenste leverdatums.
    - Als de contractregel een waarde heeft in het veld **Geschat belastingbedrag**, wordt dit veld ook gelijkelijk aan elke mijlpaal toegewezen bij het genereren van periodieke mijlpalen.

Factureringsmijlpalen moeten gelijk zijn aan de gecontracteerde waarde van de projectgebaseerde contractregel. Als ze niet gelijk zijn, treedt er een fout op. U kunt die fout verhelpen door te controleren of de factureringsmijlpalen de totale waarde van de regel vertegenwoordigen door mijlpalen te maken, te bewerken of te verwijderen. Vernieuw de pagina nadat de wijzigingen zijn aangebracht.

### <a name="manually-create-milestones"></a>Handmatig mijlpalen maken

Mijlpalen met een vaste prijs kunnen handmatig worden gegenereerd als ze niet periodiek worden opgesplitst. Voer de volgende stappen uit om handmatig een mijlpaal te maken.

1. Open de contractregel met een vaste prijs waarvoor u een mijlpaal wilt maken. 
2. Selecteer op het tabblad **Factuurschema** in het subraster **+ Een nieuwe mijlpaal voor de contractregel maken**.
3. Voer in het formulier **Mijlpaal maken** de vereiste informatie in op basis van de volgende tabel. 

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Naam van mijlpaal | Snelle invoer | Tekstveld voor de naam van de mijlpaal. | Dit veld wordt opgenomen in de mijlpaal van de projectcontractregel en de factuur. |
| Projecttaak | Snelle invoer | Als de mijlpaal is gekoppeld aan een projecttaak, gebruikt u deze referentie om aangepaste logica toe te voegen en de mijlpaalstatus in te stellen op basis van de taakstatus. | Er is geen impact voor vervolgtaken van deze verwijzing naar een taak. |
| Datum van mijlpaal | Snelle invoer | De datum waarop het proces voor het automatisch maken van facturen moet zoeken naar de status van deze mijlpaal om deze in aanmerking te nemen voor facturering. | Dit wordt opgenomen in de mijlpaal van de projectcontractregel en de factuur. |
| Factuurstatus | Snelle invoer | Wanneer de mijlpaal wordt gemaakt, wordt deze status altijd ingesteld op **Niet gereed voor facturering** of **Niet begonnen**. | Dit wordt opgenomen in de mijlpaal van de projectcontractregel en de factuur. |
| Regelbedrag | Snelle invoer | Het bedrag of de waarde van de mijlpaal die aan de klant wordt gefactureerd. | Dit veld wordt opgenomen in de mijlpaal van de projectcontractregel en de factuur. |
| Belastingen | Snelle invoer | Het belastingbedrag dat is toegepast op de mijlpaal. | Dit wordt opgenomen in de mijlpaal van de projectcontractregel en de factuur. |

4. Selecteer **Opslaan en sluiten**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]