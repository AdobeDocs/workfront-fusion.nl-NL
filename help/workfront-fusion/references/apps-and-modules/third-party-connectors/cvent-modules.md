---
title: Cilummodules
description: In een  [!DNL Adobe Workfront Fusion]  scenario, kunt u werkschema's automatiseren die Cvent gebruiken, evenals het met veelvoudige derdetoepassingen en de diensten verbinden.
author: Becky
feature: Workfront Fusion
exl-id: b7e16180-1db8-4aff-bb7b-69ca98194b00
source-git-commit: 1ea2bf76b0fe6e0b0c7c3c894fbdede224d2cae2
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 0%

---

# [!DNL Cvent] modules

In een [!DNL Adobe Workfront Fusion] -scenario kunt u workflows automatiseren die [!DNL Cvent] gebruiken en deze koppelen aan meerdere toepassingen en services van derden.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md).

Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

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
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] [!DNL Adobe Workfront] -abonnement hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Vereisten

Als u [!DNL Cvent] -modules wilt gebruiken, moet u een [!DNL Cvent] -account hebben.

## API-gegevens verzamelen

De aansluiting Cvent gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> V200611.ASMX </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.7.14</td> 
  </tr>
 </tbody> 
 </table>

## Verbinden [!DNL Cvent] met [!DNL Adobe Workfront Fusion] {#connect-cvent-to-adobe-workfront-fusion}

>[!NOTE]
>
>De [!DNL Cvent] -modules gebruiken een [!UICONTROL SOAP] API. Als u een verbinding met [!DNL Cvent] wilt maken, moet u het volgende controleren:
>
>* U hebt [!UICONTROL SOAP] toegang tot de [!DNL Cvent] API.
>* De [!DNL Workfront Fusion] IP adressen zijn toegevoegd aan de lijst van gewenste personen van uw organisatie.
>
>  Voor een lijst van [!DNL Workfront Fusion] IP adressen, zie [ IP Adressen voor Fusie in de lijst van gewenste personen van uw organisatie ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/set-up-and-manage-orgs-and-teams/set-up-orgs-teams-and-users/set-up-ip-addresses-for-fusion.md) vormen


U kunt rechtstreeks vanuit een [!DNL Cvent] -module verbinding maken met uw [!DNL Cvent] -account.

1. Klik in een willekeurige [!DNL Cvent] -module op **[!UICONTROL Add]** naast het [!UICONTROL Connection] -veld.
1. Selecteer het gebied waarmee u verbinding wilt maken.

   * [!UICONTROL North America]
   * [!UICONTROL Europe]
   * [!UICONTROL Sandbox]

1. Klik op **[!UICONTROL Continue]** om de verbinding te maken en terug te gaan naar de module.

## [!DNL Cvent] modules en hun velden

