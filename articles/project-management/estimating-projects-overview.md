---
title: Concepten voor financiële schattingen
description: Dit onderwerp biedt informatie over financiële schattingen van projecten in Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597746"
---
# <a name="financial-estimation-concepts"></a>Concepten voor financiële schattingen

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

In Dynamics 365 Project Operations kunt u uw projecten in twee fasen financieel schatten: 
1. Tijdens de voorverkoopfase voordat de deal wordt binnengehaald. 
2. Tijdens de uitvoeringsfase nadat het projectcontract is gemaakt. 

U kunt een financiële schatting maken voor projectgebaseerd werk met behulp van een van de volgende drie pagina's:
- De pagina **Offerteregel**, via de prijsopgaveregeldetails.  
- De pagina **Projectcontractregel**, via de contractregeldetails. 
- De pagina **Project**, via het tabblad **Taken** of **Onkostenschattingen**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Een projectprijsopgave gebruiken om een schatting te maken
Voor een projectgebaseerde prijsopgave kunt u de entiteit **Detail van prijsopgaveregel** gebruiken om het werk te schatten dat nodig is om een project te leveren. U kunt die schatting vervolgens delen met de klant.

Projectgebaseerde prijsopgaveregels kunnen geen, enkele of vele prijsopgaveregeldetails bevatten. Prijsopgaveregeldetails worden gebruikt om tijd, onkosten of tarieven te schatten. In Microsoft Dynamics 365 Project Operations zijn materiaalschattingen in prijsopgaveregeldetails niet toegestaan. Dit worden transactieklassen genoemd. Geschatte belastingbedragen kunnen ook worden ingevoerd voor een transactieklasse.

Naast transactieklassen bevatten prijsopgaveregeldetails een transactietype. Er worden twee transactietypen ondersteund voor prijsopgaveregeldetails: **Kosten** en **Projectcontract**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Een projectcontract gebruiken om een schatting te maken

Als u een prijsopgave hebt gebruikt bij het maken van een projectgebaseerd contract, wordt uw schatting voor elke prijsopgaveregel in de prijsopgave naar het projectcontract gekopieerd. De structuur van een projectcontract is als de structuur van de projectprijsopgave met regels, regeldetails en factuurschema's.

Schattingen kunnen rechtstreeks in een projectcontract worden uitgevoerd, net als in een projectprijsopgave. Voor een projectprijsopgave wordt de schatting uitgevoerd met behulp van contractregels en contractregeldetails. Contractregeldetails kunnen ook worden gegenereerd op basis van een projectplan dat is gemaakt met behulp van een bottom-up-schatting.

Contractregeldetails kunnen worden gebruikt om tijd, onkosten of tarieven te schatten. Geschatte belastingbedragen kunnen ook worden ingevoerd voor een contractregeldetail.

Materiaalschattingen zijn niet toegestaan in contractregeldetails.

## <a name="use-a-project-to-create-an-estimate"></a>Een project gebruiken om een schatting te maken 

U kunt schattingen voor tijd en onkosten maken voor projecten. Project Operations ondersteunt geen schattingen van materialen of vergoedingen voor projecten.

Tijdschattingen worden gegenereerd wanneer u een taak maakt en de kenmerken identificeert van een algemene resource die nodig is om de taak uit te voeren. Tijdschattingen worden gegenereerd op basis van planningstaken. Tijdschattingen worden niet gemaakt als u algemene teamleden buiten de context van de planning maakt.

Onkostenschattingen kunnen worden ingevoerd in het raster op de pagina **Onkostenschattingen**.

Het maken van een schatting voor een project wordt als best practice beschouwd omdat u bottom-up gedetailleerde schattingen voor arbeid of tijd en onkosten kunt maken voor elke taak in het projectplan. U kunt deze gedetailleerde schatting vervolgens gebruiken om schattingen voor elke prijsopgaveregel te maken en een meer geloofwaardige prijsopgave voor de klant op te bouwen. Wanneer u met het projectplan een gedetailleerde schatting op de prijsopgaveregel importeert of maakt, worden de verkoop- en kostenwaarde van deze schattingen in Project Operations geïmporteerd. Na het importeren kunt u de winstgevendheid, marges en haalbaarheidsstatistieken voor de projectprijsopgave bekijken.

## <a name="understanding-estimates"></a>Schattingen begrijpen

Gebruik de volgende tabel als richtlijn voor het begrijpen van de bedrijfslogica in de schattingsfase.

