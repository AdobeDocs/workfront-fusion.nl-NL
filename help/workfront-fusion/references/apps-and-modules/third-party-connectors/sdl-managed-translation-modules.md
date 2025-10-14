---
title: Door SDL beheerde vertaalmodules
description: In een Adobe Workfront Fusion-scenario kunt u uw SDL Managed Translation-account aansluiten op meerdere toepassingen en services van derden.
author: Becky
feature: Workfront Fusion
exl-id: 41953b04-9011-4ddb-9f53-cdf11e807e04
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# [!DNL SDL Managed Translation] modules

In een Adobe Workfront Fusion-scenario kunt u uw [!DNL SDL Managed Translation] -account verbinden met meerdere toepassingen en services van derden.

## Toegangsvereisten

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Adobe Workfront-abonnement*</td>
  <td> <p>[!UICONTROL Pro] of hoger</p> </td>
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie*</td>
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidige vergunningsvereiste: geen Workfront Fusion-vergunningsvereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL Workfront Fusion for Work Automation and Integration] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het [!UICONTROL Select] - of [!UICONTROL Prime] Adobe Workfront-abonnement hebt, moet uw organisatie zowel Adobe Workfront Fusion als Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. Workfront Fusion is opgenomen in het Workfront-plan van [!UICONTROL Ultimate] .</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet Adobe Workfront Fusion en Adobe Workfront aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met uw Workfront-beheerder om te weten te komen welk plan, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

## Informatie over SDL Managed Translation API

De SDL Managed Translation-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td>https://languagecloud.sdl.com</td> 
  </tr>
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.4.26</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL SDL Managed Translation] Modules

>[!NOTE]
>
>De verrichtingstijdout voor vraag aan [!DNL SDL Managed Translation] is **120 seconden**.

### Bestanden

#### [!UICONTROL Download Translated File]

Deze module wint de inhoud van één enkel vertaald dossier, binnen het gespecificeerde project terug. Als het gewenste bestand nog niet de status Downland heeft, is het mogelijk dat de inhoud van het bestand nog niet volledig is vertaald. Als het bestand de status Downloaden heeft en u hebt het opgehaald, moet u controleren of het bestand is voltooid met de methode `Cancel or Complete File` .

#### [!UICONTROL Upload a File]

Deze module staat uploads van dossiers voor vertaling of voor opneming in een vertaalproject als verwijzingsmateriaal toe. Uploads moeten worden verzonden met behulp van multipart/form-data en kunnen meerdere bestanden bevatten. U geeft de `ProjectOptionId` op die moet worden gebruikt om het geüploade bestand of de bestanden te evalueren. Hiermee bepaalt u of elk bestand dat u uploadt, mogelijk kan worden omgezet of als referentiemateriaal moet worden verwerkt. In het geval van archieven (`zip `, `rar`, `7z`, `tar` dossiers) onderzoekt app de inhoud van het archief en wijst erop of het archief als geheel kan worden vertaald, of het een mengeling van vertaalbare en niet-vertaalbare dossiers bevat.

>[!NOTE]
>
>Het uploaden van meerdere bestanden tegelijk wordt afgeraden, omdat dit de impact van een fout kan vergroten.

#### [!UICONTROL Add a Reference File]

Deze module voegt een referentiebestand toe.

### Projecten

#### [!UICONTROL Create a project]

Deze module leidt tot het gespecificeerde project.

#### Een project annuleren of voltooien

Deze module annuleert of voltooit het gespecificeerde project. Als het project op download wacht, overgaat het project door om het even welke definitieve stappen in het werkschema, en uiteindelijk beweegt zich om te voltooien. Als het project op goedkeuring wacht of de selectie van de leverancier wordt geannuleerd. Als het project op een andere status is, zal het verzoek ontbreken.

#### [!UICONTROL Download Project Zip]

Deze module krijgt het `zip` dossier van vertaalde dossiers voor het gespecificeerde project.

#### [!UICONTROL Read a Project]

Deze module krijgt het gespecificeerde project.

#### [!UICONTROL Get Projects at Status]

Deze module krijgt alle beschikbare projecten in de gespecificeerde status. Met deze methode kunnen de resultaten worden gepagineerd door parameters voor `$top` , `$skip` en `$orderby` query op te geven.

#### [!UICONTROL Get Projects List]

Haalt een eenvoudige lijst op van alle projecten, die algemene informatie over elk project verstrekken. Met deze methode kunnen de resultaten pagina&#39;s zijn, door de parameters `$top` , `$skip` en `$orderby` query op te geven.

#### [!UICONTROL Search Project Creation Options]

Deze module krijgt de Opties van de Making van het Project.

### Overige

#### [!UICONTROL Make an API Call]

Deze module voert een willekeurige geautoriseerde API-aanroep uit.
