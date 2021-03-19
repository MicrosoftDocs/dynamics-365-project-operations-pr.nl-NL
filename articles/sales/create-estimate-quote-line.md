---
title: Schattingen maken op een prijsopgaveregel
description: Deze onderwerp biedt informatie over hoe u een schatting op een prijsopgaveregel voor een project kunt maken.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d525bd86621178761346221306dfc83e13e720d2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278457"
---
# <a name="create-estimates-on-a-quote-line"></a>Schattingen maken op een prijsopgaveregel

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

Voor een projectgebaseerde prijsopgave kunt u de entiteit Detail van prijsopgaveregel gebruiken om het werk te schatten dat nodig is om een project te leveren. U kunt die schatting vervolgens delen met de klant.

Projectgebaseerde prijsopgaveregels hoeven geen prijsopgaveregeldetails te bevatten. Ze kunnen ook een groot aantal prijsopgaveregeldetails bevatten. Prijsopgaveregeldetails worden gebruikt om tijd, onkosten of tarieven te schatten. In Dynamics 365 Project Operations zijn materiaalschattingen in prijsopgaveregeldetails niet toegestaan. Dit worden transactieklassen genoemd. Geschatte belastingbedragen kunnen ook worden ingevoerd voor een transactieklasse.

Naast transactieklassen bevatten prijsopgaveregeldetails een transactietype. Er zijn twee transactietypen voor prijsopgaveregeldetails, **Kosten** en **Projectcontract**.

## <a name="estimate-by-using-a-contract"></a>Schatting op basis van een contract

Als u een Project Operations-prijsopgave hebt gebruikt bij het maken van een projectgebaseerd contract, wordt uw schatting voor elke prijsopgaveregel in de prijsopgave naar het projectcontract gekopieerd. De structuur van een projectcontract is als de structuur van de projectprijsopgave met regels, regeldetails en factuurschema's.

Schattingen kunnen rechtstreeks in een projectcontract worden uitgevoerd, net als in een projectprijsopgave. Voor een projectprijsopgave wordt de schatting uitgevoerd met behulp van contractregels en contractregeldetails. Contractregeldetails kunnen ook worden gegenereerd op basis van een projectplan dat is gemaakt met behulp van een bottom-up-schatting.

Contractregeldetails kunnen worden gebruikt om tijd, onkosten of tarieven te schatten. Geschatte belastingbedragen kunnen ook worden ingevoerd voor een contractregeldetail.

Materiaalschattingen zijn niet toegestaan in contractregeldetails.

De processen die worden ondersteund in een projectcontract zijn het maken en bevestigen van facturen. Bij het maken van een factuur wordt een concept gemaakt van een projectgebaseerde factuur die alle niet-gefactureerde werkelijke verkoopwaarden tot de huidige datum bevat.

Bij bevestiging wordt het contract alleen-lezen en wordt de status van **Concept** in **Bevestigd** gewijzigd. Deze actie kan niet ongedaan worden gemaakt. Omdat deze actie permanent is, kunt u voor een contract de status **Concept** het beste behouden.

De enige verschillen tussen conceptcontracten en bevestigde contracten zijn de status en het feit dat conceptcontracten wel kunnen worden bewerkt en bevestigde contracten niet. Zowel voor conceptcontracten als voor bevestigde contracten kunnen facturen worden gemaakt en werkelijke waarden worden bijgehouden.

Wijzigingsorders zijn niet toegestaan voor contracten of projecten.

## <a name="estimating-projects"></a>Projecten schatten

U kunt de tijd en kosten voor projecten schatten, maar geen materialen of kosten.

Tijdschattingen worden gegenereerd wanneer u een taak maakt en de kenmerken identificeert van een algemene resource die nodig is om de taak uit te voeren. Tijdschattingen worden gegenereerd op basis van planningstaken. Tijdschattingen worden niet gemaakt als u algemene teamleden buiten de context van de planning maakt.

Onkostenschattingen kunnen worden ingevoerd in het raster op de pagina **Schattingen**.

## <a name="understand-estimation"></a>Inzicht in schattingen

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

Als u een aangepast veld hebt toegevoegd voor de prijsopgaveregeldetails en de waarde van het veld als standaardwaarde moet worden ingevoerd op de bijbehorende kostenregel die hiermee wordt gemaakt, gebruikt u de hulpmiddelen voor invoegtoepassingsregistratie PreOperationContractLineDetailUpdate en PreOperationQuoteLineDetailUpdate. Deze invoegtoepassingen moeten opnieuw worden geregistreerd als er prijsopgave- of contractregeldetails worden gewijzigd. Volg deze stappen om het proces te voltooien.

1. Open PluginRegistrationTool en maak verbinding met uw online-exemplaar.
2. Selecteer **Zoeken** en zoek de invoegtoepassing om bij te werken.
3. Selecteer de invoegtoepassing en selecteer vervolgens op de hoofdpagina **Selecteren**.
4. Selecteer de stap van de invoegtoepassing die moet worden bijgewerkt, klik met de rechtermuisknop en selecteer **Bijwerken**.
5. Selecteer in het dialoogvenster **Bestaande stap bijwerken** in het veld **Filterkenmerken** de ellipsknop (**...**):
6. Schakel in het dialoogvenster **Kenmerken selecteren** selectievakjes voor aangepaste kenmerken in.
7. Selecteer **OK** om het dialoogvenster te sluiten en selecteer vervolgens **Stap bijwerken**.
8. Herhaal stap 1 tot en met 7 voor de tweede invoegtoepassing.
9. Sluit PluginRegistrationTool.


[!INCLUDE[footer-include](../includes/footer-banner.md)]