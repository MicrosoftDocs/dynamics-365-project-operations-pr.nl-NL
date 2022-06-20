---
title: Problemen oplossen met het werken in het taakraster
description: Dit artikel bevat informatie over het oplossen van problemen bij het werken in het taakraster.
author: ruhercul
ms.date: 04/05/2022
ms.topic: article
ms.product: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e6ab4f34fe3f6732f7bef252f298671e07a3c3ca
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911038"
---
# <a name="troubleshoot-working-in-the-task-grid"></a>Problemen oplossen met het werken in het taakraster 


_**Van toepassing op:** Project Operations voor scenario's op basis van resources/niet-voorradige artikelen, Lite-implementatie - van deal tot pro-formafacturering, Project for the web_

Het taakraster dat wordt gebruikt door Dynamics 365 Project Operations is een gehost iFrame binnen Microsoft Dataverse. Als gevolg van dit gebruik moet aan specifieke vereisten worden voldaan om ervoor te zorgen dat verificatie en autorisatie correct werken. In dit artikel worden de veelvoorkomende problemen beschreven die van invloed kunnen zijn op de mogelijkheid om het raster weer te geven of taken te beheren in de structuur voor werkspecificatie (WBS).

Tot de algemene problemen behoren:

- Het tabblad **Taak** in het taakraster is leeg.
- Bij het openen van het project, wordt het project niet geladen en blijft de gebruikersinterface (UI) hangen bij de draaischijf.
- Beheer van bevoegdheden voor **Project for the Web**.
- Wijzigingen worden niet opgeslagen wanneer u een taak maakt, bijwerkt of verwijdert.

## <a name="issue-the-task-tab-is-empty"></a>Probleem: het tabblad Taak is leeg

### <a name="mitigation-1-enable-cookies"></a>Oplossing 1: schakel cookies in

Project Operations vereist dat cookies van derden zijn ingeschakeld om de structuur voor werkspecificatie weer te geven. Wanneer cookies van derden niet zijn ingeschakeld, ziet u in plaats van taken een lege pagina wanneer u het tabblad **Taken** selecteert op de pagina **Project**.

Voor Microsoft Edge of Google Chrome-browsers, beschrijven de volgende procedures hoe u uw browserinstellingen kunt bijwerken om cookies van derden in te schakelen.

#### <a name="microsoft-edge"></a>Microsoft Edge

1. Open de Microsoft Edge-browser.
2. Selecteer in de rechterbovenhoek het **beletselteken** (...) en selecteer vervolgens **Instellingen**.
3. Selecteer onder **Cookies en sitemachtigingen**, **Cookies en sitegegevens**.
4. Schakel **Cookies van derden blokkeren** uit.
5. Vernieuw de browser. 

#### <a name="google-chrome"></a>Google Chrome

1. Open uw Chrome-browser.
2. Selecteer in de rechterbovenhoek de drie verticale puntjes en selecteer vervolgens **Instellingen**.
3. Selecteer onder **Privacy en beveiliging**, **Cookies en overige sitegegevens**.
4. Selecteer **Alle cookies toestaan**.
5. Vernieuw de browser. 

> [!NOTE]
> Als u cookies van derden blokkeert, worden alle cookies en sitegegevens van andere sites geblokkeerd, zelfs als de site is toegestaan op uw uitzonderingenlijst.

### <a name="mitigation-2-validate-the-pex-endpoint-has-been-correctly-configured"></a>Oplossing 2: valideer of het PEX eindpunt correct is geconfigureerd

Project Operations vereist dat een projectparameter verwijst naar het PEX-eindpunt. Dit eindpunt is vereist om te communiceren met de service die wordt gebruikt om de structuur voor werkspecificatie weer te geven. Als de parameter niet is ingeschakeld, ontvangt u de fout 'De projectparameter is niet geldig'. Voer de volgende stappen uit om het PEX-eindpunt bij te werken.

