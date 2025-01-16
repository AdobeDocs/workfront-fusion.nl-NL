---
title: E-mailmodules
description: In a  [!DNL Adobe Workfront Fusion]  scenario, kunt u uw E-mailrekening met veelvoudige derdetoepassingen en de diensten verbinden. Dit staat u toe om e-mails via IMAP te downloaden, e-mails via SMTP te verzenden, nieuwe ontwerpen te creëren, e-mails van één omslag naar een andere omslag te verplaatsen en te kopiëren, e-mails als gelezen of ongelezen te merken, en e-mails te schrappen.
author: Becky
feature: Workfront Fusion
exl-id: 28a04bad-d3ef-4f3a-be93-8b04761a75e4
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '2103'
ht-degree: 0%

---

# E-mailmodules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u uw e-mailaccount verbinden met meerdere toepassingen en services van derden. Hierdoor kunt u e-mails downloaden via IMAP, e-mails verzenden via SMTP, nieuwe concepten maken, e-mails verplaatsen en kopiëren van de ene map naar de andere, e-mails markeren als gelezen of ongelezen en e-mails verwijderen.

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Sluit uw e-mail aan op Workfront Fusion {#connect-your-email-to-workfront-fusion}

* [Verbinding maken met Google](#connect-to-google)
* [Verbinding maken met andere e-mailservices (SMAP)](#connect-to-other-email-services-smap)

### Verbinden met [!DNL Google]

Met deze optie kunt u scenario&#39;s maken met e-mailmodules waarvoor een verbinding met uw [!DNL Google] -account is vereist. Dit is een account met beperkt bereik.

U kunt rechtstreeks vanuit een e-mailmodule een verbinding maken met uw [!DNL Google] -account.

1. Klik in een willekeurige e-mailmodule op **[!UICONTROL Add]** naast het veld [!UICONTROL Connection] .
1. Selecteer **[!DNL Google]** als verbindingstype.
1. Voer een naam in voor de verbinding.
1. (Optioneel) Voer uw [!UICONTROL [!DNL Google] Client ID] en [!UICONTROL Client Secret] in.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

### Verbinding maken met andere e-mailservices (SMAP)

De verbinding van SMAP staat u toe om tot uw brievenbus ver toegang te hebben en berichten in uw brievenbus te lezen of te manipuleren. De SMAP-verbinding wordt door de meeste e-mailmodules gebruikt.

1. Klik in een willekeurige e-mailmodule op **[!UICONTROL Add]** naast het veld [!UICONTROL Connection] .
1. Selecteer **[!UICONTROL Others (SMTP)]** als verbindingstype.
1. Voer een **[!UICONTROL Name]** in voor de verbinding.
1. Selecteer de **[!UICONTROL Email provider]** in de lijst. Selecteer Overige als uw e-mailprovider niet in de lijst voorkomt.
1. Voer uw **[!UICONTROL Email address]** , **[!UICONTROL Your full name]** , uw **[!UICONTROL User name]** en uw **[!UICONTROL Password]** in.
1. (Voorwaardelijk) Als uw provider zich niet in de lijst bevindt, voert u uw **[!UICONTROL SMTP server]** en **[!UICONTROL Port]** in en geeft u op of u **[!UICONTROL Use a secure connection (TLS)]** wilt gebruiken. Om deze informatie te vinden, controleer de [!UICONTROL Help] sectie voor uw brievenbus. Neem contact op met uw e-mailprovider als deze gegevens niet beschikbaar zijn.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!UICONTROL Email] modules en hun velden

Wanneer u [!UICONTROL Email] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Afhankelijk van factoren zoals uw toegangsniveau in de app of service, kunnen er naast deze velden mogelijk extra velden worden weergegeven. Een bolde titel in een module wijst op een vereist gebied.

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

Triggers wanneer een nieuw e-mailbericht wordt ontvangen voor verwerking volgens opgegeven criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td> 
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
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
   <td> <p> Voer het e-mailadres in van de ontvanger van wie u de e-mails wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subject] </td> 
   <td> <p>Voer het onderwerp in van het e-mailbericht dat u wilt bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Phrase] </td> 
   <td> <p>Voer trefwoorden in om alleen die e-mailberichten met specifieke zinsdelen te bekijken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Mark message(s) as read when fetched]</td> 
   <td> <p>Schakel deze optie in om de ongelezen e-mail te markeren zoals deze wordt gelezen nadat de details zijn opgehaald.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Het maximumaantal e-mailberichten [!DNL Workfront Fusion] moet worden geretourneerd tijdens de uitvoeringscyclus van één scenario.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Send an Email]](#send-an-email)
* [[!UICONTROL Create a Draft]](#create-a-draft)
* [[!UICONTROL Mark an Email as Read]](#mark-an-email-as-read)
* [[!UICONTROL Mark an Email as Unread]](#mark-an-email-as-unread)
* [[!UICONTROL Move an Email]](#move-an-email)
* [[!UICONTROL Copy an Email]](#copy-an-email)
* [[!UICONTROL Delete an Email]](#delete-an-email)
* [[!UICONTROL Get Emails]](#get-emails)

#### [!UICONTROL Send an Email]

Hiermee verzendt u een nieuwe e-mail.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Save Message after Sending]</td> 
   <td>Nadat het e-mailbericht is verzonden, wordt het opgeslagen in uw postvak. Schakel deze optie in als u e-mailberichten wilt opslaan die met [!DNL Workfront Fusion] naar de map <i>[!UICONTROL Sent mail]</i> of een andere map in uw postvak zijn verzonden. Bij sommige e-mailservices, zoals [!DNL Gmail] , worden verzonden berichten automatisch opgeslagen.</td> 
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
   <td> <p>Typ of wijs de e-mailinhoud in HTML-indeling toe met behulp van HTML-tags of in de normale tekst, afhankelijk van wat u hebt gekozen in het veld [!UICONTROL Content Type] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Een bijlage toevoegen:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Voer de bestandsnaam in. Bijvoorbeeld voorbeeld voorbeeld voorbeeld.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Voer het pad naar de map in waar u de bijlage wilt uploaden.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Voer de [!UICONTROL content ID] in om de bijlage (afbeelding) in de inhoud in te voegen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Voer een of meer e-mailadressen in of wijs deze toe waarnaar u een kopie van deze e-mail wilt verzenden. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Voer een of meer e-mailadressen in of wijs deze toe waarnaar u een kopie van deze e-mail wilt verzenden zonder dat het e-mailadres in de e-mail wordt weergegeven.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Voer het e-mailadres (en de naam, indien nodig) dat in het veld [!UICONTROL From] in de e-mail wordt weergegeven in of wijs dit toe. </p> <p>Belangrijk: gebruik de juiste syntaxis: <code>name@email.com</code> of <code>"Name" name@email.com</code> .</p> <p>Opmerking: doorgaans gebruikt [!DNL Workfront Fusion] het e-mailadres dat u hebt ingevoerd bij het maken van de verbinding als het verzendadres. Als u een ander e-mailadres opgeeft, kan er een fout optreden bij het verzenden van een bericht omdat uw account geen toestemming heeft om e-mails van een ander adres te verzenden dan uw eigen adres. Bijvoorbeeld <code>test@mail.com</code> of "<code>John Bush" test@email.com</code>.</p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Create a Draft]

Hiermee maakt u een nieuw concept en voegt u dit toe aan een geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
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
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Content Type]</p> </td> 
   <td> <p>Selecteer het inhoudstype voor de e-mail:</p> 
    <ul> 
     <li>HTML</li> 
     <li>[!UICONTROL Plain Text]</li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Content] </td> 
   <td> <p>Typ of wijs de e-mailinhoud in HTML-indeling toe met behulp van HTML-tags of in de normale tekst, afhankelijk van wat u hebt gekozen in het veld [!UICONTROL Content Type] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Attachments]</p> </td> 
   <td> <p>Een bijlage toevoegen:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File name]</strong> </p> <p>Voer de bestandsnaam in. Bijvoorbeeld voorbeeld voorbeeld voorbeeld.doc.</p> </li> 
     <li> <p><strong>[!UICONTROL Data]</strong> </p> <p>Voer het pad naar de map in waar u de bijlage wilt uploaden.</p> </li> 
     <li> <p><strong>[!UICONTROL Content-ID]</strong> </p> <p>Voer de inhoud-id in om de bijlage (afbeelding) in de inhoud in te voegen.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Copy Recipient] </td> 
   <td> <p>Voer een of meer e-mailadressen in of wijs deze toe waarnaar u een kopie van deze e-mail wilt verzenden. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Blind Copy Recipient]</td> 
   <td> <p> Voer een of meer e-mailadressen in of wijs deze toe waarnaar u een kopie van deze e-mail wilt verzenden zonder dat het e-mailadres in de e-mail wordt weergegeven.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL From] </td> 
   <td> <p>Voer het e-mailadres (en de naam, indien nodig) dat in het veld [!UICONTROL From] in de e-mail wordt weergegeven in of wijs dit toe. </p> <p>Belangrijk: gebruik de juiste syntaxis: <code>name@email.com</code> of <code>"Name" name@email.com</code> .</p> <p>Opmerking: doorgaans gebruikt [!DNL Workfront Fusion] het e-mailadres dat u hebt ingevoerd bij het maken van de verbinding als het verzendadres. Als u een ander e-mailadres opgeeft, kan er een fout optreden bij het verzenden van een bericht omdat uw account geen toestemming heeft om e-mails van een ander adres te verzenden dan uw eigen adres. Bijvoorbeeld <code>test@mail.com</code> of "<code>John Bush" test@email.com</code>.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Sender]</p> </td> 
   <td> <p>Typ of wijs het e-mailadres toe dat in het veld [!UICONTROL Sender] in de e-mail wordt weergegeven.</p> <p>Tip: als u niet zeker weet of u dit veld of het veld Van wilt gebruiken, raden we u aan het veld Van te kiezen.</p> <p>Belangrijk: gebruik de juiste syntaxis: <code>name@email.com</code> of <code>"Name" name@email.com</code></p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL Reply-To]</td> 
   <td> <p> Als u wilt dat antwoorden op deze e-mail naar een ander adres worden verzonden dan het adres "[!UICONTROL from]", voert u het e-mailadres in waarnaar u antwoorden op deze e-mail wilt verzenden.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL In-Reply-To]</td> 
   <td> <p> Als u een specifieke e-mail beantwoordt, voert u de id in van het e-mailbericht waarop u reageert of wijst u deze toe.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL References] </td> 
   <td> <p>Voer de bericht-id's in van alle reacties in de thread.</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Priority]</p> </td> 
   <td> <p>Selecteer de prioriteit van de e-mail:</p> 
    <ul> 
     <li>[!UICONTROL High]</li> 
     <li>[!UICONTROL Normal]</li> 
     <li>[!UICONTROL Low]</li> 
    </ul> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader"> <p>[!UICONTROL Headers]</p> </td> 
   <td> <p>Voeg de kopteksten toe:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Key]</strong> </p> <p>Voeg de toets toe. Bijvoorbeeld Afzender, Datum, Aan, enzovoort.</p> </li> 
     <li> <p><strong>[!UICONTROL Value]</strong> </p> <p>Voer de waarde voor de toets in.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Mark an Email as Read]

