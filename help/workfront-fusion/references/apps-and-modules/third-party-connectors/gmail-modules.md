---
title: Gmail-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Gmail gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: 62269eca-c3cf-42fe-a866-fb66d2363b8d
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1580'
ht-degree: 0%

---

# [!DNL Gmail] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Gmail] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
   <p>of</p>
   <p>Verouderd: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!DNL Gmail] -modules wilt gebruiken, moet u een [!DNL Gmail] -account hebben.

## Verbinden [!DNL Gmail] met Workfront Fusion {#connect-gmail-to-workfront-fusion}

* [Verbind  [!DNL Gmail]  met de Fusie van Workfront gebruikend  [!DNL Google Workspace]](#connect-gmail-to-workfront-fusion-usinggoogle-workspace)
* [Verbind  [!DNL Gmail]  met de Fusie van Workfront gebruikend  [!DNL gmail.com]  of  [!DNL googlemail].com](#connect-gmail-to-workfront-fusion-using-gmailcom-or-googlemailcom)

### Verbinding maken [!DNL Gmail] met Workfront Fusion via [!DNL  Google Workspace]

Voor instructies over het verbinden van uw [!DNL Google Workspace] rekening met [!UICONTROL Workfront Fusion], zie [ een verbinding tot stand brengen - Basisinstructies ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md).

### Verbind [!DNL Gmail] met Workfront Fusion gebruikend [!DNL gmail.com] of [!DNL googlemail].com

Als u [!DNL @gmail.com] of [!DNL @googlemail.com] gebruiker bent moet u een cliënt OAuth op [ creëren  [!DNL Google Cloud Platform] ](https://console.developers.google.com/projectselector2/apis/dashboard?supportedpurview=project) om a [!UICONTROL Client ID] en [!UICONTROL Client Secret] te verkrijgen.

Voor geleidelijke instructies op hoe te om de cliënt OAuth tot stand te brengen en a [!UICONTROL Client ID] en [!UICONTROL Client Secret] te verkrijgen, zie [ de Fusie van Adobe Workfront aan de Diensten van Google verbinden gebruikend een douaneOAuth cliënt ](/help/workfront-fusion/create-scenarios/connect-to-apps/connect-fusion-to-google-using-oauth.md).

## [!DNL Gmail] modules en hun velden

Wanneer u [!DNL Gmail] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Gmail] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Iteratoren](#iterators)

### Triggers

#### [!UICONTROL Watch emails]

Deze triggermodule voert een scenario uit wanneer een nieuwe e-mail wordt ontvangen om te worden verwerkt.

De module retourneert alle standaardvelden die zijn gekoppeld aan de record of records, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de e-mailmap die u wilt controleren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Filter type] </td> 
   <td> <p>Selecteer het filtertype dat u wilt gebruiken om e-mailberichten te bekijken</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Simple filter]</strong> </p> <p>Vul de velden [!UICONTROL Criteria] , [!UICONTROL Sender Email Address] , [!UICONTROL Subject] en [!UICONTROL Search Phrase] in</p> </li> 
     <li> <p> <strong>[!UICONTROL Gmail filter]</strong> </p> <p>Voer in het veld [!UICONTROL Query] de query in die u wilt gebruiken om e-mailberichten te filteren.</p> <p>Voor meer informatie over [!DNL Gmail] filters, zie <a href="https://support.google.com/mail/answer/7190"> onderzoeken </a> in de [!DNL Gmail] documentatie verfijnen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Criteria]</td> 
   <td>Geef op of u e-mails [!UICONTROL all email] , [!UICONTROL only read emails] of [!UICONTROL only unread] wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Sender email address]</td> 
   <td> <p> Voer een e-mailadres in om alleen e-mails te volgen die van dat adres zijn verzonden.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject]</td> 
   <td>Voer een tekstreeks in om alleen e-mails te bekijken waarin die tekstreeks in het onderwerp voorkomt.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Search phrase]</td> 
   <td>Voer een tekstreeks in om alleen e-mailberichten te bekijken die die tekstreeks ergens in de e-mail hebben.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Mark email message(s) as read when fetched]</td> 
   <td> <p> Schakel deze optie in om opgehaalde e-mails te markeren als gelezen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Maximum number of results]</td> 
   <td> <p> Stel het maximale aantal resultaten in waarmee Workfront Fusion gedurende één cyclus werkt.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

