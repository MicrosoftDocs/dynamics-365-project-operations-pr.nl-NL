---
title: Overzicht van inkomstenverantwoording
description: Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531398"
---
# <a name="revenue-recognition-overview"></a>Overzicht van inkomstenverantwoording

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

In Dynamics 365 Project Operations verschillen de principes van inkomstenverantwoording op basis van de geselecteerde factureringsmethode voor een project of een deel van het project. Dit onderwerp bevat informatie over inkomstenverantwoording in Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transacties die worden geboekt met de factureringsmethode voor tijd en materiaal

- Kosten en inkomstenverantwoording hangen samen. Transactiekosten en niet-gefactureerde verkopen worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md).
- Het profiel voor projectkosten en omzet bepaalt of niet-gefactureerde verkooptransacties naar het grootboek worden geboekt. Als **Inkomsten toerekenen** is geselecteerd, gebruikt het systeem de rekeningen **OHW-verkoopwaarde** en de **Waarde van de toegerekende inkomsten** tijdens het boeken. Hieronder ziet u een voorbeeld van deze methode.  

  | Transactietype | Debet/Credit | Bedrag |
  | --- | --- | --- |
  | OHW-verkoopwaarde | Debet | 100 |
  | Verkoopwaarde toegerekende inkomsten | Credit | 100 |

- Omzet wordt toegerekend bij facturering. Het systeem gebruikt de rekening **Gefactureerde omzet** tijdens het boeken. Hieronder ziet u een voorbeeld van deze methode.  

  | Transactietype | Debet/Credit | Bedrag |
  | --- | --- | --- |
  | Klantensaldo | Debet | 120 |
  | Te betalen omzetbelasting | Credit | 20 |
  | Gefactureerde omzet | Credit | 100 |

- Als er inkomsten zijn toegerekend toen de niet-gefactureerde verkopen werden geboekt, zal het systeem de toegerekende inkomsten bij facturering terugboeken.

  | Transactietype | Debet/Credit | Bedrag |
  | --- | --- | --- |
  | OHW-verkoopwaarde | Credit | 100 |
  | Verkoopwaarde toegerekende inkomsten | Debet | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transacties die worden geboekt met de factureringsmethode voor vaste prijs

- Kosten en inkomstenverantwoording hangen niet samen. Transactiekosten worden geboekt met het [Project Operations-integratiejournaal](../project-accounting/project-operations-integration-journal.md). Niet-gefactureerde verkooptransacties worden niet gemaakt.
- Opbrengsten kunnen tijdens de facturering worden verantwoord als voor het projectkosten- en opbrengstenprofiel **Principe gebruikt voor berekeningen van de voltooiing van projecten** is ingesteld op **Geen OHW**. Gebruik deze methode alleen voor korte, eenvoudige projecten.
- Opbrengsten kunnen worden verantwoord op basis van omzetschattingen met vaste prijs, met de methode **Voltooid contract** of **Inkomstenverantwoording voor voltooiingspercentage**.

## <a name="additional-resources"></a>Aanvullende bronnen
[Artikel Boekhouding configureren voor factureerbare projecten](../project-accounting/configure-accounting-billable-projects.md)

[Projecten met omzetschattingen met een vaste prijs](rev-rec-percentage-completion-method.md)

[Omzetschattingen beheren](rev-rec-completed-contract-method.md)

[Kosten om methoden te voltooien](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]