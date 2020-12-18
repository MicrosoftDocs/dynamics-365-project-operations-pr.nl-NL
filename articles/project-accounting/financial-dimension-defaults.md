---
title: Standaardwaarden voor financiële dimensies
description: Dit onderwerp biedt informatie over het instellen van standaardinstellingen voor financiële dimensies.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642357"
---
# <a name="financial-dimension-defaults"></a>Standaardwaarden voor financiële dimensies

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations gebruikt het raamwerk [Financiële dimensies](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) in Dynamics 365 Finance om aanvullende inzichten te bieden in projecttransacties in subadministratie en grootboek.

Standaard financiële dimensies kunnen worden ingesteld voor een klant, projectfinancieringsbron, mijlpaal, projectcontractregel of project.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Financiële standaarddimensies voor een klant definiëren

Standaardinstellingen voor klantdimensies worden opgegeven in Finance. Voer de volgende stappen uit om standaardwaarden voor dimensies in te stellen.

1. Ga naar **Klanten** > **Klanten** > **Alle klanten**.
2. Stel op de pagina **Klanten**, op het tabblad **Financiële dimensies** de financiële dimensiewaarden in voor een specifieke klant.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Financiële standaarddimensies voor projectcontracten definiëren

Projectcontracten worden aangemaakt en onderhouden in Common Data Service (CDS). Boekhoudkundige kenmerken voor projectcontracten worden ingesteld in de module **Projectbeheer en boekhouding** in Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Financiële dimensies instellen voor een financieringsbron voor een project

1. Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Projectcontracten**.
2. Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Projectcontract** de optie **Standaardboekhouding weergeven**.
3. Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Financieringsbronnen**.
4. Stel de standaardwaarden voor financiële dimensies in. Merk op dat de financiële dimensies standaard afkomstig zijn van de klantrekening.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Financiële dimensies instellen voor een contractregel voor een project

1. Ga naar **Projectmanagement en financiële administratie** > **Projecten** > **Projectcontracten**.
2. Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Projectcontract** de optie **Standaardboekhouding weergeven**.
3. Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Contractregels**.
4. Stel de standaardwaarden voor financiële dimensies in. De standaardinstellingen van de financiële dimensie zijn van toepassing en kunnen alleen worden gebruikt met contractregels met een vaste prijs (mijlpaal).

Deze standaardwaarden worden gebruikt voor gerelateerde projecttransacties op rekening en factuurregels.

## <a name="define-default-financial-dimensions-for-projects"></a>Financiële standaarddimensies voor projecten definiëren

Projecten worden aangemaakt en onderhouden in CDS. Boekhoudkundige kenmerken voor projecten worden ingesteld in de module **Projectbeheer en boekhouding** in Finance.

1. Ga naar **Projectbeheer en boekhouding** > **Projecten** > **Alle projecten**.
2. Selecteer de record die u wilt bijwerken en selecteer op het tabblad **Project** de optie **Standaardboekhouding weergeven**.
3. Vouw **Gerelateerde informatie** uit en selecteer het tabblad **Instellen**.
4. Stel de standaardwaarden voor financiële dimensies in. Merk op dat de financiële dimensies standaard afkomstig zijn van de klantrekening. Als het project is gekoppeld aan een contractregel met meerdere projectcontractklanten, wordt de primaire klant gebruikt om de financiële standaarddimensies te bepalen.

Financiële standaarddimensies van projecten worden gebruikt om de standaardwaarden van journaalregels in te stellen voor transacties voor tijd, onkosten en vergoedingen in het **Project Operations-integratiejournaal** en op gerelateerde projectfactuurregels.
