---
title: Unieke concepten voor projectgebaseerde contracten
description: Dit artikel bevat informatie over de belangrijkste concepten van projectcontracten in Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 48053bf6209d0a997e4e8766e29d77f994da06b4
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825840"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Unieke concepten voor projectgebaseerde contracten

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen_



Dit artikel biedt de belangrijkste concepten waarmee u rekening moet houden voordat u Project-contracten gaat gebruiken in Dynamics 365 Project Operations:

## <a name="owning-company"></a>Bedrijf dat eigenaar is

De eigenaar is de rechtspersoon van de module **Projectbeheer en financiële administratie** voor Project Operations vanuit Dynamics 365 Finance. Het bedrijf dat eigenaar is, vertegenwoordigt de rechtspersoon die verantwoordelijk is voor de kosten en opbrengsten van een deal.

## <a name="contracting-unit"></a>Contracterende eenheid

De contracterende eenheid vertegenwoordigt de divisie of de methode die eigenaar is van het project. U kunt voor elke contracterende eenheid resourcekosten instellen. Wanneer u de resourcekosten voor een resource opgeeft, kunt u ook verschillende kostentarieven voor resources instellen. Deze contracterende eenheid leent deze resources van andere divisies of methoden binnen de onderneming. De kostentarieven voor de resources worden verrekenprijzen of kosten voor het lenen of ruilen van resources genoemd. Wanneer u de kostentarieven voor het lenen van resources van andere divisies instelt, gebruikt u de valuta van de uitlenende divisie.

## <a name="cost-currency"></a>Kostenvaluta

De kostenvaluta is de valuta waarin kosten op het scherm worden gerapporteerd. Deze valuta wordt afgeleid van de valuta die is gekoppeld aan het veld **Contracterende eenheid** op het contract en het project. Kosten kunnen in elke valuta voor een project worden geregistreerd. Er wordt echter een valutaconversie uitgevoerd van de valuta waarin de kosten zijn geboekt, naar de kostenvaluta van het project wanneer deze op het scherm worden weergegeven.

Omdat de wisselkoersen op het Common Data Service-platform (CDS) niet datumafhankelijk kunnen zijn, kunnen de totalen op het scherm voor kosten in de loop van de tijd veranderen als u de wisselkoersen bijwerkt. De kosten die in de database worden geregistreerd, blijven echter ongewijzigd, omdat de bedragen worden opgeslagen in de valuta waarin ze zijn gemaakt.

## <a name="sales-currency"></a>Verkoopvaluta

Verkoopvaluta in Project Operations is de valuta waarin de geschatte en werkelijke verkoopbedragen worden geregistreerd en weergegeven. Verkoopvaluta is ook de valuta waarin de klant wordt gefactureerd voor de deal. In een projectcontract wordt de verkoopvaluta standaard ingesteld op basis van de klant- of accountrecord. Dit kan worden gewijzigd wanneer het contract wordt gemaakt. Wanneer een contract wordt gemaakt door een prijsopgave als gewonnen te sluiten, wordt de valuta op het contract standaard ingesteld op de valuta op de prijsopgave.

Wanneer u een geheel nieuw projectcontract maakt, kan het veld **Verkoopvaluta** niet worden bewerkt. Product- en projectprijslijsten worden standaard gebaseerd op deze valuta in het contract.

In tegenstelling tot kosten kunnen verkoopwaarden alleen worden geregistreerd in de verkoopvaluta.

## <a name="billing-method"></a>Factureringsmethode

Er zijn doorgaans twee soorten contractmodellen voor projecten: op basis van vaste kosten en op basis van verbruik. Deze modellen worden in Project Operations weergegeven als factureringsmethoden met twee mogelijke waarden:

