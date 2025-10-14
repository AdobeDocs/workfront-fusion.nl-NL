---
title: Math-variabelen
description: De volgende wiskundige variabelen zijn beschikbaar in het  [!DNL Adobe Workfront Fusion mapping]  paneel.
author: Becky
feature: Workfront Fusion
exl-id: b309f035-4d46-473b-b915-6938587b0bcf
source-git-commit: 3aa896867bd143c67157fb886fafa37eaee2bc00
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# Math-variabelen

## pi

Vertegenwoordigt het wiskundige symbool $\pi$.

## [!UICONTROL random]

Retourneert een pseudo-willekeurig getal met drijvende komma in het bereik [`0` , `1`] (inclusief `0` , maar niet `1` ).

Gebruik de volgende formule om een geheel pseudo-willekeurig aantal in de waaier [`min`, `max`] (met inbegrip van zowel `min` als `max`) te produceren:

![&#x200B; Willekeurig &#x200B;](assets/math-variable-random-350x61.png)

```
floor(random * (1.max - 1.min + 1)) + 1.min
```
