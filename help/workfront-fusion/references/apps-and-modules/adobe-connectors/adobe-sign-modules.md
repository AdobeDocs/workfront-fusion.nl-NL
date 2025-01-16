---
title: Adobe Acrobat Sign-modules
description: Met de  [!DNL Adobe Acrobat Sign]  modules, kunt u een  [!DNL Adobe Workfront Fusion]  scenario beginnen dat op gebeurtenissen in uw  [!DNL Adobe]  rekening van Acrobat Sign wordt gebaseerd, overeenkomsten en andere verslagen tot stand brengen, lezen of bijwerken, onderzoek naar verslagen gebruikend criteria u plaatst, en documenten uploadt.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: 0ef9d40e-8ad6-434e-8fa0-076920ff29ea
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '5489'
ht-degree: 0%

---

# [!DNL Adobe Acrobat Sign] modules

Met de modules [!DNL Adobe Acrobat Sign] kunt u een [!DNL Adobe Workfront Fusion] -scenario starten dat is gebaseerd op gebeurtenissen in uw [!DNL Adobe Acrobat Sign] -account, overeenkomsten en andere records maken, lezen of bijwerken, records zoeken aan de hand van criteria die u instelt en documenten uploaden.

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

## [!DNL Adobe Acrobat Sign] API-informatie

De Adobe Acrobat Sign-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v6 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.35.1</td> 
  </tr>
 </tbody> 
</table>


## [!DNL Adobe Acrobat Sign] aanbevelingen voor connectorgebruik

De [!DNL Adobe Sign] app maakt het automatiseren van de bedrijfsprocessen van eSignature in [!DNL Fusion] veel gemakkelijker en krachtiger.

Nieuwe gebruikers van [!DNL Adobe Sign] moeten bepaalde beperkingen rond het bijwerken van overeenkomsten nauwlettend in de gaten houden. Overeenkomsten worden gewoonlijk niet gewijzigd als ze eenmaal zijn gestart. We raden nieuwe gebruikers van [!DNL Adobe Sign] aan zich te richten op het maken van nieuwe overeenkomsten met behulp van de module voor het maken van overeenkomsten. Hierdoor worden [!DNL Fusion] -automatiseringen eenvoudiger en beter met [!DNL Adobe Sign].

[!DNL Adobe Sign] -overeenkomsten hebben een veld nodig om mee te werken. Er zijn enkele opties om dit te doen, maar de eenvoudigste en meest voorkomende is het uploaden van een tijdelijk document en het vervolgens toewijzen van dat document aan uw overeenkomst.

![](/help/workfront-fusion/references/apps-and-modules/assets/adobe-sign-recommendations-350x168.png)

## [!DNL Adobe Acrobat Sign] modules en hun velden

Wanneer u [!DNL Adobe Acrobat Sign] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe Acrobat Sign] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

<!--
* [Watch for agreements](#watch-for-agreements) 
* [Watch for events](#watch-for-events)
-->

+++ **[!UICONTROL Watch for agreements]**

Deze triggermodule start een scenario wanneer een overeenkomst wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Voor instructies over het aansluiten van uw [!DNL Adobe Acrobat Sign] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Filter]</td> 
   <td>Selecteer of u naar nieuwe verslagen, bijgewerkte verslagen, of allebei wilt letten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type] </td> 
   <td>Selecteer het type record dat de record moet controleren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Find text]</td> 
   <td> <p>Voer termen in waarnaar u wilt zoeken. De module retourneert records die deze termen als veldwaarden bevatten.</p> <p>Voor meer informatie bij het zoeken van gebieden in [!DNL Adobe Acrobat Sign], zie "hoe het zoeken van tekst"in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks"> Onderzoek van Adobe Sign werkt - hoe het </a> werkt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned agreements]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Watch for events]**

Deze triggermodule start een scenario wanneer een gebeurtenis plaatsvindt die u selecteert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td>Selecteer de webhaak die u wilt gebruiken of klik op <b>[!UICONTROL Add]</b> en vul de volgende velden in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook name]</td> 
   <td> <p>Geef een naam op voor de webhaak</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Scopes]</td> 
   <td> 
    <ul> 
     <li> <p>[!UICONTROL Account]</p> </li> 
     <li> <p>[!UICONTROL Group]</p> </li> 
     <li> <p>[!UICONTROL User]</p> </li> 
     <li> <p>[!UICONTROL Resource]</p> <p>Als u [!UICONTROL Resource] selecteert, ga identiteitskaart van het Middel en het type van Middel in.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Resource level]</td> 
   <td> <p>Selecteer het type bron dat u wilt bekijken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Agreements]</p> </li> 
     <li> <p>[!UICONTROL Widgets]</p> </li> 
     <li> <p>[!UICONTROL Megasigns]</p> </li> 
     <li> <p>[!UICONTROL Library Documents]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook subscription events]</td> 
   <td>Selecteer de [!DNL Adobe Sign] -gebeurtenissen die u in de module wilt bekijken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application display name]</td> 
   <td>De weergavenaam van de toepassing waarmee de webhaak wordt gemaakt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Application name]</td> 
   <td>De weergavenaam van de toepassing waarmee de webhaak wordt gemaakt.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Problem notification emails]</td> 
   <td> <p>Deze instelling werkt alleen voor beheerdersaccounts</p> <p>Voor elk e-mailadres waarnaar u e-mailberichten over problemen wilt verzenden, klikt u op <b>[!UICONTROL Add]</b> en voert u het e-mailadres in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement conditional parameters]</td> 
   <td>Als u voorwaardelijke parameters wilt toevoegen, selecteert u <b>[!UICONTROL Yes]</b> in het recordtype waaraan u parameters wilt toevoegen en selecteert u vervolgens <b>[!UICONTROL Yes]</b> in de parameters die u wilt inschakelen.</td> 
  </tr> 
 </tbody> 
</table>

+++

### Handelingen

