---
title: MIME-modules
description: U kunt MIME-typen gebruiken in Adobe Workfront Fusion. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type text/html wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type image/jpeg. MIME-typen werken onafhankelijk van het besturingssysteem en de hardware.
author: Becky
feature: Workfront Fusion
exl-id: 9259356b-5b42-4b6d-9854-fce9718d14e3
source-git-commit: 4697ea1449f77ddb8648658990098b3b4bc58ad2
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# [!UICONTROL MIME] modules

U kunt MIME-typen gebruiken in Adobe Workfront Fusion. MIME-typen (Multipurpose Internet Mail Extension) zijn labels waarmee software verschillende typen gegevens kan identificeren die op internet worden gedeeld. Webservers en browsers gebruiken het MIME-type om te bepalen wat er met een bestand moet worden gedaan. Een bestand met het MIME-type `text/html` wordt bijvoorbeeld anders verwerkt in een browser dan een bestand met het MIME-type `image/jpeg` . MIME-typen werken onafhankelijk van het besturingssysteem en de hardware.

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



## [!UICONTROL MIME] modules en hun velden

* [Een bestandsextensie ophalen](#get-a-file-extension)
* [Een MIME-type ophalen](#get-a-mime-type)

### [!UICONTROL Get a file extension]

Deze transformatormodule retourneert de oorspronkelijke bestandsextensie voor een bepaald MIME-type.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL MIME type]</td> 
   <td> <p>Typ of wijs het MIME-type toe waarvoor u de bestandsextensie wilt bepalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

### [!UICONTROL Get a MIME type]

Deze transformatormodule retourneert het MIME-type dat is gekoppeld aan een bepaalde bestandsnaam, een bepaald pad of een bepaalde extensie.

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!UICONTROL File]</td> 
   <td> <p>Typ of wijs het bestand toe waarvoor u het MIME-type wilt bepalen. </p> <p>U kunt het bestand invoeren met:</p> 
    <ul> 
     <li> <p><strong>[!UICONTROL File path]</strong> </p> <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b> Voorbeeld: </b></span></span> /file/image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File name]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b> Voorbeeld: </b></span></span> image.jpeg</p> </li> 
     <li><strong>[!UICONTROL File extension]</strong>  <p class="example" data-mc-autonum="<b>Example: </b>"><span class="autonumber"><span><b> Voorbeeld: </b></span></span> jpeg</p> </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>