<!--* [Add labels](#add-labels)-->
* [[!UICONTROL Copy an email]](#copy-an-email)
* [[!UICONTROL Create a draft]](#create-a-draft)
* [[!UICONTROL Delete an email]](#delete-an-email)
  <!--* [Delete labels](#delete-labels)-->
* [[!UICONTROL Mark an email as read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an email as unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an email]](#move-an-email)
* [[!UICONTROL Modify email labels]](#modify-email-labels)
* [[!UICONTROL Send an email]](#send-an-email)
  <!--* [Set labels](#set-labels)-->

<!--#### Add labels-->

#### [!UICONTROL Copy an email]

Deze actiemodule kopieert een e-mail- of e-mailconcept naar een map die u opgeeft.

U geeft de map, de doelmap en de id van de e-mail op.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de [!DNL Gmail] -bronmap die het e-mailbericht bevat dat u wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p>Selecteer de doelmap van [!DNL Gmail] waarnaar u de e-mail wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p>Voer de e-mailid in of wijs deze toe van het e-mailbericht dat u wilt kopiëren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a draft]

In deze actiemodule wordt een nieuw e-mailconcept gemaakt en toegevoegd aan een map die u opgeeft.

U geeft de map op waarin u een concept wilt maken.

De module retourneert de id van het e-mailconcept en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map [!DNL Gmail] waarin u een concept wilt maken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Voer het onderwerp van de e-mail in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Voer de e-mailinhoud (hoofdtekst van bericht) in of wijs deze toe. HTML-tags zijn toegestaan.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Klik op <strong>[!UICONTROL Add]</strong> om een bijlage toe te voegen. U kunt een bestand uit de vorige modules toewijzen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger van de kopie in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger van de blinde kopie in of wijs dit toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete an email]

Met deze actiemodule verwijdert u een e-mail- of e-mailconcept uit een map die u opgeeft.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL [!DNL Gmail] Bericht-ID]</p> </td> 
   <td> <p>Voer de e-mailid in of wijs deze toe van het e-mailbericht dat u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Permanently] </td> 
   <td> <p>Schakel deze optie in als u wilt dat de module de e-mail permanent kan verwijderen in plaats van deze naar de prullenbak te verplaatsen.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Delete labels-->



#### [!UICONTROL Mark an email as read]

Deze actiemodule markeert een e-mail als gelezen.

U geeft de id van het e-mailbericht en de bijbehorende map op.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map [!DNL Gmail] die de e-mail bevat.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Voer de e-mailid in of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an email as unread]

Deze actiemodule markeert een e-mail- of e-mailconcept als ongelezen.

U geeft de id van het e-mailbericht en de bijbehorende map op.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map [!DNL Gmail] die de e-mail bevat.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)] </td> 
   <td> <p>Voer de e-mailid in of wijs deze toe aan het e-mailadres dat u als ongelezen wilt markeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Modify email labels]

Deze actiemodule wijzigt het label van een e-mailbericht dat u opgeeft.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL [!DNL Gmail] Bericht-ID]</td> 
   <td> <p> Voer de e-mailid in of wijs deze toe van het e-mailbericht dat u wilt verwijderen.</p> </td> 
  </tr> 
  <tr> 
   <td> <p>[!UICONTROL Labels to add]</p> </td> 
   <td> <p>Selecteer of wijs het label toe u aan het geselecteerde e-mailbericht wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Labels to remove]</td> 
   <td> <p> Selecteer of wijs het label toe u uit het geselecteerde e-mailbericht wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>[!UICONTROL Label to add] en [!UICONTROL Label to remove] worden alleen door de gebruiker gemaakte labels geladen.

#### [!UICONTROL Move an email]

Met deze handelingsmodule wordt een e-mail- of e-mailconcept verplaatst naar een map die u opgeeft.

U geeft de map, de doelmap en de id van de e-mail op.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Zie [!DNL Gmail] Verbinding maken <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> met [!DNL Gmail] in dit artikel voor instructies voor het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de [!DNL Gmail] -bronmap met het e-mailbericht dat u wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Destination folder]</td> 
   <td> <p> Selecteer de doelmap van [!DNL Gmail] waarnaar u de e-mail wilt verplaatsen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Voer de e-mailid in of wijs deze toe aan het e-mailbericht dat u wilt verplaatsen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send an email]

Deze actiemodule verzendt een nieuwe e-mail.

U geeft de ontvanger van de e-mail op.

De module retourneert de id van de e-mail en alle bijbehorende velden, samen met eventuele aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Connection] </td> 
   <td> <p>Voor instructies bij het aansluiten van uw [!DNL Gmail] rekening aan Workfront Fusion, zie <a href="#connect-gmail-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Gmail] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL From]</td> 
   <td> <p>Voer een e-mailadres van een afzender in of wijs dit toe.</p> <p>Opmerking: als u een onjuist e-mailadres opgeeft, kan er een fout optreden bij het verzenden van een bericht omdat uw account geen toestemming heeft om e-mails te verzenden van een ander adres dan uw eigen adres.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL To] </td> 
   <td> <p>Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Subject] </td> 
   <td> <p>Voer het onderwerp van de e-mail in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Content] </td> 
   <td> <p>Voer de e-mailinhoud (hoofdtekst van bericht) in of wijs deze toe. HTML-tags zijn toegestaan.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Attachments] </td> 
   <td> <p>Klik op <strong>[!UICONTROL Add]</strong> om een bijlage toe te voegen. U kunt een bestand uit de vorige modules toewijzen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Copy recipients]</td> 
   <td> <p> Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger van de kopie in of wijs dit toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Blind copy recipients]</td> 
   <td> <p> Klik op <strong>[!UICONTROL Add]</strong> en voer het e-mailadres voor elke ontvanger van de blinde kopie in of wijs dit toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

<!--#### Set labels-->

### Iteratoren

#### [!UICONTROL Iterate attachments]

U kunt e-mailbijlagen doorlopen. Elke bijlage is een afzonderlijke bundel in de output van de module. Voor meer informatie, zie {de module van de Teller 0} [.](/help/workfront-fusion/references/modules/iterator-module.md)

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module] </td> 
   <td> <p>Selecteer de module waarvan u bijlagen wilt doorlopen. </p> </td> 
  </tr> 
 </tbody> 
</table>