<!--
* [Create a record](#create-a-record) 
* [Create an agreement](#create-an-agreement) 
* [Create related records](#create-related-records) 
* [Custom API Call](#custom-api-call) 
* [List records](#list-records) 
* [Read a record](#read-a-record) 
* [Read related records](#read-related-records) 
* [Update a record](#update-a-record) 
* [Update related record](#update-related-record) 
* [Upload document](#upload-document)
-->

+++ **[!UICONTROL Create a record]**

Deze actiemodule maakt een nieuwe record van het geselecteerde type.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td>Voor instructies over het aansluiten van uw [!DNL Adobe Acrobat Sign] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Voeg de kopteksten van de aanvraag toe in de vorm van een standaard JSON-object. Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Group]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL Widget]) </b> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group info]</td> 
   <td> <p>Voer de gegevens [!UICONTROL Name] en [!UICONTROL ID] van de groep in of wijs deze toe en geef aan of deze groep de standaardgroep voor de account is.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library document info]</td> 
   <td> <p>Vul de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Files to send]</b> </p> <p>Klik voor elk bestand dat u wilt toevoegen op <b>[!UICONTROL Add item]</b> en vul de velden in.</p> 
      <ul> 
       <li><b>[!UICONTROL Transient document ID]</b> <p>Voer de id van het tijdelijke document in</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Vul de volgende velden in:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Voer het mime-type van het oorspronkelijke bestand in. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type <code>text/html</code> wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type <code>image/jpeg</code> .</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer een naam in voor het bestand.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Voer de URL in van het bestand dat u wilt verzenden.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Selecteer of dit document notaristisch moet worden gemaakt.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Library template name]</b> </p> <p>Voer de naam van de bibliotheeksjabloon in of wijs deze toe</p> </li> 
     <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Geef op wie toegang moet hebben tot het bibliotheekdocument.</p> </li> 
     <li> <p><b>[!UICONTROL Library document state]</b> </p> <p>Selecteer of het document in ontwerpstatus of actief is.</p> </li> 
     <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Klik voor elk type bibliotheeksjabloon dat u wilt gebruiken op <b>[!UICONTROL Add item]</b> en selecteer het sjabloontype.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Voer de laatste datum in waarop een gebeurtenis heeft plaatsgevonden in het bibliotheekdocument.</p> <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref"> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
     <li> <p><b>[!UICONTROL Library document status]</b> </p> <p>Selecteer de status van het bibliotheekdocument.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User info]</td> 
   <td> <p>Vul de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Voer het e-mailadres van de gebruiker in.</p> </li> 
     <li> <p><b>[!UICONTROL Is account admin]</b> </p> <p>Schakel deze optie in als de nieuwe gebruiker een accountbeheerder is.</p> </li> 
     <li> <p><b>[!UICONTROL User ID]</b> </p> <p>Voer de unieke id van de gebruiker in</p> </li> 
     <li> <p><b>[!UICONTROL Account ID]</b> </p> <p>Voer de unieke id in van de [!DNL Adobe Acrobat Sign] -account die aan deze gebruiker is gekoppeld.</p> </li> 
     <li> <p><b>[!UICONTROL First name]</b> </p> <p>Voer de voornaam van de gebruiker in.</p> </li> 
     <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Voer de achternaam van de gebruiker in</p> </li> 
     <li> <p><b>[!UICONTROL Company]</b> </p> <p>Voer de naam van het bedrijf van de gebruiker in.</p> </li> 
     <li> <p><b>[!UICONTROL Initials]</b> </p> <p>Voer de initialen van de gebruiker in.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de landinstelling van de gebruiker in. Dit bepaalt de taal van UI. </p> </li> 
     <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Voer het telefoonnummer van de gebruiker in</p> </li> 
     <li> <p><b> Primaire groep identiteitskaart </b> </p> <p>Voer de groep in waaraan de nieuwe gebruiker wordt toegevoegd. Als er niets is ingevoerd, wordt de gebruiker toegevoegd aan de standaardgroep voor de account.</p> </li> 
     <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Voer de functie van de gebruiker in.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Web form info]</td> 
   <td> <p>De volgende velden invullen</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File info]</b> </p> <p>Voor elk bestand dat u aan het webformulier wilt toevoegen, klikt u op Toevoegen en vult u de volgende velden in:</p> 
      <ul> 
       <li> <p>[!UICONTROL File type]</p> <p>[!UICONTROL Document]</p> </li> 
       <li> <p>[!UICONTROL Transient document]</p> </li> 
       <li> <p>[!UICONTROL URL file info]</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form name]</b> </p> <p>Voer een naam in voor het webformulier. Deze naam wordt gebruikt om het webformulier te identificeren op plaatsen zoals e-mails en websites.</p> </li> 
     <li> <p><b>[!UICONTROL Web form state]</b> </p> <p>Selecteer het frame waarin het nieuwe webformulier moet worden gemaakt.</p> </li> 
     <li> <p><b>[!UICONTROL Web form participant set info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Voor elk lid dat u aan de deelnemersreeks wilt toevoegen, klik <b>[!UICONTROL Add item]</b>. </p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Laat deze optie leeg.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Als u een beveiligingsoptie voor het verifiëren van deze gebruiker wilt toevoegen, selecteert u <b>[!UICONTROL Yes]</b> en vult u de beveiligingsoptie in.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> <p>Selecteer de rol. Alle leden van deze deelnemersreeks delen de rol.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form additional participant sets info]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Voor elk lid dat u aan de deelnemersreeks wilt toevoegen, klik <b>[!UICONTROL Add item]</b>.</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Laat deze optie leeg.</p> </li> 
         <li> <p><b>[!UICONTROL Security option]</b> </p> <p>Als u een beveiligingsoptie voor het verifiëren van deze gebruiker wilt toevoegen, selecteert u <b>[!UICONTROL Yes]</b> en vult u de beveiligingsoptie in.</p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Role]</b> </p> </li> 
       <li> <p><b>[!UICONTROL Web form participant ID] </b> </p> <p>Voer de id van de deelnemer aan het webformulier in.</p> </li> 
       <li> <p><b>[!UICONTROL Order]</b> </p> <p>Geef de volgorde op waarin deze deelnemersset moet communiceren met het webformulier. Bijvoorbeeld, moet de deelnemersgroep die een ordewaarde van 1 heeft eerst gaan, 2 volgende gaan, etc. De aantallen van de orde moeten met beginnen, en hebben geen hiaten in de reeks. </p> </li> 
       <li> <p><b>[!UICONTROL Provider participant set info]</b> </p> <p>Als de deelnemer onbekend is, ga binnen of de leverancier details voor de deelnemer moet verstrekken, en ga een bericht met de details in die u voor de onbekende deelnemer vereist.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Authentication failure info]</b> </p> <p>Als u een pagina met fouten of fouten voor uw gebruikers wilt opgeven, selecteert u <b>[!UICONTROL Yes]</b> en vult u de volgende velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Voer de URL voor de foutpagina in</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Schakel deze optie in als u de foutpagina in het webformulier wilt weergeven</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Voer de vertraging in seconden in voordat de gebruiker wordt omgeleid naar de foutpagina.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL CC info]</b> </p> <p>Voor elk e-mailadres dat u een e-mail wilt ontvangen wanneer de definitieve overeenkomst op het webformulier wordt ondertekend, klikt u op <b>[!UICONTROL Add item]</b> en voert u het e-mailadres in.</p> </li> 
     <li> <p><b>[!UICONTROL Completion info]</b> </p> <p style="font-style: normal;">Als u een succespagina voor uw gebruikers wilt opgeven, selecteert u <b>[!UICONTROL Yes]</b> en vult u de volgende velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL URL]</b> </p> <p>Voer de URL voor de succespagina in</p> </li> 
       <li> <p><b>[!UICONTROL Deframe]</b> </p> <p>Schakel deze optie in als u de succespagina in het webformulier wilt weergeven</p> </li> 
       <li> <p><b>[!UICONTROL Delay]</b> </p> <p>Voer de vertraging in seconden in voordat de gebruiker wordt omgeleid naar de succespagina.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Group ID]</b> </p> <p>Voer de id in van de groep waartoe het webformulier behoort. Als er niets is ingevoerd, behoort het webformulier tot de primaire groep van de accountgebruiker.</p> </li> 
     <li> <p><b>[!UICONTROL Last event date]</b> </p> <p>Voer de datum in waarop de laatste gebeurtenis heeft plaatsgevonden op het webformulier. Gebruik de indeling <code>yyyy-MM-dd'T'HH:mm:ssZ</code> .</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de landinstelling van de gebruiker in. Dit bepaalt de taal van UI. </p> </li> 
     <li> <p><b>[!UICONTROL Security optio] n </b> </p> <p>Voer het wachtwoord in dat wordt gebruikt om het document te beveiligen. U moet dit wachtwoord afzonderlijk doorgeven aan relevante partijen.</p> </li> 
     <li> <p><b>[!UICONTROL Vaulting info]</b> </p> <p>Als uw account is ingesteld voor het archiveren van documenten en de optie om per overeenkomst in te schakelen, kunt u deze optie inschakelen om deze overeenkomst te voltooien.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create an agreement]**

