---
title: Unieke concepten voor projectgebaseerde prijsopgaven
description: Dit artikel biedt informatie over projectprijsopgaven in Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824321"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Unieke concepten voor projectgebaseerde prijsopgaven

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_

Voordat u start met het gebruik van projectprijsopgaven in Microsoft Dynamics 365 Project Operations moet u op de hoogte zijn van de volgende belangrijke concepten.

## <a name="owning-company"></a>Bedrijf dat eigenaar is

Het bedrijf dat eigenaar is, vertegenwoordigt de rechtspersoon die eigenaar is van de projectlevering. De klant op de prijsopgave moet een geldige klant zijn in die rechtspersoon in apps voor financiën en bedrijfsactiviteiten. De valuta van het bedrijf dat eigenaar is en de valuta van de contracterende eenheid die is geselecteerd op een projectgebaseerde prijsopgave, moeten overeenkomen.

## <a name="contracting-unit"></a>Contracterende eenheid

Een contracterende eenheid vertegenwoordigt de divisie of de methode die eigenaar is van de projectlevering. U kunt voor elke contracterende eenheid resourcekosten instellen. Wanneer u resourcekosten opgeeft voor een resource in een contracterende eenheid, kunt u verschillende kostentarieven instellen voor resources waarvan deze contracterende eenheid leent, of voor andere divisies of methoden binnen de onderneming. Deze kostentarieven worden verrekenprijzen of kosten voor het lenen of ruilen van resources genoemd. Wanneer u de kosten voor het lenen van resources van andere divisies instelt, kunt u de kostentarieven instellen in de valuta van de uitlenende divisie.

## <a name="cost-currency"></a>Kostenvaluta

De kostenvaluta in Project Operations is de valuta waarin kosten worden gerapporteerd. Deze valuta wordt afgeleid van de valuta die is gekoppeld aan het veld **Contracterende eenheid** op de prijsopgave, het contract en het project. Kosten voor een project kunnen in elke valuta worden geboekt. Er wordt echter een valutaconversie uitgevoerd van de valuta waarin de kosten zijn geboekt, naar de kostenvaluta van het project.

Omdat de wisselkoersen op het Dataverse-platform niet datumafhankelijk kunnen zijn, kunnen de totalen op het scherm voor kosten in de loop van de tijd veranderen als u de wisselkoersen bijwerkt. De kosten die in de database worden geregistreerd, blijven echter ongewijzigd, omdat de bedragen worden opgeslagen in de valuta waarin ze zijn gemaakt.

## <a name="sales-currency"></a>Verkoopvaluta

De verkoopvaluta in Project Operations is de valuta waarin de geschatte en werkelijke verkoopbedragen worden geregistreerd en weergegeven. Het is ook de valuta waarin de klant voor de deal wordt gefactureerd. Voor een projectprijsopgave wordt de standaardverkoopvaluta ingesteld op basis van de klant- of accountrecord. Dit kan worden gewijzigd wanneer de prijsopgave wordt gemaakt. Nadat de prijsopgave is opgeslagen, kan de verkoopvaluta echter niet worden gewijzigd. Standaardproduct- en projectprijslijsten zijn ingesteld op basis van de verkoopvaluta van de prijsopgave.

In tegenstelling tot kosten kunnen verkoopwaarden **alleen** worden geregistreerd in de verkoopvaluta.

## <a name="billing-method"></a>Factureringsmethode

Projecten hebben doorgaans contractmodellen op basis van vaste vergoedingen en verbruik. In project Operations wordt het contractmodel van een project vertegenwoordigd door de factureringsmethode. De factureringsmethode heeft twee waardes: tijd en materiaal of vaste prijs.

- **Tijd en materiaal:** – Een op verbruik gebaseerd contractmodel waarbij alle gemaakte kosten worden gedekt door overeenkomstige omzet. Naarmate u hogere kosten schat of maakt, zullen de bijbehorende geschatte en werkelijke verkopen ook toenemen. U kunt niet-te-overschrijden limieten opgeven voor prijsopgaveregels die deze factureringsmethode hebben. Op deze manier kunt u de werkelijke omzet begrenzen. De geschatte omzet wordt niet beïnvloed door niet te overschrijden limieten.
- **Vaste prijs** – Een contractmodel met vaste kosten waarin verkoopkosten onafhankelijk zijn van de gemaakte kosten. De verkoopwaarde is vast en verandert niet wanneer u hogere kosten schat of maakt.

## <a name="project-price-lists"></a>Projectprijslijsten

