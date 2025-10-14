---
title: Marketo-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Marketo] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1880'
ht-degree: 0%

---

# [!DNL Marketo] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Marketo] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Ga voor een video-introductie over de Marketo-connector naar:

* [&#x200B; Marketo &#x200B;](https://video.tv.adobe.com/v/3427026/){target=_blank}

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Als u [!DNL Marketo] -modules wilt gebruiken, moet u een [!DNL Marketo] -account hebben.

## Marketo API-informatie

De Marketo-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.14.19</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Marketo] met Workfront Fusion {#connect-marketo-to-workfront-fusion}

U kunt rechtstreeks vanuit een [!DNL Marketo] -module verbinding maken met uw [!DNL Marketo] -account.

1. In om het even welke module van Marketo, voegt de klik **naast het gebied van de Verbinding toe.**
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor de nieuwe verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>
          <p>Selecteer of u verbinding maakt met een productieomgeving of niet.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>
          <p>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Account / Munchkin ID]</td>
        <td>
          <p>Voer uw [!DNL Marketo] account of [!DNL Marketo] [!UICONTROL Munchkin] id in. Dit is het unieke gedeelte van de basis-URL of het eindpunt dat aan uw account is toegewezen en dat u gebruikt om via de [!DNL Marketo] -API toegang te krijgen tot [!UICONTROL REST] . Zie [Basis-URL] (https://developers.marketo.com/rest-api/base-url/) in de [!DNL Marketo] documentatie voor instructies over het zoeken naar deze URL.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw Marketo-client-id in. Zie [Verificatie](https://developers.marketo.com/rest-api/authentication/) in de [!DNL Marketo] -documentatie voor instructies over het zoeken naar deze functie.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw Marketo-clientgeheim in. Zie [Verificatie](https://developers.marketo.com/rest-api/authentication/) in de [!DNL Marketo] -documentatie voor instructies over de locatie van deze instructies.</td>
      </tr>
     </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Marketo] Modules en de bijbehorende velden

Wanneer u [!DNL Marketo] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Marketo] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

* [[!UICONTROL Watch events (Instant)]](#watch-events-instant)
* [[!UICONTROL Watch records]](#watch-records)

#### [!UICONTROL Watch events (Instant)]

Deze triggermodule start een scenario wanneer een record wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Webhook]</p> </td> 
   <td> <p>Ga webhaak in die u de module wilt gebruiken.</p> <p>Voor meer informatie over webhooks, zie <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref"> Webhooks </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Watch records]

Deze triggermodule start een scenario wanneer een record wordt gemaakt of bijgewerkt.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Selecteer het type activiteit dat u wilt controleren. </p> <p>De module kijkt slechts voor nieuwe activiteiten.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Op het <b> gebied van het Type van Gebeurtenis 0&rbrace; &lbrace;, selecteer of u voor nieuwe verslagen, bijgewerkte verslagen, zowel nieuwe als bijgewerkte verslagen, of specifieke gebiedsupdates wilt letten. </b> Als u bepaalde veldupdates wilt bekijken, selecteert u het veld dat de module moet controleren.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>Op het <b> gebied van het Type van Gebeurtenis 0&rbrace; &lbrace;, selecteer of u voor nieuwe verslagen, bijgewerkte verslagen, of zowel nieuwe als bijgewerkte verslagen wilt letten.</b></p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u wilt opnemen in de uitvoerbundel voor deze module.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [[!UICONTROL Add Leads to a List]](#add-leads-to-a-list)
* [[!UICONTROL Clone a Program]](#clone-a-program)
* [[!UICONTROL Create a record]](#create-a-record)
* [[!UICONTROL Custom API call]](#custom-api-call)
* [[!UICONTROL Download a File]](#download-a-file)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Remove Leads from a List]](#remove-leads-from-a-list)
* [[!UICONTROL Schedule a Campaign]](#schedule-a-campaign)
* [[!UICONTROL Update a record]](#update-a-record)
* [[!UICONTROL Upload a File]](#upload-a-file)

#### [!UICONTROL Add Leads to a List]

Met deze actiemodule voegt u een of meer leads toe aan een lijst met de lead-id. U kunt maximaal 300 leads tegelijk toevoegen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Voer de id van de lijst in of wijs deze toe op de plaats waar u leads wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Voor elke lood die u aan de lijst wilt toevoegen, klik <b>[!UICONTROL Add]</b>, dan ga identiteitskaart van de lood in of kaart u wilt toevoegen. U kunt maximaal 300 leads toevoegen aan de lijst.</p> <p>Klik op de kaartovergang om een bestaande verzameling leads toe te wijzen die u aan de lijst wilt toevoegen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Clone a Program]

Deze actiemodule maakt een kopie van een programma met de id van het bestaande programma.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Existing Program ID]</td> 
   <td>Voer de id in van het programma dat u wilt kopiëren of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL New Program Name]</p> </td> 
   <td> <p>Geef een naam op of wijs een naam toe aan het nieuwe programma</p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Voer de id van de map in of wijs deze toe aan de locatie van het nieuwe programma.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create a record]

Deze actiemodule maakt een nieuwe record in [!DNL Marketo]

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Folder]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Als u een Bedrijf of een Lood creeert, selecteer de gebieden die u waarden voor wilt plaatsen wanneer het nieuwe verslag wordt gecreeerd, dan waarden voor deze gebieden ingaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Type]</td> 
   <td>Als u een programma maakt, selecteert u het type programma dat u wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Channel] </td> 
   <td>Als u een programma maakt, selecteert u het programmakanaal waar u het programma wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder] / [!UICONTROL Program Name]</td> 
   <td>Als u een map of programma maakt, voert u een naam voor de nieuwe record in of wijst u deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Als u een map of programma maakt, voert u een beschrijving voor de nieuwe record in of wijst u deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Parent Folder ID]</td> 
   <td>Als u een map of programma maakt, voert u de id van de bovenliggende map in of wijst u deze toe op de plaats waar u de nieuwe record wilt maken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Als u een programma maakt, voegt u de gewenste kosten toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Als u een programma maakt, voegt u codes toe</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Marketo] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Marketo] -modules kan worden uitgevoerd.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://{your-base-url}.mktorest.com/</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>[!UICONTROL Workfront Fusion] Hiermee voegt u de machtigingsheaders voor u toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Query String]</td> 
   <td> <p>Voeg de query voor de API-aanroep toe als een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"name":"something-urgent"}</code></p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Voor elk gebied dat u aan uw API vraag wilt toevoegen, <b> klikt toevoegt punt </b> en gaat de sleutel en de waarde van het gebied in.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Download a File]

