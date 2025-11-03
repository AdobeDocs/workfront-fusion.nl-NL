---
title: E-mailmodules
description: In een Adobe Workfront Fusion-scenario kunt u uw e-mailaccount verbinden met meerdere toepassingen en services van derden. Hierdoor kunt u e-mails downloaden via IMAP, e-mails verzenden via SMTP, nieuwe concepten maken, e-mails verplaatsen en kopiëren van de ene map naar de andere, e-mails markeren als gelezen of ongelezen en e-mails verwijderen.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '2054'
ht-degree: 0%

---

# E-mailmodules

In een Adobe Workfront Fusion-scenario kunt u uw e-mailaccount verbinden met meerdere toepassingen en services van derden. Hierdoor kunt u e-mails downloaden via IMAP, e-mails verzenden via SMTP, nieuwe concepten maken, e-mails verplaatsen en kopiëren van de ene map naar de andere, e-mails markeren als gelezen of ongelezen en e-mails verwijderen.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Elk Adobe Workfront Workflow-pakket en elk Adobe Workfront Automation and Integration-pakket</p><p>Workfront Ultimate</p><p>Workfront Prime en Select packages, met extra aanschaf van Workfront Fusion.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licenties</td> 
   <td> <p>Standard</p><p>Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie</td> 
   <td>
   <p>Exploitatie gebaseerd: geen Workfront Fusion-licentievereisten</p>
   <p>Connectorgebaseerde (verouderde): Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Sluit uw e-mail aan op Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Verbinding maken met Google](#connect-to-google)
* [Verbinding maken met andere e-mailservices (IMAP)](#connect-to-other-email-services-smap)

### Verbinden met [!DNL Google]

Met deze optie kunt u scenario&#39;s maken met e-mailmodules waarvoor een verbinding met uw [!DNL Google] -account is vereist. Dit is een account met beperkt bereik.

U kunt rechtstreeks vanuit een e-mailmodule een verbinding maken met uw [!DNL Google] -account.

1. Klik in een willekeurige e-mailmodule op **[!UICONTROL Add]** naast het veld [!UICONTROL Connection] .
1. Selecteer **[!DNL Google]** als verbindingstype.
1. Voer een naam in voor de verbinding.
1. (Optioneel) Voer uw [!UICONTROL [!DNL Google] Client ID] en [!UICONTROL Client Secret] in.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

### Verbinding maken met andere e-mailservices (IMAP)

De verbinding IMAP staat u toe om tot uw brievenbus ver toegang te hebben en berichten in uw brievenbus te lezen of te manipuleren. De verbinding IMAP wordt gebruikt door de meeste modules E-mail.

1. Klik in een willekeurige e-mailmodule op **[!UICONTROL Add]** naast het veld [!UICONTROL Connection] .
1. Selecteer **[!UICONTROL Others (SMTP)]** als verbindingstype.
1. Voer een **[!UICONTROL Name]** in voor de verbinding.
1. Selecteer de **[!UICONTROL Email provider]** in de lijst. Selecteer Overige als uw e-mailprovider niet in de lijst voorkomt.
1. Voer **[!UICONTROL User name]** en uw **[!UICONTROL Password]** in voor het e-mailaccount.
1. (Voorwaardelijk) Als uw provider zich niet in de lijst bevindt, voert u uw **[!UICONTROL SMTP server]** en **[!UICONTROL Port]** in en geeft u op of u **[!UICONTROL Use a secure connection (TLS)]** wilt gebruiken. Om deze informatie te vinden, controleer de [!UICONTROL Help] sectie voor uw brievenbus. Neem contact op met uw e-mailprovider als deze gegevens niet beschikbaar zijn.
1. Om een zelf-ondertekend certificaat te gebruiken, laat **toe verwerp onbevoegde certificaten** optie en upload uw zelf-ondertekend certificaat. Voor instructies, zie [ een zelf-ondertekend certificaat ](#upload-a-self-signed-certificate) uploaden
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

#### Een zelfondertekend certificaat uploaden

Een zelfondertekend certificaat toevoegen:

1. Klik **Extraheren**.
1. Selecteer het type bestand dat u extraheert.
1. Selecteer het bestand dat het certificaat of certificaat bevat.
1. Voer het wachtwoord voor het bestand in.
1. Klik **sparen** om het dossier te halen en aan de moduleopstelling terug te keren.

## [!UICONTROL Email] modules en hun velden

Wanneer u [!UICONTROL Email] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Afhankelijk van factoren zoals uw toegangsniveau in de app of service, kunnen er naast deze velden mogelijk extra velden worden weergegeven. Een bolde titel in een module wijst op een vereist gebied.

Sommige e-mailvelden bevatten mogelijk al gegevens omdat u deze in een andere module hebt gebruikt in het scenario. Raadpleeg de documentatie bij de e-mail Help als u hierover informatie nodig hebt.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

>[!NOTE]
>
>De unieke e-mailidentiteitskaart die als &quot;[!UICONTROL Email ID (UID)] wordt bekend is het herkenningsteken van e-mail. De e-mailid is specifiek voor elk van de mappen van de e-mail.

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Iteratoren](#iterators)

### Triggers

#### [!UICONTROL Watch Emails]

Deze triggermodule start een scenario wanneer een nieuwe e-mail wordt ontvangen voor verwerking volgens opgegeven criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map met de e-mails die u wilt controleren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Selecteer de criteria aan de hand waarvan je e-mailberichten wilt bekijken:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Voer het e-mailadres in van de afzender wiens e-mails u wilt volgen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Voer het onderwerp in van het e-mailbericht dat u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Voer trefwoorden in om alleen die e-mails met de trefwoorden te bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Schakel deze optie in om de ongelezen e-mail te markeren zoals deze wordt gelezen nadat de details zijn opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Voer het maximale aantal e-mailberichten in dat Workfront Fusion tijdens één cyclus van uitvoering van het scenario moet retourneren of wijs het maximumaantal e-mails toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Send an Email]](#send-an-email)

#### [!UICONTROL Copy an Email]

Deze actiemodule kopieert een e-mail of een concept naar een geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Selecteer de map waaruit u de e-mail wilt kopiëren. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecteer de map waarnaar u de e-mail wilt kopiëren. Voorbeeld: werken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u naar de doelmap wilt kopiëren.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] of [!UICONTROL Search Email] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

Deze actiemodule maakt een nieuw concept en voegt dit toe aan een geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map waarin u het concept-e-mailbericht wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Voer het e-mailadres in of wijs het toe waarnaar u de e-mail wilt verzenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Voer de onderwerpregel van de e-mail in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Voer de e-mailinhoud in of wijs deze toe in HTML-indeling met HTML-tags of in de normale tekst.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Voor elke gehechtheid wilt u toevoegen, <b> toevoegen punt </b> en ga het volgende in:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Voer de bestandsnaam in, inclusief de extensie. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Voer het pad in naar de map waarnaar u de bijlage wilt uploaden.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Voer de inhoud-id in om de bijlage (afbeelding) in de inhoud in te voegen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Voor elk e-mailadres waarnaar u een exemplaar van deze e-mail wilt verzenden klikt <b> punt </b> toevoegen en gaat het e-mailadres in. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Voor elk e-mailadres waarnaar u een exemplaar van deze e-mail wilt verzenden zonder het hebben van het e-mailadres in e-mail verschijnen, klik <b> toevoegen punt </b> en ga het e-mailadres in.</p> </td> 
  </tr> 
  <!--<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Enter or map the email address (and name, if needed) that appears in the [!UICONTROL From] field in the email. </p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code>.</p> <p>Note:  Normally, Workfront Fusion uses the email address that you entered when creating the connection as the sender address. If you enter any other email address, an error may occur when sending a message because your account may not have permission to send emails from a different address than your own. E.g. <code>test@mail.com</code> or "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Enter or map the email address that appears in the [!UICONTROL Sender] field in the email.</p> <p>Tip:  If you are unsure whether to use this field or the From field, we recommend choosing the From field.</p> <p>Important: Use the correct syntax: <code>name@email.com</code> or <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> If you want replies to this email sent to a different address than the "[!UICONTROL from]" address, enter the email address where you want replies to this email sent.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> If you are replying to a specific email, enter or map the ID of the email you are replying to.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Enter the message IDs of all the replies in the thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Select the priority of the email:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Add the headers:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Add the key. For example, Sender, Date, To, and so on.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Enter the value for the key.</p> </li> 
    </ul> </td> 
  </tr> -->
 </tbody> 
</table>

#### [!UICONTROL Delete an Email]

Deze actiemodule verwijdert een e-mail of een concept uit de geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map met het e-mailbericht dat u wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u wilt verwijderen.</p> <p>U kunt de UID van de e-mail ophalen via de module E-mail &gt; E-mail controleren of de module [!UICONTROL Search Email] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Schakel deze optie in om alle berichten die als [!UICONTROL Deleted] zijn gemarkeerd, permanent te verwijderen in de momenteel geopende postbus.</p> <p>Opmerking: in [!DNL Gmail] wordt dit gedrag aangestuurd door de instelling in de sectie [!UICONTROL Settings] &gt; [!UICONTROL Forwarding POP/IMAP in IMAP access] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

Deze module retourneert e-mailberichten die voldoen aan de opgegeven criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] </td> 
   <td> <p>Selecteer de map met de e-mails die u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched] </td> 
   <td> <p>Schakel deze optie in als u de ongelezen e-mail wilt markeren zoals deze is gelezen nadat u de details hebt opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Criteria]</p> </td> 
   <td> <p>Selecteer de criteria voor de e-mails die u wilt ophalen:</p> 
    <ul> 
     <li>[!UICONTROL All Emails]</li> 
     <li>[!UICONTROL Only Read Emails]</li> 
     <li>[!UICONTROL Only Unread Emails]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sender Email Address] </td> 
   <td> <p>Voer het e-mailadres in of wijs het e-mailadres toe van de afzender van wie u de e-mails wilt ophalen.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email]</td> 
   <td> <p> Voer het e-mailadres in of wijs het e-mailadres toe van de ontvanger van wie u de e-mails wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL From date] </td> 
   <td> <p>Voer de datum in of wijs de datum toe waarop de e-mails die op of na de opgegeven datum zijn verwerkt, moeten worden opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Before date]</td> 
   <td> <p> Voer de datum in of wijs de datum toe waarop de e-mails die op of voor de opgegeven datum zijn verwerkt, moeten worden opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Voer het onderwerp in van de e-mail die u wilt ophalen of wijs het onderwerp ervan toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Voer trefwoorden in of wijs deze toe om alleen die e-mails met die trefwoorden op te halen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Voer de e-mailadres (UID) in van het e-mailbericht waarvan u de gegevens wilt ophalen.</p> <p>U kunt de UID van de e-mail krijgen door de module van Workfront Fusion [!UICONTROL  Watch Email] of [!UICONTROL Search Email] te gebruiken module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Het maximumaantal e-mailberichten dat Workfront Fusion mag retourneren tijdens de uitvoeringscyclus van één scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Selecteer deze optie als u de module wilt blijven uitvoeren, zelfs als er geen resultaten worden geretourneerd.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

