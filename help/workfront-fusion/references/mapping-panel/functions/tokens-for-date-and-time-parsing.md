---
title: Tokens voor datum- en tijdparsering
description: De volgende tokens voor datum en tijd het ontleden zijn beschikbaar in het  [!DNL Adobe Workfront Fusion mapping]  paneel.
author: Becky
feature: Workfront Fusion
exl-id: d3242af3-89e8-45ae-81a1-3b4dadf824fd
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Tokens voor datum- en tijdparsering

## Jaar-, maand- en dag-tokens

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Invoer </th> 
   <th>Voorbeeld </th> 
   <th> <p>Beschrijving</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>YYYY </code> </td> 
   <td><code>2014 </code> </td> 
   <td> <p>Jaar met 4 of 2 cijfers</p> </td> 
  </tr> 
  <tr> 
   <td><code>YY</code></td> 
   <td><code>14</code></td> 
   <td> <p>2-cijferige jaar</p> </td> 
  </tr> 
  <tr> 
   <td><code>Y</code> </td> 
   <td><code>-25</code> </td> 
   <td> <p>[!UICONTROL Year with any number of digits and sign]</p> </td> 
  </tr> 
  <tr> 
   <td><code>Q</code> </td> 
   <td><code>1..4</code> </td> 
   <td> <p> Kwartaal van het jaar. Stelt maand in op eerste maand in kwartaal.</p> </td> 
  </tr> 
  <tr> 
   <td><code>M MM</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> Maandnummer</p> </td> 
  </tr> 
  <tr> 
   <td><code>MMM MMMM</code> </td> 
   <td><code>Jan..December</code> </td> 
   <td> <p> Naam maand</p> </td> 
  </tr> 
  <tr> 
   <td><code>D DD</code> </td> 
   <td><code>1..31</code> </td> 
   <td> <p> Dag van de maand</p> </td> 
  </tr> 
  <tr> 
   <td><code>Do </code> </td> 
   <td><code>1st..31st</code> </td> 
   <td> <p> Dag van de maand met de rangorde</p> </td> 
  </tr> 
  <tr> 
   <td><code>DDD DDDD</code> </td> 
   <td><code>1..365</code></td> 
   <td> <p> Dag van jaar</p> </td> 
  </tr> 
  <tr> 
   <td><code>X</code> </td> 
   <td><code>1410715640.579</code> </td> 
   <td> <p> Unix timestamp</p> </td> 
  </tr> 
  <tr> 
   <td><code>x</code> </td> 
   <td><code>1410715640579</code> </td> 
   <td> <p> Tijdstempel Unix ms</p> </td> 
  </tr> 
 </tbody> 
</table>

## Weekjaar-, week- en weekdagtokens

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Invoer </th> 
   <th>Voorbeeld </th> 
   <th> <p>Beschrijving</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>ddd dddd</code> </td> 
   <td><code>Mon...Sunday</code> </td> 
   <td> <p> Dagnaam</p> </td> 
  </tr> 
  <tr> 
   <td><code>GGGG</code> </td> 
   <td><code>2014</code> </td> 
   <td> <p> Jaar van de ISO 4-cijferige week</p> </td> 
  </tr> 
  <tr> 
   <td><code>GG </code> </td> 
   <td><code>14</code> </td> 
   <td> <p> Jaar van de ISO 2-cijferweek</p> </td> 
  </tr> 
  <tr> 
   <td><code>W WW</code> </td> 
   <td><code>1..53</code></td> 
   <td> <p> ISO-week van jaar</p> </td> 
  </tr> 
  <tr> 
   <td><code>E</code> </td> 
   <td><code>1..7</code> </td> 
   <td> <p> ISO-dag van de week</p> </td> 
  </tr> 
 </tbody> 
</table>

## Uur-, minuut-, seconde-, milliseconde- en offsettokens

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <col> 
 <thead> 
  <tr> 
   <th>Invoer </th> 
   <th>Voorbeeld </th> 
   <th> <p>Beschrijving</p> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td><code>H HH</code> </td> 
   <td><code>0..23</code></td> 
   <td> <p> Uren (24 uur)</p> </td> 
  </tr> 
  <tr> 
   <td><code>h hh</code> </td> 
   <td><code>1..12</code> </td> 
   <td> <p> Uren (12 uur gebruikt bij A.)</p> </td> 
  </tr> 
  <tr> 
   <td><code>k kk</code> </td> 
   <td><code>1..24</code> </td> 
   <td> <p> Uren (24 uur tijd van 1 tot 24)</p> </td> 
  </tr> 
  <tr> 
   <td><code>a A</code> </td> 
   <td><code>am pm</code> </td> 
   <td> <p> Post of ante meridiem (Merk op dat één karakter a p ook als geldig wordt beschouwd)</p> </td> 
  </tr> 
  <tr> 
   <td><code>m mm</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> Minuten</p> </td> 
  </tr> 
  <tr> 
   <td><code>s ss</code> </td> 
   <td><code>0..59</code> </td> 
   <td> <p> Seconden</p> </td> 
  </tr> 
  <tr> 
   <td><code>S SS SSS</code> </td> 
   <td><code>0..999</code> </td> 
   <td> <p> Fractionele seconden</p> </td> 
  </tr> 
  <tr> 
   <td><code>Z ZZ</code> </td> 
   <td><code>+12:00</code> </td> 
   <td> <p> Verschuiving vanaf UTC als +-HH:mm, +-HHmm, of Z</p> </td> 
  </tr> 
 </tbody> 
</table>