Projectprijslijsten zijn prijslijsten die worden gebruikt om standaardprijzen (en geen kostprijzen) in te voeren voor tijd, onkosten en andere projectgerelateerde componenten. Er kunnen meerdere prijslijsten zijn en elke lijst kan een eigen ingangsdatum hebben voor elke projectprijsopgave. Project Operations ondersteunt geen overlappende datumeffectiviteit voor projectprijslijsten.

## <a name="product-price-lists"></a>Productprijslijsten

Productprijslijsten zijn prijslijsten waarmee standaardprijzen (dus geen kostentarieven) worden ingevoerd voor productgebaseerde regels op een prijsopgave. Er is slechts één productprijslijst per prijsopgave.

## <a name="transaction-classes"></a>Transactieklassen

Project Operations ondersteunt vier soorten transactieklassen:

- Tijd
- Onkosten
- Materiaal
- Tarief

Kosten- en verkoopwaarden kunnen worden geschat en gemaakt in de transactieklassen **Tijd**, **Onkosten** en **Materiaal**. **Tarief** is een transactieklasse voor alleen omzet.

## <a name="work-entities-and-billing-entities"></a>Werkentiteiten en factureringsentiteiten

Projecten en Taken zijn entiteiten die werk vertegenwoordigen. Prijsopgaveregels en Contractregels zijn entiteiten die facturering vertegenwoordigen. U kunt verschillende werkentiteiten aan factureringsopties koppelen door ze te koppelen aan prijsopgave- of contractregels.

## <a name="multi-customer-deals"></a>Deals voor meerdere klanten

Deals voor meerdere klanten vinden plaats als er meer dan één klant per factuur is. Hieronder volgen een aantal typische voorbeelden:

- **Fabrikanten van originele apparatuur (OEM) en hun partners** – Partners en wederverkopers verkopen een product waarin diensten met toegevoegde waarde zijn inbegrepen. Tijdens een bepaalde deal met een klant biedt de OEM meestal aan om een deel van het project te financieren.
- **Projecten in de publieke sector:** – Meerdere afdelingen van een lokale overheid komen overeen om een project te financieren en worden gefactureerd volgens een eerder overeengekomen splitsing. Zo komen een schooldistrict en het stads- of gemeentebestuur overeen om de bouw van een zwembad te financieren.

## <a name="invoice-schedules"></a>Factuurschema's

Factuurschema's zijn specifiek voor elke prijsopgaveregel en zijn optioneel. Factuurschema's worden gemaakt op basis van specifieke start- en einddatums en een factuurfrequentie. Ze worden gebruikt in de contractfase wanneer het proces voor het automatisch maken van facturen wordt geconfigureerd. Gedurende de prijsopgavefase zijn factuurschema's optioneel. Als ze worden gemaakt tijdens de fase Prijsopgave, worden ze gekopieerd naar het projectcontract dat wordt gecreëerd wanneer een projectprijsopgave wordt geaccepteerd.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Verschillen met een Dynamics 365 Sales-prijsopgave

Prijsopgaven voor Project Operations zijn gebaseerd op prijsopgaven van Dynamics 365 Sales. Er zijn echter enkele belangrijke verschillen in functionaliteit waarvan u op de hoogte moet zijn:

- Project Operations-prijsopgaven hebben twee verschillende soorten regels: één voor projecten en één voor producten.
- Prijsopgaven voor Project Operations hebben hun eigen pagina en UI-elementen, bedrijfsregels, bedrijfslogica in invoegtoepassingen en client-side scripts die ze uniek maken ten opzichte van verkoopprijsopgaven.
- In Verkoop kunt meerdere orders aan een enkele verkoopprijsopgave koppelen. In Project Operations kunt u slechts één projectcontract aan een projectprijsopgave koppelen.
- Als een prijsopgave wordt geaccepteerd, kan de gerelateerde verkoopkans open blijven. Als u een order binnenhaalt met een projectprijsopgave, wordt de gerelateerde verkoopkans gesloten.
- Een verkoopprijsopgave bevat niet alle velden en concepten die zijn opgenomen in een projectprijsopgave. De velden omvatten **Contracterende eenheid**, **Accountmanager** en **Naam van de contactpersoon voor de factuur**.
- Verkoopprijsopgaven en projectprijsopgaven kunnen worden geïdentificeerd aan de hand van het op een optieset gebaseerde veld **Type**. Voor een verkoopprijsopgave is de waarde van dit veld **Artikelgebaseerd**. Voor een projectprijsopgave is de waarde **Werkgebaseerd**.

Vanwege deze verschillen raden wij u aan verkoopprijsopgaven en Project Operations-prijsopgaven niet door elkaar gebruiken.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
