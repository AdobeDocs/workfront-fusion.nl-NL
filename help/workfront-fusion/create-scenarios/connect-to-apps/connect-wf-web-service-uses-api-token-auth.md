---
title: Connect Adobe Workfront Fusion naar een webservice die API-tokenverificatie gebruikt
description: Bij sommige services is het niet mogelijk om met integratieoplossingen zoals Adobe Workfront Fusion een app te maken die u eenvoudig kunt gebruiken in uw scenario.
author: Becky
feature: Workfront Fusion
exl-id: 4a8ac816-52de-41e8-96d7-1c8cde2ebe32
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '983'
ht-degree: 0%

---

# Connect Adobe Workfront Fusion naar een webservice die API-tokenverificatie gebruikt

Bij sommige services is het niet mogelijk om met integratieoplossingen zoals Adobe Workfront Fusion een app te maken die u eenvoudig kunt gebruiken in uw scenario.

U kunt deze situatie omzeilen door de gewenste service (app) aan te sluiten op Workfront Fusion via HTTP > Een aanvraag maken.

In dit artikel wordt uitgelegd hoe u bijna elke webservice kunt verbinden met Workfront Fusion via een API-sleutel/API-token.

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
   <p>Connectorgebaseerde (verouderde): als u verbinding wilt maken met toepassingen buiten de Workfront-productreeks, hebt u Workfront Fusion for Work Automation and Integration nodig </p>
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

## Verbinding maken met een webservice die een API-token gebruikt

De procedure voor het verbinden van de service via een API-token is vergelijkbaar voor de meeste webservices.