- Tijd en materiaal: dit is een op verbruik gebaseerd contractmodel waarbij alle gemaakte kosten worden gedekt door bijbehorende omzet. Naarmate u hogere kosten schat of maakt, zullen de bijbehorende geschatte en werkelijke verkopen ook toenemen. Geef niet te overschrijden limieten op voor contractregels die deze factureringsmethode gebruiken waarmee de werkelijke omzet wordt begrensd. De geschatte omzet wordt niet beïnvloed door niet te overschrijden limieten.
- Vaste prijs: dit is een contractmodel met vaste kosten waarmee wordt aangegeven dat de verkoopwaarden onafhankelijk zijn van de gemaakte kosten. De verkoopwaarde is vast en verandert niet wanneer u hogere kosten schat of maakt.

## <a name="project-price-lists"></a>Projectprijslijsten

Projectprijslijsten worden gebruikt voor standaardprijzen, niet voor kostentarieven, tijd, onkosten en andere projectgerelateerde onderdelen. Er kunnen meerdere prijslijsten zijn. Elke prijslijst heeft eigen geldigheidsdatums voor elk projectcontract. Overlappende geldigheidsdatums in projectprijslijsten worden niet ondersteund in Project Operations.

Wanneer een projectcontract wordt gemaakt door het winnen van een projectofferte, worden projectprijslijsten gekopieerd waarin de contractnaam en de datum zijn opgenomen. Door deze gegevens te kopiëren krijgt u aangepaste prijzen voor projectonderdelen in dit projectcontract.

## <a name="transaction-classes"></a>Transactieklassen

Project Operations ondersteunt vier soorten transactieklassen:

- Tijd
- Onkosten
- Materiaal
- Tarief

Kosten- en verkoopwaarden kunnen worden geschat en gemaakt in de transactieklassen Tijd, Onkosten en Materiaal. Kosten is een transactieklasse voor alleen omzet.

## <a name="work-entities-and-billing-entities"></a>Werkentiteiten en factureringsentiteiten

Entiteiten voor werk zijn projecten en taken. Entiteiten voor facturering zijn contractregels. U kunt verschillende werkentiteiten aan factureringsopties koppelen door ze te koppelen aan contractregels.

## <a name="multi-customer-deals"></a>Deals voor meerdere klanten

Deals voor meerdere klanten hebben meer dan één klant die moet worden gefactureerd in een deal. Dit zijn een aantal veelvoorkomende voorbeelden:

- OEM-ondernemingen en hun partners: partners en wederverkopers verkopen een product met een aantal diensten met toegevoegde waarde, meestal heeft dit betrekking op een bepaalde deal met een klant. De OEM biedt aan om een deel van het project te financieren. 

- Projecten in de publieke sector: meerdere afdelingen van een lokale overheid komen overeen om een project te financieren en worden gefactureerd volgens een eerder overeengekomen splitsing. Zo komen een schooldistrict en de lokale overheid overeen om de bouw van een zwembad te financieren.

## <a name="invoice-schedules"></a>Factuurschema's

Factuurschema's zijn specifiek voor elke contractregel en zijn vereist voor automatische facturering. Factuurschema's worden gemaakt op basis van bepaalde start- en einddatums en factuurfrequentie. De schema´s worden gebruikt in de contractfase wanneer het proces voor het automatisch maken van facturen wordt geconfigureerd. Wanneer een projectcontract wordt gemaakt op basis van een offerte, wordt het factuurschema vanuit de offerte naar het projectcontract gekopieerd.

## <a name="changes-from-dynamics-365-sales-orders"></a>Wijzigingen ten opzichte van orders in Dynamics 365 Sales

Contracten in Project Operations zijn gebaseerd op orders in Dynamics 365 Sales. Er zijn echter enkele belangrijke afwijkingen en verschillen in functionaliteit. Contracten hebben hun eigen formulier- en UI-elementen, bedrijfsregels, bedrijfslogica in invoegtoepassingen en client-side scripts die ze uniek maken ten opzichte van Orders. Om deze redenen moet u een Sales-order en een Project Operations-contract niet door elkaar gebruiken.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
