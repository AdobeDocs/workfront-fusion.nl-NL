---
title: Marketo-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die  [!DNL Marketo] gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: da417ac7-e532-45f7-86d9-3643b5f9f203
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '1740'
ht-degree: 0%

---

# [!DNL Marketo] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Marketo] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Ga voor een video-introductie over de Marketo-connector naar:

* [ Marketo ](https://video.tv.adobe.com/v/3427026/){target=_blank}

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

U kunt rechtstreeks vanuit de module [!DNL Marketo] verbinding maken met uw [!DNL Marketo] -account.

1. Klik in een willekeurige [!DNL Marketo] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Voer uw [!DNL Marketo] account of [!DNL Marketo] [!UICONTROL Munchkin] id in. Dit is het unieke gedeelte van de basis-URL of het eindpunt dat aan uw account is toegewezen en dat u gebruikt om via de [!UICONTROL REST] -API toegang te krijgen tot [!DNL Marketo] . Voor instructies bij het bepalen van de plaats van dit, zie [ Basis URL ](https://developers.marketo.com/rest-api/base-url/) in de [!DNL Marketo] documentatie.
1. Voer de [!UICONTROL Client ID] en [!UICONTROL Client secret] in. Voor instructies bij de plaats bepalen van deze, zie [ Authentificatie ](https://developers.marketo.com/rest-api/authentication/) in de [!DNL Marketo] documentatie.
1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Marketo] Modules en de bijbehorende velden

Wanneer u [!DNL Marketo] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Marketo] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
   <td> <p>Ga webhaak in die u de module wilt gebruiken.</p> <p>Zie <!--<a href="For instructions, see [Instant triggers (webhooks) in Adobe Workfront Fusion](/help/workfront-fusion/).-->" class="MCXref xref"&gt;Instant triggers (webhaken) in [!DNL Adobe Workfront Fusion]</a> voor meer informatie over websites.</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record Type]</td> 
   <td> <p>Selecteer het type record dat u wilt maken.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Activity]</strong> </p> <p>Selecteer het type activiteit dat u wilt controleren. </p> <p>De module kijkt slechts voor nieuwe activiteiten.<br></p> </li> 
     <li> <p><strong>[!UICONTROL Lead]</strong> </p> <p>Selecteer of u op nieuwe verslagen, bijgewerkte verslagen, zowel nieuwe als bijgewerkte verslagen, of specifieke gebiedsupdates wilt letten. Als u bepaalde veldupdates wilt bekijken, selecteert u het veld dat de module moet controleren.</p> </li> 
     <li> <p><strong>[!UICONTROL Program]</strong> </p> <p>Selecteer of u naar nieuwe verslagen, bijgewerkte verslagen, of zowel nieuwe als bijgewerkte verslagen wilt letten.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen.</p> </td> 
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

Met deze actiemodule voegt u een of meer leads toe aan een lijst met de lead-id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://{your-base-url}.mktorest.com/</code> .</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP-aanvraagmethoden in [!DNL Adobe Workfront Fusion]</a> voor meer informatie.</p> </td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td> <p>Ga of kaart het maximumaantal verslagen in u de module wilt werken met tijdens elke cyclus van de scenariouitvoering.</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL File ID]</td> 
   <td>Wijs de id toe van het bestand dat u wilt downloaden.</td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td role="rowheader">[!UICONTROL <Object> ID]</td> 
   <td>Voer de id in of wijs deze toe aan het object waarover u informatie wilt ophalen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remove Leads from a List]

Deze actiemodule verwijdert een of meer leads uit een lijst met behulp van de lead-id.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL List ID]</td> 
   <td>Voer de id van de lijst in of wijs deze toe op de plaats waar u leads wilt verwijderen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Lead IDs]</td> 
   <td> <p>Voor elke lead die u uit de lijst wilt verwijderen, klikt u op <b>[!UICONTROL Add]</b> en voert u de id in van de lead die u wilt verwijderen. U kunt maximaal 300 leads toevoegen die de module uit de lijst kan verwijderen. </p> <p>Klik op de kaartovergang om een bestaande verzameling leads toe te wijzen die u uit de lijst wilt verwijderen.</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Campaign ID]</td> 
   <td>Voer de id in van de campagne die u wilt plannen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Schedule for Date]</p> </td> 
   <td>Selecteer de datum waarop de campagne moet worden uitgevoerd. Als dit gebied leeg wordt gelaten, loopt de campagne vijf minuten nadat het scenario begon.</td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Zie <a href="#connect-marketo-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Marketo] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Marketo] -account met [!DNL Workfront Fusion] .</p> </td> 
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
   <td> <p>Geef op of u wilt zoeken op naam, naam van het programma of naam van de werkruimte.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Values]</td> 
   <td>Klik voor elke waarde die u wilt zoeken op <b>[!UICONTROL Add item]</b> en voer de waarde in.</td> 
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