1. Creeer een toepassing op de website van de Webdienst, zoals verklaard in de sectie [&#x200B; creeer een nieuwe toepassing en verkrijg het API teken &#x200B;](#create-a-new-application-and-obtain-the-api-token) in dit artikel.
1. Haal de API-sleutel of API-token op.
1. Voeg HTTP van Workfront Fusion > een module van het Verzoek aan uw scenario toe.
1. Opstelling de module volgens de API van de Webdienst documentatie en het runnen van het scenario, zoals die in de sectie [&#x200B; wordt verklaard Opstelling de module van HTTP &#x200B;](#set-up-the-http-module) in dit artikel.

>[!NOTE]
>
>In dit voorbeeld wordt verbinding gemaakt met de Pushover-meldingsservice.

## Een nieuwe toepassing maken en het API-token ophalen

>[!NOTE]
>
>Webservices maken en distribueren API-sleutels of API-tokens op verschillende manieren. Ga naar de website van de service en zoek naar &quot;API-sleutel&quot; of &quot;API-token&quot; voor instructies voor het verkrijgen van een API-sleutel en -token voor de gewenste webservice.
>
>We nemen alleen instructies voor het verkrijgen van een Pushover API-sleutel op als voorbeeld van wat u zou kunnen vinden.

1. Meld u aan bij uw Pushover-account.
1. Klik **creeer een Token van de Toepassing/API** bij de bodem van de pagina.
1. Vul de Informatie van de Toepassing in en klik **creeer een Toepassing**.
1. Sla de opgegeven API-token op een veilige plaats op. U hebt deze nodig als de Workfront Fusion HTTP > Een aanvraag-module maken verbinding moet maken met de gewenste webservice (in dit geval Pushover).

## De module HTTP instellen

Als u een webservice wilt koppelen aan uw Workfront Fusion-scenario, moet u HTTP > Een aanvraagmodule maken in het scenario gebruiken en de module instellen volgens de API-documentatie van de webservice.

1. Voeg HTTP > een module van het Verzoek aan uw scenario toe.
1. Als u een bericht wilt verzenden met Workfront Fusion, stelt u de HTTP-module als volgt in.

   >[!NOTE]
   >
   >Deze module-instellingen komen overeen met de API-documentatie van de Pushover-webservice. De instellingen voor andere webservices kunnen afwijken. De API-token kan bijvoorbeeld worden ingevoegd in de koptekst en niet in het veld Hoofdtekst.

   <table style="table-layout:auto"> 
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader"> URL</td> 
      <td> <p><code>https://api.pushover.net/1/messages.json</code> </p> <p>Het veld URL bevat het eindpunt dat u kunt vinden in de API-documentatie van de webservice.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> Methode</td> 
      <td> <p><code>POST</code> </p> <p>De gebruikte methode hangt van het overeenkomstige eindpunt af. Het eindpunt van Pushover voor het duwen van berichten gebruikt de POST methode.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Kopteksten</p> </td> 
      <td> <p>Sommige webservices kunnen headers gebruiken om de API-tokenverificatie of andere parameters op te geven. Dit is niet het geval in ons voorbeeld als eindpunt van de Pushover voor het drukken van berichten gebruikt het Lichaam (zie hieronder) voor alle verzoektypes.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Tekenreeks query</p> </td> 
      <td> <p>Sommige webservices kunnen een queryreeks gebruiken om andere parameters op te geven. Dit is niet het geval in ons voorbeeld aangezien de Pushover Webdienst Lichaam (zie hieronder) voor alle verzoektypes gebruikt.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Type body</p> </td> 
      <td> <p><code>Raw</code> </p> <p>Met deze instelling kunt u het JSON-inhoudstype selecteren in het veld Inhoudstype hieronder.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Inhoudstype</p> </td> 
      <td> <p><code>JSON (application/json)</code> </p> <p>JSON is het vereiste inhoudstype voor de Pushover-app. Dit kan verschillen van andere webservices.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader"> <p> Inhoud aanvragen</p> </td> 
      <td> <p>Voer de inhoud van het verzoek voor Body in de JSON-indeling. U kunt JSON gebruiken &gt; creeer JSON module zoals die in <a href="#map-the-json-body-using-the-json--create-json-module" class="MCXref xref"> wordt verklaard Kaart het lichaam JSON gebruikend JSON &gt; creeer JSON module </a> in dit artikel. Of u kunt de inhoud JSON manueel ingaan, zoals die in <a href="#enter-the-json-body-manually" class="MCXref xref"> wordt verklaard gaat het lichaam JSON manueel </a> in dit artikel in.</p> <p>Zie de API-documentatie van de webservice voor de vereiste parameters voor die webservice.</p> </td>

   </tr> 
    </tbody> 
   </table>

## Typ de JSON-hoofdtekst handmatig

Geef parameters en waarden op in de JSON-indeling.

>[!BEGINSHADEBOX]

**Voorbeeld:**

```
{"user":"12345c2ecu1hq42ypqzhswbyam34",
"token":"123459evz8aepwtxydndydgyumbfx",
"message":"Hello World!",
"title":"The Push Notification"}
```

>[!ENDSHADEBOX]

Dit voorbeeld bevat de volgende informatie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p> user</p> </td> 
   <td> <p>UW USER_KEY. Dit vindt u op het Pushover-dashboard.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> token </td> 
   <td> <p>Uw API-token/API-sleutel die is gegenereerd, hebt u uw Photoshop-app gemaakt.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> message </td> 
   <td> <p>De tekstinhoud van de pushmelding die naar het apparaat of de apparaten wordt verzonden.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> titel </td> 
   <td> <p>(Optioneel) De titel van je bericht. Als er geen waarde wordt ingevoerd, wordt de naam van uw app gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Wijs de JSON-hoofdtekst toe met de module JSON > JSON maken

Met de module Create JSON kunt u het opgeven van JSON eenvoudiger maken. U kunt hiermee ook dynamisch waarden definiëren.

Voor meer informatie over de modules JSON, zie [&#x200B; modules JSON &#x200B;](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/json-modules.md).

1. Voer de waarden in waarvan u JSON wilt maken of wijs deze toe.

   ![&#x200B; JSON waarden &#x200B;](/help/workfront-fusion/create-scenarios/connect-to-apps/assets/json-values-350x288.png)

1. Sluit de JSON > JSON-module maken aan op HTTP > Een aanvraag maken.
1. Wijs de JSON-tekenreeks van de module Create JSON toe aan het veld Request-inhoud in HTTP > Een aanvraag maken.

Wanneer u het scenario uitvoert, wordt het pushbericht verzonden naar het apparaat dat is geregistreerd in uw Pushover-account.
