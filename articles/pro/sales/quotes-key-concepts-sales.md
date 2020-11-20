---
title: Belangrijke concepten voor prijsopgaven - lite
description: Dit onderwerp biedt informatie over het gebruiken van projectprijsopgaven in Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e86f1a5a7b2859df5bf9569ee9ca306c6dcc6293
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178000"
---
# <a name="quotes---key-concepts---lite"></a>Belangrijke concepten voor prijsopgaven - lite

_**Van toepassing op:** Lite-implementatie - van deal tot pro-formafacturering_


Dit zijn belangrijke concepten waarvan u op de hoogte moet zijn voordat u projectprijsopgaven gaat gebruiken in Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Contracterende eenheid

De contracterende eenheid vertegenwoordigt de divisie of de methode die eigenaar is van de projectlevering. U kunt voor elke contracterende eenheid resourcekosten instellen. Wanneer u resourcekosten opgeeft voor een resource in de contracterende eenheid, kunt u ook verschillende kostentarieven instellen voor resources waarvan deze contracterende eenheid leent, of voor andere divisies of methoden binnen de onderneming. Dit worden verrekenprijzen of kosten voor het lenen of ruilen van resources genoemd. Wanneer u de kosten voor het lenen van resources van andere divisies instelt, kunt u er ook voor kiezen om die kostentarieven in te stellen in de valuta van de uitlenende divisie.

## <a name="cost-currency"></a>Kostenvaluta

De kostenvaluta in Project Operations is de valuta waarin kosten worden gerapporteerd. Deze valuta wordt afgeleid van de valuta die is gekoppeld aan het veld **Contracterende eenheid** op de prijsopgave, het contract en het project. Kosten kunnen in elke valuta voor een project worden geregistreerd. Er wordt echter een valutaconversie uitgevoerd van de valuta waarin de kosten zijn geboekt, naar de kostenvaluta van het project.

Omdat de wisselkoersen op het CDS-platform niet datumafhankelijk kunnen zijn, kunnen de totalen op het scherm voor kosten in de loop van de tijd veranderen als u de wisselkoersen bijwerkt. De kosten die in de database worden geregistreerd, blijven echter ongewijzigd, omdat de bedragen worden opgeslagen in de valuta waarin ze zijn gemaakt.

## <a name="sales-currency"></a>Verkoopvaluta

Verkoopvaluta in Project Operations is de valuta waarin de geschatte en werkelijke verkoopbedragen worden geregistreerd en weergegeven. Het is ook de valuta waarin de klant wordt gefactureerd voor de deal. Op een projectprijsopgave wordt de verkoopvaluta standaard ingesteld op basis van de klant- of accountrecord. Dit kan worden gewijzigd wanneer de prijsopgave wordt gemaakt. Nadat de prijsopgave is opgeslagen, kan de verkoopvaluta niet worden gewijzigd. Product- en projectprijslijsten zijn standaard gebaseerd op de verkoopvaluta van de offerte.

In tegenstelling tot kosten kunnen verkoopwaarden alleen worden geregistreerd in de verkoopvaluta.

## <a name="billing-method"></a>Factureringsmethode

Projecten hebben doorgaans contractmodellen op basis van vaste vergoedingen en verbruik. Dit wordt in Project Operations weergegeven als **Factureringsmethode** en heeft twee waarden: tijd en materiaal en een vaste prijs.

- **Tijd en materiaal:** dit is een op verbruik gebaseerd contractmodel waarbij alle gemaakte kosten worden gedekt door overeenkomstige inkomsten. Naarmate u hogere kosten schat of maakt, zullen de bijbehorende geschatte en werkelijke verkopen ook toenemen. U kunt niet-te-overschrijden limieten opgeven voor prijsopgaveregels die deze factureringsmethode hebben. Dit zal de werkelijke inkomsten beperken. De geschatte omzet wordt niet beïnvloed door limieten die niet overschreden mogen worden.
- **Vaste prijs:** dit is een contractmodel met een vaste vergoeding dat aangeeft dat de verkoopwaarden onafhankelijk zijn van de gemaakte kosten. De verkoopwaarde is vast en verandert niet naarmate u hogere kosten schat of maakt.