Deze actiemodule maakt een overeenkomst, verzendt deze ter ondertekening en retourneert de overeenkomst-id.

>[!NOTE]
>
>U wordt aangeraden het document te uploaden om het als een tijdelijk document te ondertekenen en het vervolgens toe te wijzen aan het veld [!UICONTROL File to send] in de module [!UICONTROL Create an agreement] . Zie &#39;Document uploaden&#39; in dit artikel voor een voorbeeld.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
<td>Voor instructies over het aansluiten van uw [!DNL Adobe Acrobat Sign] rekening aan [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a></td>  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td>Voeg de kopteksten van de aanvraag toe in de vorm van een standaard JSON-object. Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Files to send]</td> 
   <td> <p>Voor elk item dat u in de overeenkomst wilt opnemen, klikt u op <b>[!UICONTROL Add Item]</b> en vult u de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL File Type]</b> </p> 
      <ul> 
       <li> <p><b>[!UICONTROL Document]</b> </p> <p>Vul de volgende velden in:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Voer de datum in of wijs de datum toe waarop het document is gemaakt in de indeling <code>yyyy-MM-dd'T'HH:mm:ssZ</code> . <code>2016-02-25T18:46:19Z</code> vertegenwoordigt bijvoorbeeld UTC-tijd.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Voer de id van het document in of wijs deze toe.</p> </li> 
         <li> <p><b>[!UICONTROL Label]</b> </p> <p>Voer een uniek label voor het bestand in of wijs dit toe. In het geval van een aangepaste workflow wordt hiermee een bestand toegewezen aan het corresponderende bestandselement in de workflowdefinitie. Dit moet worden opgegeven in het geval van een aanvraag voor het maken van een aangepaste workflowovereenkomst.</p> </li> 
         <li> <p><b>[!UICONTROL Number of pages]</b> </p> <p>Voer het aantal pagina's in het document in of wijs dit toe.</p> </li> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Voer het mime-type van het oorspronkelijke bestand in of wijs dit toe. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type <code>text/html</code> wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type <code>image/jpeg</code> .</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer een naam voor het document in of wijs een naam toe.<br></p> </li> 
        </ul> </li> 
       <li> <p><b>[!UICONTROL Library document ID]</b> </p> <p>De id van het bibliotheekdocument invoeren</p> </li> 
       <li> <p><b>[!UICONTROL Transient document ID]</b> </p> <p>Voer de id van het tijdelijke document in</p> </li> 
       <li> <p><b>[!UICONTROL URL file transfer]</b> </p> <p>Vul de volgende velden in:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Mime-Type]</b> </p> <p>Voer het mime-type van het oorspronkelijke bestand in. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type <code>text/html</code> wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type <code>image/jpeg</code> .</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer een naam in voor het bestand.</p> </li> 
         <li> <p><b>[!UICONTROL URL]</b> </p> <p>Voer de URL in van het bestand dat u wilt verzenden.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Voer een label in voor het bestand.</p> </li> 
     <li> <p><b>[!UICONTROL Notarize]</b> </p> <p>Schakel deze optie in om aan te geven dat het bestand notaristisch moet zijn.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement name]</td> 
   <td>Voer een naam in voor de nieuwe overeenkomst. Deze naam wordt gebruikt om de overeenkomst te identificeren op plaatsen zoals e-mails en websites.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant sets info]</td> 
   <td> <p>Voor elke deelnemersset die u wilt toevoegen, klikt u op <b>[!UICONTROL Add item]</b> en vult u de volgende velden in.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Members]</b> </p> <p>Voor elke persoon die u aan de deelnemersreeks wilt toevoegen, klik <b>[!UICONTROL Add item]</b> en ga het e-mailadres van de persoon in.</p> </li> 
     <li> <p><b>[!UICONTROL Order]</b> </p> <p>Geef de volgorde op waarin deze deelnemersset de overeenkomst moet ondertekenen. Bijvoorbeeld, moet de deelnemersgroep die de een ordewaarde van 1 heeft eerst ondertekenen, 2 volgende ondertekenen, etc. De aantallen van de orde moeten met beginnen, en hebben geen hiaten in de reeks. </p> </li> 
     <li> <p><b>[!UICONTROL Role]</b> </p> <p>Selecteer een rol voor deze deelnemersreeks. Alle deelnemers aan de set ontvangen deze rol.</p> </li> 
     <li> <p><b>[!UICONTROL ID]</b> </p> <p>Ga of kaart identiteitskaart van deze deelnemersreeks in.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Ga of kaart een uniek etiket voor de deelnemersreeks in. Voor aangepaste workflows moet het label dat in de deelnemingsset is opgegeven, worden toegewezen aan de deelnemingsstap in de aangepaste workflow.</p> </li> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer een naam in voor de deelnemersset. Deze naam moet uniek zijn in de overeenkomst.</p> </li> 
     <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Ga of kaart een bericht voor deze deelnemersreeks in. Alle deelnemers aan de set ontvangen dit bericht.</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> <p>Als beperkte documentzichtbaarheid is ingeschakeld voor deze overeenkomst, geeft u op welke bestanden zichtbaar zijn voor deze deelnemersset. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Signature type]</td> 
   <td> <p>Selecteer het type handtekening dat de overeenkomst vereist.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL E-sign]</b> </p> <p>De overeenkomst moet elektronisch worden ondertekend.</p> </li> 
     <li> <p><b>[!UICONTROL Written]</b> </p> <p>De overeenkomst moet met de hand worden ondertekend en de ondertekende overeenkomst moet worden gescand en geüpload.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL State]</td> 
   <td> <p>Selecteer een status voor deze overeenkomst.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Authoring]</b> </p> <p>U kunt nog steeds velden bewerken of toevoegen aan deze overeenkomst.</p> </li> 
     <li> <p><b>[!UICONTROL Draft]</b> </p> <p>U kunt deze overeenkomst stapsgewijs samenstellen voordat u deze verstuurt.</p> </li> 
     <li> <p><b>[!UICONTROL In Process]</b> </p> <p>Deze overeenkomst wordt onmiddellijk verzonden.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL CCs]</td> 
   <td> <p>U kunt deze overeenkomst verzenden naar belanghebbende partijen die niet hoeven te ondertekenen, zoals belanghebbenden. Ze ontvangen een e-mail aan het begin van het ondertekeningsproces en een andere e-mail wanneer de definitieve handtekening wordt ontvangen. Zij ontvangen ook een PDF-exemplaar van de overeenkomst. </p> <p>Voor elke persoon die u voor deze overeenkomst wilt CC, klikt u op <b>[!UICONTROL Add item]</b> en vult u de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Email]</b> </p> <p>Voer het e-mailadres in of wijs het e-mailadres toe dat u wilt gebruiken in de overeenkomst.</p> </li> 
     <li> <p><b>[!UICONTROL Label]</b> </p> <p>Voer een label voor dit e-mailadres in of wijs dit toe, zoals in de beschrijving van de workflow wordt getoond</p> </li> 
     <li> <p><b>[!UICONTROL Visible pages]</b> </p> </li> 
     <li> <p>Als beperkte documentzichtbaarheid is ingeschakeld voor deze overeenkomst, geeft u op welke bestanden zichtbaar zijn voor deze deelnemersset. </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Email option]</td> 
   <td> <p>Geef voor elk type e-mail op of dat type e-mail naar alle deelnemers wordt verzonden of niet.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Completion emails]</b> </p> <p>Verzend een e-mail wanneer deze overeenkomst is voltooid, geannuleerd, verlopen of afgewezen.</p> </li> 
     <li> <p><b>[!UICONTROL In-Flight emails]</b> </p> <p>Verzonden een e-mail wanneer deze overeenkomst wordt gedelegeerd of vervangen.</p> </li> 
     <li> <p><b>[!UICONTROL Agreement initiation emails]</b> </p> <p>Verzend een e-mail wanneer deze overeenkomst wordt gecreeerd of wanneer een actie op het wordt gevraagd.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p>Voer een id voor deze overeenkomst in of wijs deze toe. U kunt dit specificeren wanneer de overeenkomst wordt gecreeerd, en het gebruiken om van de overeenkomst in recentere modules of vragen de plaats te bepalen.</p> <p>Opmerking: de waarde van de externe id is zichtbaar voor alle deelnemers via de API en mag daarom niet worden gebruikt voor het bevatten van een gevoelig token.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Merge field info]</td> 
   <td> <p>Klik voor elk veld in de overeenkomst waarvoor u een standaardwaarde wilt opgeven op <b>[!UICONTROL Add item]</b> en voer de standaardwaarde en de veldnaam in.</p> <p>De waarden zullen aan de ondertekenaars voor editable gebieden voor read-only gebieden worden voorgesteld de verstrekte waarden zullen niet tijdens het ondertekeningsproces editable zijn.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Notary info]</td> 
   <td> <p>Vul de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Appointment]</b> </p> <p>Voer een voorgesteld tijdstip en een voorgestelde datum voor de benoeming in of geef deze aan.</p> </li> 
     <li> <p><b>[!UICONTROL Note]</b> </p> <p>Voer notities in die u over de notarissessie wilt opnemen of wijs deze toe.</p> </li> 
     <li> <p><b>[!UICONTROL Payment]</b> </p> <p>Selecteer of de notaris door de ondertekenaar of de afzender van de overeenkomst wordt betaald.</p> </li> 
     <li> <p><b>[!UICONTROL Notary Type]</b> </p> <p>Selecteer het type notaris</p> 
      <ul> 
       <li> <p>[!UICONTROL Provider notary]</p> <p>De notaris wordt geleverd door de notarisprovider.</p> </li> 
       <li> <p>[!UICONTROL BYON notary]</p> <p>De notaris wordt verstrekt door de klant.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Post sign option]</td> 
   <td> <p>Selecteer of u wilt dat de ondertekenaars naar een succespagina worden geleid nadat de overeenkomst is ondertekend. Als u <b>[!UICONTROL Yes]</b> selecteert, vult u de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Redirect delay]</b> </p> <p>Voer een getal in of wijs een getal toe dat het aantal seconden vertegenwoordigt voordat de ondertekenaar naar de succespagina wordt omgeleid. Als deze waarde groter is dan 0, ziet de gebruiker eerst het standaard succesbericht van [!DNL Adobe Sign] en wordt na een vertraging omgeleid naar de succespagina.</p> </li> 
     <li> <p><b>[!UICONTROL Redirect URL]</b> </p> <p>Typ of wijs een openbaar toegankelijke URL toe waarnaar de gebruiker wordt verzonden nadat het ondertekeningsproces is voltooid.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Security option]</td> 
   <td> <p>Ga of kaart het secundaire wachtwoord in dat zal worden gebruikt om het document van de PDF te beveiligen. </p> <p>Belangrijk: [!DNL Adobe Sign] zal dit wachtwoord nooit delen, zodat moet u het aan om het even welke relevante partijen afzonderlijk meedelen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Vaulting info]</td> 
   <td>Als uw account is ingesteld voor het archiveren van documenten en de optie om per overeenkomst in te schakelen, kunt u deze optie inschakelen om deze overeenkomst te voltooien.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Create related records]**

