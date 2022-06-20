---
title: Een factuurschema maken voor een projectgebaseerde contractregel
description: Dit artikel bevat informatie over het maken van factuurschema's en mijlpalen op contractregels.
author: rumant
ms.date: 10/17/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 490a61b67f54bdad95ecfce905191c381dddc85b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914994"
---
# <a name="create-an-invoice-schedule-on-a-project-based-contract-line"></a>Een factuurschema maken voor een projectgebaseerde contractregel 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

U kunt een factuurschema maken voor een projectgebaseerde contractregel. Facturering is alleen toegestaan nadat het contract is binnengehaald en u een projectcontract maakt. Met een factuurschema kunnen conceptfacturen voor een projectgebaseerde contractregel automatisch worden gemaakt. Als u echter alleen handmatig facturen maakt, kunt u het maken van factuurschema's op contractregels overslaan.

## <a name="create-a-time-and-material-invoice-schedule-for-a-contract-line"></a>Een factuurschema voor tijd en materiaal voor een contractregel maken

Wanneer voor een projectgebaseerde contractregel de factureringsmethode Tijd en materiaal wordt gebruikt, kunt u een datumgebaseerd factuurschema maken. Voer de volgende stappen uit om automatisch een op datum gebaseerd factuurschema te genereren.

1. Ga naar **Instellingen** > **Factuurfrequenties** en stel een factuurfrequentie in.
2. Ga naar de projectcontractrecord en selecteer op het tabblad **Overzicht** in het veld **Aangevraagde leveringsdatum** een datum.
3. Open de contractregel **Tijd en materiaal** waarvoor u het datumgebaseerde factuurschema maakt. 
4. Selecteer op het tabblad **Factuurschema** de begindatum van de facturering en de factuurfrequentie.
5. Selecteer in het subraster **Factuurschema genereren**. Het factuurschema wordt gegenereerd terwijl de velden **Uitvoeringsdatum factuur**, **Sluitingsdatum transactie** en **Uitvoeringsstatus** als volgt zijn ingesteld:

    - **Uitvoeringsdatum factuur**: deze datum wordt bepaald door de factuurfrequentie.
    - **Sluitingsdatum transactie**: de dag vóór de uitvoeringsdatum van de factuur.
    - **Uitvoeringsstatus**: wordt automatisch ingesteld op **Niet uitvoeren**. Wanneer de taak voor het automatisch maken van facturen wordt uitgevoerd voor een bepaalde datum van factuuruitvoering, wordt dit veld bijgewerkt naar **Uitvoering geslaagd** of **Uitvoering mislukt**.

## <a name="create-a-fixed-price-invoice-schedule-for-a-contract-line"></a>Een factuurschema met een vaste prijs maken voor een contractregel

Als de contractregel een vaste factureringsmethode heeft, kunt u het op mijlpalen gebaseerde factuurschema maken. 

> [!NOTE]
> Mijlpalen kunnen niet worden gemaakt op een contractregel als er geen project is toegewezen aan de contractregel.

Voer de volgende stappen uit om een op mijlpalen gebaseerd factuurschema te genereren voor een vaste set mijlpalen die over de kalenderperiode gelijkmatig zijn verdeeld.

1. Ga naar **Instellingen** > **Factuurfrequenties** en stel een factuurfrequentie in.
2. Ga naar de projectcontractrecord en selecteer op het tabblad **Overzicht** in het veld **Aangevraagde leveringsdatum** een datum.
3. Open de contractregel **Vaste prijs** waarvoor u het mijlpaalschema maakt. Selecteer op het tabblad **Factureringsmijlpalen** de begindatum van de facturering en de factuurfrequentie. 
4. Selecteer in het subraster **Periodieke mijlpalen genereren**. Het factuurschema wordt gegenereerd terwijl de velden **Mijlpaalnaam**, **Mijlpaaldatum** en **Mijlpaalbedrag** als volgt zijn ingesteld:

    - **Mijlpaalnaam**: deze naam wordt bepaald door de factuurfrequentie.
    - **Mijlpaaldatum**: deze datum wordt bepaald door de factuurfrequentie.
    - **Mijlpaalbedrag**: dit bedrag wordt berekend door het contractbedrag op de contractregel te delen door het aantal mijlpalen zoals bepaald door de frequentie, het begin van de facturering en de aangevraagde leveringsdatums.

    Als de contractregel een waarde heeft in het veld **Geschat belastingbedrag**, wordt dit veld ook gelijkelijk over elke mijlpaal verdeeld bij het genereren van periodieke mijlpalen.

Factureringsmijlpalen moeten gelijk zijn aan de gecontracteerde waarde van de contractregel. Als dat niet het geval is, krijgt u een foutmelding op de pagina **Contractregel**. U kunt de fout oplossen door te controleren of de factureringsmijlpalen de totale gecontracteerde waarde van de regel vertegenwoordigen door mijlpalen te maken, te bewerken of te verwijderen. Vernieuw de pagina nadat de wijzigingen zijn aangebracht om de fout te verwijderen.

### <a name="manually-create-milestones"></a>Handmatig mijlpalen maken

U kunt mijlpalen met een vaste prijs handmatig genereren als deze niet periodiek worden opgesplitst. Voer de volgende stappen uit om handmatig een mijlpaal te maken.

1. Open de contractregel met een vaste prijs waarvoor u een mijlpaal maakt en selecteer op het tabblad **Factuurschema** in het subraster **+ Nieuwe mijlpaal voor contractregel maken**. 
2. Voer op de pagina **Mijlpaal maken** de vereiste informatie in op basis van de volgende tabel.

| Veld | Locatie | Beschrijving | Downstreamimpact |
| --- | --- | --- | --- |
| Naam van mijlpaal | Snelle invoer | Tekstveld voor de naam van de mijlpaal. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en de factuur. |
| Projecttaak | Snelle invoer | Als de mijlpaal is gekoppeld aan een projecttaak, gebruikt u deze referentie om aangepaste logica toe te voegen om de mijlpaalstatus op basis van de taakstatus in te stellen. | Er is geen effect van deze referentie op een taak. |
| Datum van mijlpaal | Snelle invoer | Stel de datum in waarop het proces voor het automatisch maken van facturen moet zoeken naar de status van deze mijlpaal waardoor deze in aanmerking komt voor facturering. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en de factuur. |
| Factuurstatus | Snelle invoer | Wanneer een mijlpaal wordt gemaakt, wordt deze status altijd ingesteld op **Niet gereed voor facturering** of **Niet gestart**. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en de factuur. |
| Regelbedrag | Snelle invoer | Bedrag of waarde van de mijlpaal voor facturering aan de klant. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en de factuur. |
| Belastingen | Snelle invoer | Het belastingbedrag dat is toegepast op de mijlpaal. | Dit wordt doorgegeven aan de mijlpaal van de projectcontractregel en de factuur. |

3. Selecteer **Opslaan en sluiten**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]