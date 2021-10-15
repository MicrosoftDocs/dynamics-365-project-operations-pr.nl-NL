---
title: Mijlpalen voor subcontractregels
description: In dit onderwerp wordt uitgelegd hoe u een op mijlpalen gebaseerd factuurschema maakt en onderhoudt voor een subcontract met een leverancier.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323770"
---
# <a name="subcontract-line-milestones"></a>Mijlpalen voor subcontractregels

[!include [banner](../../includes/dataverse-preview.md)]

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations kan op een subcontractregel met een factureringsmethode met een vaste prijs een op mijlpalen gebaseerd factuurschema met de leverancier worden opgegeven.

Mijlpalen voor leveranciersfacturen kunnen automatisch worden gegenereerd op basis van een ingestelde frequentie, maar u kunt ze ook handmatig maken.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Automatisch een op mijlpalen gebaseerd factuurschema voor een subcontractregel maken

Voer de volgende stappen uit om automatisch een op mijlpalen gebaseerd factuurschema te genereren voor een vaste set gelijk verdeelde mijlpalen.

1. Ga naar **Instellingen** > **Factuurfrequenties** en stel de factuurfrequentie in voor de subcontractregels.
2. Open de pagina **Subcontracten**, open het subcontract waarmee u wilt werken en open vervolgens de subcontractregel met een vaste prijs waarvoor u een mijlpaalplanning gaat maken.
3. Selecteer op het tabblad **Mijlpalen voor subcontractregels** de optie **Periodieke mijlpalen genereren**.
4. Typ of selecteer in het dialoogvenster een datumbereik, het aantal mijlpalen en de factuurfrequentie. U kunt een startdatum selecteren, het aantal mijlpalen en de factuurfrequentie of startdatum, of de einddatum en factuurfrequentie selecteren. U kunt de einddatum en het aantal mijlpalen niet selecteren.
Op basis van deze informatie genereert het systeem mijlpalen en records die worden weergegeven in het raster **Mijlpalen**.

   - **Naam van mijlpaal**: de naam van de mijlpaal wordt ingesteld op de datum van de mijlpaal op basis van de factuurfrequentie.
   - **Datum van mijlpaal**: de datum op basis van de factuurfrequentie.
   - **Bedrag van mijlpaal**: berekend door het subtotaalbedrag op de subcontractregel te delen door het aantal mijlpalen.

Als de subcontractregel een waarde in het veld **Geschat belastingbedrag** bevat, wordt deze waarde gelijkelijk aan elke mijlpaal toegevoegd bij het genereren van periodieke mijlpalen.

De som van de bedragen voor mijlpalen voor subcontractregels moet gelijk zijn aan de waarde op de subcontractregel. Als ze niet gelijk zijn, treedt er een fout op. U kunt de fout herstellen en controleren of het mijlpaaltotaal gelijk is aan de waarde van de subcontractregel door mijlpaal- en belastingbedragen te maken, te bewerken of te verwijderen. Nadat de wijzigingen zijn aangebracht, slaat u de pagina op en vernieuwt u deze om ervoor te zorgen dat er geen fouten meer zijn.

## <a name="manually-create-subcontract-line-milestones"></a>Handmatig mijlpalen voor subcontractregels maken

Mijlpalen met een vaste prijs op een subcontractregel kunnen handmatig worden gegenereerd als ze niet periodiek worden gesplitst. Voer de volgende stappen uit om handmatig een mijlpaal voor een subcontractregel te maken.

1. Selecteer in het navigatievenster de optie **Subcontracten** en open het subcontract waarmee u wilt werken.
2. Open de subcontractregel met vaste prijs waarvoor u een mijlpaal wilt maken.
3. Selecteer op het tabblad **Mijlpalen voor subcontractregels** in het subraster **+ Nieuwe mijlpaal voor subcontractregels**.
4. Voer op de pagina **Nieuwe mijlpaal voor subcontractregels** de vereiste informatie in op basis van de volgende tabel.

    | Veld | Beschrijving |
    | --- | --- |
    | Naam van mijlpaal | De naam van de mijlpaal. |
    | Beschrijving | Een beschrijving van de mijlpaal.  |
    | Datum van mijlpaal | De datum waarop het proces voor het automatisch aanmaken van facturen moet zoeken naar de status van deze mijlpaal om deze in overweging te nemen voor facturering. Deze waarde wordt opgenomen op de leveranciersfactuurregel bij facturering voor dit subcontract. |
    | Hoeveelheid | Het bedrag of de waarde van de mijlpaal die aan de klant wordt gefactureerd. Deze waarde wordt opgenomen op de leveranciersfactuurregel bij facturering voor dit subcontract. |
    | Belastingen | Het belastingbedrag dat is toegepast op de mijlpaal. Deze waarde wordt opgenomen op de leveranciersfactuurregel bij facturering voor dit subcontract. |
    | Bedrag na belasting | Dit alleen-lezen veld dat wordt berekend als bedrag + belasting. Deze waarde wordt opgenomen op de leveranciersfactuurregel bij facturering voor dit subcontract. |
    | Factuurstatus | Wanneer de mijlpaal wordt gemaakt, wordt deze status altijd ingesteld op **Niet gereed voor facturering**.  Wanneer de status **Gereed voor facturering**, wordt deze mijlpaal opgenomen in de leveranciersfactuur. |

5. Selecteer **Opslaan en sluiten**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]