In deze actiemodule worden records gemaakt die zijn gekoppeld aan een module die u selecteert.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het recordtype van de oorspronkelijke record waaraan u de gemaakte records wilt koppelen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Voer de id in van het object waarmee u de gemaakte record wilt koppelen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement related field]</td> 
   <td> <p>Selecteer het type verwant veld dat u wilt maken</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Form fields]</b> </p> <p>Voer de sjabloon-id in van de sjabloon die de velden bevat die u wilt maken</p> </li> 
     <li> <p><b>[!UICONTROL Reminders]</b> </p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Recipient participant ID]</b> </p> <p>Voor elke deelnemer die u een herinnering wilt ontvangen, klik [!UICONTROL Add item], en ga identiteitskaart van de deelnemer in.</p> </li> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Voor nieuwe records moet de status [!UICONTROL Active] zijn.</p> </li> 
       <li> <p><b>[!UICONTROL First reminder delay]</b> </p> <p>Voer de vertraging in uren in voordat u de eerste herinnering verzendt. De toegestane minimumwaarde is 1 uur en de maximale waarde kan niet meer zijn dan het verschil tussen het maken van een overeenkomst en de vervaltijd van de overeenkomst in uren. Als deze vertraging niet is ingesteld, wordt de eerste herinnering gebaseerd op de frequentie.</p> </li> 
       <li> <p><b>[!UICONTROL Reminder frequency]</b> </p> <p>Stel de frequentie in waarmee u de herinnering wilt verzenden. Als er geen frequentie wordt opgegeven, wordt de herinnering eenmaal verzonden.</p> </li> 
       <li> <p><b>[!UICONTROL Last sent date]</b> </p> <p>Dit veld wordt ingesteld door het systeem.</p> </li> 
       <li> <p><b>[!UICONTROL Next sent date]</b> </p> <p>Dit veld moet leeg zijn of zijn ingesteld op [!UICONTROL ONCE] .</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Voer een notitie in die bij de herinnering moet worden gevoegd. Dit is nuttig om de deelnemer te vertellen waarom zijn deelname wordt vereist.</p> </li> 
       <li> <p><b>[!UICONTROL Start reminder counter from]</b> </p> <p>Selecteer of de herinnering wordt verzonden gebaseerd op wanneer de overeenkomst op wordt gecreeerd wanneer het beschikbaar wordt.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Signer identity report]</b> </p> <p>Voer het wachtwoord in dat wordt gebruikt om het PDF-document te beveiligen.</p> </li> 
     <li> <p><b>[!UICONTROL Views]</b> </p> <p>Voer de volgende velden in</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecteer de naam van de weergave die u wilt maken.</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de gebruiker automatisch aan te melden bij de geretourneerde URL.</p> </li> 
       <li> <p><b>[!UICONTROL Frame Parent]</b> </p> <p>Voer een door komma's gescheiden lijst met bovenliggende domein-URL's in of wijs deze toe waar de geretourneerde URL's kunnen worden opgeslagen. Als de pagina's van [!DNL Adobe Acrobat Sign] leeg blijven, kunnen deze niet worden weergegeven in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de taal in waarin u de weergave wilt maken. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de ingesloten pagina weer te geven zonder een navigatiekop of -voettekst.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u wilt dat de sectie voor het uploaden van bestanden wordt bewerkt door bestanden toe te voegen of te verwijderen. Dit is geen toegangsbeheersysteem. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u de koppelingen van het bibliotheekdocument zichtbaar wilt maken. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u de lokale knop voor het uploaden van bestanden wilt weergeven. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u wilt dat de koppelingen documenten van webbronnen bijvoegen. De standaardwaarde is Ja.</p> </li> 
       <li> <p><b>[!UICONTROL Is preview selected]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de samenstellingspagina in te stellen op de ontwerpmodus.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Voor elk lid waarmee u de overeenkomst wilt delen, klikt u op <b>[!UICONTROL Add item]</b> en voert u het e-mailadres en een bericht van het lid in.</p> </li> 
     <li> <p>[!UICONTROL Delegate participant set]</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Participant set ID]</b> </p> <p>Voer de id van de deelnemersset in</p> </li> 
       <li> <p><b>[!UICONTROL Member info]</b> </p> <p>Voor elk lid dat u wilt toevoegen, klikt u op [!UICONTROL Add item] en voert u het e-mailadres en de telefoongegevens voor het lid in.</p> </li> 
       <li> <p><b>[!UICONTROL Private message]</b> </p> <p>Voer een bericht in. Alle leden van de deelnemersreeks ontvangen dit bericht.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Library view info]</td> 
   <td> <p>Vul de volgende velden in:</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer een naam in voor de bibliotheeksjabloon. Deze naam wordt gebruikt in e-mails en websites.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de gebruiker automatisch aan te melden bij de geretourneerde URL.</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Voer een door komma's gescheiden lijst met bovenliggende domein-URL's in of wijs deze toe waar de geretourneerde URL's kunnen worden opgeslagen. Als de pagina's van [!DNL Adobe Acrobat Sign] leeg blijven, kunnen deze niet worden weergegeven in iframe.</p> </li> 
     <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de taal in waarin u de weergave wilt maken. </p> </li> 
     <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de ingesloten pagina weer te geven zonder een navigatiekop of -voettekst.</p> </li> 
     <li> <p><b>[!UICONTROL Send view configuration]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u de [!UICONTROL Send] -weergave wilt configureren, vult u de volgende velden in.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Agreement name]</b> </p> <p>Voer de naam van de overeenkomst voor het bibliotheekdocument op de pagina voor samenstellen in of wijs deze toe.</p> </li> 
       <li> <p><b>[!UICONTROL Can edit files]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u wilt dat de sectie voor het uploaden van bestanden wordt bewerkt door bestanden toe te voegen of te verwijderen. Dit is geen toegangsbeheersysteem. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b>[!UICONTROL Local file]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u de koppelingen van het bibliotheekdocument zichtbaar wilt maken. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b>[!UICONTROL Web connectors]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u wilt dat de koppelingen documenten van webbronnen bijvoegen. De standaardwaarde is [!UICONTROL Yes] .</p> </li> 
       <li> <p><b> wordt geselecteerde voorproef </b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de samenstellingspagina in te stellen op de ontwerpmodus.</p> </li> 
      </ul> <p> </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User view info]</td> 
   <td> <p>De volgende velden invullen</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecteer de naam van de aangevraagde gebruikersweergave.</p> </li> 
     <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de gebruiker automatisch aan te melden. Selecteer <b>[!UICONTROL No]</b> om referenties te vereisen. De standaardwaarde is [!UICONTROL No] .</p> </li> 
     <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Voer een door komma's gescheiden lijst met bovenliggende domein-URL's in of wijs deze toe waar de geretourneerde URL's kunnen worden opgeslagen. Als de pagina's van [!DNL Adobe Acrobat Sign] leeg blijven, kunnen deze niet worden weergegeven in iframe.</p> </li> 
     <li> <p><b> Geen chroomvlag </b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de ingesloten pagina weer te geven zonder een navigatiekop of -voettekst.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Widget related fields]</td> 
   <td> <p>Selecteer de verwante record die u wilt maken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Views]</p> <p>Vul de volgende velden in.</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Selecteer de naam van de gewenste webformulierweergave</p> </li> 
       <li> <p><b>[!UICONTROL Auto login user]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de gebruiker automatisch aan te melden. Selecteer <b>[!UICONTROL No]</b> om referenties te vereisen. De standaardwaarde is [!UICONTROL No] .</p> </li> 
       <li> <p><b>[!UICONTROL Frame parent]</b> </p> <p>Voer een door komma's gescheiden lijst met bovenliggende domein-URL's in of wijs deze toe waar de geretourneerde URL's kunnen worden opgeslagen. Als de pagina's van [!DNL Adobe Acrobat Sign] leeg blijven, kunnen deze niet worden weergegeven in iframe.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de taal in waarin u de weergave wilt maken. </p> </li> 
       <li> <p><b>[!UICONTROL No chrome flag]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om de ingesloten pagina weer te geven zonder een navigatiekop of -voettekst.</p> </li> 
       <li> <p>[!UICONTROL Personalized signing view configuration]</p> <p>Als u een gepersonaliseerde ondertekeningsweergave wilt configureren, selecteert u <b>[!UICONTROL Yes]</b> en vult u de volgende velden in:</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Email]</b> </p> <p>Voer het e-mailadres in van de persoon die het nieuwe webformulier ontvangt</p> </li> 
         <li> <p><b>[!UICONTROL Comment]</b> </p> <p>Voer een opmerking in die beschrijft hoe de API-aanroeper de identiteit van de ondertekenaar heeft vastgesteld. Deze informatie wordt weergegeven in het audittrail van [!DNL Adobe Acrobat Sign] .</p> </li> 
         <li> <p><b>[!UICONTROL Expiration]</b> </p> <p>Voer een vervaldatum in voor de personalisatie van dit webformulier. </p> <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override=""> Druk van het Type in [!DNL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Reusable]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> als u wilt dat de bedoelde ondertekenaar het formulier meerdere keren kan ondertekenen.</p> </li> 
        </ul> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Member share]</b> </p> <p>Voor elk lid waarmee u de overeenkomst wilt delen, klikt u op <b>[!UICONTROL Add item]</b> en voert u het e-mailadres en een bericht van het lid in.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Custom API Call]**