## <a name="project-price-lists"></a>Projectprijslijsten

Projectprijslijsten zijn prijslijsten die worden gebruikt voor standaardprijzen, niet voor kostentarieven, voor tijd, onkosten en andere projectgerelateerde componenten. Er kunnen meerdere prijslijsten zijn en elke lijst kan een eigen ingangsdatum hebben voor elke projectprijsopgave. Overlappende ingangsdatums op projectprijslijsten wordt niet ondersteund in Project Operations.

## <a name="product-price-lists"></a>Productprijslijsten

Productprijslijsten zijn prijslijsten waarmee standaardprijzen, geen kostentarieven, voor productgebaseerde regels op een offerte worden gebruikt. Er is slechts één productprijslijst per prijslijst.

## <a name="transaction-classes"></a>Transactieklassen

Project Operations ondersteunt vier soorten transactieklassen:

- Tijd
- Onkosten
- Materiaal
- Tarief

Kosten- en verkoopwaarden kunnen worden geschat en gemaakt in de transactieklassen Tijd, Onkosten en Materiaal. Vergoeding is een transactieklasse met alleen inkomsten.

## <a name="work-entities-and-billing-entities"></a>Werkentiteiten en factureringsentiteiten

Entiteiten voor werk zijn projecten en taken. Entiteiten voor facturering zijn prijsopgaveregels en contractregels. U kunt verschillende werkentiteiten aan factureringsopties koppelen door ze te koppelen aan prijsopgave- of contractregels.

## <a name="multi-customer-deals"></a>Deals voor meerdere klanten

Deals voor meerdere klanten vinden plaats wanneer er meer dan één klant moet worden gefactureerd. Dit zijn een aantal veelvoorkomende voorbeelden:

- **OEM-ondernemingen en hun partners:** partners en wederverkopers verkopen een product met diensten met toegevoegde waarde. Dit is meestal een scenario waarbij tijdens een bepaalde deal met een klant de OEM aanbiedt om een deel van het project te financieren. 

- **Projecten in de publieke sector:** meerdere afdelingen van een lokale overheid komen overeen om een project te financieren en worden gefactureerd volgens een eerder overeengekomen splitsing. Zo komen een schooldistrict en het stads- of gemeentebestuur overeen om de bouw van een zwembad te financieren.

## <a name="invoice-schedules"></a>Factuurschema's

Factuurschema's zijn specifiek voor elke prijsopgaveregel en zijn ook optioneel. Factuurschema's worden gemaakt op basis van bepaalde start- en einddatums en factuurfrequentie. Factuurschema's worden gebruikt in de contractfase wanneer het proces voor het automatisch maken van facturen is geconfigureerd. In de prijsopgavefase zijn de schema's optioneel. Wanneer factuurschema's worden gemaakt in de fase **Prijsopgave**, worden ze gekopieerd naar het projectcontract dat wordt gecreëerd wanneer een projectprijsopgave wordt geaccepteerd.

## <a name="changes-from-dynamics-365-sales-quote"></a>Wijzigingen ten opzichte van een Dynamics 365 Sales-prijsopgave:

Prijsopgaven voor Project Operations zijn gebaseerd op de prijsopgaven van Dynamics 365 Sales. Er zijn echter enkele belangrijke verschillen in functionaliteit waarvan u op de hoogte moet zijn:

- De acties **Herzien** en **Activeren** worden niet ondersteund.
- Prijsopgaven voor Project Operations hebben twee verschillende soorten regels. De ene is voor projecten en de andere is voor producten.
- Prijsopgaven voor Project Operations hebben hun eigen formulier- en UI-elementen, bedrijfsregels, bedrijfslogica in invoegtoepassingen en client-side scripts die ze uniek maken ten opzichte van verkoopprijsopgaven.

Daarom wordt het niet aanbevolen om een verkoopprijsopgave en een Project Operations-prijsopgave door elkaar te gebruiken.
