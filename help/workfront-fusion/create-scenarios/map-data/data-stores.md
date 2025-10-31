---
title: Gegevensopslag in Adobe Workfront Fusion
description: Een gegevensopslag, gelijkend op een gegevensbestand of een eenvoudige lijst, kan gegevens van scenario's opslaan, die het mogelijk maken om gegevens tussen individuele scenario's of scenario looppas over te brengen. U kunt een gegevensopslag gebruiken om nieuwe gegevens van diverse systemen tijdens synchronisatie op te slaan.
author: Becky
feature: Workfront Fusion
exl-id: 8bfa3201-45db-49d7-985d-9c324acd56b6
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '1245'
ht-degree: 0%

---

# Gegevensopslag maken en beheren

Een gegevensopslag, gelijkend op een gegevensbestand of een eenvoudige lijst, kan gegevens van scenario&#39;s opslaan, die het mogelijk maken om gegevens tussen individuele scenario&#39;s of scenario looppas over te brengen. U kunt een gegevensopslag gebruiken om nieuwe gegevens van diverse systemen tijdens synchronisatie op te slaan.

Met de gegevensopslagmodules kunt u de volgende handelingen uitvoeren op records in uw Adobe Workfront Fusion-gegevensarchief:

* Toevoegen
* Vervangen
* Bijwerken
* Ophalen
* Verwijderen
* Zoeken
* Aantal

Voor informatie bij het gebruiken van de modules van de gegevensopslag, zie [[!UICONTROL Data store] modules ](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/data-store-modules.md).

Ga voor een video-introductie over gegevensopslag in Workfront Fusion naar:

