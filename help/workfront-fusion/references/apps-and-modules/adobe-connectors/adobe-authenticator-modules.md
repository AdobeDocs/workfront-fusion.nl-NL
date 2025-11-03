---
title: Adobe Authenticator-module
description: Met de Adobe Authenticator-module kunt u via één verbinding verbinding verbinding maken met elk Adobe-product met een API.
author: Becky
feature: Workfront Fusion
exl-id: af4da661-eeee-4033-a2bb-a2196e446a3d
source-git-commit: 1929bf897e9263ec551e93df776b96f419436715
workflow-type: tm+mt
source-wordcount: '1121'
ht-degree: 1%

---

# Adobe Authenticator-modules

Met de Adobe Authenticator-module kunt u verbinding maken met elke Adobe API via één verbinding. Hierdoor kunt u gemakkelijker verbinding maken met Adobe-producten die nog geen speciale Fusion-connector hebben.

Het voordeel ten opzichte van de HTTP-modules is dat u een verbinding kunt maken, zoals in een specifieke app.

Om een lijst van beschikbare Adobe APIs te zien, zie [ Adobe APIs ](https://developer.adobe.com/apis). U kunt mogelijk alleen de API&#39;s gebruiken waaraan u bent toegewezen.

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

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Vereisten

* U moet toegang hebben tot het Adobe-product waarmee u verbinding wilt maken.
* U moet toegang hebben tot de Adobe Developer Console.
* U moet een project op de Adobe Developer Console hebben dat API omvat die u de module wilt verbinden met. U kunt:

   * Maak een nieuw project met de API.

     of
   * Voeg API aan een bestaand project toe.

  Voor informatie bij het creëren van of het toevoegen van API aan een project op Adobe Developer Console, zie [ een project ](https://developer.adobe.com/dep/guides/dev-console/create-project/) in de documentatie van Adobe creëren.

## Adobe Authenticator API-informatie

De Adobe Authenticator-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.1.4</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken

Een Adobe Authenticator-verbinding maakt verbinding met één project op de Adobe Developer Console. Als u dezelfde verbinding voor meerdere Adobe API wilt gebruiken, voegt u de API&#39;s toe aan hetzelfde project en maakt u een verbinding met dat project.

U kunt afzonderlijke verbindingen aan afzonderlijke projecten tot stand brengen, maar u kunt geen verbinding gebruiken om tot API toegang te hebben die niet op het project is dat in die verbinding wordt gespecificeerd.

>[!IMPORTANT]
>
>Met de Adobe Authenticator-connector hebt u de keuze tussen het maken van een OAuth Server-to-server verbinding of een Service Account (JWT)-verbinding. Adobe heeft JWT-referenties vervangen. Deze zullen vanaf 1 januari 2025 niet meer werken. **daarom, adviseren wij hoogst creërend Verbindingen OAuth.**
>
>Voor meer informatie over deze soorten verbindingen, zie [ Server aan de authentificatie van de Server ](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/) in de documentatie van Adobe

Een verbinding maken:

1. In om het even welke module van Adobe Authenticator, voegt de klik **naast het gebied van de Verbinding toe.**
1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection type]</td>
        <td>
          <p>Selecteer of u een Server-aan-Server verbinding OAuth, of een verbinding van de de dienstrekening (JWT) wilt tot stand brengen. We raden u aan OAuth-verbindingen te maken.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!DNL Adobe] client-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] clientgeheim in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Scopes]</td>
        <td>Als u een OAuth-verbinding hebt geselecteerd, voert u het bereik in dat nodig is voor deze verbinding.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Als u een JWT-verbinding hebt geselecteerd, voert u uw [!DNL Adobe] technische account-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Organization ID]</td>
        <td>Als u een JWT-verbinding hebt geselecteerd, voert u uw [!DNL Adobe] Organisatie-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Meta Scopes]</td>
        <td>Als u een JWT-verbinding hebt geselecteerd, voert u het metabereik in dat nodig is voor deze verbinding. </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Private key]</td>
        <td>
          <p>Als u een JWT-verbinding hebt geselecteerd, voert u de persoonlijke sleutel in die is gegenereerd toen uw referenties werden gemaakt in de [!DNL Adobe Developer Console] . </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li value="1">
              <p>Klik op <b>[!UICONTROL Extract]</b>.</p>
            </li>
            <li value="2">
              <p>Selecteer het type bestand dat u extraheert.</p>
            </li>
            <li value="3">
              <p>Selecteer het bestand dat de persoonlijke sleutel of het certificaat bevat.</p>
            </li>
            <li value="4">
              <p>Voer het wachtwoord voor het bestand in.</p>
            </li>
            <li value="5">
              <p>Klik op <b>[!UICONTROL Save]</b> om het bestand uit te pakken en terug te keren naar de verbindingsinstelling.</p>
            </li>
          </ol>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Base URLs]</td>
        <td>U moet de basis-URL's toevoegen die door deze authenticator worden toegestaan. Wanneer u later in het scenario de aanroepmodule Een aangepaste API maken gebruikt, voegt u een relatief pad naar de gekozen URL toe. Door hier URLs in te gaan, kunt u controleren wat het Merk een douane API vraagmodule kan verbinden, die veiligheid verhoogt.<p>Voor elke basisURL die u aan authentiek wilt toevoegen, <b> toevoegen punt </b> klikt en de basis URL ingaan.</td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Authentication URL]</td>
        <td>Laat dit leeg als u de standaard Adobe IMS-verificatie-URL van <code>https://ims-na1.adobelogin.com</code> wilt gebruiken. Als u Adobe IMS niet gebruikt voor verificatie, voert u de URL in die u wilt gebruiken voor verificatie.</td>
      </tr>
    </tbody>
    </table>

