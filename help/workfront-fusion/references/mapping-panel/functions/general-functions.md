---
title: Algemene functies
description: De volgende algemene functies zijn beschikbaar in het Adobe Workfront Fusion-toewijzingspaneel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 295004ab7536b85124bc366d6832c08365338d08
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# Algemene functies

## Variabelen

Er zijn twee algemene variabelen die u kunt gebruiken om details over een uitvoering te identificeren:

* `executionID`: the ID of this scenario execution
* `triggerTimestamp`: The time at which this execution was triggered

## [!UICONTROL get (object or array; path)]

Returns the value path of an object or array. To access nested objects, use dot notation. The first item in an array is index 1.

>[!BEGINSHADEBOX]

**Examples:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

Returns the `value1` if the expression is evaluated to true; otherwise it returns the `value2`.

Als u een if-instructie wilt maken die alleen een waarde retourneert wanneer twee of meer expressies worden geëvalueerd op true, gebruikt u het trefwoord `and` .

Gebruik de operatoren `and` en `or` om `if` -instructies te combineren.

![ en exploitant ](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `if( 1 = 1 ; A ; B )`

  Retourneert A

* `if( 1 = 2 ; A ; B )`

  Returns B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Returns B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

Returns the `value1` if this value is not empty; otherwise it returns the `value2`.

>[!BEGINSHADEBOX]

**Examples:**

* `ifempty(` `A` `;` `B` )

  Retourneert A

* `ifempty(` `unknown` `;` `B`

  Retourneert B

* `ifempty(` `""` `;` `B`

  Retourneert B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

Evalueert één waarde (de expressie genoemd) met een lijst van waarden; retourneert het resultaat dat overeenkomt met de eerste overeenkomende waarde. To include an  `else` value, add it after the final expression or value.

>[!BEGINSHADEBOX]

**Examples:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Returns 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Returns 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Returns 4

  In this function, 4 is the value to be returned if no expressions apply (the `else` value).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Omits the given keys of the object and returns the rest.

>[!BEGINSHADEBOX]

**Voorbeeld:**

`omit(` Gebruiker `;` password `)`

Retourneert een verzameling van de gegevens van de gebruiker, exclusief het wachtwoord.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Hiermee worden alleen de opgegeven toetsen van het object geselecteerd.

>[!BEGINSHADEBOX]

**Voorbeeld:**

`pick(` User `;` password `;` email `)`

Returns a collection of only the user&#39;s password and email address.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

Merges two collections by combining their key-value pairs. If both collections contain the same key, the value from the second collection overwrites that value from the first collection.
