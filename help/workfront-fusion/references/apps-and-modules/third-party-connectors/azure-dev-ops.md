---
title: Azure DevOps-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Azure DevOps] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion
exl-id: c0919a9a-ce99-485c-9627-45353741f6d8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1627'
ht-degree: 0%

---

# [!DNL Azure DevOps] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Azure DevOps] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL Azure DevOps] -modules wilt gebruiken, hebt u een [!DNL Azure] DevOps-account nodig.

## [!DNL Azure DevOps] API-informatie

De Azure DevOps-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v5.1 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.29.33</td> 
  </tr>
 </tbody> 
</table>

## Verbinden [!DNL Azure DevOps] met Workfront Fusion {#connect-azure-devops-to-workfront-fusion}

1. Voeg een module [!DNL Azure DevOps] toe aan uw scenario.
1. Klik op **[!UICONTROL Add]** naast het veld [!UICONTROL Connection] .
1. Selecteer in het veld [!UICONTROL Connection Type] het type verbinding dat u wilt gebruiken.

   >[!NOTE]
   >
   >Met [!UICONTROL [!DNL Azure DevOps] (EntraApp)] kunt u alle bereik voor de verbinding aanvragen.

1. Vul de volgende velden in:

   <table style="table-layout:auto">
      <tr>
            <td>[!UICONTROL Connection name]</td>
            <td>Voer een naam in voor de verbinding die u maakt.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Organization]</td>
            <td>Voer de naam in van de organisatie waaronder u de [!DNL Azure DevOps] -toepassing hebt gemaakt.</td>
      </tr>
      <tr>
            <td>[!UICONTROL App ID]</td>
            <td>Voer de id in van de DevOps-toepassing waarmee u verbinding maakt.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Client Secret]</td>
            <td>Voer het clientgeheim in voor de DevOps-toepassingen waarmee u verbinding maakt.</td>
      </tr>
      <tr>
            <td>[!UICONTROL Request All Scopes]</td>
            <td>Als u het verbindingstype [!DNL Azure DevOps] (EntraApp) gebruikt, schakelt u deze optie in om alle bereik voor de verbinding aan te vragen.</td>
      </tr>
   </table>

1. Om een Azure App ID DevOps of Geheim van de Cliënt in te gaan, klik <b> toon geavanceerde montages </b> en ga hen op de gebieden in die openen.
1. Klik op **[!UICONTROL Continue]** om het instellen van de verbinding te voltooien en door te gaan met het maken van uw scenario.

## [!UICONTROL Azure DevOps] modules en hun velden

Wanneer u [!DNL Azure DevOps] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Azure DevOps] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### [!UICONTROL Watch for work items]

Deze instant trigger-module voert een scenario uit wanneer een record wordt toegevoegd, bijgewerkt of verwijderd in [!UICONTROL Azure DevOps] .

De module retourneert alle standaardvelden die aan de record zijn gekoppeld, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhook]</td> 
   <td> <p>Selecteer of voeg een webhaak voor de module toe.</p> <p>Voor meer informatie over websites in trekkermodules, zie <a href="/help/workfront-fusion/references/modules/webhooks-reference.md" class="MCXref xref"> Onmiddellijke trekkers (webhooks) </a>.</p> <p>Voor informatie over hoe te om een webhaak tot stand te brengen, zie <a href="/help/workfront-fusion/references/apps-and-modules/universal-connectors/webhooks-updated.md" class="MCXref xref"> Webhooks </a>.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Handelingen

* [Een record maken](#create-a-record)
* [Aangepaste API-aanroep](#custom-api-call)
* [Een bijlage downloaden](#download-an-attachment)
* [Werkitems koppelen](#link-work-items)
* [Record lezen](#read-record)
* [Een tijdelijk item bijwerken](#update-a-work-item)
* [[!UICONTROL Upload an attachment]](#upload-an-attachment)

#### [!UICONTROL Create a record]

Deze actiemodule leidt tot een nieuw project of het werkpunt.

De module geeft de object-id weer voor het nieuwe werkitem of de URL en statuscode van een nieuw gemaakt project.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer of u een het werkpunt of een project wilt tot stand brengen.</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong> </p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Name]</strong>: Voer een naam voor het nieuwe project in of wijs een naam toe.</p> </li> 
       <li> <p><strong>[!UICONTROL Description]</strong>: Voer een beschrijving voor het nieuwe project in of wijs deze toe. </p> </li> 
       <li> <p><strong>[!UICONTROL Visibility]</strong>: Selecteer of u wilt dat uw project openbaar of privé is. De gebruikers moeten in uw organisatie worden ondertekend en moeten toegang tot het project hebben verleend om met een privé project in wisselwerking te staan. De openbare projecten zijn zichtbaar aan gebruikers die niet binnen aan uw organisatie worden ondertekend.</p> </li> 
       <li> <p><strong>[!UICONTROL Version control]</strong>: Selecteer of u het project [!DNL Git] of [!UICONTROL Team Foundation Version Control (TFCV)] wilt gebruiken voor versiebeheer.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item process]</strong>: Selecteer het werkproces dat u voor het project wilt gebruiken. De opties zijn [!UICONTROL Basic] , [!UICONTROL Scrum] , [!UICONTROL Capability Maturity Model Integration (CMMI)] en [!UICONTROL Agile] .</p> <p>Voor meer informatie over [!DNL Azure DevOps] processen, zie <a href="https://docs.microsoft.com/en-us/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops&tabs=basic-process"> Standaardprocessen en procesmalplaatjes </a> in de [!DNL Azure DevOps] Documentatie.</p> </li> 
      </ul> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong> </p> <p>Vul de volgende velden in:</p> 
      <ul> 
       <li> <p><strong>[!UICONTROL Project]</strong>: Selecteer het project waar u het het werkpunt wilt tot stand brengen.</p> </li> 
       <li> <p><strong>[!UICONTROL Work item type]</strong>: Selecteer het type werkitem dat u wilt maken.</p> </li> 
       <li> <p><strong>[!UICONTROL Other fields]</strong>: Voer in deze velden de waarde in die het werkitem moet hebben voor een bepaalde eigenschap. Beschikbare velden zijn afhankelijk van het type werkitem.</p> </li> 
      </ul> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Azure DevOps] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Azure DevOps] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Base URL]</td> 
   <td> <p>Selecteer of wijs de basis-URL toe die u gebruikt om verbinding te maken met uw [!DNL Azure DevOps] -account</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Relative URL]</td> 
   <td> <p>Voer de relatieve URL in waarmee u verbinding wilt maken voor deze API-aanroep.</p> <p><b> Voorbeeld: </b><code>{organization}/_apis[/{area}]/{resource}</code> </p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!UICONTROL API Version]</td> 
   <td>Selecteer of wijs de versie van [!DNL Azure DevOps] API toe die u voor deze API vraag wilt verbinden. Als er geen versie is geselecteerd, maakt Workfront Fusion verbinding met [!DNL Azure DevOps] API versie 5.1.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> </td> 
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
 </tbody> 
