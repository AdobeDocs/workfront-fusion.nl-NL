---
title: Modules archiveren
description: In a  [!DNL Adobe Workfront Fusion]  scenario, kunt u een archief, zoals een gecomprimeerd dossier, met veelvoudige derdetoepassingen en de diensten verbinden. U kunt bijvoorbeeld een scenario configureren dat
author: Becky
feature: Workfront Fusion
exl-id: 4b5ff3d5-601c-4119-ad70-3612ad5ba1ab
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# [!UICONTROL Archive] modules

In een [!DNL Adobe Workfront Fusion] scenario, kunt u een archief, zoals een gecomprimeerd dossier, in uw scenario gebruiken, toestaand u om het in uw automatiseringen of integraties te gebruiken.

Voor instructies bij het creëren van een scenario, zie de artikelen onder [ scenario&#39;s creëren: artikelindex ](/help/workfront-fusion/create-scenarios/create-scenarios-toc.md). Voor informatie over modules, zie de artikelen onder [ Modules: artikelindex ](/help/workfront-fusion/references/modules/modules-toc.md).

## [!UICONTROL Archive] modules en hun velden

Wanneer u [!UICONTROL Archive] modules configureert, geeft [!DNL Workfront Fusion] de onderstaande velden weer. Daarnaast kunnen aanvullende [!UICONTROL Archive] -velden worden weergegeven, afhankelijk van factoren zoals uw toegangsniveau in de app of service. Een bolde titel in een module wijst op een vereist gebied.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [ informatie van de Kaart van één module aan een andere ](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![ Kaart knevel ](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [[!UICONTROL Extract an archive]](#extract-an-archive)
* [[!UICONTROL Create an archive]](#create-an-archive)
* [[!UICONTROL Inflate]](#inflate)
* [[!UICONTROL Deflate]](#deflate)

## [!UICONTROL Extract an archive]

Deze actiemodule extraheert een bestand dat u uit een archief identificeert.

De module retourneert de id van het bestand en de bijbehorende velden, samen met aangepaste velden en waarden die door de verbinding worden geopend. U kunt deze informatie in verdere modules in het scenario in kaart brengen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p> Selecteer het bestand dat u wilt extraheren. Dit dossier kan van een vorige module (zoals [!DNL Workfront] worden in kaart gebracht &gt; [!UICONTROL Download a document] module).</p>  </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Voorbeeld:** krijg het dossier van het PIT van de bepaalde [!DNL Dropbox] omslag (bijvoorbeeld, Archives), haalt het uit gebruikend de [!UICONTROL Archive] module en verzendt geciteerde dossiers naar het gewenste e-mailadres als gehechtheid met [!UICONTROL Email] of [!DNL Gmail] module.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-dropbox-350x134.png)

## [!UICONTROL Create an archive]

Deze aggregatormodule voegt de gewenste bestanden toe aan een [!UICONTROL ZIP] - of [!UICONTROL TAR] -archief.

Als u deze module configureert, worden de volgende velden weergegeven.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Source module]</td> 
   <td> <p> Selecteer de module waarvan u de bestanden wilt ophalen.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Type] </td> 
   <td> <p>Selecteer of u bestanden wilt toevoegen aan een [!UICONTROL ZIP] archief of een [!UICONTROL TAR] archief.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Comment]</td> 
   <td>Voer een opmerking in die u aan het archief wilt toevoegen.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Group by]</td> 
   <td> <p>Definieer een expressie waarop u de geaggregeerde uitvoer wilt groeperen. Deze expressie kan een of meer toegewezen items bevatten. De geaggregeerde gegevens worden vervolgens in groepen verdeeld op basis van de waarde van deze expressie. Elke groep voert als een afzonderlijke bundel met een sleutel (de geëvalueerde uitdrukking) en een waarde (de samengevoegde tekst) uit. U kunt de sleutel als filter in verdere modules gebruiken.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Stop processing after an empty aggregation]</td> 
   <td>Selecteer deze optie om het scenario te stoppen als er geen resultaten zijn.</td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Archive name]</td> 
   <td> <p> Voer een naam in voor het gemaakte archief. Voeg geen extensie toe.</p> </td> 
  </tr> 
  <tr> 
   <td>[!UICONTROL Source file]</td> 
   <td> <p>Selecteer een bronbestand uit een vorige module of wijs de naam en gegevens van het bronbestand toe.</p> </td> 
  </tr> 
 </tbody> 
</table>

>[!INFO]
>
>**Voorbeeld:** bekijk inkomende e-mails gebruikend [!DNL Gmail] > [!UICONTROL Watch emails] module. Als een e-mail wordt ontvangen, worden de bijlagen herhaald in afzonderlijke bundels, vervolgens naar het [!DNL ZIP] -bestand gearchiveerd en in de gedefinieerde map Dropbox opgeslagen.
>
>![](/help/workfront-fusion/references/apps-and-modules/assets/example-gmail-350x102.png)

## [!UICONTROL Inflate]

Deze transformatormodule decomprimeert binaire gegevens met behulp van een inflatiealgoritme.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Voer de gegevens in die u wilt decomprimeren of wijs deze toe met behulp van de inflate-functie.</p> </td> 
  </tr> 
 </tbody> 
</table>

## [!UICONTROL Deflate]

Deze transformatormodule comprimeert binaire gegevens met behulp van een deflatiealgoritme.

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td>[!UICONTROL Data] </td> 
   <td> <p>Voer de gegevens in die u wilt comprimeren of wijs deze toe met de functie deflate.</p> </td> 
  </tr> 
 </tbody> 
</table>
