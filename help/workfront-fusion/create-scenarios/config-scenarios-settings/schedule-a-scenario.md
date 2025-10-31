---
content-type: reference
title: Een scenario plannen
description: Door gebrek, loopt een scenario om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak een geactiveerd scenario loopt. De scenario's van de fusie kunnen worden gepland zo vaak zoals om de 5 minuten te lopen.
author: Becky
feature: Workfront Fusion
recommendations: noDisplay, noCatalog
exl-id: 9b74af0d-e7ff-4bf5-974e-0651d0d51f71
source-git-commit: b2ca63ca5af26ee79758798118817b55113b3bd0
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Een scenario plannen

Door gebrek, loopt een scenario om de 15 minuten. U kunt dit veranderen door te bepalen wanneer en hoe vaak een geactiveerd scenario loopt. De scenario&#39;s van de fusie kunnen worden gepland zo vaak zoals om de 5 minuten te lopen.

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

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

+++

## Een scenario plannen

1. Klik het **lusje van het Scenario** in het linkerpaneel.
1. Selecteer het scenario dat u wilt plannen.
1. Klik in de rechterbovenhoek van de vervolgkeuzelijst Scenario op **[!UICONTROL Options]** > **[!UICONTROL Scheduling]**

   of

   Klik op het pictogram **[!UICONTROL Scheduling]** (klok) op de triggermodule van het scenario.

1. Voer gegevens in de volgende velden in:

   <table style="table-layout:auto">   
    <col> 
    <col> 
    <tbody> 
     <tr> 
      <td role="rowheader">[!UICONTROL Run scenario]</td> 
      <td> <p>Selecteer de frequentie waarmee u het scenario wilt uitvoeren, en selecteer dan het interval.</p> 
       <ul> 
        <li> <p><strong>[!UICONTROL At regular intervals]</strong> </p> <p>Voer het aantal minuten in tussen de uitvoeringen. De standaardwaarde is 15 minuten.</p> </li> 
        <li> <p><strong>[!UICONTROL Once]</strong> </p> <p>Voer de datum en tijd in waarop het scenario moet worden uitgevoerd. Gebruik de indeling <code>MM/DD/YYYY h:mm A</code> . Voorbeeld: <code>06/25/2019 11:00 PM</code> .</p> </li> 
        <li> <p><strong>[!UICONTROL Every day]</strong> </p> <p>Voer de tijd in waarop het scenario moet worden uitgevoerd. Gebruik de indeling <code>h:mm A</code> . Voorbeeld: <code>11:00 PM</code> .</p> </li> 
        <li> <p><strong>[!UICONTROL Days of the week]</strong> </p> <p>Dagen: selecteer de dagen van de week dat u het scenario wilt lopen. U kunt een of meer dagen selecteren.</p> <p>Tijd: ga de tijd in dat u het scenario op de geselecteerde dagen wilt lopen. Gebruik de indeling <code>h:mm A</code> . Voorbeeld: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Days of the month]</strong> </p> <p>Dagen: selecteer de dagen van de maand die u het scenario wilt lopen. U kunt een of meer dagen selecteren.</p> <p>Tijd: ga de tijd in dat u het scenario op de geselecteerde dagen wilt lopen. Gebruik de indeling <code>h:mm A</code> . Voorbeeld: <code>11:00 PM</code></p> </li> 
        <li> <p><strong>[!UICONTROL Specified dates]</strong> </p> <p>Maanden: selecteer de maanden die u het scenario wilt uitvoeren. U kunt een of meer maanden selecteren.</p> <p>Dagen: selecteer de dagen van de maand die u het scenario wilt lopen. U kunt een of meer dagen selecteren.</p> <p>Tijd: ga de tijd in dat u het scenario op de geselecteerde dagen wilt lopen. Gebruik de indeling <code>h:mm A</code> . Voorbeeld: <code>11:00 PM</code></p> </li> 
       </ul> <p>Opmerking: een scenario kan alleen op die datum worden uitgevoerd als er een datum is. Een scenario dat bijvoorbeeld alleen voor de 31e van de maand is gepland, loopt niet in februari, april, juni, september of november, omdat die maanden geen 31e dag hebben.</p> </td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Advanced scheduling]</td> 
      <td>U kunt specifieke tijdintervallen bepalen waarin uw scenario moet lopen. U kunt tijdsintervallen van dagen, weekdagen of maanden opgeven. Klik voor elk interval op <strong>[!UICONTROL Add]</strong> en vul de velden in zoals wordt beschreven in het veld [!UICONTROL Run scenario] .</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL Start]</td> 
      <td>Ga de datum en de tijd in waarna u het scenario wilt lopen. Gebruik de indeling <code>MM/DD/YYYY h:mm A</code> . Voorbeeld: <code>06/25/2019 11:00 PM</code> .</td> 
     </tr> 
     <tr> 
      <td role="rowheader">[!UICONTROL End]</td> 
      <td>Voer de datum en tijd in waarop het scenario moet worden uitgevoerd. Gebruik de indeling <code>MM/DD/YYYY h:mm A</code> . Voorbeeld: <code>06/25/2019 11:00 PM</code> .</td> 
     </tr> 
    </tbody> 
   </table>

1. Klik **[!UICONTROL OK]** om de planningsmontages te bewaren en aan het scenario terug te keren.