Hiermee markeert u een e-mail of concept in een geselecteerde map zoals gelezen door de markering [!UICONTROL Read] in te stellen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map van het e-mailbericht dat u als gelezen wilt markeren. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u als gelezen wilt markeren.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] of [!UICONTROL Search Email] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map van het e-mailbericht dat u als ongelezen wilt markeren. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u als ongelezen wilt markeren.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] of [!UICONTROL Search Email] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Folder]</td> 
   <td>Selecteer de map met het e-mailbericht waaruit u het e-mailbericht wilt verplaatsen. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Destination Folder]</td> 
   <td> <p> Selecteer de map waaraan u de e-mail wilt toevoegen. Voorbeeld: werken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u naar de doelmap wilt verplaatsen.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] of [!UICONTROL Search Email] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy an Email]

Hiermee kopieert u een e-mail of concept naar een geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
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

#### [!UICONTROL Delete an Email]

Hiermee verwijdert u een e-mail of concept uit de geselecteerde map.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder]</td> 
   <td>Selecteer de map van het e-mailbericht dat u wilt verwijderen. Voorbeeld: Primair.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Email ID (UID)]</p> </td> 
   <td> <p>Voer de UID-mailadres in van het e-mailbericht dat u wilt verwijderen.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL Email] &gt; [!UICONTROL Watch Email] of [!UICONTROL Search Email] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expunge]</td> 
   <td> <p>Schakel deze optie in als u wilt dat de module alle berichten die als [!UICONTROL Deleted] zijn gemarkeerd, permanent kan verwijderen in het momenteel geopende postvak.</p> <p>Opmerking: in [!DNL Gmail] wordt dit gedrag aangestuurd door de instelling in de sectie [!UICONTROL Settings] &gt; [!UICONTROL Forwarding POP/IMAP in IMAP access] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get Emails]

