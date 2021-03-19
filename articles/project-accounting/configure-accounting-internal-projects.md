---
title: Boekhouding configureren voor interne projecten
description: Dit onderwerp bevat informatie over het instellen van boekhoudkundige principes voor interne projecten in Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9f1cc75b12fec81d726e46f8d970dcfe030f6b29
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287592"
---
# <a name="configure-accounting-for-internal-projects"></a>Boekhouding configureren voor interne projecten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Met interne projecten kunnen bedrijven kosten bijhouden die zijn gerelateerd aan activiteiten die niet aan een klant zijn gefactureerd. Voorbeelden van interne projecten zijn:

- Een product ontwikkelen, zoals een mobiele app, en de kosten bijhouden die aan de ontwikkeling zijn gekoppeld.
- De tijd en onkosten vóór verkoop beheren. Dit interne project vóór verkoop kan later naar een factureerbaar project worden omgezet als de offerte wordt geaccepteerd.

Elk project dat niet aan een contract is gekoppeld in Dynamics 365 Project Operations wordt als intern behandeld. Projectkosten en opbrengstprofielen worden niet gebruikt om boekhoudregels voor het project te bepalen. Interne projectkosten worden altijd geboekt met behulp van winst- en verliesprincipes. Grootboekrekeningen voor boekingen worden gedefinieerd op de pagina **Boeking in grootboek instellen**.

- Tijdtransacties worden geboekt door de rekening **Kosten** te debiteren en de rekening **Salaristoewijzing** te crediteren.
- Onkostentransacties worden geboekt door de rekening **Kosten** te debiteren en de **Tegenrekening voor onkosten** te crediteren.

Nadat transacties naar het project zijn geboekt, worden als het project aan een projectcontract is gekoppeld alle samengevoegde transacties omgekeerd en worden nieuwe factureerbare transacties gemaakt. De factureerbare transacties volgen de boekhoudregels die zijn gedefinieerd met betrekking tot projectkosten en het opbrengstprofiel.




[!INCLUDE[footer-include](../includes/footer-banner.md)]