---
filename: adobe-indesign-modules
content-type: reference
product-previous: workfront-fusion
product-area: workfront-integrations
navigation-topic: apps-and-their-modules
title: Adobe InDesign-modules
description: In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Adobe InDesign gebruiken en deze koppelen aan meerdere toepassingen en services van derden.
author: Becky
source-git-commit: 30ddefa8519e6f2052308482137d0fa018676902
workflow-type: tm+mt
source-wordcount: '1691'
ht-degree: 0%

---


# Adobe InDesign-modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die Adobe InDesign gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

Voordat u de Adobe InDesign-connector kunt gebruiken, moet u een actieve Adobe InDesign-account hebben.

## Verbinding maken met Adobe InDesign

Verbinding maken voor uw Adobe InDesign-modules:

1. In om het even welke module van Adobe InDesign, voegt de klik **naast het vakje van de Verbinding toe.**

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
      <col>
      </col>
      <col>
      </col>
      <tbody>
        <tr>
          <td role="rowheader">Verbindingsnaam</td>
          <td>
            <p>Voer een naam in voor deze verbinding.</p>
          </td>
        </tr>
      <tr>
        <td role="rowheader">Omgeving</td>
        <td>
          <p>Selecteer of u verbinding maakt met een productieomgeving of niet.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">Type</td>
        <td>
          <p>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</p>
        </td>
      </tr>
        <tr>
          <td role="rowheader">Client-id</td>
          <td>Voer uw Adobe-client-id in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">Clientgeheim</td>
          <td>Voer uw Adobe-clientgeheim in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
        </tr>
        <tr>
          <td role="rowheader">IMS-organisatie-id</td>
          <td>Voer je Adobe-organisatie-id in. Dit vindt u in de sectie Credentials details van de Adobe Developer Console</td>
        </tr>
      </tbody>
    </table>
1. Klik **verdergaan** om de verbinding te bewaren en aan de module terug te keren.

## InDesign-modules en hun velden

Wanneer u Adobe InDesign-modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen er aanvullende Adobe InDesign-velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Handelingen

