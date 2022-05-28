---
title: Integratie van projectfacturen
description: Dit onderwerp biedt informatie over integratie voor klantfacturering via twee keer wegschrijven in Project Operations.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581232"
---
# <a name="project-invoice-integration"></a>Integratie van projectfacturen

Dit onderwerp biedt informatie over integratie voor klantfacturering via twee keer wegschrijven in Project Operations.

In Project Operations beheert de projectmanager de achterstand in projectfacturering en maakt een pro-formafactuur voor de klant in Microsoft Dataverse. Op basis van deze pro-formafactuur maakt de klantenadministrateur of projectaccountant een klantgerichte factuur aan. Integratie van twee keer wegschrijven zorgt ervoor dat de pro forma-factuurgegevens worden gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten. Nadat de klantgerichte factuur is geboekt, werkt het systeem de relevante werkelijke projectwaarden bij in Dataverse met de boekhoudkundige details. De volgende afbeelding geeft een conceptueel overzicht op hoofdlijnen van deze integratie.

   ![Integratie van projectfacturen.](./media/DW5Invoicing.png)

Nadat de projectmanager de pro forma-factuur heeft bevestigd in Dataverse, wordt de koptekstinformatie van de pro forma-factuur gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing voor twee keer wegschrijven **Projectfactuurvoorstel V2 (facturen)**. Dit is een eenrichtingsintegratie van Dataverse naar apps voor financiën en bedrijfsactiviteiten. Het rechtstreeks maken of verwijderen van projectfactuurvoorstellen in apps voor financiën en bedrijfsactiviteiten wordt niet ondersteund.

Factuurbevestiging in Dataverse activeert ook de bedrijfslogica om factureringsgerelateerde records te maken in de entiteit **Werkelijke waarden**. Deze records worden gesynchroniseerd met apps voor financiën en bedrijfsactiviteiten met behulp van de tabeltoewijzing voor twee keer wegschrijven **Integratie van werkelijke waarden in Project Operations (msdyn\_actuals)**. Zie [Schattingen en werkelijke waarden voor projecten](resource-dual-write-estimates-actuals.md) voor meer informatie . 

Voorstelregels voor projectfacturen worden gemaakt door het periodieke proces **Formulieropslag importeren**. Dit proces is gebaseerd op de gefactureerde werkelijke verkoopgegevens in de tabel **Opslag van werkelijke waarden**. Zie [Projectfactuurvoorstellen beheren](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals) voor meer informatie. 
