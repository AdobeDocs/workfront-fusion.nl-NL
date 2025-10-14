---
title: HTTP > Overige modules
description: De Adobe Workfront Fusion HTTP-toepassing biedt verschillende modules voor communicatie op basis van het HTTP-protocol (Hypertext Transfer Protocol). HTTP is de stichting van gegevensmededeling voor het World Wide Web. U kunt de modules gebruiken om Web-pagina's en dossiers te downloaden, Web-haken en API eindpunten te roepen, etc.
author: Becky
feature: Workfront Fusion
exl-id: 7db97e6e-262d-4be2-823b-423f56a7d886
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# HTTP > Overige modules

De Adobe Workfront Fusion [!UICONTROL HTTP] -app biedt verschillende modules voor communicatie op basis van het HTTP-protocol (Hypertext Transfer Protocol). HTTP is de stichting van gegevensmededeling voor het World Wide Web. U kunt de modules gebruiken om Web-pagina&#39;s en dossiers te downloaden, Web-haken en API eindpunten te roepen, etc.

De juiste keuze van de module is afhankelijk van het verificatie-/verificatiemechanisme waartoe de bron waartoe u toegang wilt hebben, behoort. Hieronder volgen voorbeelden van modules

* **doe een verzoek**: Primair bedoeld voor middelen die geen type van authentificatie of vergunning gebruiken
* **maak een Basis verzoek van de Auth**: Voor middelen die [!DNL HTTP] Basisauthentificatie (BA) gebruiken
* **maak een OAuth 2.0 verzoek**: Voor middelen die het OAuth 2.0 vergunningsprotocol gebruiken
* **maak een verzoek van de Auteur van het Certificaat van de Cliënt**: Voor middelen die vergunningsprotocol gebruiken dat een cliënt-zijcertificaat vereist
* **maak een API Zeer belangrijke vergunningsverzoek**: Voor middelen die API Sleutels voor vergunning gebruiken

>[!NOTE]
>
>Als u verbinding maakt met een Adobe-product dat momenteel geen speciale aansluiting heeft, raden we u aan de Adobe Authenticator-module te gebruiken.
>
>Voor meer informatie, zie [&#x200B; module van Adobe Authenticator &#x200B;](/help/workfront-fusion/references/apps-and-modules/adobe-connectors/adobe-authenticator-modules.md).

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
   <td role="rowheader">[!UICONTROL Evaluate all states as errors (except for 2xx and 3xx )] </td> 
   <td> <p>Gebruik deze optie om foutafhandeling in te stellen.</p> <p>Voor meer informatie, zie <a href="/help/workfront-fusion/create-scenarios/config-error-handling/error-handling.md" class="MCXref xref"> de behandeling van de Fout in de Fusie van Adobe Workfront </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL URL] </td> 
   <td> <p>Voer de URL in van het bestand dat u wilt downloaden of wijs deze toe. </p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Share cookies with other HTTP modules] </td> 
   <td> <p>Schakel deze optie in als u de cookies voor deze site beschikbaar wilt maken voor andere modules. </p> </td> 
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

![&#x200B; kopbal JWT &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/jwt-header-350x19.png)

Code voor kopiëren en plakken:

```
{{replace(replace(replace(base64("{""alg"":""HS256"",""typ"":""JWT""}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Payload:

![&#x200B; JWT nuttige lading &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/jwt-payload-350x17.png)

Code voor kopiëren en plakken:

```
{{replace(replace(replace(base64("{""iss"":""key"",""exp"":" + (timestamp + 60) + "}"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```

Token:

![&#x200B; het teken van JWT &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/jwt-token-350x15.png)

Code voor kopiëren en plakken:

```
{{1.value}}.{{2.value}}.{{replace(replace(replace(sha256(1.value + "." + 2.value; "base64"; "secret"); "/=/g"; emptystring); "/\+/g"; "-"); "/\//g"; "_")}}
```
