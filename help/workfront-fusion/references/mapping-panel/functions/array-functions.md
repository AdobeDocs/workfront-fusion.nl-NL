---
title: Arrayfuncties
description: De volgende arrayfuncties zijn beschikbaar in het Adobe Workfront Fusion-toewijzingspaneel.
author: Becky
feature: Workfront Fusion
exl-id: 16c3915c-add1-4aab-a0e1-75fc590c42a6
source-git-commit: d141738a7e013ed817cb657b883fc5e1061e2165
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 0%

---

# Arrayfuncties

## [!UICONTROL join (array; separator)]

Hiermee worden alle items van een array samengevoegd in een tekenreeks, waarbij het opgegeven scheidingsteken tussen elk item wordt gebruikt.

## [!UICONTROL length (array)]

Retourneert het aantal items in een array.

## [!UICONTROL keys (object)]

Retourneert een array van de eigenschappen van een bepaald object of een bepaalde array.

## [!UICONTROL slice (array; start; [end])]

Retourneert een nieuwe array die alleen geselecteerde items bevat.

## [!UICONTROL merge (array1; array2; ...)]

Voegt een of meer arrays samen tot één array.

## [!UICONTROL contains (array; value)]

Controleert of een array de waarde bevat.

## [!UICONTROL remove (array; value1; value2; ...)]

Verwijdert waarden die zijn opgegeven in de parameters van een array. Deze functie is alleen effectief op primitieve arrays met tekst of getallen.

## [!UICONTROL add (array; value1; value2; ...)]

Voegt waarden die in parameters zijn opgegeven toe aan een array en retourneert die array.

## [!UICONTROL map (complex array; key;[key for filtering];[possible values for filtering])]

Retourneert een primitieve array met waarden van een complexe array. Deze functie staat het filtreren waarden toe. Gebruik namen van onbewerkte variabelen voor sleutels.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `map(Emails[];email)`

  Retourneert een primitieve array met e-mails

* `map(Emails[];email;label;work;home)`

  Retourneert een primitieve array met e-mails met een label dat gelijk is aan werk of privé

>[!ENDSHADEBOX]

Voor meer informatie, zie [&#x200B; een serie of serieelement &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md) in kaart brengen.

## schudden

## [!UICONTROL sort (array; [order]; [key])]

Sorteert waarden van een array. De geldige waarden voor de parameter `order` zijn:

* `asc`

  (standaardwaarde) - oplopende volgorde: 1, 2, 3, ... voor het type Number. A, B, C, a, b, c... voor tekst

* `desc`

  Aflopende volgorde: ..., 3, 2, 1 voor type Number. ..., c, b, a, C, B, A voor tekst.

* `asc ci`

  niet-hoofdlettergevoelige oplopende volgorde: A, a, B, b, C, c, ... voor tekst.

* `desc ci`

  niet-hoofdlettergevoelige aflopende volgorde: ..., C, c, B, b, A, a voor tekst.

Gebruik de parameter `key` om eigenschappen binnen complexe objecten te benaderen.

Gebruik namen van onbewerkte variabelen voor sleutels.

Gebruik puntnotatie voor toegang tot geneste eigenschappen.

Het eerste item in een array is index 1.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `sort(Contacts[];name)`

  Hiermee wordt een array van contactpersonen gesorteerd op de eigenschap &quot;name&quot; in oplopende volgorde

* `sort(Contacts[];desc;name)`

  Hiermee wordt een array van contactpersonen gesorteerd op de eigenschap &quot;name&quot; in aflopende volgorde

* `sort(Contacts[];asc ci;name)`

  Hiermee wordt een array van contactpersonen gesorteerd op de eigenschap &quot;name&quot; in hoofdlettergevoelige oplopende volgorde

* `sort(Emails[];sender.name)`

  Hiermee wordt een array met e-mailberichten gesorteerd op de eigenschap &quot;sender.name&quot;

>[!ENDSHADEBOX]

## [!UICONTROL reverse (array)]

Het eerste element van de array wordt het laatste element, het tweede het op een na laatste element enzovoort.

## [!UICONTROL flatten (array)]

Hiermee wordt een nieuwe array gemaakt waarin alle elementen van de subarray recursief tot de opgegeven diepte zijn samengevoegd.

## [!UICONTROL distinct (array; [key])]

Hiermee worden duplicaten uit een array verwijderd. Gebruik het argument &quot;[!UICONTROL key]&quot; om toegang te krijgen tot eigenschappen binnen complexe objecten. Gebruik puntnotatie voor toegang tot geneste eigenschappen. Het eerste item in een array is index 1.

>[!BEGINSHADEBOX]

**Voorbeeld:** `distinct(Contacts[];name)`

Verwijdert duplicaten binnen een array van contactpersonen door de eigenschap &quot;name&quot; te vergelijken

>[!ENDSHADEBOX]

## toCollection

* Deze functie neemt een serie die zeer belangrijk-waardeparen bevat en zet het in een inzameling om. De functie heeft drie argumenten:

* (array) met sleutelwaardeparen
* (tekenreeks) de naam van het veld dat als sleutel moet worden gebruikt
* (tekenreeks) de naam van het veld dat als waarde moet worden gebruikt

>[!BEGINSHADEBOX]

Voorbeeld:

Bij een array:

```
[{"name":"Bob", "age":22}, {"name":"Tim", "age":23}]
```

en argumenten

```
{{toCollection(6.array; "name"; "age")}}
```

de functie retourneert

```
{
    "Bob": 22,
    "Tim": 23
}
```

>[!ENDSHADEBOX]

## toArray

Deze functie converteert een verzameling naar een array van sleutelwaardeparen.

>[!BEGINSHADEBOX]

**Voorbeelden:**

Gezien de collectie

`{ key1: "value1", key2: "value2:}`

De functie

`toArray({ key1: "value1", key2: "value2:})`

Retourneert de array van sleutelwaardeparen

`[{ key1: "value1"}, { key2: "value2"}]`

>[!ENDSHADEBOX]

## [!UICONTROL arrayDifference [array1, array2, mode]]

Geeft het verschil tussen twee arrays.

Voer een van de volgende waarden in voor de parameter `mode` .

* `classic`: Geeft een nieuwe array met alle elementen van `array1` die niet bestaan in `array2` .

* `symmetric`: retourneert een array met elementen die niet voor beide arrays hetzelfde zijn.

  Met andere woorden, de functie retourneert een array die alle elementen van `array1` bevat die niet bestaan in `array2` , en alle elementen van `array2` die niet bestaan in `array1` .

>[!BEGINSHADEBOX]

**Voorbeelden:**

Op basis van de volgende arrays:

```
myArray = [1,2,3,4,5]
```

```
yourArray = [3,4,5,6,7]
```

* `arrayDifference [myArray, yourArray, classic]`

  Retourneert `[1,2]`

* `arrayDifference [yourArray, myArray, classic]`

  Retourneert `[6,7]`

* `arrayDifference [myArray, yourArray, symmetric]`

  Retourneert `[1,2,6,7]`

>[!ENDSHADEBOX]

## dedupliceren

## Trefwoorden

## emptyarray