Deze actiemodule downloadt een bestand met de bestands-id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Voer de id in van het bestand dat u wilt downloaden of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest informatie over een verslag door zijn identiteitskaart te gebruiken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaign]</p> </li> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL List]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen. De velden zijn beschikbaar op basis van de geselecteerde [!UICONTROL Record Type] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL &lt;Object> ID]</td> 
   <td>Voer de id in of wijs deze toe aan het object waarover u informatie wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

Deze actiemodule verwijdert een of meer leads uit een lijst met behulp van de lead-id. U kunt maximaal 300 leads tegelijk verwijderen.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Voer de id van de lijst in of wijs deze toe op de plaats waar u leads wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Voor elke lead die u uit de lijst wilt verwijderen, klikt u op <b>[!UICONTROL Add item]</b> en voert u de id in van de lead die u wilt verwijderen. U kunt maximaal 300 leads toevoegen die de module uit de lijst kan verwijderen. </p> <p>Klik op de kaartovergang om een bestaande verzameling leads toe te wijzen die u uit de lijst wilt verwijderen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Schedule a Campaign]

Deze actiemodule plant een bestaande campagne voor een bepaalde datum.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Voer de id in van de campagne die u wilt plannen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Selecteer de datum waarop de campagne moet worden uitgevoerd. Als dit gebied leeg wordt gelaten, loopt de campagne vijf minuten nadat het scenario begint.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Deze actiemodule werkt een bestaande record bij met behulp van de bijbehorende id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Company]</p> </li> 
     <li> <p>[!UICONTROL Lead]</p> </li> 
     <li> <p>[!UICONTROL Program]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Company] / [!UICONTROL Lead] / [!UICONTROL Program ID]</td> 
   <td>Voer de id in van de record die u wilt bijwerken of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Select fields to map]</td> 
   <td>Als u een Bedrijf of een Lood bijwerkt, selecteer de gebieden die u waarden voor wilt bijwerken, dan waarden voor deze gebieden ingaan.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Program Name]</td> 
   <td>Als u een Programma bijwerkt, ga of kaart een nieuwe naam voor het programma in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td> <p>Als u een Programma bijwerkt, ga of kaart een nieuwe beschrijving voor het programma in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Start Date]</td> 
   <td>Als u een Programma bijwerkt, ga of kaart een nieuwe begindatum voor het programma in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL End Date]</td> 
   <td>Als u een Programma bijwerkt, ga of kaart een nieuwe einddatum voor het programma in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Costs]</td> 
   <td>Als u een programma bijwerkt, voegt u de kosten toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td>Als u een programma bijwerkt, voegt u codes toe</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload a File]

Deze actiemodule uploadt een nieuw bestand naar [!UICONTROL Marketo] .

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file]</td> 
   <td>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Folder ID]</td> 
   <td>Voer de id van de map in of wijs deze toe aan de locatie van het nieuwe bestand.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Description]</td> 
   <td>Voer een beschrijving in voor het geüploade bestand.</td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

* [[!UICONTROL List records]](#list-records)
* [[!UICONTROL Search Records]](#update-a-record)

#### [!UICONTROL List records]

Deze actiemodule wint alle verslagen van een specifiek type terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt weergeven.</p> 
    <ul> 
     <li> <p>[!UICONTROL Read all campaigns]</p> </li> 
     <li> <p>[!UICONTROL Read all programs]</p> </li> 
     <li> <p>[!UICONTROL Read all leads] </p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Field]</td> 
   <td>Als u hebt geselecteerd om leads op te halen, selecteert u of u leads wilt ophalen uit een lijst of uit een programma.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen. De velden zijn beschikbaar op basis van de geselecteerde [!UICONTROL Record Type] .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Search Records]

Deze zoekmodule haalt een lijst op met records die voldoen aan specifieke zoekcriteria.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Marketo] rekening aan Workfront Fusion, zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> verbinden [!DNL Marketo] met Workfront Fusion </a> in dit artikel.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer het type record dat u wilt zoeken.</p> 
    <ul> 
     <li> <p>[!UICONTROL Campaigns]</p> </li> 
     <li> <p>[!UICONTROL Leads]</p> </li> 
     <li> <p>[!UICONTROL Programs]</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Field]</p> </td> 
   <td> <p>Selecteer het veld waarop u wilt zoeken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Value / values]</td> 
   <td>Voer de waarde in van het veld waarnaar u wilt zoeken. Als u in het veld naar meerdere waarden kunt zoeken, klikt u voor elke waarde die u wilt zoeken op <b>[!UICONTROL Add item]</b> en voert u de waarde in.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Output]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p> </td> 
  </tr> 
 </tbody> 
</table>
