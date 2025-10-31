---
title: Fouten opsporen in een scenario
description: Met Adobe Workfront Fusion Devtool kunt u scenario's begrijpen en problemen oplossen. Met het gereedschap Ontwikkelen voegt u een extra deelvenster toe aan de Chrome Developer Tools. Gebruikend dit debugger paneel, kunt u alle handlooppas van uw scenario controleren, alle uitgevoerde verrichtingen herzien, en de details van elke uitgevoerde API vraag zien. U kunt zien welke module, verrichting, of enige reactie de fout veroorzaakte, en die kennis gebruiken om uw scenario te verfijnen.
author: Becky
feature: Workfront Fusion
exl-id: 34215370-27e3-4c28-8bd1-a16268900b86
source-git-commit: 93d06cb917680f9cabc1bad6be0f9cd843449d07
workflow-type: tm+mt
source-wordcount: '1360'
ht-degree: 0%

---

# Fouten opsporen in een scenario

Met Adobe Workfront Fusion Devtool kunt u scenario&#39;s begrijpen en problemen oplossen. Met het gereedschap Ontwikkelen kunt u alle handmatige uitvoering van uw scenario controleren, alle uitgevoerde bewerkingen controleren en de details van elke uitgevoerde API-aanroep bekijken. U kunt zien welke module, verrichting, of enige reactie de fout veroorzaakte, en die kennis gebruiken om uw scenario te verfijnen.

>[!NOTE]
>
>Het registreren in het debugger paneel zal beperkt of niet beschikbaar voor vertrouwelijke scenario&#39;s, automatische uitvoeringen, en succesvolle verrichtingen zijn.

Ga voor een video-introductie en doorloop van het Fusion Devtool naar

