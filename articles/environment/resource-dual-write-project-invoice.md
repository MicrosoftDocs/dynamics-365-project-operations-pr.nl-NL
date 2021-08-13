---
title: Integratie van projectfacturen
description: Dit onderwerp biedt informatie over integratie voor klantfacturering via twee keer wegschrijven in Project Operations.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 37549080d76e3bffd7cb002aee8e3c46b9eeb18e3cec915cd971881b69747534
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993235"
---
# <a name="project-invoice-integration"></a>Integratie van projectfacturen

Dit onderwerp biedt informatie over integratie voor klantfacturering via twee keer wegschrijven in Project Operations.

In Project Operations beheert de projectmanager de achterstand in projectfacturering en maakt een pro-formafactuur voor de klant in Microsoft Dataverse. Op basis van deze pro-formafactuur maakt de klantenadministrateur of projectaccountant een klantgerichte factuur aan. Integratie van twee keer wegschrijven zorgt ervoor dat de pro-formafactuurgegevens worden gesynchroniseerd met Finance and Operations-apps. Nadat de klantgerichte factuur is geboekt, werkt het systeem de relevante werkelijke projectwaarden bij in Dataverse met de boekhoudkundige details. De volgende afbeelding geeft een conceptueel overzicht op hoofdlijnen van deze integratie.

   ![Integratie van projectfacturen.](./media/DW5Invoicing.png)

Nadat de projectmanager de pro-formafactuur heeft bevestigd in Dataverse, wordt de kopinformatie van de pro-formafactuur gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing voor twee keer wegschrijven **Projectfactuurvoorstel V2 (facturen)**. Dit is een eenrichtingsintegratie van Dataverse met Finance and Operations-apps. Het maken of verwijderen van projectfactuurvoorstellen rechtstreeks in Finance and Operations-apps wordt niet ondersteund.

Factuurbevestiging in Dataverse activeert ook de bedrijfslogica om factureringsgerelateerde records te maken in de entiteit **Werkelijke waarden**. Deze records worden gesynchroniseerd met Finance and Operations-apps met behulp van de tabeltoewijzing voor twee keer wegschrijven **Werkelijke waarden voor Project Operations-integratei (msdyn\_actuals)**. Zie [Schattingen en werkelijke waarden voor projecten](resource-dual-write-estimates-actuals.md) voor meer informatie . 

Voorstelregels voor projectfacturen worden gemaakt door het periodieke proces **Formulieropslag importeren**. Dit proces is gebaseerd op de gefactureerde werkelijke verkoopgegevens in de tabel **Opslag van werkelijke waarden**. Zie [Projectfactuurvoorstellen beheren](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals) voor meer informatie. 
