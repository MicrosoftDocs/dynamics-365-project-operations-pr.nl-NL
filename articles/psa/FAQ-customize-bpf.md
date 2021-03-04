---
title: Het pas ik de bedrijfsprocesstroom Projectfasen aan?
description: Een overzicht van de manier waarop u de bedrijfsprocesstroom Projectfasen aanpast.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148997"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Het pas ik de bedrijfsprocesstroom Projectfasen aan?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Er bestaat een bekende beperking in eerdere versies van de Project Service-toepassing dat de namen van de fasen in de bedrijfsprocesstroom Projectfasen exact moeten overeenkomen met de verwachte Engelse namen (**Quote**, **Plan**, **Close**). Anders werkt de bedrijfslogica, die is gebaseerd op de Engelse fasenamen, niet zoals verwacht. Daarom zijn vertrouwde acties, zoals **Proces omwisselen** of **Proces bewerken**, niet beschikbaar in het projectformulier en het aanpassen van de bedrijfsprocesstroom wordt niet aangeraden. 

Deze beperking is opgelost in versie 2.4.5.48 en hoger. Dit artikel bevat voorgestelde oplossingen als u de standaardbedrijfsprocesstroom moet aanpassen voor eerdere versies.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Bedrijfslogica vereist een exacte overeenkomst met Engels fasenamen

De bedrijfsprocesstroom Projectfasen bevat bedrijfslogica die het volgende gedrag aanstuurt in de app:
- Wanneer het project aan een offerte wordt gekoppeld, wordt de bedrijfsprocesstroom ingesteld op de fase **Quote**.
- Wanneer het project aan een contract wordt gekoppeld, wordt de bedrijfsprocesstroom ingesteld op de fase **Plan**.
- Wanneer de bedrijfsprocesstroom in de fase **Close** terechtkomt, wordt de projectrecord gedeactiveerd. Wanneer het project wordt gedeactiveerd, zijn het projectformulier en de structuur voor werkspecificatie alleen-lezen, worden de benoemde resourceboekingen vrijgegeven en worden eventueel gekoppelde prijslijsten gedeactiveerd.

De bedrijfslogica is voor de projectfasen afhankelijk van de Engelse namen. De afhankelijkheid van de Engelse fasenamen is de belangrijkste reden waarom aanpassingen van de bedrijfsprocesstroom Projectfasen niet wordt aangeraden en waarom u gangbare bedrijfsprocesstroomacties als **Proces omwisselen** of **Proces bewerken** niet tegenkomt in de projectentiteit.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Wat gebeurt er als de fasenamen niet overeenkomen met de Engelse namen?

Als in versie 1.x van de Project Service-app op het 8.2-platform de fasenamen in de bedrijfsprocesstroom niet exact overeenkomen met de Engelse fasenamen, wordt de bedrijfslogica waarmee de juiste fase voor prijsopgaven of contracten wordt ingesteld, of het project wordt gesloten, overgeslagen. Er worden geen foutberichten weergegeven. Daarom lijkt het alsof u de bedrijfsprocesstroom Projectfasen kunt aanpassen. U zult er echter achterkomen dat de automatische processen voor prijsopgaven, contracten en het sluiten van projecten niet werken.

In versie 2.4.4.30 of eerder van de Project Service-app op het 9.0-platform was er een aanzienlijke architectuurverandering in bedrijfsprocesstromen, waarvoor de bedrijfslogica van bedrijfsprocesstromen moest worden herschreven. Als gevolg daarvan wordt er een foutbericht weergegeven als de namen van procesfasen niet overeenkomen met de verwachte Engelse namen. 

Als u de bedrijfsprocesstroom Projectfasen voor de projectentiteit wilt aanpassen, kunt u alleen nieuwe fasen toevoegen aan de standaardbedrijfsprocesstroom voor de projectentiteit en de fasen **Quote**, **Plan** en **Close** ongewijzigd laten. Deze beperking zorgt ervoor dat u geen fouten over de bedrijfslogica ontvangt omdat er Engels fasenamen worden verwacht in de bedrijfsprocesstroom.

In versie 2.4.5.48 of hoger is de in dit artikel beschreven bedrijfslogica verwijderd uit de standaardbedrijfsprocesstroom voor de projectentiteit. Wanneer u bijwerkt naar die versie of hoger, kunt u de standaardbedrijfsprocesstroom aanpassen of vervangen door een van uw eigen bedrijfsprocesstromen. 