In deze module kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL URL]</p> </td> 
   <td> <p>Een pad invoeren ten opzichte van <code>https://api.[region].adobesign.com/api/rest/v6/</code></p> <p>Opmerking: raadpleeg de [!DNL Adobe Sign] API-naslaggids voor de lijst met beschikbare eindpunten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Method]</p> </td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String] </td> 
   <td> <p>Voer de queryreeks voor de aanvraag in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Upload a transient document]</td> 
   <td> <p>Als u een tijdelijk document wilt uploaden, voert u het bronbestand in voor het document dat u wilt uploaden.</p> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL List records]**

Deze actiemodule bevat een lijst met alle records van het geselecteerde type waartoe de account toegang heeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record waarvoor u gerelateerde records wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Locale]</td> 
   <td> <p>Voer de landinstelling van de gebruiker in. Dit bepaalt de taal van UI. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td>Voer de externe id (een id die buiten [!DNL Adobe Acrobat Sign] is toegewezen) in of wijs deze toe voor de overeenkomsten die u wilt retourneren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td>Voer de id in van de groep die is gekoppeld aan de records die u wilt weergeven.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Show hidden (records)]</td> 
   <td>Schakel deze optie in als u verborgen records in de resultaten wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Cursor] / [!UICONTROL Start index]</td> 
   <td> <p>Voer het nummer in van de eerste record die de module moet retourneren. </p> <p>Opmerking: dit veld wordt gecombineerd met het veld [!UICONTROL Maximum number of returned records] voor paginering. Als de waarde van [!UICONTROL Maximum number of returned events] bijvoorbeeld 100 is en de waarde van [!UICONTROL Start index] 101, retourneert de module de records 101-200 of de tweede pagina met resultaten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned records]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module aan [actie] tijdens elke cyclus van de scenariouitvoering wilt.</p> <p>Opmerking: dit veld wordt gecombineerd met het veld [!UICONTROL Cursor] of [!UICONTROL Start Index] voor paginering. Als de waarde van [!UICONTROL Maximum number of returned events] bijvoorbeeld 100 is en de waarde van [!UICONTROL Start index] 101, retourneert de module de records 101-200 of de tweede pagina met resultaten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent domain URLs]</td> 
   <td> <p>Voer een door komma's gescheiden lijst met bovenliggende domein-URL's in of wijs deze toe waar de geretourneerde URL's kunnen worden opgeslagen. Als de pagina's van [!DNL Adobe Acrobat Sign] leeg blijven, kunnen deze niet worden weergegeven in iframe.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read a record]**