1. Voeg het veld **PEX-eindpunt** toe aan de pagina **Projectparameters**.
2. Identificeer het producttype dat u gebruikt. Deze waarde wordt gebruikt wanneer de PEX-eindpunt is ingesteld. Bij het ophalen is het producttype al gedefinieerd in de PEX-eindpunt. Bewaar die waarde.
3. Werk het veld bij met de volgende waarde: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=<id>&type=2`. De volgende tabel bevat de typeparameter die moet worden gebruikt op basis van het producttype.

      | **Producttype**                     | **Typeparameter** |
      |--------------------------------------|--------------------|
      | Project for the Web in standaardorganisatie   | type=0             |
      | Project for the Web in CDS-organisatie | type=1             |
      | Project Operations                   | type=2             |

4. Verwijder het veld uit de pagina **Projectparameters**.

### <a name="mitigation-3-sign-in-to-projectmicrosoftcom"></a>Correctie 3: meld u aan bij project.microsoft.com.
Open een nieuw tabblad in uw Microsoft Edge-browser, ga naar project.microsoft.com en meld u aan met de gebruikersrol die u gebruikt om toegang te krijgen tot Project Operations.

## <a name="issue-the-project-doesnt-load-and-the-ui-is-stuck-on-the-spinner"></a>Probleem: het project laadt niet en de gebruikersinterface blijft hangen bij de draaischijf

Voor verificatiedoeleinden moeten pop-ups zijn ingeschakeld om het takenraster te kunnen laden. Als pop-ups niet zijn ingeschakeld, blijft het scherm hangen bij de draaischijf voor laden. De volgende afbeelding toont de URL met een geblokkeerd pop-uplabel in de adresbalk, waardoor de draaischrijf vastloopt bij een poging om de pagina te laden. 

   ![Vastgelopen draaischijf en pop-upblokkering.](media/popupsblocked.png)

### <a name="mitigation-1-enable-pop-ups"></a>Oplossing 1: schakel pop-ups in

Wanneer uw project blijft hangen bij de draaischijf, is het mogelijk dat pop-ups niet zijn ingeschakeld.

#### <a name="microsoft-edge"></a>Microsoft Edge

Er zijn twee manieren om pop-ups in te schakelen in uw Edge-browser.

1. Selecteer in uw Edge-browser de melding in de rechterbovenhoek van de browser.
2. Selecteer **Altijd pop-ups en omleidingen toestaan** in de specifieke Dataverse-omgeving.
 
     ![Venster bij geblokkeerde pop-ups.](media/enablepopups.png)

U kunt ook de volgende stappen uitvoeren.

1. Open de Microsoft Edge-browser.
2. Selecteer in de rechterbovenhoek het **beletselteken** (...) en selecteer vervolgens **Instellingen** > **Sitemachtigingen** > **Pop-ups en omleidingen**.
3. Schakel **Pop-ups en omleidingen** uit om pop-ups te blokkeren of schakel deze optie in om pop-ups op uw apparaat toe te staan.
4. Vernieuw uw browser nadat u pop-ups hebt ingeschakeld. 

#### <a name="google-chrome"></a>Google Chrome
1. Open uw Chrome-browser.
2. Navigeer naar een pagina waar pop-ups zijn geblokkeerd.
3. Selecteer **Pop-up geblokkeerd** in de adresbalk.
4. Selecteer de koppeling voor de pop-up die u wilt zien.
5. Vernieuw uw browser nadat u pop-ups hebt ingeschakeld. 

> [!NOTE]
> Als u altijd pop-ups voor de site wilt zien, selecteert u **Altijd pop-ups en omleidingen toestaan van [site]** en selecteer vervolgens **Gereed**.

## <a name="issue-3-administration-of-privileges-for-project-for-the-web"></a>Probleem 3: beheer van bevoegdheden voor Project for the Web

Project Operations is afhankelijk van een externe planningsservice. De service vereist dat een gebruiker verschillende rollen heeft toegewezen die hem in staat stellen te lezen en te schrijven naar entiteiten die verband houden met de WBS. Deze entiteiten omvatten projecttaken, resourcetoewijzingen en taakafhankelijkheden. Als een gebruiker de WBS niet kan weergeven wanneer hij naar het tabblad **Taken** navigeert, komt dat waarschijnlijk doordat **Project** niet is ingeschakeld voor **Project Operations**. Een gebruiker kan ofwel een beveiligingsrol-fout ontvangen of een fout gerelateerd aan een weigering van toegang.

### <a name="mitigation-1-validate-the-application-user-and-end-user-security-roles"></a>Oplossing 1: valideer de beveiligingsrollen toepassingsgebruiker en eindgebruiker

1. Ga naar **Instellingen** > **Beveiliging** > **Gebruikers** > **Toepassingsgebruikers**.  

   ![Toepassingslezer.](media/applicationuser.jpg)
   
2. Dubbelklik op de gebruikersrecord van de toepassing om te verifiëren:

     - De gebruiker heeft toegang tot het project. U kunt dit doen door te controleren of de gebruiker de beveiligingsrol **Projectmanager** heeft.
     - De gebruiker van de Microsoft Project-toepassing bestaat en is correct geconfigureerd.
 
3. Als deze gebruiker niet bestaat, maakt u een nieuwe gebruikersrecord. 
4. Selecteer **Nieuwe gebruikers**, wijzig het invulformulier in **Toepassingsgebruiker** en voeg vervolgens de **toepassings-id** toe.

   ![Gegevens van toepassingsgebruiker.](media/applicationuserdetails.jpg)


## <a name="issue-4-changes-arent-saved-when-you-create-update-or-delete-a-task"></a>Probleem 4: wijzigingen worden niet opgeslagen wanneer u een taak maakt, bijwerkt of verwijdert

Wanneer u een of meer updates toepast op de WBS, mislukken de wijzigingen en worden deze niet opgeslagen. Er treedt een fout op in het schemaraster met een bericht dat zegt: "Recente wijziging die u hebt aangebracht, kan niet worden opgeslagen".

### <a name="mitigation-1-validate-the-license-assignment"></a>Oplossing 1: valideer de licentietoewijzing

1. Controleer of de gebruiker de juiste licentie heeft gekregen en of de service is ingeschakeld in de gegevens van de serviceplannen van de licentie.  
2. Controleer of de gebruiker **project.microsoft.com** kan openen.
    
### <a name="mitigation-2-validation-configuration-of-the-project-application-user"></a>Oplossing 2: validatieconfiguratie van de Project-toepassingsgebruiker
1. Controleer of de Project-toepassingsgebruiker is gemaakt.
2. Pas de volgende beveiligingsrollen toe op de gebruiker:
  
  - Dataverse-gebruiker of -standaardgebruiker
  - Project Operations-systeem
  - Projectsysteem
  - Systeem voor twee keer wegschrijven in Project Operations Deze rol is vereist voor het implementatiescenario op basis van resources/niet-voorradige artikelen van Project Operations.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
