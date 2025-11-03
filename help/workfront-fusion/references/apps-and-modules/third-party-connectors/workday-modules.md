---
filename: workday-modules
title: Workday-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Workday] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: 363df430b8cc3133961e77d3bd5934490440314c
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# [!DNL Workday] modules

In een Adobe Workfront Fusion-scenario kunt u workflows automatiseren die [!DNL Workday] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [&#x200B; scenario&#39;s creëren: artikelindex &#x200B;](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [&#x200B; Modules: artikelindex &#x200B;](/help/workfront-fusion/references/modules/modules-toc.md).

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

Als u de modules [!DNL Workday] wilt gebruiken, moet u:

* Hebt u een [!DNL Workday] -account.

* Maak een OAuth-toepassing in [!DNL Workday] . Zie de documentatie van [!DNL Workday] voor instructies.

## Workday API-informatie

De Workday-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://{connection.servicesUrl}/api</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.6.4</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Workday] met Workfront Fusion

1. Klik in een willekeurige Workfront Fusion-module op [!UICONTROL Add] naast het veld [!UICONTROL Connection]

2. Vul de volgende velden in:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Voer een naam in voor de verbinding.</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Workday host]</td>
                <td>Voer het adres van de [!DNL Workday] -host in zonder <code>https://</code> . Bijvoorbeeld: <code>mycompany.workday.com</code> .</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Services URL]</td>
                <td>Voer het adres in van uw [!DNL Workday] webservices zonder <code>https://</code> . Bijvoorbeeld: <code>mycompany-services.workday.com</code> .</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Tenant name]</td>
                <td>Voer de huurder voor deze [!DNL Workday] -account in. Uw huurder is de id van uw organisatie en kan worden weergegeven in de URL die u gebruikt om u aan te melden bij Workday. Voorbeeld: in het adres <code>https://www.myworkday.com/mycompany</code> is de huurder <code>mycompany</code> .</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Client ID]</td>
                <td>Voer de client-id in voor de toepassing [!DNL Workday] die door deze verbinding wordt gebruikt. Dit wordt bereikt wanneer u de toepassing maakt in [!DNL Workday] .</td>
            </tr>
            <tr>
                <td  role="rowheader">[!UICONTROL Client Secret]</td>
                <td>Voer het clientgeheim in voor de toepassing [!DNL Workday] die door deze verbinding wordt gebruikt. Dit wordt bereikt wanneer u de toepassing maakt in [!DNL Workday] .</td>
            </tr>
            <tr>
                <td role="rowheader">[!UICONTROL Session timeout (min)]</td>
                <td >Voer het aantal minuten in waarna het verificatietoken verloopt.</td>
            </tr>
        </tbody>
    </table>


3. Klik op [!UICONTROL Continue] om de verbinding op te slaan en terug te keren naar de module

## [!DNL Workday] modules en hun velden