Deze actiemodule wint informatie van één enkel verslag terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record waarvoor u gerelateerde records wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Voer de id in of wijs deze toe aan de record die u wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Read related records]**

Lees aanvullende informatie over één record.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record waarvoor u gerelateerde records wilt ophalen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] (Voorbeeld: [!UICONTROL Account ID])</td> 
   <td>Voer de id in van de record waarvoor u gerelateerde records wilt ophalen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td>Voer informatie in specifieke velden in op basis van het recordtype en verwante velden.</td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update a record]**

Deze actiemodule werkt één record bij in [!DNL Adobe Acrobat Sign] .

>[!IMPORTANT]
>
>* Als beste praktijk, als u aanzienlijke veranderingen in een overeenkomst verwacht, adviseren wij het creëren van een nieuwe overeenkomst eerder dan het bijwerken van de bestaande overeenkomst.
>* Voor sommige updates zijn verplichte velden beschikbaar. Zorg ervoor dat u alle vereiste velden invult wanneer u de update configureert. Vereiste velden worden vet weergegeven in [!DNL Workfront Fusion] -modules.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID] </td> 
   <td>Voer de id in van de record die u wilt bijwerken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het type record dat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Voer informatie in specifieke velden in op basis van het recordtype en verwante velden.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Als beste praktijk, als u aanzienlijke veranderingen in een overeenkomst verwacht, adviseren wij het creëren van een nieuwe overeenkomst eerder dan het bijwerken van de bestaande overeenkomst.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecteer de velden die u wilt bijwerken en vul de geselecteerde velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Status]</b> </p> <p>Selecteer de nieuwe status voor het bibliotheekdocument.</p> </li> 
       <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer de naam van de bibliotheeksjabloon in of wijs deze toe</p> </li> 
       <li> <p><b>[!UICONTROL Sharing mode]</b> </p> <p>Geef op wie toegang moet hebben tot het bibliotheekdocument.</p> </li> 
       <li> <p><b>[!UICONTROL Library template type]</b> </p> <p>Klik voor elk type bibliotheeksjabloon dat u wilt gebruiken op <b>[!UICONTROL Add item]</b> en selecteer het sjabloontype.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Selecteer de velden die u wilt bijwerken en vul de geselecteerde velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL First name]</b> </p> <p>Voer de voornaam van de gebruiker in.</p> </li> 
       <li> <p><b>[!UICONTROL Last name]</b> </p> <p>Voer de achternaam van de gebruiker in</p> </li> 
       <li> <p><b>[!UICONTROL Company]</b> </p> <p>Voer de naam van het bedrijf van de gebruiker in.</p> </li> 
       <li> <p><b>[!UICONTROL Phone]</b> </p> <p>Voer het telefoonnummer van de gebruiker in</p> </li> 
       <li> <p><b>[!UICONTROL Primary group ID]</b> </p> <p>Voer de groep in waaraan de nieuwe gebruiker wordt toegevoegd. Als er niets is ingevoerd, wordt de gebruiker toegevoegd aan de standaardgroep voor de account.</p> </li> 
       <li> <p><b>[!UICONTROL Job title]</b> </p> <p>Voer de functie van de gebruiker in.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget]) </b> </p> <p>Voer informatie in specifieke velden in op basis van het recordtype en verwante velden.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Update related record]**