1. Klik op **[!UICONTROL Continue]** om de verbinding op te slaan en terug te keren naar de module.

## Modules

* [Een aangepaste API-aanroep maken](#make-a-custom-api-call)
* [Een aangepaste API-aanroep maken (verouderd)](#make-a-custom-api-call-legacy)

### Een aangepaste API-aanroep maken

Met deze actiemodule kunt u een aanroep naar elke Adobe API maken. Het ondersteunt grote bestanden in plaats van tekst als enige hoofdtekst.

Deze module is beschikbaar gesteld op 14 november 2024. Elke Adobe Authenticator > Aangepaste API-aanroep die vóór deze datum is geconfigureerd, verwerkt geen grote bestanden en wordt nu beschouwd als de module Aangepaste API-aanroep (verouderd) maken.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Voor instructies bij het creëren van een verbinding aan de module van Adobe Authenticator, zie <a href="#create-a-connection" class="MCXref xref" > een verbinding </a> in dit artikel creëren.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Voer de basis-URL in van het API-punt waarmee u verbinding wilt maken.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Voer het pad in ten opzichte van de basis-URL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body Type]</td>
   <td> Selecteer het hoofdtype voor deze API-aanvraag:
   <ul>
   <li>Ruw</li>
   <li>application/x-www-form-urlencoded</li>
   <li>multipart/form-data</li>
   </ul>
      </td>
      </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Output Type]  </td>
      <td>
        <p>Selecteer het type gegevens dat de module moet uitvoeren. Als u geen type selecteert, selecteert de module automatisch een type.</p>
      </td>
    </tr>
  </tbody>
</table>

### Een aangepaste API-aanroep maken (verouderd)

Met deze actiemodule kunt u een aanroep naar elke Adobe API maken.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
     <td role="rowheader">[!UICONTROL Connection]</td>
     <td>Voor instructies bij het creëren van een verbinding aan de module van Adobe Authenticator, zie <a href="#create-a-connection" class="MCXref xref" > een verbinding </a> in dit artikel creëren.</td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Base URL]</p>
      </td>
      <td>
        <p>Voer de basis-URL in van het API-punt waarmee u verbinding wilt maken.</p>
      </td>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL URL]</p>
      </td>
      <td>
        <p>Voer het pad in ten opzichte van de basis-URL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
   <td> <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders toe.</p>
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
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"></p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