* [&#x200B; het Hulpmiddel van de Ontwikkeling van de Fusie &#x200B;](https://video.tv.adobe.com/v/3427031/){target=_blank}
* [&#x200B; Devtool walkthrough &#x200B;](https://experienceleague.adobe.com/docs/workfront-learn/tutorials-workfront/fusion/troubleshooting-and-error-handling/dev-tool-walkthrough.html?lang=nl-NL)

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Toegang krijgen tot het gereedschap Ontwikkelen

Als u Fusion in Adobe verenigde Shell gebruikt, of aan de nieuwe ervaring van de Fusie bijgewerkt hebt, kunt u tot Devtool van de redacteur toegang hebben Scenario.

1. Klik het **hulpmiddel van de Helper** ![&#x200B; Hulpmiddelen &#x200B;](assets/debugger-icon.png) pictogram dichtbij de bodem van het scherm.

Of:

1. Ga naar de redacteur Scenario voor het scenario u wilt zuiveren.

   Om van de redacteur van het Scenario de plaats te bepalen, zie [&#x200B; de scenarioredacteur &#x200B;](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).

1. Klik met de rechtermuisknop in een leeg gebied van de pagina (niet in een module).
1. Selecteer **Open Devtool**.

## Workfront Fusion-hulpprogramma gebruiken

Workfront Fusion Devtool bestaat uit drie hoofdsecties. Deze vindt u in het linkerdeelvenster van het venster Ontwikkelen.

* [&#x200B; Levende Stroom &#x200B;](#live-stream)
* [&#x200B; Foutopsporing van het Scenario &#x200B;](#scenario-debugger)
* [Gereedschappen](#tools)

### Live stream

Met Live stream kunt u zien wat er op de achtergrond gebeurt wanneer u eenmaal in uw scenario op Uitvoeren klikt.

1. Klik het **[!UICONTROL Live Stream]** pictogram ![&#x200B; Actieve stroompictogram &#x200B;](assets/live-stream-icon.png) om de Levende sectie van de Stream te openen.
1. Voer een van de volgende handelingen uit:

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <thead> 
     <tr> 
      <th>Handeling</th> 
      <th>Instructies</th> 
     </tr> 
    </thead> 
    <tbody> 
     <tr> 
      <td role="rowheader">Aanvraaggegevens weergeven</td> 
      <td> <p>U kunt de volgende informatie voor elke module in uw scenario bekijken</p> 
       <ul> 
        <li> <p>De Kopballen van het verzoek (API eindpunt URL, de methode van http, de tijd en de datum het verzoek werd geroepen, verzoekkopballen, en vraagkoord)</p> </li> 
        <li> <p>Indieningsinstantie</p> </li> 
        <li> <p>Antwoordheaders</p> </li> 
        <li> <p>Reactieorgaan</p> </li> 
       </ul> <p>Klik op het desbetreffende tabblad in het rechterdeelvenster van het Workfront Fusion Devtool om deze informatie weer te geven.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Gebeurtenissen zoeken op inhoud</p> </td> 
      <td> <p>Typ de zoekterm in het zoekveld in het linkerdeelvenster van het Workfront Fusion Devtool om alleen aanvragen weer te geven die de zoekterm bevatten.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p>Lijst met verzoeken wissen </p> </td> 
      <td> <p>Klik op het prullenbakpictogram in de rechterbovenhoek van het linkerdeelvenster van het apparaat om de lijst met aanvragen te wissen die is opgenomen met het gereedschap Workfront Fusion Devtool. </p> </td> 
     </tr> 
     <!--<tr> 
      <td role="rowheader"> <p>Enable Console Logging</p> </td> 
      <td> <p>Click the computer icon <img src="assets/console-computer-icon.png"> in the top-right corner of the Devtool's left panel.</p> <p>Logging in the console is enabled when the computer icon is green.</p> </td> 
     </tr>-->
     <tr> 
      <td role="rowheader"> <p>De aanvraag ophalen in de Raw JSON-indeling of cURL</p> </td> 
      <td> 
       <ul> 
        <li> <p><strong> Ruwe JSON </strong> </p> <p>Klik op <strong>[!UICONTROL Copy RAW]</strong> in de rechterbovenhoek van het rechterdeelvenster van het gereedschap Ontwikkelen.</p> </li> 
        <li> <p><strong> cURL </strong> </p> <p>Klik op <strong>[!UICONTROL Copy cURL]</strong> in de rechterbovenhoek van het rechterdeelvenster van het gereedschap Ontwikkelen.</p> </li> 
       </ul> </td> 
     </tr> 
    </tbody> 
   </table>

### Scenario-foutopsporing

>[!NOTE]
>
>Om snel naar debugger van een scenario te gaan dat uit heeft geëist, kunt u **klikken krijgt details** in het foutenbericht in de moduleoutput.
>
>![&#x200B; krijgt details in moduleoutput &#x200B;](assets/go-to-debugger.png)

Scenario Debugger is nuttig voor complexere scenario&#39;s. Het toont de geschiedenis van de scenario looppas en laat u toe om modules door hun naam of identiteitskaart te zoeken.

1. Klik het **[!UICONTROL Scenario Debugger]** pictogram ![&#x200B; Debugger pictogram &#x200B;](assets/scenario-debugger-icon.png) om debugger van het Scenario te openen.
1. (Optioneel) Voer de zoekterm (naam of module-id) in het zoekveld in.
1. Klik op de modulenaam.
1. Klik op de bewerking om de aanvraagdetails weer te geven.

### Gereedschappen

De Workfront Fusion Devtool beschikt over gereedschappen waarmee u uw scenario gemakkelijker kunt instellen.

1. Klik het **[!UICONTROL Tools]** pictogram van de pictogramhulpmiddelen van de pictogram ![&#x200B; Console &#x200B;](assets/console-tools-icon.png) om de Hulpmiddelen te openen.
1. Selecteer het gewenste gereedschap
1. Configureer de velden zoals hieronder wordt beschreven.
1. Klik op **[!UICONTROL Run]**.

Gereedschappen en de bijbehorende velden:

* [&#x200B; Focus een Module &#x200B;](#focus-a-module)
* [&#x200B; vind Modules door Afbeelding &#x200B;](#find-modules-by-mapping)
* [&#x200B; krijg Meta-gegevens van de App &#x200B;](#get-app-metadata)
* [&#x200B; Toewijzing van het Exemplaar &#x200B;](#copy-mapping)
* [&#x200B; de Filter van het Exemplaar &#x200B;](#copy-filter)
* [&#x200B; Naam van de Module van het Exemplaar &#x200B;](#copy-module-name)
* [&#x200B; Verbinding van het Wisselen &#x200B;](#swap-connection)
* [&#x200B; Veranderlijke van het Wisselen &#x200B;](#swap-variable)
* [&#x200B; Basis 64 &#x200B;](#base-64)
* [&#x200B; Remap Source &#x200B;](#remap-source)

#### [!UICONTROL Focus a Module]

Hiermee opent u instellingen van de opgegeven module op ID.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Module ID]</td>
        <td>Voer de id van de module in om de instellingen te openen.</td>
    </tr>
</table>

#### [!UICONTROL Find Modules by Mapping]

Staat u toe om de waarden van modules voor een gespecificeerde termijn te zoeken. De output bevat IDs van modules die de termijn bevatten u naar hebt gezocht.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Keyword]</td> 
   <td> <p> Voer de term in waarnaar u wilt zoeken. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Use Only Values]</p> </td> 
   <td> <p>Schakel deze optie in als u alleen in de waarden van de modulevelden wilt zoeken.</p> <p>Schakel deze optie uit als u ook wilt zoeken in de namen van modulevelden.</p> <p>De zoekopdracht wordt uitgevoerd via de parameters name en label.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Get App Metadata]

Hiermee worden metagegevens van de toepassing opgehaald op basis van de modulenaam of -id van de app. Dit is bijvoorbeeld handig wanneer u moet weten welke versie van de app in uw scenario wordt gebruikt.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecteer de module waarvoor u metagegevens wilt ophalen.</td>
    </tr>
</table>

#### [!UICONTROL Copy Mapping]

Hiermee kopieert u waarden uit de bronmodule naar de doelmodule.

>[!CAUTION]
>
>Zorg ervoor u de correcte bron en doelmodules plaatst. Als u een ander type module selecteert, worden de waarden in de doelmodule verwijderd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Selecteer de module of voer de id in van de module waaruit u de veldwaarden wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Selecteer de module of ga identiteitskaart van de module in waarin u de waarden van de bronmodule wilt opnemen.</p> <p>Belangrijk: waarden in de doelmodule worden overschreven.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Copy Filter]

Hiermee kopieert u de filterinstellingen van de bronmodule naar de doelmodule.

>[!NOTE]
>
>De kopieeractie wordt uitgevoerd op het filter dat op de linkerkant van de geselecteerde module wordt geplaatst.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Selecteer de module of voer de id in van de module waaruit u filterwaarden wilt kopiëren.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Selecteer de module of typ de id van de module waarin u de filterwaarden uit de bronmodule wilt invoegen.</p> <p>Belangrijk: waarden in de doelmodule worden overschreven.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Preserve Fallback Route setting]</p> </td> 
   <td> <p>De bronfilter wordt geplaatst als reserveroute. Schakel deze optie in om ook in te stellen dat het doelfilter is ingesteld als fallback-route.</p> </td> 
  </tr> 
 </tbody> 
</table>


#### [!UICONTROL Copy Module Name]

Hiermee kopieert u de naam van de geselecteerde module naar het klembord.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Module] </td> 
   <td> <p>Selecteer de module waarvan u de naam wilt kopiëren.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Swap Connection]

Dupliceert een verbinding van de bronmodule aan elke module in het scenario van zelfde app.

<table style="table-layout:auto">
    <tr>
        <td>[!UICONTROL Source Module]</td>
        <td>Selecteer de module of voer de id in van de module waaruit u de verbinding wilt dupliceren.</td>
    </tr>
</table>

#### [!UICONTROL Swap Variable]

Zoekt naar opgegeven variabelen in het scenario en vervangt deze door een nieuwe variabele.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Variable to Find]</td> 
   <td> <p> Bepaal de plaats van de veranderlijke pil die u van de veranderlijke module in uw scenario wilt vervangen en het kopiëren aan dit ([!UICONTROL Variable to Find]) gebied. In het veld wordt de markering weergegeven met dubbele accolades. Voorbeeld: <code>&#123;&#123;5.value&#125;&#125;</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Replace With]</p> </td> 
   <td> <p>Bepaal de plaats van de veranderlijke pil die u de variabele met van de variabelen module in uw scenario wilt vervangen en het kopiëren aan dit ([!UICONTROL Variable to Find]) gebied. In het veld wordt de markering weergegeven met dubbele accolades. Voorbeeld: <code>&#123;&#123;5.value&#125;&#125;</code> .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module]</p> </td> 
   <td> <p>Selecteer de variabelemodule waarin u de variabele wilt vervangen. Als geen module wordt geselecteerd, zal de variabele in het volledige scenario worden vervangen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Base 64]

Staat u toe om de ingegaan gegevens aan Base64 te coderen of Base64 te decoderen. Sommige verzoeken worden gecodeerd aan Base64. Dit hulpmiddel kan nuttig zijn wanneer u naar bepaalde gegevens in het gecodeerde verzoek wilt zoeken.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Operation] </td> 
   <td> <p>Selecteer of u de gegevens van het [!UICONTROL Raw Data] gebied aan Base64 wilt coderen of Base64 aan Ruwe Gegevens decoderen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Raw Data]</p> </td> 
   <td> <p> Voer de gegevens in die u wilt coderen naar Base64 of Base64 als u wilt decoderen naar onbewerkte gegevens, afhankelijk van de optie die is geselecteerd in het bovenstaande veld [!UICONTROL Operation] .</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Remap Source]

Hiermee kunt u de toewijzingsbron wijzigen van de ene module in de andere.

U moet eerst de module toevoegen u als bronmodule aan de route in uw scenario wilt gebruiken.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module] </td> 
   <td> <p> Selecteer de module u als toewijzingsbron voor andere modules in uw scenario wilt worden vervangen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Target Module]</p> </td> 
   <td> <p>Selecteer de module die u als nieuwe toewijzingsbron wilt gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Module to Edit]</p> </td> 
   <td> <p>Selecteer de module u de afbeelding voor wilt veranderen als u niet de afbeelding in het volledige scenario wilt veranderen. </p> </td> 
  </tr> 
 </tbody> 
</table>