Deze actiemodule werkt records bij die betrekking hebben op een specifiek object.

>[!IMPORTANT]
>
>* Als beste praktijk, als u aanzienlijke veranderingen in een overeenkomst verwacht, adviseren wij het creëren van een nieuwe overeenkomst eerder dan het bijwerken van de bestaande overeenkomst.
>* Voor sommige updates zijn verplichte velden beschikbaar. Zorg ervoor dat u alle vereiste velden invult wanneer u de update configureert. Vereiste velden worden vet weergegeven in [!DNL Workfront Fusion] -modules.
>



<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td>Selecteer het recordtype van de record waaraan de verwante velden zijn gekoppeld.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Agreement]/[!UICONTROL Library document]/[!UICONTROL User]/[!UICONTROL Widget ID]</td> 
   <td>Voer de id in van het object waarmee u de gemaakte record wilt koppelen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other fields]</td> 
   <td> <p>Voer informatie in specifieke velden in op basis van het recordtype en verwante velden.</p> 
    <ul> 
     <li> <p><b>[!UICONTROL Agreement]</b> </p> <p>Als beste praktijk, als u aanzienlijke veranderingen in een overeenkomst verwacht, adviseren wij het creëren van een nieuwe overeenkomst eerder dan het bijwerken van de bestaande overeenkomst.</p> </li> 
     <li> <p><b>[!UICONTROL Library document]</b> </p> <p>Selecteer de velden die u wilt bijwerken en vul de geselecteerde velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selecteer de nieuwe status voor het bibliotheekdocument.</p> </li> 
       <li> <p><b>[!UICONTROL Note]</b> </p> <p>Voer de tekst van de notitie in of wijs deze toe.</p> </li> 
       <li> <p><b>[!UICONTROL Visibility]</b> </p> <p>Selecteer of het bibliotheekdocument wordt weergegeven of verborgen.</p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL User]</b> </p> <p>Selecteer de velden die u wilt bijwerken en vul de geselecteerde velden in:</p> 
      <ul> 
       <li> <p><b>[!UICONTROL Group info list]</b> </p> <p>De volgende velden invullen</p> 
        <ul> 
         <li> <p><b>[!UICONTROL Status]</b> </p> <p>Selecteer de nieuwe status voor de gebruiker.</p> </li> 
         <li> <p><b>[!UICONTROL ID]</b> </p> <p>Voer de unieke id van de groep in</p> </li> 
         <li> <p><b>[!UICONTROL Is group admin]</b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om van deze gebruiker een groepsbeheerder te maken.</p> </li> 
         <li> <p><b> is primaire groep </b> </p> <p>Selecteer <b>[!UICONTROL Yes]</b> om deze groep bij te werken naar de primaire groep van de gebruiker.</p> </li> 
         <li> <p><b>[!UICONTROL Created date]</b> </p> <p>Voer de datum in waarop de groep is gemaakt.</p> <p>Voor een lijst van gesteunde datum en tijdformaten, zie <a href="/help/workfront-fusion/references/mapping-panel/data-types/type-coercion.md" class="MCXref xref" data-mc-variable-override=""> Druk van het Type in [!UICONTROL Adobe Workfront Fusion]</a>.</p> </li> 
         <li> <p><b>[!UICONTROL Name]</b> </p> <p>Voer de naam van de groep in of wijs deze toe.</p> </li> 
         <li> <p><b>[!UICONTROL Library document creation visible]</b> </p> <p>Deze instellingen bepalen of de gebruiker bibliotheekdocumenten kan maken</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Toestaan</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Groepsinstelling overnemen van groep of account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL Send restricted to workflows]</b> </p> <p>Deze instellingen bepalen of de gebruiker alleen met behulp van workflows overeenkomsten kan maken.</p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Toestaan</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Groepsinstelling overnemen van groep of account</p> </li> 
          </ul> </li> 
         <li> <p><b>[!UICONTROL User can send]</b> </p> 
          <ul> 
           <li> <p>[!UICONTROL Value]</p> <p>Toestaan</p> </li> 
           <li> <p>[!UICONTROL Inherited]</p> <p>Groepsinstelling overnemen van groep of account</p> </li> 
          </ul> </li> 
        </ul> </li> 
      </ul> 
      <ul> 
       <li> <p><b>[!UICONTROL State]</b> </p> <p>Selecteer de nieuwe status voor de gebruiker en voer een opmerking in over de reden waarom u de gebruiker wilt activeren of deactiveren.</p> </li> 
       <li> <p><b>[!UICONTROL Locale]</b> </p> <p>Voer de landinstelling van de gebruiker in. Dit bepaalt de taal van UI. </p> </li> 
      </ul> </li> 
     <li> <p><b>[!UICONTROL Web form] ([!UICONTROL widget]) </b> </p> <p>Voer informatie in specifieke velden in op basis van het recordtype en verwante velden.</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