* [Uitvoering maken](#create-rendition)
* [Een aangepast script verwijderen](#delete-a-custom-script)
* [Gegevens samenvoegen](#merge-data)
* [Koppelingen opnieuw toewijzen](#remap-links)
* [Een aangepaste aanvraag voor scriptuitvoering indienen](#submit-a-custom-script-execution-request)

#### Uitvoering maken

Met deze actiemodule maakt en retourneert u een JPEG-, PNG- of PDF-uitvoering van een specifiek InDesign-document. Zie `StatusCompletedRespons/output/data` voor de structuur van `RenditionOutputData` . Zie ook `FailedEvent` voor de lijst met mogelijke foutcodes in `RenditionFailedData` .

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Type</p>
      </td>
      <td>Selecteer het bestandstype van de vertoning die u wilt maken. 
      <ul><li>JPEG</li><li>PNG</li><li>PDF</li></ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element dat u aan de vertoning wilt toevoegen:<ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Doeldocument</td>
      <td>Typ of wijs het document toe dat wordt verwerkt en gerenderd. Momenteel wordt slechts één document tegelijk ondersteund.</td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

#### Een aangepast script verwijderen

Deze actiemodule verwijdert één geregistreerd aangepast script. Alle versies van het script worden definitief verwijderd.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Scriptnaam</p>
      </td>
      <td>Voer de naam in van het script dat u wilt verwijderen of wijs de naam ervan toe.</td>
    </tr>
  </tbody>
</table>

#### Gegevens samenvoegen

In deze module worden InDesign-documenten of PDF-bestanden gemaakt door CSV-gegevens samen te voegen met InDesign-sjablonen. Uitvoerindelingen zijn onder andere JPEG-, PNG-, PDF- en InDesign-documenten.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element dat u wilt toevoegen aan het samenvoegen van gegevens:<ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Doeldocument</td>
      <td>Typ of wijs het document toe dat u als sjabloon voor samenvoegen wilt gebruiken.</td>
    </tr>
    <tr>
      <td role="rowheader">Gegevensbron</td>
      <td>Voer de te gebruiken bronbestanden in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

#### Koppelingen opnieuw toewijzen

Deze module vervangt op bestanden gebaseerde koppelingen in InDesign-documenten door Adobe Experience Manager (AEM) URL&#39;s. Dit kan handig zijn als u met Adobe Experience Manager werkt met Adobe Asset Link.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
      </tr>
    <tr>
      <td role="rowheader">AEM Token</td>
      <td>Voer het token voor toonder dat is gegenereerd voor de technische AEM-account in of wijs dit toe, zonder het trefwoord voor toonder.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element dat u aan de module wilt toevoegen:<ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Doeldocument</td>
      <td>Voer het document in waarin u koppelingen opnieuw wilt toewijzen of wijs het document toe.</td>
    </tr>
    <tr>
      <td role="rowheader">Gegevensbron</td>
      <td>Voer de bronbestanden in die u wilt gebruiken voor het uitpakken en afstemmen van tags of wijs deze bestanden toe.</td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

#### Een aangepaste aanvraag voor scriptuitvoering indienen

Deze actiemodule verzendt een uitvoeringsverzoek voor een douanescript. U definieert de invoerelementen en parameters die het aangepaste script tijdens de uitvoering zal gebruiken.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Script-id</p>
      </td>
      <td>Voer de id van het aangepaste script in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element waarvoor u een verzoek van een uitvoerder wilt indienen, <ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

### Zoekopdrachten

* [Aangepaste scriptdetails ophalen](#get-custom-script-details)
* [Codes voor gegevenssamenvoeging ophalen](#get-data-merge-tags)
* [Documentgegevens ophalen](#get-document-information)
* [Aangepaste scripts weergeven](#list-custom-scripts)

#### Aangepaste scriptdetails ophalen

Deze zoekmodule haalt details op van één geregistreerd aangepast script, zoals versie, downloadkoppeling, registratiedatum en scriptnaam.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Scriptnaam</p>
      </td>
      <td>Typ of wijs de naam van het script toe waarvoor u details wilt ophalen.</td>
    </tr>
  </tbody>
</table>

#### Codes voor gegevenssamenvoeging ophalen

In deze module worden de samenvoegcodes uit een document opgehaald.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element dat u aan de module wilt toevoegen:<ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Doeldocument</td>
      <td>Typ of wijs het document toe waaruit u de codes wilt ophalen.</td>
    </tr>
    <tr>
      <td role="rowheader">Gegevensbron</td>
      <td>Voer de bronbestanden in die u wilt gebruiken voor het uitpakken en afstemmen van tags of wijs deze bestanden toe.</td>
    </tr>
    <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

#### Documentgegevens ophalen

Deze module wint uitvoerige informatie over documenten terug INDD/IDML en keert gegevens terug die op de toegelaten informatietypes worden gebaseerd in het verzoek worden gespecificeerd.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
      </tr>
    <tr>
      <td role="rowheader">
        <p>Assets</p>
      </td>
      <td>Voor elk element dat u aan de module wilt toevoegen:<ol><li>Klik <b> toevoegen punt </b>.</li><li>Selecteer of wijs de bron van het element toe.</li><li>Voer een doel in. De bestemming is een weg met betrekking tot een tijdelijke basisfolder (werkende folder) waar het middel wordt gedownload. Dit identificeert de activa binnen de parameters. Het kan niet omhoog gaan met '..' of '/'. Er moet een geldige bestandsnaam zijn.</td>
    </tr>
    <tr>
      <td role="rowheader">Doeldocument</td>
      <td>Typ of wijs het document toe waaruit u de gegevens wilt ophalen.</td>
    </tr>
     <tr>
      <td role="rowheader">Overige velden</td>
   <td>Voor andere gebieden, zie informatie inbegrepen in de module.</td>     </tr>
  </tbody>
</table>

#### Aangepaste scripts weergeven

Deze module wint details van de recentste versie van alle geregistreerde douanescripts, met inbegrip van versie, downloadverbinding, registratiedatum, en manuscriptnaam terug. De resultaten worden gepagineerd op basis van de lengte van de lijst.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
      </tr>
    <tr>
      <td role="rowheader">Paginanummer</td>
      <td>Typ of wijs het paginanummer toe waarmee u wilt beginnen.</td>
    </tr>
  <tr> 
   <td>Maximum aantal geretourneerde resultaten</td> 
   <td>Stel het maximumaantal teams of groepen in dat Workfront Fusion tijdens één uitvoeringscyclus retourneert.</td> 
  </tr> 
  </tbody>
</table>


### Overige

#### Een aangepaste API-aanroep maken

Deze module maakt een aangepaste API-aanroep naar de Adobe InDesign API

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">Verbinding</td>
      <td>Voor instructies bij het creëren van een verbinding aan Adobe InDesign, zie <a href="#create-a-connection-to-adobe-indesign" class="MCXref_0"> een verbinding aan Adobe InDesign </a> in dit artikel tot stand brengen.</td>
    </tr>
       <tr>
      <td role="rowheader">
        <p>Pad</p>
      </td>
      <td>
        <p>Voer een pad in dat relatief is ten opzichte van <code>https://indesign.adobe.io/v3</code> .</p><p> Voorbeeld: <code>/create-rendition</code></p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>Methode</p>
      </td>
      <td>
        <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Zie [HTTP request methods] (/help/workfront-fusion/references/modules/http-request-methods.md) voor meer informatie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Kopteksten</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">Tekenreeks query  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
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
