---
filename: workday-modules
title: Workday-modules
description: In een scenario van de Fusie van Adobe Workfront, kunt u werkschema's automatiseren die  [!DNL Workday] gebruiken, evenals het verbinden met veelvoudige derdetoepassingen en de diensten.
author: Becky
feature: Workfront Fusion
exl-id: 77237a1b-2acd-4350-9cc0-ec43b8b08137
source-git-commit: ec2388ab509e89aec71278210bc4ab6f55ed38fd
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 0%

---

# [!DNL Workday] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Workday] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

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

## Verbinden [!DNL Workday] met [!DNL Workfront Fusion]

1. Klik in een willekeurige [!DNL Workfront Fusion] -module op [!UICONTROL Add] naast het [!UICONTROL Connection] -veld

2. Vul de volgende velden in:

   <table style="table-layout:auto"> 
        <col/>
        <col/>
        <tbody>
            <tr>
                <td role="rowheader">
                    <p role="rowheader">[!UICONTROL Connection name]</p>
                </td>
                <td>Geef een naam op voor de verbinding</td>
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

Wanneer u [!DNL Workday] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Workday] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

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
            <td>Zie <a href="#Connect" class="MCXref xref" > Verbinding maken [!DNL Workday] met [!DNL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Workday] -account met Workfront Fusion.</td>
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
            <td>Zie <a href="#Connect" class="MCXref xref" > Verbinding maken [!DNL Workday] met [!DNL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Workday] -account met [!DNL Workfront Fusion] .</td>
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
            <td>Zie <a href="#Connect" class="MCXref xref" > Verbinding maken [!DNL Workday] met [!DNL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Workday] -account met [!DNL Workfront Fusion] .</td>
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
              <td>Zie <a href="#Connect" class="MCXref xref" > Verbinding maken [!DNL Workday] met [!DNL Workfront Fusion]</a> voor instructies over het verbinden van uw [!DNL Workday] -account met [!DNL Workfront Fusion] .</td>
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
