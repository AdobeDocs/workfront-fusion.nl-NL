---
title: Adobe I/O Events-modules
description: Met de Adobe I/O Events-modules kunt u een Adobe Workfront Fusion-scenario starten op basis van gebeurtenissen in uw Adobe-toepassingen.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: b2229f3e-a2a7-4b07-8ead-a37d193c2ec7
source-git-commit: 9cea5de748873720247db39161cea12c7e9c7186
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# Adobe I/O Events-modules

Met de Adobe I/O Events-modules kunt u een Adobe Workfront Fusion-scenario starten op basis van gebeurtenissen in Adobe-accounts en -services die geen speciale Workfront Fusion-connector hebben.

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
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
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

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Voordat u de Adobe I/O Events-connector kunt gebruiken, moet u ervoor zorgen dat aan de volgende voorwaarden wordt voldaan:

* Je moet een actieve Adobe-account hebben.

## Adobe I/O Events API-informatie

De Adobe I/O Events-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://api.adobe.io/events</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.6.7</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met Adobe I/O Events

Verbinding maken voor uw Adobe I/O Events-modules:

1. Klik naast het vak Verbinding op Toevoegen.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">Verbindingsnaam</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Selecteer of u verbinding wilt maken met een serviceaccount of een persoonlijke account.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Extra bereik</td>
        <td>Om om het even welk extra werkingsgebied toe te voegen, <b> voeg punt </b> toe en ga het werkingsgebied in.</td>
      </tr>
      <tr>
        <td role="rowheader">Client-id</td>
        <td>Voer uw Adobe-client-id in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
      </tr>
      <tr>
        <td role="rowheader">Clientgeheim</td>
        <td>Voer uw Adobe-clientgeheim in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
      </tr>
      </tr>
        <tr>
        <td role="rowheader">Consumentenorganisatie-id</td>
        <td>Voer je consumentenorg-id in. Dit vindt u in de referentie-URL van het project: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">Referentie-id</td>
        <td>Voer je referentie-id in. Dit vindt u in de referentie-URL van het project: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">IMS-organisatie-id</td>
        <td>Voer je Adobe-organisatie-id in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
      </tr>
        <tr>
        <td role="rowheader">Project-id</td>
        <td>Voer uw project-id in. Dit vindt u in de referentie-URL van het project: <code>https://developer.adobe.com/console/projects/{consumer org ID}/ {project ID}/credentials/{credential ID}/details</code></td>
      </tr>
      <tr>
        <td role="rowheader">Workspace-id</td>
        <td>Als u de Workspace-id van uw project wilt weergeven, downloadt u de projectgegevens van de overzichtspagina van het project in Adobe Developer Console. </td>
      </tr>
    </tbody>
    </table>

1. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.

## Adobe I/O Events-modules en hun velden

Wanneer u [!DNL Adobe I/O Events] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Adobe I/O Events] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Triggers](#triggers)
* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Triggers

#### Een gebeurtenisregistratie maken

Deze actiemodule gebruikt een webhaak om een gebeurtenisbeschrijving te maken. U kunt hier een webhaak configureren. Als u een bestaande webhaak gebruikt, zijn de velden in deze module alleen-lezen.

Een webhaak maken:

1. Klik **toevoegen** naast het gebied van de Webhaak.
1. Vul de volgende velden in:

   <table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Webhook name]</td>
        <td>Voer een naam in voor deze webhaak.</td>
       </tr>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Zie <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" > Verbinding maken met [!DNL Adobe I/O Events]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe I/O Events] .</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Webhook description]
         </td>
         <td>
           Voer een beschrijving in voor deze website.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Selecteer het product of account waarvan u gebeurtenissen wilt maken.
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
           Selecteer de gebeurtenissen die de webhaak moet bekijken. Het scenario wordt geactiveerd wanneer deze gebeurtenissen plaatsvinden.
         </td>
       </tr>
     </tbody>
   </table>

1. Klik op Opslaan om de webhaak op te slaan en terug te keren naar de module.

### Handelingen

#### Alle gebeurtenissen ophalen uit een dagboek

Deze zoekmodule haalt alle gebeurtenissen voor een registratie uit een journaal op.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Zie <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" > Verbinding maken met [!DNL Adobe I/O Events]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe I/O Events] .</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Registration ID]
         </td>
         <td>
           Selecteer de registratie waarvoor u gebeurtenissen wilt ophalen.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Maximum number of returned records]
         </td>
         <td>
              Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren. 
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Return events that occur after]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Seek]
         </td>
         <td>
         </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Latest]
         </td>
         <td>
         Schakel deze optie in om de laatste gebeurtenis te retourneren.
         </td>
       </tr>
     </tbody>
   </table>

#### Een aangepaste API-aanroep maken

Deze actiemodule maakt een aangepaste API-aanroep naar de [!DNL Adobe I/O Events] API

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Zie <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" > Verbinding maken met [!DNL Adobe I/O Events]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe I/O Events] .</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Een pad invoeren ten opzichte van <code>https://api.adobe.io/events</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
  <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p>  
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders en x-api-sleutelkopballen toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>

### Zoekopdrachten

#### Provider- en gebeurtenis-id&#39;s ophalen

Deze zoekmodule haalt de Adobe I/O Events-id&#39;s voor de opgegeven provider en gebeurtenissen op.

<table>
     <col/>
     <col/>
     <tbody>
       <tr>
         <td role="rowheader">[!UICONTROL Connection]</td>
        <td>Zie <a href="#create-a-connection-to-adobe-io-events" class="MCXref xref" > Verbinding maken met [!DNL Adobe I/O Events]</a> in dit artikel voor instructies over het maken van een verbinding met [!DNL Adobe I/O Events] .</td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event provider]
         </td>
         <td>
           Selecteer de provider waarvoor u de id wilt ophalen.
        </td>
       </tr>
       <tr>
         <td role="rowheader">
           [!UICONTROL Event type]
         </td>
         <td>
              Selecteer de gebeurtenissen waarvoor u id's wilt opgeven. Gebeurtenissen zijn beschikbaar op basis van de gebeurtenisprovider. 
         </td>
       </tr>
     </tbody>
   </table>

<!--

Watch Events

This trigger module starts a scenario when an event occurs in the chosen Adobe product or service.

<table style="table-layout:auto"> 
   <col> 
   <col> 
   <tbody> 
   <tr> 
   <td role="rowheader">Webhook</td> 
   <td><p>Select the webhook that you want to use for this trigger, or add a new webhook. </p><p>To add a new webhook, <ol><li>Click <b>Add</b> next to the webhook field.</li><li>Enter the following: <ul><li>A name for the webhook</li><li>The connection that you want to use for this webhook</li><li>The source of the events you want to watch</li></ul></li><li>Click <b>Save</b> to save the webhook and return to the module. </td> 
   </tr> 
   </tbody> 
</table>

-->