## <a name="workarounds-for-earlier-versions"></a>Oplossingen voor eerdere versies

Als een upgrade geen optie is, kunt u de bedrijfsprocesstroom Projectfasen voor de projectentiteit op een van deze twee manieren aanpassen:

1. Voeg extra fasen toe aan de standaardconfiguratie terwijl u de Engelse fasenamen **Quote**, **Plan** en **Close** behoudt.


![Schermafbeelding van het toevoegen van fasen aan de standaardconfiguratie](media/FAQ-Customize-BPF-1.png)
 
2. Maak uw eigen bedrijfsprocesstroom en stel deze in als de primaire bedrijfsprocesstroom voor de projectentiteit. In dat geval kunt u de gewenste fasenamen instellen. Als u echter dezelfde standaardprojectfasen **Quote**, **Plan** en **Close** wilt gebruiken, moet u enkele aanpassingen doorvoeren. De meer complexe logica heeft betrekking op de sluiting van het project, die u nog wel kunt wel activeren door de projectrecord te deactiveren.

![BPF-aanpassing](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Extra overwegingen voor appversie 2.4.4.30 of eerder van Project Service of op platform 9.0

Wanneer in Project Service 2.4.4.30 of eerdere versies op platform 9.0 aangepaste bedrijfsprocesstromen worden gebruikt, worden het veld **Fasenaam** voor de projectentiteit in het diagram **Project per fase** en projectlijstweergaven niet bijgewerkt omdat deze zijn gekoppeld aan de standaardbedrijfsprocesstroom Projectfasen. U lost dit probleem als volgt op:

- Voeg een aangepast veld toe om de huidige bedrijfsprocesstroomfase vast te leggen die wordt bijgewerkt terwijl de gebruiker de aangepaste bedrijfsprocesstroom doorloopt.

- Wijzig het diagram **Project per fase** om met uw aangepaste velden te werken in plaats van met de standaardconfiguratie.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Stappen om uw eigen bedrijfsprocesstroom voor de projectentiteit te maken

Ga als volgt te werk om uw eigen bedrijfsprocesstroom voor de projectentiteit te maken:

1. Ga naar **Instellingen** > **Verwerkingscentrum**. Kopieer de bedrijfsprocesstroom Projectfasen niet omdat dan ook de bedrijfslogica van Project Service wordt gekopieerd.

  ![Proces maken](media/FAQ-Customize-BPF-3.png)

2. Gebruik de procesontwerper om de gewenste fasenamen te maken. Als u dezelfde functionaliteit als de standaardfasen voor **Quote**, **Plan** en **Close** wilt gebruiken, moet u deze maken op basis van de fasenamen van uw aangepaste bedrijfsprocesstroom.

   ![Schermafbeelding van procesontwerper om bedrijfsprocesstromen aan te passen](media/FAQ-Customize-BPF-4.png) 

3. Klik in de procesontwerper op **Orderprocesstroom** om de aangepaste bedrijfsprocesstroom als primaire bedrijfsprocesstroom voor de projectentiteit in te stellen door deze boven de bedrijfsprocesstroom Projectfasen boven aan de lijst te plaatsen.


   [Schermafbeelding van het gebruik van Orderprocesstroom](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>De volgende stappen gelden voor Project Service-app 2.4.4.30 of eerder op het 9.0-platform.

4. Voeg een nieuw aangepast veld aan de projectentiteit toe om de aangepaste fasen in uw aangepaste bedrijfsprocesstroom vast te leggen. U moet bedrijfslogica (invoegtoepassing/werkstroom) toevoegen om dit veld bij te werken wanneer de fase in de aangepaste bedrijfsprocesstroom wordt bijgewerkt.

   ![Schermafbeelding van het aanpassen van een projectentiteit](media/FAQ-Customize-BPF-6-720.png)

5. Wijzig het diagram **Project per fase** om uw nieuwe aangepaste veld voor fasen te gebruiken.

   ![Schermafbeelding van het gebruik van het diagram Project per fase](media/FAQ-Customize-BPF-7-720.png)

6. Wijzig de weergaven voor de projectentiteit om uw nieuwe aangepaste veld voor fasen op te nemen.

   ![Schermafbeelding van het wijzigen van weergaven in de projectentiteit](media/FAQ-Customize-BPF-8-720.png)

