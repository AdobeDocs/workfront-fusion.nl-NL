---
title: Math-functies
description: De volgende rekenkundige functies zijn beschikbaar in het Adobe Workfront Fusion mapping panel.
author: Becky
feature: Workfront Fusion
exl-id: 3d08b09d-b395-4226-b7e3-d5650c428a59
source-git-commit: 24a6c1558fd6349c022df8a1847a7f39fafddd67
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# Math-functies

## [!UICONTROL average ([array of values]) average(value1; [value2], ...)]

Retourneert de gemiddelde waarde van de numerieke waarden in een specifieke array, of de gemiddelde waarde van numerieke waarden die afzonderlijk zijn ingevoerd.

## [!UICONTROL ceil (number)]

Retourneert het kleinste gehele getal dat groter dan of gelijk is aan een opgegeven getal.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `ceil(` `1.2` `)`

  Retourneert 2

* `ceil(` `4` `)`

  Retourneert 4

>[!ENDSHADEBOX]

## [!UICONTROL floor (number)]

Retourneert het grootste gehele getal dat kleiner dan of gelijk is aan een opgegeven getal.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `floor(` `1.2` `)`

  Retourneert 1

* `floor(` `1.9` `)`

  Retourneert 1

* `floor(` `4` `)`

  Retourneert 4

>[!ENDSHADEBOX]

## [!UICONTROL max ([array of values]), max(value1;value2; ...)]

Retourneert het grootste getal in een opgegeven array of het grootste getal onder getallen die afzonderlijk zijn ingevoerd.

## [!UICONTROL min ([array of values]), min(value1; value2; ...)]

Retourneert het kleinste getal in een opgegeven array of het kleinste getal onder getallen die afzonderlijk zijn ingevoerd.

## [!UICONTROL round (number)]

Rondt een numerieke waarde af op het dichtstbijzijnde gehele getal.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `round(` `1.2` `)`

  Retourneert 1

* `round(` `1.5` `)`

  Retourneert 2

* `round(` `1.7` `)`

  Retourneert 2

* `round(` `2` `)`

  Retourneert 2

>[!ENDSHADEBOX]

## [!UICONTROL sum ([array of values]), sum(value1; value2; ...)]

Retourneert de som van de waarden in een opgegeven array of de som van de getallen die afzonderlijk zijn ingevoerd.

## [!UICONTROL parseNumber (number; decimal separator)]

Parseert een tekenreeks met een getal en retourneert het getal. Bijvoorbeeld, parseNumber(1 756,456;,)

## [!UICONTROL formatNumber (number; decimalPOINTS; [decimalSeparator]; [thousandsSeparator])]

Retourneert een getal in de gewenste notatie. Het decimale punt is standaard een komma (,) en het scheidingsteken voor duizendtallen is een punt (.).

>[!BEGINSHADEBOX]

**Voorbeeld:**

`formatNumber( 123456789 ; 3 ; , ; . )`

Retourneert 123.456.789.000

>[!ENDSHADEBOX]