| Scenario                                                                                                                                                                                                                                                                                                                                          | Entiteitsrecord                                                                                                                                                                                                       | Transactietype | Transactieklasse | Aanvullende informatie                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Wanneer u de verkoopwaarde van tijd in een prijsopgave moet schatten                                                                                                                                                                                                                                                                                    | Een record Detail van prijsopgaveregel wordt gemaakt                                                                                                                                                                               | Projectcontract | Time        | Het veld Oorsprong van transactie in de rij Detail van prijsopgaveregel aan de verkoopzijde verwijst naar Detail van prijsopgaveregel aan de kostenzijde |
|                                                                                                                                                                                                                                                                                     | Er wordt een tweede record Detail van prijsopgaveregel gemaakt om de bijbehorende kostenwaarden op te slaan. Alle niet-geldvelden worden gekopieerd uit de rij Detail van prijsopgaveregel aan de verkoopzijde naar de rij Detail van prijsopgaveregel aan de kostenzijde.                                                                                                                                                                               | Kosten | Time        | Het veld Oorsprong van transactie in de rij Detail van prijsopgaveregel aan de verkoopzijde verwijst naar Detail van prijsopgaveregel aan de kostenzijde |
| Wanneer u de verkoopwaarde van tijd in een contract moet schatten                                                                                                                                                                                                                                                                                 | Een projectrecord Detail van contractregel wordt gemaakt                                                                                                                                                                    | Projectcontract | Time        | Het veld Oorsprong van transactie in de rij Detail van contractregel aan de verkoopzijde verwijst naar Detail van contractregel aan de kostenzijde      |
|                                                                                                                                                                                                                                                                                  | Er wordt een tweede record Detail van contractregel gemaakt om de bijbehorende kostenwaarden op te slaan. Alle niet-geldvelden worden gekopieerd uit de rij Detail van contractregel aan de verkoopzijde naar de rij Detail van contractregel aan de kostenzijde.                                                                                                                                                                    | Kosten | Time        | Het veld Oorsprong van transactie in de rij Detail van contractregel aan de verkoopzijde verwijst naar Detail van contractregel aan de kostenzijde      |
| Wanneer de gebruiker een resource in een projecttaak beschrijft                                                                                                                                                                                                                                                                                            | Er wordt een schattingsregelrecord voor de verkoopwaarde van de taak gemakt wanneer een taak wordt gemaakt met alle vereiste prijsdimensies. Rol en organisatie-eenheden zijn de prijsdimensies | Projectcontract | Tijd        |                                                                                   |
|     | De schattingsregelrecord voor de kostenwaarde van de taak wordt gemaakt wanneer een taak wordt gemaakt met alle vereiste prijsdimensies. Alle niet-geldvelden worden gekopieerd uit de verkoopschattingsregel naar de kostenschattingsregel. Rol en organisatie-eenheid zijn de prijsdimensies voor kosten- en factuurtarieven.                                                                                                                                                                                                                | Kosten             | Tijd           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>De entiteiten Detail van prijsopgaveregel en Detail van contractregel aanpassen

Als u een aangepast veld hebt toegevoegd voor de prijsopgaveregeldetails en de waarde van het veld als standaardwaarde moet worden ingevoerd op de bijbehorende kostenregel die hiermee wordt gemaakt, gebruikt u de hulpmiddelen voor invoegtoepassingsregistratie **PreOperationContractLineDetailUpdate** en **PreOperationQuoteLineDetailUpdate**. Deze invoegtoepassingen moeten opnieuw worden geregistreerd als er prijsopgave- of contractregeldetails worden gewijzigd. Volg deze stappen om het proces te voltooien.

1. Open PluginRegistrationTool en maak verbinding met uw online-exemplaar.
2. Selecteer **Zoeken** en zoek de invoegtoepassing om bij te werken.
3. Selecteer de invoegtoepassing en klik vervolgens op de hoofdpagina op **Selecteren**.
4. Selecteer de stap van de invoegtoepassing die moet worden bijgewerkt, klik met de rechtermuisknop en selecteer **Bijwerken**.
5. Selecteer in het dialoogvenster **Bestaande stap bijwerken** in het veld **Filterkenmerken** de ellipsknop (**...**):
6. Schakel in het dialoogvenster **Kenmerken selecteren** selectievakjes voor aangepaste kenmerken in.
7. Selecteer **OK** om het dialoogvenster te sluiten en selecteer vervolgens **Stap bijwerken**.
8. Herhaal stap 1 tot en met 7 voor de tweede invoegtoepassing.
9. Sluit de **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
