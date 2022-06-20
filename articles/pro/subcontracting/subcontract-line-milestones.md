---
title: Mijlpalen voor subcontractregels
description: In dit artikel wordt uitgelegd hoe u een op mijlpalen gebaseerd factuurschema maakt en onderhoudt voor een subcontract met een leverancier.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b146bf0becff5d0fa0da59f50c0d04aafaf5115f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927598"
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

    | Veld | Beschrijving |Functionele impact|
    | --- | --- |----------------------|
    | Naam van mijlpaal | De naam van de mijlpaal. |Dit wordt weergegeven als de eerste kolom in alle zoekopdrachten op basis van mijlpalen voor subcontractregels. De leveranciersfactuurregel die op basis van deze mijlpaal wordt gemaakt, gebruikt ook de naam van de mijlpaal van de subcontractregel als de standaardnaam van de leveranciersfactuurregel.|
    | Beschrijving | Een beschrijving van de mijlpaal. |De leveranciersfactuurregel die op basis van deze mijlpaal wordt gemaakt, gebruikt ook de beschrijving van de mijlpaal van de subcontractregel als de standaardbeschrijving van de leveranciersfactuurregel.|
    | Datum van mijlpaal | De datum waarop het proces voor het automatisch aanmaken van facturen moet zoeken naar de status van deze mijlpaal om deze in overweging te nemen voor facturering.| Deze waarde wordt gebruikt als de standaarddatum van de leveranciersfactuurregel bij facturering van deze subcontractregel. |
    | Hoeveelheid | Het bedrag of de waarde van de mijlpaal die aan de klant wordt gefactureerd. |Deze waarde wordt gebruikt als het standaardbedrag op de leveranciersfactuurregel bij facturering van deze subcontractregel. |
    | Belastingen | Het belastingbedrag dat is toegepast op de mijlpaal.| Deze waarde wordt gebruikt als het standaardbelastingbedrag op de leveranciersfactuurregel bij facturering van deze subcontractregel. |
    | Bedrag na belasting | Dit alleen-lezen veld wordt berekend als Bedrag + Btw.|Deze waarde wordt gebruikt als de standaardwaarde op de leveranciersfactuurregel bij facturering van deze subcontractregel. |
    | Factuurstatus | Wanneer de mijlpaal wordt gemaakt, wordt deze status altijd ingesteld op **Niet gereed voor facturering**.|  Wanneer de status **Gereed voor facturering**, wordt deze mijlpaal opgenomen in de leveranciersfactuur. |

5. Selecteer **Opslaan en sluiten**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
