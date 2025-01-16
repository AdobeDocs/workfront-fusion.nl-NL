---
title: Afgedwongen typegebruik
description: Dit document beschrijft hoe  [!DNL Adobe Workfront Fusion]  zich in situaties gedraagt wanneer het waarden in verwachte en onverwachte gegevensformaten ontvangt.
author: Becky
feature: Workfront Fusion
exl-id: a8bdd36d-c01f-4019-a3ea-fb185101500e
source-git-commit: b7c511c51a2f27292cd0cb754673515e67c8a397
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# Afgedwongen typegebruik

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">[!DNL Adobe Workfront] plan*</td> 
   <td> <p>[!DNL Pro] of hoger</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie*</td> 
   <td> <p>[!UICONTROL Plan], [!UICONTROL Work]</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidige licentievereiste: geen [!DNL Workfront Fusion] licentievereiste.</p>
   <p>of</p>
   <p>Vereiste voor oudere licenties: [!UICONTROL [!DNL Workfront Fusion] voor werkautomatisering en integratie] </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Huidige productvereiste: als u het abonnement [!UICONTROL Select] of [!UICONTROL Prime] [!DNL Adobe Workfront] hebt, moet uw organisatie [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken. [!DNL Workfront Fusion] wordt opgenomen in het [!UICONTROL Ultimate] [!DNL Workfront] -abonnement.</p>
   <p>of</p>
   <p>Vereiste verouderd product: uw organisatie moet [!DNL Adobe Workfront Fusion] en [!DNL Adobe Workfront] aanschaffen om de in dit artikel beschreven functionaliteit te kunnen gebruiken.</p>
   </td> 
  </tr> 
 </tbody> 
</table>

Neem contact op met de [!DNL Workfront] -beheerder als u wilt weten welk abonnement, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

### Afgedwongen typegebruik

In dit document wordt beschreven hoe [!DNL Adobe Workfront Fusion] zich gedraagt in situaties waarin waarden worden ontvangen in verwachte en onverwachte gegevensindelingen.

<table style="table-layout:auto">
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Verwacht</th> 
   <th>Ontvangen</th> 
   <th> <p>Beschrijving</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>array </td> 
   <td>array </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>array </td> 
   <td>overige </td> 
   <td> <p>Als de ontvangen waarde niet van het arraytype is, maakt [!DNL Workfront Fusion] een array en is het eerste (en enige) element de ontvangen waarde.</p> </td> 
  </tr> 
  <tr> 
   <td>boolean </td> 
   <td>boolean </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>boolean </td> 
   <td>getal </td> 
   <td> <p>De waarde wordt omgezet in logische ja, zelfs als de waarde 0 is.</p> </td> 
  </tr> 
  <tr> 
   <td>boolean </td> 
   <td>text </td> 
   <td> <p>Als de waarde gelijk is aan false of als de waarde leeg is, wordt deze omgezet in logische Nee. Als niet, wordt het omgezet in logische ja.</p> </td> 
  </tr> 
  <tr> 
   <td>boolean </td> 
   <td>overige </td> 
   <td> <p>De waarde wordt in logische Ja omgezet wanneer de ontvangen waarde bestaat (is niet null).</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>buffer </td> 
   <td> <p>De waarde wordt alleen ongewijzigd overgedragen als de codepage naar verwachting is. Als de codepage anders is, probeert [!DNL Workfront Fusion] de ontvangen waarde om te zetten in de gewenste codepage. Als deze conversie niet wordt ondersteund, retourneert [!DNL Workfront Fusion] een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>boolean </td> 
   <td> <p>De waarde wordt omgezet in tekst (true/false) en vervolgens in binaire gegevens volgens de bovenstaande stappen voor het omzetten in tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>date </td> 
   <td> <p>De waarde wordt omgezet in ISO 8601-tekst en vervolgens in binaire gegevens volgens de stappen die worden beschreven voor het omzetten in tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>getal </td> 
   <td> <p>De waarde wordt omgezet in tekst en vervolgens in binaire gegevens volgens de stappen hierboven voor het omzetten in tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>text </td> 
   <td> <p>De waarde wordt omgezet in binaire gegevens en gecodeerd zoals verwacht. Als de verwachte codering niet is opgegeven, wordt utf8-codering gebruikt.</p> </td> 
  </tr> 
  <tr> 
   <td>buffer </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>collectie </td> 
   <td>collectie </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>collectie </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>date </td> 
   <td>date </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>date </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] probeert de tekst om te zetten in een datum. Als de conversie mislukt, wordt een validatiefout geretourneerd. Datum moet dag, maand en jaar bevatten. Datum kan tijd en tijdzone bevatten. De standaardtijdzone is gebaseerd op uw instellingen. Voorbeelden:</p> <p><code>2016-06-20T17:26:44.356Z</code> </p> <p><code>2016-06-20 19:26:44 GMT+02:00</code> </p> <p><code>2016-06-20 19:26+0200</code> </p> <p><code>2016-06-20 17:26:44</code> </p> <p><code>2016-06-20</code> </p> <p><code>2016/06/20 17:26:44</code> </p> <p><code>2016/06/20 19:26:44+02:00</code> </p> <p><code>2016/06/20 17:26</code> </p> <p><code>2016/06/20 5:26 PM</code> </p> <p><code>2016/06/20</code> </p> <p><code>06/20/2016 17:26:44</code> </p> <p><code>06/20/2016 19:26:44+02:00</code> </p> <p><code>06/20/2016 17:26</code> </p> <p><code>06/20/2016 5:26 PM</code> </p> <p><code>06/20/2016</code> </p> <p><code>20.6.2016 17:26:44</code> </p> <p><code>20.6.2016 19:26:44+02:00</code> </p> <p><code>20.6.2016 17:26</code> </p> <p><code>20.6.2016</code> </p> </td> 
  </tr> 
  <tr> 
   <td>date </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>getal </td> 
   <td>getal </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>getal </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] probeert de tekst om te zetten in een getal. Als de conversie mislukt, wordt een validatiefout geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td>getal </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>text </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>array </td> 
   <td> <p>Als de opgegeven array conversie naar tekst ondersteunt, wordt de waarde omgezet. Als dat niet het geval is, retourneert [!DNL Workfront Fusion] een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>boolean </td> 
   <td> <p>De waarde wordt omgezet in tekst (true/false).</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>buffer </td> 
   <td> <p>Als tekstcodering is opgegeven voor binaire gegevens, wordt de waarde omgezet in tekst. Als dat niet het geval is, retourneert [!DNL Workfront Fusion] een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>date </td> 
   <td> <p>De waarde wordt omgezet in ISO 8601-tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>getal </td> 
   <td> <p>De waarde wordt omgezet in tekst.</p> </td> 
  </tr> 
  <tr> 
   <td>text </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
  <tr> 
   <td>tijd </td> 
   <td>tijd </td> 
   <td> <p>De waarde wordt ongewijzigd overgedragen.</p> </td> 
  </tr> 
  <tr> 
   <td>tijd </td> 
   <td>text </td> 
   <td> <p>[!DNL Workfront Fusion] wordt geprobeerd de tijd om te zetten in de <code>hours:minutes:seconds</code> -indeling. Als de conversie mislukt, wordt een validatiefout geretourneerd.</p> </td> 
  </tr> 
  <tr> 
   <td>tijd </td> 
   <td>overige </td> 
   <td> <p>[!DNL Workfront Fusion] retourneert een validatiefout.</p> </td> 
  </tr> 
 </tbody> 
</table>
