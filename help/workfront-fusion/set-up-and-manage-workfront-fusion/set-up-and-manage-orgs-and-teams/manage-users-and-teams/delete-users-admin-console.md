---
content-type: reference
title: 'Organisaties en teams instellen en beheren: artikelindex'
description: Deze sectie bevat artikelen over het instellen en beheren van organisaties en teams in Adobe Workfront Fusion.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: aa570f28-7387-47c5-9968-e3554921b0f5
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Gebruikers verwijderen via de [!DNL Adobe Admin Console]

U kunt een gebruiker alleen uit Adobe Workfront Fusion verwijderen en toegang tot andere [!DNL Adobe] -productprofielen behouden. U kunt de gebruiker ook volledig uit [!DNL Adobe Admin Console] verwijderen.

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
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront-abonnement: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een [!DNL Adobe Admin Console] beheerder voor uw organisatie zijn.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Een gebruiker alleen uit Adobe Workfront Fusion verwijderen

U kunt een gebruiker uit Workfront Fusion verwijderen terwijl de andere Adobe-productmachtigingen intact blijven.

Voor instructies, zie &quot;verwijder gebruikers en gebruikersgroepen uit een product&quot;in artikel [ producten op Admin Console ](https://helpx.adobe.com/nl/enterprise/using/manage-products.html) leiden.

## Een gebruiker deactiveren in alle producten in de [!DNL Adobe Admin Console]

Als u een gebruiker wilt verwijderen, moet u de gebruiker deactiveren via de [!DNL Adobe Admin Console] .

Een gebruiker wordt gedeactiveerd vanuit [!DNL Adobe Admin Console] wanneer een van de volgende situaties van toepassing is:

* De gebruiker wordt uit een product of productprofiel verplaatst en wordt niet toegewezen aan een ander product of productprofiel.
* De gebruiker wordt verwijderd uit een groep die is gekoppeld aan een productprofiel en die niet is opgenomen in een andere groep die is gekoppeld aan een productprofiel.
* De gebruiker wordt verwijderd uit een productprofiel en niet toegewezen aan een ander productprofiel.
* De gebruiker wordt verwijderd of gedeactiveerd in de organisatie die Workfront Fusion bevat.

  Voor instructies, zie de sectie &quot;verwijder gebruikers&quot;in [ individuele gebruikers beheren ](https://helpx.adobe.com/nl/enterprise/using/manage-users-individually.html).

In Workfront Fusion heeft de deactivering op een van de volgende manieren invloed op de gebruiker:

* Als de gebruiker zich in slechts één organisatie bevindt, wordt de gebruiker gedeactiveerd.
* Als de gebruiker in meer dan één organisatie is, wordt de gebruiker verwijderd uit de organisatie waarin de gebruiker op [!DNL Adobe Admin Console] werd gewijzigd.
* Houd rekening met het volgende wanneer u een gebruiker verwijdert.

### Overwegingen bij het verwijderen van een gebruiker in Workfront Fusion

Houd rekening met het volgende wanneer u een gebruiker verwijdert.

* Wanneer een gebruiker wordt verwijderd, worden de verbindingen, toetsen en webhaken van de gebruiker verwijderd.
* Alle scenario&#39;s die bij de gebruiker horen, worden overgedragen aan de eigenaar van de organisatie. De verbindingen in deze scenario&#39;s moeten worden bijgewerkt, omdat de verbindingen die tot de gebruiker behoren niet meer geldig zijn.
* Als de verwijderde gebruiker eigenaar is van toepassingen of openbare sjablonen, worden de toepassingen of openbare sjablonen overgebracht naar de eigenaar van de organisatie. Als er geen organisatieeigenaar is, worden de toepassingen of openbare sjablonen overgebracht naar een andere gebruiker.