* [ de Opslag van Gegevens ](https://video.tv.adobe.com/v/3427029/){target=_blank}

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
   <td role="rowheader">Product</td> 
   <td>
   <p>Als uw organisatie een Select- of Prime Workfront-pakket heeft dat geen Workfront Automation and Integration bevat, moet uw organisatie Adobe Workfront Fusion aanschaffen.</li></ul>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Gegevensruimte beschikbaar

Als uw organisatie zich op het nieuwe het planmodel van Workfront (Uitgezochte, Prime, en de pakketten van Ultimate) bevindt, beïnvloedt het plan van uw organisatie de grootte en het aantal gegevensopslag beschikbaar uw instantie van Fusion.

### Ultimate-plan

Fusion-instanties op het Ultimate-pakket ontvangen:

* 100 MB aan ruimte
* 50 gegevensopslag

### Abonnementen selecteren en Prime

Fusion-instanties op de pakketten Select of Prime ontvangen :-->

* 100 MB voor de eerste 500K verrichtingen.

* 10 MB voor elke extra 100K-bewerking.

  Een organisatie met 600K-bewerkingen ontvangt bijvoorbeeld 110 MB.

Uw organisatie kan tot 50 gegevensopslag hebben. De gecombineerde grootte van deze gegevensopslag kan niet de totale grootte van de gegevensopslag van uw organisatie overschrijden.

## Een gegevenswinkel maken in Workfront Fusion

* [De gegevensopslag instellen](#set-up-the-data-store)
* [De gegevensstructuur instellen](#set-up-the-data-structure)

### De gegevensopslag instellen

Voordat u een gegevensopslag in een module kunt gebruiken, moet u de gegevensopslag in Workfront Fusion maken.

>[!NOTE]
>
>Uw organisatie heeft een beperkt aantal beschikbare gegevensopslagruimten. Als u probeert meer gegevensopslagruimte te maken dan beschikbaar is, wordt een [!UICONTROL Maximum stores reached] -fout geretourneerd.
>
>Voor meer informatie, zie [ Maximale opslag bereikte fout ](#maximum-stores-reached-error) in dit artikel.

1. Meld u aan bij uw Workfront Fusion-account.
1. Klik op **[!UICONTROL Data stores]** in het navigatievenster aan de linkerkant.
1. Klik op **[!UICONTROL Add data store]** in de rechterbovenhoek van het scherm.
1. Voer instellingen in voor de nieuwe gegevensopslag.

   Een bolvormige titel op een veld in een Workfront Fusion-module geeft een vereiste instelling aan.

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data store name] </td> 
      <td> <p>Voer een naam in voor de gegevensopslag. </p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Data Structure]</p> </td> 
      <td> <p>Een gegevensstructuur is een lijst van de kolommen voor een lijst. Deze lijst geeft de kolomnaam en het gegevenstype aan.</p> <p>Voer een van de volgende handelingen uit:</p> 
       <ul> 
        <li><b>Selecteer een gegevensstructuur die al is gemaakt</b></li> 
        <li><b> voeg een nieuwe gegevensstructuur </b> toe <p>Klik op <strong>[!UICONTROL Add]</strong> om een nieuwe gegevensstructuur te maken.</p> <p>Voor meer informatie, zie de <a href="#set-up-the-data-structure" class="MCXref xref"> Opstelling de sectie van de gegevensstructuur </a> in dit artikel.</p> </li> 
        <li style="font-weight: bold;"> <p>Het veld leeg laten</p> <p style="font-weight: normal;">Als u geen gegevensstructuur selecteert of toevoegt, zal het gegevensbestand slechts de primaire sleutel bevatten. Een dergelijk databasetype is handig als u alleen sleutels wilt opslaan en alleen wilt weten of een bepaalde sleutel al dan niet bestaat in de database.</p> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>Grootte gegevensopslag in MB</td> 
      <td> <p>Wijs de grootte voor de gegevensopslag toe vanuit uw totale interne gegevensopslag.</p> <p> De standaardwaarde is 10 MB. Als u minder dan 10 MB aan niet toegewezen ruimte van de Opslag van Gegevens van uw toewijzing 95 MB hebt, is de standaardgrootte de hoeveelheid niet toegewezen opslag.  <p>Opmerking: het gereserveerde bedrag kan op elk gewenst moment worden gewijzigd.</p>  </td> 
     </tr> 
    </tbody> 
   </table>

### De gegevensstructuur instellen

1. Klik op **[!UICONTROL Add]** wanneer u een gegevensopslag maakt of bewerkt.
1. Configureer de volgende velden in het vak **[!UICONTROL Add data structure]** dat wordt weergegeven:

   <table style="table-layout:auto">
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td>[!UICONTROL Data structure name]</td> 
      <td> <p> Voer een naam in voor de nieuwe gegevensstructuur.</p> </td> 
     </tr> 
     <tr> 
      <td> <p>[!UICONTROL Specification]</p> </td> 
      <td> <p>Voer een van de volgende handelingen uit om de kolommen in de gegevensopslagruimte in te stellen.</p> 
       <ul> 
        <li> <p>Klik op <strong>[!UICONTROL Add item]</strong> om handmatig de eigenschappen van één kolom op te geven.</p> <p>Voer de <strong>[!UICONTROL Name]</strong> en <strong>[!UICONTROL Type]</strong> in voor de kolom in de gegevensopslagruimte en definieer de corresponderende eigenschappen.</p> </li> 
        <li> <p>Klik op <strong>[!UICONTROL Generator]</strong> om de kolommen te bepalen uit de voorbeeldgegevens die u opgeeft.</p> 
         <div class="example" data-mc-autonum="<b>Example: </b>">
          <span class="autonumber"><span><b> Voorbeeld: </b></span></span> 
          <p>Met de volgende JSON-voorbeeldgegevens worden bijvoorbeeld drie kolommen gemaakt: naam, leeftijd en telefoonnummer. Telefoonnummer is een verzameling mobiele en vaste telefoonnummers.</p> 
          <p><code>&lbrace;</code> </p> 
          <p><code>"name":"John",</code> </p> 
          <p><code>"age":30,</code> </p> 
          <p><code>"phone number": &lbrace;</code> </p> 
          <p><code>"mobile":"987654321",</code> </p> 
          <p><code>"landline":"123456789"</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p><code>&rbrace;</code> </p> 
          <p>De lege kolommen in de mening van de gegevensopslag:</p> 
          <p> <img src="assets/empty-columns-350x132.png" style="width: 350;height: 132;"> </p> 
          <p>U kunt waarden handmatig toevoegen aan de gegevensopslag of met de Workfront Fusion-modules voor gegevensopslag.</p> 
         </div> </li> 
       </ul> </td> 
     </tr> 
     <tr> 
      <td>[!UICONTROL Strict] </td> 
      <td> <p>Schakel deze optie in om ervoor te zorgen dat de lading overeenkomt met de gegevensstructuren. De ladingen die extra punten bevatten die niet in de gegevensstructuur worden gespecificeerd worden verworpen.</p> </td> 
     </tr> 
    </tbody> 
   </table>

## Een bestaande gegevensopslag bewerken

U kunt de eigenschappen en inhoud van een bestaande gegevensopslag bewerken in het gebied [!UICONTROL Data stores] van Workfront Fusion.

* [De eigenschappen van een gegevensopslagruimte bewerken](#edit-the-properties-of-a-data-store)
* [De inhoud van een gegevensopslagruimte bewerken](#edit-the-contents-of-a-data-store)

### De eigenschappen van een gegevensopslagruimte bewerken

De eigenschappen van een gegevensopslag omvatten de gegevensstructuur die de gegevensopslag gebruikt, evenals de grootte van de gegevensopslag.

1. Klik **[!UICONTROL Data stores]** {het pictogram van de 1} opslag van Gegevens ![ in het linkernavigatievenster om het ](assets/data-store-icon.png) gebied te openen.[!UICONTROL Data stores]
1. Klik **[!UICONTROL Edit]** ![ uitgeeft gegevensopslag ](assets/data-store-edit.png) naast de gegevensopslag die u wilt uitgeven.
1. (Optioneel) Als u de gegevensstructuur die door deze gegevensopslag wordt gebruikt, wilt wijzigen in een andere bestaande gegevensstructuur, selecteert u deze in de vervolgkeuzelijst **[!UICONTROL Data structure]** .

   of

   (Facultatief) als u de gegevensstructuur wilt veranderen die door deze gegevensopslag aan een volledig nieuwe gegevensstructuur wordt gebruikt, zie [ Opstelling de gegevensstructuur ](#set-up-the-data-structure) in dit artikel.

1. (Optioneel) Wijzig de grootte van de gegevensopslagruimte door de nieuwe grootte in te voeren in het veld **[!UICONTROL Data storage size in MB]** .
1. Klik op **[!UICONTROL Save]**.

### De inhoud van een gegevensopslagruimte bewerken

1. Klik het **[!UICONTROL Data Store]** pictogram van de de opslagplaats van 1} Gegevens ![ in het linkernavigatievenster om het ](assets/data-store-icon.png) gebied te openen.[!UICONTROL Data Store]
1. Klik op **[!UICONTROL Browse]** naast de gegevensopslagruimte die u wilt bewerken.
1. (Optioneel) U kunt kolommen opnieuw ordenen door deze naar de gewenste locatie te slepen.
1. (Optioneel) [!UICONTROL Edit] één cel door op het pictogram **[!UICONTROL Edit]** in die cel te klikken en vervolgens de gewenste waarde in te voeren.
1. (Optioneel) Voeg een nieuw item aan de gegevensopslag toe door op **[!UICONTROL Add]** te klikken en vervolgens de gegevens voor het nieuwe item in te voeren.
1. Klik op **[!UICONTROL Save]**.

## Problemen oplossen

* [Verloren gegevens uit een gegevensopslagruimte herstellen](#restoring-lost-data-from-a-data-store)
* [Fout: onvoldoende ruimte](#out-of-space-error)
* [Maximum aantal winkels bereikt fout](#maximum-stores-reached-error)

### Verloren gegevens uit een gegevensopslagruimte herstellen

Er is momenteel geen gereedschap waarmee u het herstellen van verloren gegevens kunt automatiseren.

#### Workaround

1. Onderzoek alle uitvoeringslogboeken van scenario&#39;s waar de punten aan de gegevensopslag werden opgenomen.

   Voor meer informatie bij het onderzoeken van uitvoeringslogboeken, zie [ Mening de uitvoeringshistorie van een scenario ](/help/workfront-fusion/manage-scenarios/view-scenario-execution-history.md).

1. Kopieer de gegevens.
1. Voeg de gegevens opnieuw in de gegevensopslag in.

   Voor informatie bij het opnemen van gegevens in een gegevensopslag, zie [ de inhoud van een gegevensopslag ](#edit-the-contents-of-a-data-store) in dit artikel uitgeven.

### [!UICONTROL Out of space] fout

Er treedt een [!UICONTROL Out of Space] -fout op omdat aan uw eerder gemaakte gegevensopslagruimten al opslagruimte is toegewezen.

#### Workaround

1. Bewerk de bestaande gegevensopslagruimten om minder ruimte te gebruiken. Hierdoor komt er ruimte vrij voor uw nieuwe gegevensopslag.

   Voor meer informatie, zie [ de eigenschappen van een gegevensopslag ](#edit-the-properties-of-a-data-store) in dit artikel uitgeven.

>[!NOTE]
>
>Wij adviseren dat u niet al uw ruimte aan één enkele gegevensopslag toewijst tenzij u zeker bent u niet meer gegevensopslag zult vereisen.

### [!UICONTROL Maximum stores reached] fout

Er treedt een [!UICONTROL Maximum stores reached] -fout op omdat uw organisatie alle beschikbare gegevensopslagruimten heeft gebruikt.

#### Workaround

Als u het aantal bestaande gegevensopslagruimten wilt verminderen, kunt u een van de volgende handelingen uitvoeren:

* Bestaande gegevensopslagruimten combineren
* Ongebruikte gegevensopslagruimten verwijderen