Wanneer u [!DNL Cvent] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!DNL Cvent] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Handelingen](#actions)
* [Zoekopdrachten](#searches)

### Handelingen

* [[!UICONTROL Custom API Call]](#create-meeting-request)
* [[!UICONTROL Read a record]](#read-a-record)
* [[!UICONTROL Register Invitee]](#register-invitee)
* [[!UICONTROL Add Invitee]](#add-invitee)
* [[!UICONTROL Delete Contact]](#delete-contact)
* [[!UICONTROL Update Contact]](#update-contact)
* [[!UICONTROL Create meeting request]](#create-meeting-request)

#### [!UICONTROL Custom API Call]

Met deze actiemodule kunt u een aangepaste, geverifieerde aanroep van de [!DNL Cvent] API maken. Op deze manier kunt u een automatisering van de gegevensstroom maken die niet door de andere [!DNL Cvent] -modules kan worden uitgevoerd.

Als u deze module configureert, worden de volgende velden weergegeven.

De module keert een statuscode, samen met de kopballen en het lichaam van de API vraag terug.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Bewerking</td> 
   td&gt; <p>Selecteer de HTTP- verzoekmethode u de API vraag moet vormen. Voor meer informatie, zie <a href="/help/workfront-fusion/references/modules/http-request-methods.md" class="MCXref xref" data-mc-variable-override=""> HTTP- verzoekmethodes </a>.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Hoofdtekst (XML)</td> 
   <td> <p>Ga of kaart het lichaam van de API vraag in. Dit mag alleen de XML bevatten. De module zal automatisch authentificatiekopballen omvatten. </p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Read a record]

Deze actiemodule leest informatie over een specifieke record.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td>Selecteer het itemtype van de record die u wilt lezen.</td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact] / [!UICONTROL Event] / [!UICONTROL Invitee ID]</td> 
   <td> <p>Voer de id in van het item dat u wilt lezen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Outputs]</td> 
   <td> <p>Selecteer de velden die u in de uitvoer van de module wilt opnemen. De velden zijn beschikbaar op basis van het geselecteerde itemtype.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Register Invitee]

In deze actiemodule wordt een genodigde voor een gebeurtenis geregistreerd.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>Id genodigde</p> </td> 
   <td> <p>Voer de id in van de genodigde die u voor een gebeurtenis wilt registreren of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Gebeurtenis-id</td> 
   <td> <p>Voer de id in van de gebeurtenis waarvoor u de genodigde wilt registreren of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Add Invitee]

Deze actiemodule nodigt een contactpersoon voor een gebeurtenis uit.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Voer de id in van de contactpersoon die u aan een gebeurtenis wilt toevoegen of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Voer de id in van de gebeurtenis waaraan u de contactpersoon wilt toevoegen of wijs deze toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Delete Contact]

Deze actiemodule schrapt één enkel contact in Gebeurtenis.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Contact ID]</td> 
   <td> <p>Ga of kaart identiteitskaart van het contact in u wilt schrappen.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Update Contact]

Deze actiemodule werkt een bestaand contact bij gebruikend zijn identiteitskaart

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Contact ID]</p> </td> 
   <td> <p>Ga of kaart identiteitskaart van het contact in u wilt bijwerken.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Fields]</td> 
   <td> <p>Selecteer de velden waarvoor u informatie wilt invoeren en vul vervolgens de gewenste waarden voor die velden in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Custom fields]</td> 
   <td> <p>Selecteer de velden waarvoor u informatie wilt invoeren en vul vervolgens de gewenste waarden voor die velden in.</p> </td> 
  </tr> 
 </tbody> 
</table>

#### [!UICONTROL Create meeting request]

Met deze actiemodule voegt u een verzoek voor een vergadering toe aan uw account.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Form ID]</p> </td> 
   <td> <p>Voer de id in van het formulier dat u wilt gebruiken om de nieuwe vergaderingsaanvraag te maken of wijs deze toe.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Meeting Request Fields]</td> 
   <td> <p>Selecteer de velden voor vergaderingsverzoeken waarvoor u informatie wilt invoeren en vul vervolgens de gewenste waarden voor die velden in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event Request Fields]</td> 
   <td> <p>Selecteer de velden met gebeurtenisaanvragen waarvoor u informatie wilt invoeren en vul vervolgens de gewenste waarden voor die velden in.</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL RFP Request Fields]</td> 
   <td> <p>Selecteer het verzoek om voorstellen gebieden die u informatie voor, dan de gewenste waarden voor die gebieden wilt invoeren.</p> </td> 
  </tr> 
 </tbody> 
</table>

### Zoekopdrachten

#### [!UICONTROL List records]

Deze onderzoeksmodule wint informatie over alle verslagen van een specifiek type terug.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Connection]</p> </td> 
   <td> <p>Zie <a href="#connect-cvent-to-adobe-workfront-fusion" class="MCXref xref"> Verbinding maken [!DNL Cvent] met [!DNL Adobe Workfront Fusion]</a> in dit artikel voor instructies over het verbinden van uw [!DNL Cvent] -account met [!DNL Workfront Fusion] .</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader"> <p>[!UICONTROL Record type]</p> </td> 
   <td> <p>Selecteer het type record dat u wilt weergeven.</p> 
    <ul> 
     <li> <p>Alle gebeurtenissen van uw [!DNL Cvent] -account</p> </li> 
     <li> <p>Alle sessies voor een gebeurtenis</p> </li> 
     <li> <p>Alle genodigden voor een gebeurtenis</p> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Event ID]</td> 
   <td> <p>Als u genodigden of sessies opsomt, voert u de id in of wijst u deze toe aan de gebeurtenis waaraan deze genodigden of sessies zijn gekoppeld.</p> </td> 
  </tr> 
 </tbody> 
</table>