</table>

#### [!UICONTROL Download an attachment]

Deze actiemodule downloadt een bijlage.

De module retourneert de bestandsinhoud van de bijlage.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Attachment URL]</td> 
   <td> <p>Voer de URL in van de bijlage die u wilt downloaden of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Link work items]

Deze actiemodule verbindt twee het werkpunten en bepaalt het verband tussen hen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Voer de id in van het hoofdwerkitem waarnaar u een ander werkitem wilt koppelen of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Linked work item ID]</td> 
   <td>Voer de id in van het werkitem dat u wilt koppelen aan het hoofdwerkitem of wijs deze toe.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Link Type]</td> 
   <td> <p>Bepaal de verhouding tussen de het werkpunten die u wilt verbinden.</p> <p>Voor meer informatie, zie <a href="https://docs.microsoft.com/en-us/azure/devops/boards/queries/link-type-reference?view=azure-devops"> gids van de Verwijzing voor verbindingstypes </a> in de [!UICONTROL Azure DevOps] Documentatie.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Voer de tekst van een opmerking in of wijs deze toe. Dit is nuttig om de redenering of de intentie van het verband uit te leggen.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read record]

Deze actiemodule leest gegevens uit één record in [!DNL Azure DevOps] .

U geeft de id van de record op.

De module retourneert de id van de record en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Record type]</td> 
   <td> <p>Selecteer of u een project of een het werkpunt wilt lezen</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL Project]</strong>: Selecteer het project dat u wilt lezen.</p> </li> 
     <li> <p><strong>[!UICONTROL Work item]</strong>: Selecteer het project dat het het werkpunt bevat u wilt lezen, dan het type van het het werkpunt selecteren.</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de informatie die u in de uitvoerbundel voor deze module wilt opnemen. Beschikbare velden zijn afhankelijk van het type werkitem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL ID]</td> 
   <td>Voer de id in van de record die u wilt lezen of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a work item]

Deze actiemodule werkt een bestaand werkitem bij met behulp van de bijbehorende id.

De module keert identiteitskaart van het bijgewerkte het werkpunt terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selecteer het project dat het het werkpunt bevat u wilt bijwerken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work Item Type]</td> 
   <td> <p>Selecteer het type werkitem dat u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Other Fields]</td> 
   <td>Op elk van deze gebieden, ga de waarde in die u het het werkpunt voor een bepaalde bezit wilt hebben. Beschikbare velden zijn afhankelijk van het type werkitem.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td>Voer de id in van het werkitem dat u wilt bijwerken of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Upload an attachment]

Deze actiemodule uploadt een bestand en koppelt dit aan een tijdelijk item.

De module retourneert de bijlage-id en een download-URL voor de bijlage.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project] </td> 
   <td> <p>Selecteer het project waar u een gehechtheid wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item ID]</td> 
   <td> <p>Ga of kaart identiteitskaart van het het werkpunt in waar u een gehechtheid wilt uploaden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Comment]</td> 
   <td>Voer de tekst in van een opmerking die u aan de geüploade bijlage wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source file] </td> 
   <td>Selecteer een bronbestand uit een vorige module of voer de naam en inhoud van het bronbestand in of wijs deze toe.</td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

#### [!UICONTROL List work items]

Deze actiemodule wint alle het werkpunten van een specifiek type in een [!DNL Azure DevOps] project terug.

De module retourneert de id van het hoofdwerkitem en alle bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie [!DNL Azure DevOps] Verbinding maken <a href="#connect-azure-devops-to-workfront-fusion" class="MCXref xref"> met [!DNL Azure DevOps] in dit artikel voor instructies over het verbinden van uw [!UICONTROL Workfront Fusion]</a> -account met Workfront Fusion.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Project]</td> 
   <td>Selecteer het project waarvan u de het werkpunten wilt terugwinnen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Work item type]</td> 
   <td> <p>Selecteer het type werkitem dat u wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td>Selecteer de eigenschappen die u in de uitvoer van de module wilt weergeven. De beschikbare velden zijn afhankelijk van het type werkitem dat u wilt ophalen. U moet ten minste één eigenschap selecteren.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Limit]</td> 
   <td>Voer het maximale aantal werkitems in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert of wijs dit aantal toe.</td> 
  </tr> 
 </tbody> 
</table>
