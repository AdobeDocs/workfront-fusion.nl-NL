---
title: HTTP&gt; Overige modules
description: De  [!DNL Adobe Workfront Fusion]  app van HTTP verstrekt diverse modules voor mededeling die op het protocol van de Overdracht van de Hypertext (HTTP) wordt gebaseerd. HTTP is de stichting van gegevensmededeling voor het World Wide Web. U kunt de modules gebruiken om Web-pagina's en dossiers te downloaden, Web-haken en API eindpunten te roepen, etc.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: 6398261775584e33515c546de4e7a72d5830ebe0
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# HTTP > Overige modules

>[!NOTE]
>
>[!UICONTROL Adobe Workfront Fusion] vereist een [!UICONTROL Adobe Workfront Fusion] licentie naast een [!UICONTROL Adobe Workfront] licentie.

De app [!DNL Adobe Workfront Fusion] [!UICONTROL HTTP] biedt verschillende modules voor communicatie op basis van het HTTP-protocol (Hypertext Transfer Protocol). HTTP is de stichting van gegevensmededeling voor het World Wide Web. U kunt de modules gebruiken om Web-pagina&#39;s en dossiers te downloaden, Web-haken en API eindpunten te roepen, etc.

De juiste keuze van de module is afhankelijk van het verificatie-/verificatiemechanisme waartoe de bron waartoe u toegang wilt hebben, behoort. Hieronder volgen voorbeelden van modules

* Voer een verzoek in:universele module hoofdzakelijk bedoeld voor middelen die geen enkele vorm van authentificatie/vergunning gebruiken
* Voer een Basic Auth-verzoek uit:voor bronnen die gebruikmaken van [!DNL HTTP] Basic authentication (BA)
* Maak een OAuth 2.0 verzoek: voor middelen die OAuth 2.0 vergunningsprotocol gebruiken
* Maak een verzoek van de Auteur van het Certificaat van de Cliënt: voor middelen die vergunningsprotocol gebruiken dat een cliënt-zijcertificaat vereist.
* Maak een aanvraag voor een API-sleutelautorisatie: voor bronnen die API-sleutels gebruiken voor autorisatie.

>[!NOTE]
>
>Als u verbinding maakt met een product van de Adobe dat momenteel geen speciale aansluiting heeft, raden we u aan de Adobe Authenticator-module te gebruiken.
>
>Voor meer informatie, zie [ module van Adobe Authenticator ](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

## Aanvraagmodules

Zie de volgende artikelen voor specifieke instructies van de verzoekmodule:

* [[!UICONTROL HTTP] > [!UICONTROL Make a request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Basic Authorization request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-basic-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an OAuth 2.0 request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-oauth-2-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make a Client Certificate Authorization request] module](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-a-client-cert-auth-request.md)
* [[!UICONTROL HTTP] > [!UICONTROL Make an API Key Authorization request]](/help/workfront-fusion/references/apps-and-modules/universal-connectors/http-module-make-an-api-key-auth-request.md)

## Overige actiemodules

* [[!UICONTROL Get a File]](#get-a-file)
* [[!UICONTROL Resolve a target URL]](#resolve-a-target-url)

### [!UICONTROL Get a File]

Deze actiemodule downloadt een bestand van de opgegeven URL. Nadat het bestand is gedownload, kunt u het bestand verder verwerken (de bestandsgegevens toewijzen) met behulp van andere modules in het scenario.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Voer de URL in van het bestand dat u wilt downloaden of wijs deze toe. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Resolve a target URL]

Deze actiemodule verhelpt een keten van HTTP-omleidingen en retourneert een doel-URL.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Voer de URL die u wilt omzetten in of wijs deze toe, bijvoorbeeld een [!DNL bit.ly] URL.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Method] </td> 
   <td> <p>Selecteer of u de methode [!UICONTROL HEAD] of [!UICONTROL GET] wilt gebruiken.</p> </td> 
  </tr> 
 </tbody> 
</table>

## Iteratormodules

### [!UICONTROL Retrieve headers]

Deze module retourneert elke header (naam en waarde) van de opgegeven HTTP-module in een aparte bundel.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Source Module]</td> 
   <td> <p> Selecteer de module waarvan u kopteksten wilt terugwinnen.</p> </td> 
  </tr> 
 </tbody> 
</table>

## JSON-webtokens genereren (JWT)

Het is mogelijk om een token JWT te genereren met behulp van ingebouwde functies:

Koptekst:

![](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Code voor kopiëren en plakken:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload:

![](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Code voor kopiëren en plakken:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Code voor kopiëren en plakken:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