Retourneert e-mailberichten die voldoen aan de opgegeven criteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection] </td> 
   <td> <p>Zie <a href="#connect-your-email-to-workfront-fusion" class="MCXref xref"> Uw e-mailadres verbinden met [!UICONTROL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw e-mailaccount met [!UICONTROL Workfront Fusion] .</p> </td>
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
   <td role="rowheader">[!UICONTROL Recipient Email Address]</td> 
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
   <td> <p>Voer trefwoorden in of wijs deze toe om alleen die e-mails met specifieke woordgroepen op te halen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email ID (UID)]</td> 
   <td> <p> Voer de e-mailadres (UID) in van het e-mailbericht waarvan u de gegevens wilt ophalen.</p> <p>U kunt de UID van de e-mail ophalen met de module [!UICONTROL  Watch Email] of [!UICONTROL Search Email] van [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of results]</td> 
   <td> <p> Het maximumaantal e-mailberichten [!DNL Workfront Fusion] moet worden geretourneerd tijdens de uitvoeringscyclus van één scenario.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Continue the execution of the route even if the module returns no results]</td> 
   <td> <p> Selecteer deze optie als u de module wilt blijven uitvoeren, zelfs als er geen resultaten worden geretourneerd.</p> </td> 
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

Voor meer informatie over iterators, zie {de module van de Teller 0} ](/help/workfront-fusion/references/modules/iterator-module.md).[
