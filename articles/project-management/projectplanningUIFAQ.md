---
title: Problemen oplossen met het werken in het taakraster
description: Dit onderwerp biedt informatie over het oplossen van problemen, die nodig is bij het werken in het taakraster.
author: ruhercul
ms.date: 08/02/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 07e7bd42db48842edee17fdfdd22fdcd8207644c1751f453ec29c3194aac625e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989095"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problemen oplossen met het werken in het taakraster 

_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, vereenvoudigde implementatie - van deal tot pro-formafacturering_

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die u kunt tegenkomen tijdens het werken met Cost Management.

## <a name="enable-cookies"></a>Cookies inschakelen

Project Operations vereist dat cookies van derden worden ingeschakeld om de structuur voor werkspecificatie weer te geven. Wanneer cookies van derden niet zijn ingeschakeld, ziet u in plaats van taken een lege pagina wanneer u het tabblad **Taken** selecteert op de pagina **Project**.

![Leeg tabblad wanneer cookies van derden niet zijn ingeschakeld.](media/blankschedule.png)


### <a name="workaround"></a>Oplossing
Voor Microsoft Edge of Google Chrome-browsers, beschrijven de volgende procedures hoe u uw browserinstellingen kunt bijwerken om cookies van derden in te schakelen.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Open de Microsoft Edge-browser.
2. Selecteer in de rechterbovenhoek het **beletselteken** (...) en selecteer vervolgens **Instellingen**.
3. Selecteer onder **Cookies en sitemachtigingen**, **Cookies en sitegegevens**.
4. Schakel **Cookies van derden blokkeren** uit.

#### <a name="google-chrome"></a>Google Chrome

1. Open uw Chrome-browser.
2. Selecteer in de rechterbovenhoek de drie verticale puntjes en selecteer vervolgens **Instellingen**.
3. Selecteer onder **Privacy en beveiliging**, **Cookies en overige sitegegevens**.
4. Selecteer **Alle cookies toestaan**.

> [!IMPORTANT]
> Als u cookies van derden blokkeert, worden alle cookies en sitegegevens van andere sites geblokkeerd, zelfs als de site is toegestaan op uw uitzonderingenlijst.

## <a name="pex-endpoint"></a>PEX-eindpunt

Project Operations vereist dat een projectparameter verwijst naar het PEX-eindpunt. Dit eindpunt is vereist om te communiceren met de service die wordt gebruikt om de structuur voor werkspecificatie weer te geven. Als de parameter niet is ingeschakeld, ontvangt u de fout 'De projectparameter is niet geldig'. 

### <a name="workaround"></a>Oplossing

1. Voeg het veld **PEX-eindpunt** toe aan de pagina **Projectparameters**.
2. Identificeer het producttype dat u gebruikt. Deze waarde wordt gebruikt wanneer de PEX-eindpunt is ingesteld. Bij het ophalen is het producttype al gedefinieerd in de PEX-eindpunt. Bewaar die waarde. 
   
    ![Het veld PEX-eindpunt op de projectparameter.](media/pex-endpoint.png)

3. Werk het veld bij met de volgende waarde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`.

   
   | Producttype                         | Typeparameter |
   |--------------------------------------|----------------|
   | Project for the Web in standaardorganisatie   | type=0         |
   | Project for the Web in CDS-organisatie | type=1         |
   | Project Operations                   | type=2         |
   
4. Verwijder het veld uit de pagina **Projectparameters**.

## <a name="privileges-for-project-for-the-web"></a>Bevoegdheden voor Project for the Web

Project Operations is afhankelijk van een externe planningsservice. De service vereist dat een gebruiker verschillende rollen heeft toegewezen gekregen om te lezen en te schrijven naar entiteiten die verband houden met de structuur voor werkspecificatie. Deze entiteiten omvatten projecttaken, resourcetoewijzingen en taakafhankelijkheden. Als een gebruiker de structuur voor werkspecificatie niet kan weergeven wanneer hij naar het tabblad **Taken** gaat, is dit waarschijnlijk omdat Project voor Project Operations niet is ingeschakeld. Een gebruiker kan ofwel een beveiligingsrol-fout ontvangen of een fout gerelateerd aan een weigering van toegang.


## <a name="workaround"></a>Oplossing

1. Ga naar **Instellingen > Beveiliging > Gebruikers > Toepassingsgebruikers**.  

   ![Toepassingslezer.](media/applicationuser.jpg)
   
2. Dubbelklik op de toepassingsgebruikersrecord om het volgende te controleren:

 - De gebruiker heeft toegang tot het project. Deze verificatie wordt meestal gedaan door ervoor te zorgen dat de gebruiker de beveiligingsrol **Projectleider** heeft.
 - De gebruiker van de Microsoft Project-toepassing bestaat en is correct geconfigureerd.
 
3. Als deze gebruiker niet bestaat, kunt uw een nieuwe gebruikersrecord maken. Selecteer **Nieuwe gebruikers**. Wijzig het inschrijfformulier in **Toepassingsgebruiker** en voeg vervolgens de **Toepassings-id** toe.

   ![Gegevens van toepassingsgebruiker.](media/applicationuserdetails.jpg)

4. Controleer of de gebruiker de juiste licentie heeft gekregen en of de service is ingeschakeld in de gegevens van de serviceplannen van de licentie.
5. Controleer of de gebruiker project.microsoft.com kan openen.
6. Controleer via de projectparameters of het systeem naar het juiste projecteindpunt verwijst.
7. Controleer of de gebruiker van de projecttoepassing is gemaakt.
8. Pas de volgende beveiligingsrollen toe op de gebruiker:

  - Dataverse-gebruiker
  - Project Operations-systeem
  - Projectsysteem

## <a name="error-when-updating-the-work-breakdown-structure"></a>Fout bij het bijwerken van de structuur voor werkspecificatie

Wanneer een of meer updates worden aangebracht in de structuur voor werkspecificatie, mislukken de wijzigingen uiteindelijk en worden deze niet opgeslagen. Er treedt een fout op in het planningsraster dat aangeeft 'Recente wijzigingen die u hebt aangebracht, konden niet worden opgeslagen'.

### <a name="workaround"></a>Oplossing

1. Controleer of de gebruiker de juiste licentie heeft gekregen en of de service is ingeschakeld in de gegevens van de serviceplannen van de licentie.
2. Controleer of de gebruiker project.microsoft.com kan openen.
3. Controleer of het systeem naar het juiste projecteindpunt verwijst.
4. Controleer of de gebruiker van de projecttoepassing is gemaakt.
5. Pas de volgende beveiligingsrollen toe op de gebruiker:
  
  - Dataverse-gebruiker of standaardgebruiker
  - Project Operations-systeem
  - Projectsysteem
  - Twee keer wegschrijven in Project Operations (deze rol is vereist als u het scenario op basis van resource/ niet-voorradige artikelen van project Operations implementeert.)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