Deze actiemodule markeert een e-mail of een concept in een geselecteerde map als gelezen door de markering [!UICONTROL Read] in te stellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map met het e-mailbericht dat u als gelezen wilt markeren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u als gelezen wilt markeren.</p> <p>U kunt de UID van de e-mail ophalen via de module E-mail &gt; E-mail controleren of de module [!UICONTROL Search Email] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Unread]

Hiermee markeert u een e-mail of concept in een geselecteerde map als ongelezen door de markering Ongelezen in te stellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map met het e-mailbericht dat u als ongelezen wilt markeren. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u als ongelezen wilt markeren.</p> <p>U kunt de UID van de e-mail ophalen via de module E-mail &gt; E-mail controleren of de module [!UICONTROL Search Email] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Move an Email]

Hiermee verplaatst u een gekozen e-mail of concept naar een geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie [!UICONTROL Workfront Fusion] Uw e-mailadres verbinden met <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion]</a> .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Selecteer de map met het e-mailbericht dat u wilt verplaatsen. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecteer de map waaraan u de e-mail wilt toevoegen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u naar de doelmap wilt verplaatsen.</p> <p>U kunt de UID van de e-mail ophalen via de module E-mail &gt; E-mail controleren of de module [!UICONTROL Search Email] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Send an Email]

