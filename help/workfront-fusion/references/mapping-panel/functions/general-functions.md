---
title: Algemene functies
description: De volgende algemene functies zijn beschikbaar in het Adobe Workfront Fusion-toewijzingspaneel.
author: Becky
feature: Workfront Fusion
exl-id: 6d4b8801-aa7e-47d4-80b3-aceac10c073f
source-git-commit: 2c732659f3f3e81e13b7b12a5df5bde19c0e0928
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Algemene functies

## [!UICONTROL get (object or array; path)]

Retourneert het waardepad van een object of array. Gebruik puntnotatie om geneste objecten te openen. Het eerste item in een array is index 1.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `get( array ; 1 + 1 )`
* `get( array ; 5.raw_name )`
* `get( object ; raw_name )`
* `get( object ; raw_name.sub_raw_name )`

>[!ENDSHADEBOX]

## [!UICONTROL if (expression; value1; value2)]

Retourneert `value1` als de expressie wordt geëvalueerd op true; anders wordt de `value2` geretourneerd.

Als u een if-instructie wilt maken die alleen een waarde retourneert wanneer twee of meer expressies worden geëvalueerd op true, gebruikt u het trefwoord `and` .

Gebruik de operatoren `and` en `or` om `if` -instructies te combineren.

![ en exploitant ](assets/and-in-if-statement.png)

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `if( 1 = 1 ; A ; B )`

  Retourneert A

* `if( 1 = 2 ; A ; B )`

  Retourneert B

* `if( 1 = 2 and 1 = 2 ; A ; B )`

  Retourneert B

>[!ENDSHADEBOX]

## [!UICONTROL ifempty (value1; value2)]

Retourneert de waarde `value1` als deze waarde niet leeg is; anders wordt de waarde `value2` geretourneerd.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `ifempty(` `A` `;` `B`

  Retourneert A

* `ifempty(` `unknown` `;` `B`

  Retourneert B

* `ifempty(` `""` `;` `B`

  Retourneert B

>[!ENDSHADEBOX]

## [!UICONTROL switch (expression; value1; result1; [value2; result2; ...]; [else])]

Evalueert één waarde (de expressie genoemd) met een lijst van waarden; retourneert het resultaat dat overeenkomt met de eerste overeenkomende waarde. Als u een `else` -waarde wilt opnemen, voegt u deze waarde toe na de laatste expressie of waarde.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* `switch( B ; A ; 1 ; B ; 2 ; C ; 3 )`

  Retourneert 2

* `switch( C ; A ; 1 ; B ; 2 ; C ; 3 )`

  Retourneert 3

* `switch( X ; A ; 1 ; B ; 2 ; C ; 3 ; 4 )`

  Retourneert 4

  In deze functie is 4 de waarde die moet worden geretourneerd als er geen expressies van toepassing zijn (de `else` waarde).

>[!ENDSHADEBOX]

## [!UICONTROL omit(object; key1; [key2; ...])]

Hiermee worden de opgegeven sleutels van het object weggelaten en wordt de rest geretourneerd.

>[!BEGINSHADEBOX]

**Voorbeeld:**

`omit(` Gebruiker `;` password `)`

Retourneert een verzameling van de gegevens van de gebruiker, exclusief het wachtwoord.

>[!ENDSHADEBOX]

## [!UICONTROL pick(object; key1; [key2; ...])]

Hiermee worden alleen de opgegeven toetsen van het object geselecteerd.

>[!BEGINSHADEBOX]

**Voorbeeld:**

`pick(` E-mail met het `;` wachtwoord `;` van de gebruiker `)`

Retourneert alleen een verzameling van het wachtwoord en het e-mailadres van de gebruiker.

>[!ENDSHADEBOX]

## mergeCollections(collection1; collection2)

Voegt twee verzamelingen samen door hun sleutel-waarde paren te combineren. Als beide verzamelingen dezelfde sleutel bevatten, overschrijft de waarde van de tweede verzameling die waarde van de eerste verzameling.