Wanneer u [!DNL Workday] modules configureert, geeft Workfront Fusion de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Workday] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handeling](#action)

* [Zoeken](#search)


### Handeling

* [[!UICONTROL Create a record]](#create-a-record)

* [[!UICONTROL Delete a record]](#delete-a-record)

* [[!UICONTROL Make a custom API call]](#make-a-custom-api-call)

* [[!UICONTROL Update a record]](#update-a-record)


#### [!UICONTROL Create a record]

Deze actiemodule maakt één record in [!DNL Workday] .

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Voor instructies over het aansluiten van uw [!DNL Workday] rekening aan Workfront Fusion, zie <a href="#Connect" class="MCXref xref" > verbinden [!DNL Workday] met Workfront Fusion </a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Selecteer het type record dat u wilt maken.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Voer de id in van de record die u wilt maken of wijs deze toe.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Ga of kaart identiteitskaart van submiddel in u wilt tot stand brengen.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL Delete a record]

Deze actiemodule verwijdert één record in [!DNL Workday] .

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Voor instructies over het aansluiten van uw [!DNL Workday] rekening aan Workfront Fusion, zie <a href="#Connect" class="MCXref xref" > verbinden [!DNL Workday] met Workfront Fusion </a>.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Selecteer het type record dat u wilt verwijderen.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Selecteer het specifieke type record dat u wilt verwijderen. Deze zijn gebaseerd op het recordtype dat u hebt gekozen.</td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Subresource ID]</td>
            <td>Ga of kaart identiteitskaart van subresource in u wilt schrappen.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Voer de id in van de record die u wilt verwijderen of wijs deze toe.</td>
        </tr>
    </tbody>
</table>


### [!UICONTROL Make a custom API call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Workday] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Workday] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

De module keert een statuscode, samen met de kopballen en het lichaam van de API vraag terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!DNL Connection]</p> </td> 
            <td>Voor instructies over het aansluiten van uw [!DNL Workday] rekening aan Workfront Fusion, zie <a href="#Connect" class="MCXref xref" > verbinden [!DNL Workday] met Workfront Fusion </a>.</td>
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code style="color: #ff1493;">https://&lt;tenantHostname>/api/&lt;serviceName>/&lt;version>/&lt;tenant></code> .</td> 
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
   <td role="rowheader">[!UICONTROL Body]</td> 
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update a record]

Deze actiemodule werkt één record bij in [!DNL Workday] .

<table style="table-layout:auto"> 
    <col/>
    <col/>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Voor instructies over het aansluiten van uw [!DNL Workday] rekening aan Workfront Fusion, zie <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] aan Workfront Fusion] </a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record Type]</td>
            <td>Selecteer het type record dat u wilt bijwerken.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td>Voer de id in van de record die u wilt bijwerken of wijs deze toe.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Subresource ID]</td>
            <td >Ga of kaart identiteitskaart van submiddel in u wilt bijwerken.</td>
        </tr>
    </tbody>
</table>

### Zoeken

* [[!UICONTROL Read a record]](#read-a-record)

* [[!UICONTROL List records]](#list-records)


#### [!UICONTROL Read a record]

Deze actiemodule leest één record.

<table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
        <tr>
            <td role="rowheader">[!UICONTROL Connection]</td>
            <td>Voor instructies over het aansluiten van uw [!DNL Workday] rekening aan Workfront Fusion, zie <a href="#Connect" class="MCXref xref" >[!UICONTROL Connect [!DNL Workday] aan Workfront Fusion] </a></td>
        </tr>
        <tr>
            <td  role="rowheader">[!UICONTROL Record type]</td>
            <td>Selecteer het type record dat u wilt verwijderen.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL Specific record type]</td>
            <td>Selecteer het specifieke type record dat u wilt lezen. Deze zijn gebaseerd op het recordtype dat u hebt gekozen.</td>
        </tr>
        <tr>
            <td role="rowheader">[!UICONTROL ID] </td>
            <td >Voer de id in van de record die u wilt verwijderen of wijs deze toe.</td>
        </tr>
    </tbody>
</table>

#### [!UICONTROL List records]

Deze zoekmodule haalt een lijst met records van het opgegeven type op.

<table style="table-layout:auto"> 
      <col/>
      <col/>
      <tbody>
          <tr>
              <td role="rowheader">[!UICONTROL Connection]</td>
              <td>Voor instructies over het verbinden van uw [!DNL Workday] rekening met Workfront Fusion, zie <a href="#Connect" class="MCXref xref" > verbind [!DNL Workday] met Workfront Fusion </a></td>
          </tr>
          <tr>
              <td  role="rowheader">[!UICONTROL Record Type]</td>
              <td>Selecteer het type record dat u wilt ophalen.</td>
          </tr>
          <tr>
              <td role="rowheader">[!UICONTROL Limit]</td>
              <td >
                  <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugwinnen.</p>
              </td>
          </tr>
      </tbody>
  </table>
