---
title: Adobe Experience Manager Forms-modules
description: Met de  [!DNL Adobe Experience Manager Forms]  schakelaar voor  [!DNL Adobe Workfront Fusion], you can start a scenario based on events in your [!DNL Adobe Experience Manager Forms]  rekening, creeer, upload, en werk activa bij, en kopieer of verplaats omslagen en activa.
author: Becky
feature: Workfront Fusion, Digital Content and Documents
exl-id: e0d7a655-1353-4d24-83d4-7da73d859a63
source-git-commit: 4f97980dce7c8df47ab73d51537d4700ac34dedf
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# [!DNL Adobe Experience Manager Forms] modules

Met de [!DNL Adobe Experience Manager Forms] -connector voor [!DNL Adobe Workfront Fusion] kunt u een scenario starten op basis van gebeurtenissen in uw [!DNL Adobe Experience Manager Forms] -account door een webhaak te maken.

U kunt een formulier binnen [!DNL Adobe Experience Manager Forms] configureren om formulierverzendingen naar deze website te verzenden.

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] plan*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor een oudere licentie: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en -integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het abonnement [!UICONTROL Select] of [!UICONTROL Prime] [!DNL Adobe Workfront] hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] is opgenomen in het abonnement [!UICONTROL Ultimate] [!DNL Workfront] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

* U moet een [!DNL Adobe Experience Manager Forms] -account hebben om deze module te kunnen gebruiken.

## Adobe Experience Manager Assets API-informatie

De Adobe Experience Manager Assets-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.2.27</td> 
  </tr>
 </tbody> 
 </table>

## Verbinding maken met Adobe Experience Manager Forms

Verbinding maken voor uw [!DNL Adobe Experience Manager Forms] -modules:

1. In om het even welke module, voegt de klik **[!UICONTROL toe]** naast het vakje van de Verbinding.

1. Vul de volgende velden in:

   <table style="table-layout:auto"> 
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column1">
    </col>
    <col class="TableStyle-TableStyle-List-options-in-steps-Column-Column2">
    </col>
    <tbody>
      <tr>
        <td role="rowheader">[!UICONTROL Connection name]</td>
        <td>
          <p>Voer een naam in voor deze verbinding.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-omgeving]</td>
        <td>
          <p>Selecteer of deze verbinding met een Productie- of niet-productieomgeving verbindt.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-type]</td>
        <td>
          <p>Selecteer of deze account een serviceaccount of een persoonlijke account is.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Instance URL zonder een sluitslash]</td>
        <td>
          <p>Voer de URL in die u gebruikt om het account te openen, zonder de laatste schuine streep.</p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL IMS-eindpunt]</td>
        <td>
          <p><code>https://ims-na1.adobelogin.com</code></p>
        </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client ID]</td>
        <td>Voer uw [!DNL Adobe] client-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Client Secret]</td>
        <td>Voer uw [!DNL Adobe] clientgeheim in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-organisatie-ID]</td>
        <td>Voer uw [!DNL Adobe] Organisatie-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Technical account ID]</td>
        <td>Voer uw [!DNL Adobe] technische account-id in. Dit vindt u in de sectie [!UICONTROL Credentials details] van de [!DNL Adobe Developer Console] .
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL-metagegevensbereiken]</td>
        <td>Voer een geschikt metabereik in       </td>
      </tr>
      <tr>
        <td role="rowheader">[!UICONTROL Persoonlijke sleutel]</td>
        <td>
          <p>Voer de persoonlijke sleutel in die is gegenereerd toen uw referenties werden gemaakt in de [!DNL Adobe Developer Console] . </p>
          <p>Uw persoonlijke sleutel of certificaat uitnemen:</p>
          <ol>
            <li value="1">
              <p>Klik <b> [!UICONTROL Extraheren] </b>.</p>
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
              <p>Klik <b> [!UICONTROL sparen] </b> om het dossier uit te halen en aan de verbindingsopstelling terug te keren.</p>
            </li>
          </ol>
        </td>
      </tr>
    </tbody>
    </table>

1. Klik **[!UICONTROL verdergaan]** om de verbinding te bewaren en aan de module terug te keren.

## Adobe Experience Manager Forms-module en de bijbehorende velden

Er is momenteel slechts één module in de Adobe Experience Manager Forms-connector.

### Controleren op formuliergebeurtenissen

Met deze instant trigger (webhaak) kunt u een scenario starten wanneer een handeling Verzenden plaatsvindt op een Adobe Experience Manager-formulier.

>[!IMPORTANT]
>
>Voor deze module is ook configuratie in Adobe Experience Manager vereist. Nadat u deze webhaak hebt ingesteld, moet u Adobe Experience Manager openen en het formulier configureren om verzendingen naar de webhaak te verzenden.
>
><!--For instructions on the required form configuration, see insert url here-->

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL Webhaak naam]</td> 
   <td> <p>Geef een naam op voor de webhaak</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL-verbinding]</td> 
   <td> <p>Zie <a href="/help/workfront-fusion/references/apps-and-modules/adobe-connectors/aem-forms-modules.md#create-a-connection-to-adobe-experience-manager-forms" class="MCXref xref"> Verbinding maken met [!DNL Adobe Experience Manager Forms]</a> voor instructies over het verbinden van uw [!DNL Adobe Experience Manager] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr>

De module maakt een webhaak en geeft u het adres van de webhaak, dat u kunt invoeren in het dialoogvenster voor het verzenden van formulieren in [!DNL Adobe Experience Manager Forms] .