+++

+++ **[!UICONTROL Upload document]**

Upload een tijdelijk document. Een tijdelijk document is 7 dagen na het uploaden beschikbaar.

>[!NOTE]
>
>U wordt aangeraden het document te uploaden om het als een tijdelijk document te ondertekenen en het vervolgens toe te wijzen aan het bestand om het veld te verzenden in de module Een overeenkomst maken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!DNL Workfront Fusion] voegt automatisch machtigingsheaders toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record ID]</td> 
   <td>Voer de id in van de record die u wilt bijwerken of wijs deze toe</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td>Voer het mime-type van het oorspronkelijke bestand in. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type <code>text/html</code> wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type <code>image/jpeg</code> .</td> 
  </tr> 
 </tbody> 
</table>

**Voorbeeld:** In dit werkschema, wordt het document om (eerder gedownload van Workfront) te ondertekenen geupload als transient document.

![](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-1-350x308.png)

In de module [!UICONTROL Upload document] krijgt het document een [!DNL Adobe Acrobat Sign] -id waarnaar in latere modules kan worden verwezen. Wanneer de overeenkomst is gemaakt, wordt de id van het geüploade document opgenomen in het veld [!UICONTROL Files to send] .

![](/help/workfront-fusion/references/apps-and-modules/assets/sign-example-2-350x356.png)

+++

### Zoekopdrachten

+++ **[!UICONTROL Search agreements]**

Deze zoekmodule zoekt naar overeenkomsten op basis van criteria die u opgeeft.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Voor instructies over het verbinden van uw [!DNL Adobe Acrobat Sign] rekening met [!DNL Workfront Fusion], zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref"> een verbinding tot stand brengen [!DNL Adobe Workfront Fusion] - Basisinstructies </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Text filter]</td> 
   <td> <p>Zoeken naar tekst in de metagegevens van de overeenkomst. </p> 
    <ul> 
     <li> <p><b>[!UICONTROL Find text]</b> </p> <p>Typ de tekst die u wilt zoeken in de metagegevens van de overeenkomst. Elk woord wordt behandeld als een afzonderlijk tekstitem. </p> </li> 
     <li> <p><b>[!UICONTROL Find text in]</b> </p> <p>Selecteer de metagegevensvelden waarin u tekst wilt zoeken. Als u niets selecteert, zoeken de modules alle meta-gegevens.</p> </li> 
    </ul> <p>De module retourneert elke overeenkomst die een van de ingevoerde tekst in een van de geselecteerde velden bevat. Voorbeeld: als u "Voorjaarscampagne" invoert en de opties Titel en Notitie selecteert, worden alle overeenkomsten geretourneerd met de woorden "Lente" of "Campagne" in Titel of Notitie.</p> <p>Voor meer informatie bij het zoeken van gebieden in [!DNL Adobe Acrobat Sign], zie "hoe het zoeken van de tekst"in <a href="https://helpx.adobe.com/sign/using/adobesign-search-users-agreements.html#HowSearchWorks">[!DNL Adobe Sign] Onderzoek - hoe het werkt </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Created date]</td> 
   <td>Datums selecteren. De module keert slechts verslagen terug waar de gecreeerde datum deze criteria aanpast.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Expiration date]</td> 
   <td>Datums selecteren. De module retourneert alleen records waarbij de vervaldatum overeenkomt met deze criteria.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p role="rowheader">[!UICONTROL Modified date]</p> </td> 
   <td>Datums selecteren. De module keert slechts verslagen terug waar de gewijzigde datum deze criteria aanpast.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL External ID]</td> 
   <td> <p> Externe id is een door de afzender toegewezen id voor de overeenkomst die elke vorm kan hebben, maar gewoonlijk in de vorm van "&lt;groupID&gt;:&lt;ID&gt;".</p> <p>Voor elke externe id die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de externe id in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Group ID]</td> 
   <td> <p>Groep-id is een id die is toegewezen toen de groep werd gemaakt.</p> <p>Voor elke externe id die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de externe id in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Asset ID]</td> 
   <td> <p>Dit is de id die aan de specifieke overeenkomst is toegewezen. </p> <p>Voor elke externe id die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de externe id in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent ID]</td> 
   <td> <p>Dit is de id die aan het bovenliggende object van de overeenkomst is toegewezen. </p> <p>Voor elke externe id die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de externe id in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Participant email]</td> 
   <td> <p>Het e-mailadres van een deelnemer. </p> <p>Voor elke externe id die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de externe id in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Role]</td> 
   <td>Selecteer rollen die u de teruggekeerde resultaten wilt omvatten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort by]</td> 
   <td>Als u wilt dat de module de resultaten sorteert, selecteert u het veld waarop u de resultaten wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Sort orde]r</td> 
   <td>Als u wilt dat de module de resultaten sorteert, selecteert u of u oplopend of aflopend wilt sorteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Status]</td> 
   <td>Selecteer de statussen die de geretourneerde resultaten moeten bevatten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td>Selecteer de typen overeenkomsten die u in de geretourneerde resultaten wilt opnemen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Subtypes]</td> 
   <td>Selecteer de overeenkomstsubtypes die u de teruggekeerde resultaten wilt omvatten. Alleen bibliotheeksjabloonovereenkomsten hebben subtypen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL User ID]</td> 
   <td> <p>De gebruikersnaam van de gebruiker waarmee de overeenkomst wordt gedeeld.</p> <p>Voor elke gebruikersnaam die u wilt toevoegen, klikt u op <b>[!UICONTROL Add]</b> en voert u de gebruikersnaam in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Visibility]</td> 
   <td>Selecteer het zichtbaarheidsniveau dat de geretourneerde resultaten moeten bevatten.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start index]</td> 
   <td> <p>Voer de positie in van het eerste resultaat dat u wilt retourneren. Combineer dit met [!UICONTROL maximum returned results] om resultaten te pagineren</p> <p>Voorbeeld: als u 100 resultaten tegelijk retourneert, voert u 100 in om de resultaten 100-200 te retourneren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Maximum number of returned results]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module aan [actie] tijdens elke cyclus van de scenariouitvoering wilt.</p> </td> 
  </tr> 
 </tbody> 
</table>

+++
