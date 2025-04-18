---
title: Datadog-modules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Datadog gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: c8c5f2e3-5af1-4957-bb6f-6c19c35102c5
source-git-commit: 8a4e54a4c1783e4bc679778c6fcf21dcb4d3d537
workflow-type: tm+mt
source-wordcount: '850'
ht-degree: 0%

---

# [!DNL Datadog] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Datadog] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

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

Als u [!DNL Datadog] -modules wilt gebruiken, moet u een [!DNL Datadog] -account hebben.

## DataHond-API-gegevens

De gegevenshondenconnector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>1.0.11.</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Datadog] met [!DNL Workfront Fusion] {#connect-datadog-to-workfront-fusion}

### De API-sleutel en toepassingssleutel ophalen {#retrieve-your-api-key-and-application-key}

Als u uw [!DNL Datadog] -account wilt verbinden met [!DNL Workfront Fusion] , moet u een API-sleutel en een toepassingssleutel ophalen van uw [!DNL Datadog] -account.

1. Meld u aan bij uw [!DNL Datadog] -account.
1. Klik in het navigatievenster aan de linkerkant op **[!UICONTROL Integrations]** en klik vervolgens op **[!UICONTROL APIs]** .
1. Klik op **[!UICONTROL API Keys]** in het hoofdscherm.
1. Houd de muisaanwijzer boven de paarse balk om de API-sleutel weer te geven.
1. Kopieer de API-sleutel naar een beveiligde locatie.
1. Klik op **[!UICONTROL Application Keys]** in het hoofdscherm.
1. Houd de muisaanwijzer boven de paarse balk om de toepassingstoets weer te geven.
1. Kopieer de toepassingssleutel naar een veilige locatie.

### Verbinding maken met [!DNL Datadog] in [!DNL Workfront Fusion]

U kunt rechtstreeks vanuit een [!UICONTROL Datadog] -module verbinding maken met uw [!DNL Datadog] -account.

1. Klik in een willekeurige [!UICONTROL Datadog] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Vul de velden van de module als volgt in:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Connection Name]</td> 
      <td> <p> Voer een naam in voor de verbinding.</p> </td> 
     </tr> 
        <tr>
        <td role="rowheader">[!UICONTROL Environment]</td>
        <td>Selecteer of deze verbinding voor een productie of een non-productie milieu is.</td>
        </tr>
        <tr>
        <td role="rowheader">[!UICONTROL Type]</td>
        <td>Selecteer of u verbinding maakt met een serviceaccount of een persoonlijke account.</td>
        </tr>
     <tr> 
      <td role="rowheader">[!UICONTROL Domain] </td> 
      <td> <p>Selecteer het domein waarmee u verbinding wilt maken (VS of EU).</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key Location] </td> 
      <td> <p>Selecteer of u de API-sleutel wilt opnemen in de koptekst of in de queryreeks.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL API Key]</td> 
      <td> <p> Voer uw API-sleutel voor [!DNL Datadog] in. </p> <p>Voor instructies bij het terugwinnen van de API sleutel, zie <a href="#retrieve-your-api-key-and-application-key" class="MCXref xref"> uw API sleutel en toepassingssleutel </a> in dit artikel terugwinnen.</p> </td> 
     </tr> 
    </tbody> 
   </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Datadog] modules en hun velden

Wanneer u [!DNL Datadog] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Datadog] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

### Handelingen

* [[!UICONTROL Make an API Call]](#make-an-api-call)
* [[!UICONTROL Post Timeseries Points]](#post-timeseries-points)

#### [!UICONTROL Make an API Call]

Met deze actiemodule kunt u een aangepaste API-aanroep uitvoeren.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Datadog] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Datadog] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Use Dedicated Domain]</td> 
   <td>Sommige eindpunten van Datadog API die veel inkomend verkeer verwachten lopen op hun specifieke domeinen. Schakel dit selectievakje in als u het toegewezen domein voor uw API-aanroep wilt gebruiken.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL]</td> 
   <td>Voer een pad in dat relatief is ten opzichte van <code>https://api.datadoghq.com/api/</code> . Voorbeeld:<code> /v1/org</code>.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method]</td> 
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref"> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Headers]</td> 
   <td> <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p> <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p> <p>Workfront Fusion voegt de machtigingsheaders voor u toe.</p> </td> 
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

**Voorbeeld:** de volgende API vraag keert alle dashboards in uw [!DNL Datadog] rekening terug:

URL: `/v1/dashboard`

Methode: `GET`

![ Datadog API vraagvoorbeeld ](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-example.png)

Het resultaat is te vinden in de Uitvoer van de module onder Bundel > Tekst > dashboards.

In ons voorbeeld werden 3 dashboards geretourneerd:

![ Datadog API reactie ](/help/workfront-fusion/references/apps-and-modules/assets/datadog-api-response-example.png)

#### [!UICONTROL Post Timeseries Points]

Met de module kunt u gegevens uit een tijdreeks posten die op de dashboards van [!DNL Datadog] kunnen worden weergegeven.

De limiet voor gecomprimeerde ladingen is 3,2 megabyte (3200000) en 62 megabyte (62914560) voor gedecomprimeerde ladingen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Connection]</td> 
   <td> <p>Zie <a href="#connect-datadog-to-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Datadog] met [!DNL Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Datadog] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Type]</td> 
   <td> Selecteer het type metrisch dat u wilt gebruiken. 
   <ul>
   <li>Gage</li>
   <li>Snelheid</li>
   <li>Aantal</li>
   </ul>
   </td> 
  <tr> 
   <td role="rowheader">[!UICONTROL Interval]</td> 
   <td> Als het type van metrisch tarief of telling is, bepaal het overeenkomstige interval.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Points]</td> 
   <td><p>Voeg punten met betrekking tot metrisch toe.</p> <p>Dit is een JSON-array van punten. Elk punt heeft het formaat: <code>[[POSIX_timestamp, numeric_value], ...] </code></p> <p>Opmerking:  <p>De tijdstempel moet in seconden staan.</p> <p>De tijdstempel moet actueel zijn. De stroom wordt gedefinieerd als niet meer dan 10 minuten in de toekomst of meer dan 1 uur in het verleden.</p> <p> De numerieke notatie moet een drijvende-kommawaarde zijn.</p> </p> <p>Dit veld moet ten minste 1 item bevatten.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Host]</td> 
   <td>Ga de naam van de gastheer in die metrisch produceerde. </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Tags]</td> 
   <td> Voor elke markering die u aan metrisch wilt toevoegen, klik <b> toevoegen punt </b> en ga de waarde van de markering in.</td> 
  </tr> 
 </tbody> 
</table>