Hiermee verzendt u een nieuwe e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>Nadat het e-mailbericht is verzonden, wordt het opgeslagen in uw postvak. Schakel deze optie in als u e-mailberichten die met Workfront Fusion zijn verzonden, wilt opslaan in de map <i>[!UICONTROL Sent mail]</i> of in een andere map in uw postvak. Bij sommige e-mailservices, zoals [!DNL Gmail] , worden verzonden berichten automatisch opgeslagen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL To] </td> 
   <td> <p>Voeg de e-mailadressen toe waarnaar u de e-mail wilt verzenden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Voer de onderwerpregel van de e-mail in of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Selecteer het type [!UICONTROL content] voor de e-mail:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plaintext]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Typ of wijs de e-mailinhoud in HTML-indeling toe met HTML-tags of in de normale tekst, afhankelijk van wat u hebt gekozen in het veld [!UICONTROL Content Type] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Voor elke gehechtheid wilt u toevoegen, <b> toevoegen punt </b> en ga het volgende in:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Voer de bestandsnaam in, inclusief de extensie. </p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Voer het pad in naar de map waarnaar u de bijlage wilt uploaden.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Voer de inhoud-id in om de bijlage (afbeelding) in de inhoud in te voegen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Voor elk e-mailadres waarnaar u een exemplaar van deze e-mail wilt verzenden klikt <b> punt </b> toevoegen en gaat het e-mailadres in. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Voor elk e-mailadres waarnaar u een exemplaar van deze e-mail wilt verzenden zonder het hebben van het e-mailadres in e-mail verschijnen, klik <b> toevoegen punt </b> en ga het e-mailadres in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Typ of wijs het e-mailadres toe dat in het veld [!UICONTROL Sender] in de e-mail wordt weergegeven.</p> <p>Tip: als u niet zeker weet of u dit veld of het veld Van wilt gebruiken, raden we u aan het veld Van te kiezen.</p> <p>Belangrijk: gebruik de juiste syntaxis: <code>name@email.com</code> of <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Als u op deze e-mail antwoorden wilt verzenden naar een ander adres dan het adres 'van', voer dan het e-mailadres in waarnaar u op deze e-mail wilt antwoorden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Als u een specifieke e-mail beantwoordt, voert u de id in van het e-mailbericht waarop u reageert of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Voer de bericht-id's in van alle reacties in de thread.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Selecteer de prioriteit van de e-mail:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Voeg de kopteksten toe:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Voeg de toets toe. Bijvoorbeeld [!UICONTROL Sender] , [!UICONTROL Date] , [!UICONTROL To] , enzovoort.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Voer de waarde voor de toets in.</p> </li> 
    </ul> </td> 
  </tr> 
<tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Voer het e-mailadres (en de naam, indien nodig) dat in het veld [!UICONTROL From] in de e-mail wordt weergegeven in of wijs dit toe. </p> <p>Belangrijk: gebruik de juiste syntaxis: <code>name@email.com</code> of <code>"Name" name@email.com</code> .</p> <p>Opmerking: Workfront Fusion gebruikt doorgaans het e-mailadres dat u hebt ingevoerd bij het maken van de verbinding als het verzendadres. Als u een ander e-mailadres opgeeft, kan er een fout optreden bij het verzenden van een bericht omdat uw account geen toestemming heeft om e-mails van een ander adres te verzenden dan uw eigen adres. Bijvoorbeeld <code>test@mail.com</code> of "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Iteratoren

#### [!UICONTROL Iterate Attachments]

De rentetarieven ontvingen gehechtheid één voor één.

In de module E-mailiterator kunt u e-mailbijlagen afzonderlijk beheren. U kunt bijvoorbeeld instellen dat u e-mailberichten wilt bekijken om de e-mails met bijlagen te doorlopen en waarschuwingen te ontvangen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source module]</td> 
   <td> <p>Selecteer de module die het e-mailbericht weergeeft met de bijlagen die u wilt doorlopen.</p> </td> 
  </tr> 
 </tbody> 
</table>

Voor meer informatie over iterators, zie {de module van de Teller 0} [.](/help/workfront-fusion/references/modules/iterator-module.md)
