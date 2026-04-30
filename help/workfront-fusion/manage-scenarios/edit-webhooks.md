---
title: Webhaken bewerken
description: U kunt bestaande websites bewerken voor de Workfront- en Workfront-planningsconnectors.
author: Becky
feature: Workfront Fusion
source-git-commit: 2561c911b9b542a7b143fae745baf4e1de45be38
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Webhaken bewerken

U kunt bestaande webhaken bewerken. De scenario&#39;s die deze webhooks gebruiken zullen de nieuwe configuratie gebruiken die zich door:bewegen, die de behoefte elimineert om een nieuwe webhaak tot stand te brengen en het manueel toe te wijzen aan alle beïnvloede scenario&#39;s.

Webhaken kunnen alleen voor de volgende connectors worden bewerkt:

* Workfront
* Workfront Planning

>[!IMPORTANT]
>
>Houd rekening met het volgende wanneer u een webhaak bijwerkt:
>
>* De bewerkte webhaak wordt door Workfront-gebeurtenisabonnementen behandeld als een nieuw abonnement. De abonnementsgeschiedenis van gebeurtenissen blijft niet behouden voor de vorige webhaakconfiguratie, omdat dit wordt beschouwd als een apart gebeurtenisabonnement.
>* De overgang van oud naar nieuw gebeurtenisabonnement is mogelijk niet perfect gesynchroniseerd. Het is daarom mogelijk om een gebeurtenis tweemaal te ontvangen (als het nieuwe abonnement begint te lopen vóór de oude wordt gestopt) of om een gebeurtenis te missen (als het oude abonnement stopt voordat het nieuwe abonnement begint te lopen).

## Webhaak bewerken

U kunt webhaken bewerken vanuit een scenario of vanuit de lijst Webhooks.

### Webhaak in een scenario bewerken

>[!NOTE]
>
>Deze functionaliteit is alleen beschikbaar voor scenario&#39;s met een Workfront- of Workfront-planningsinstant-triggermodule.

1. Ga naar het scenario dat de webhaak omvat u wilt uitgeven.
1. In de de trekkermodule van het scenario, klik dropdown naast het gebied van de Webhaak, en selecteer **geef punt** uit.

   Het de configuratievenster van de website opent, bevolkt met de bestaande configuratie.

1. Breng de gewenste wijzigingen in de webhaak aan.
1. Klik **sparen** om webhaak te bewaren en aan de module terug te keren.

### Webhaak bewerken in de lijst Webhaken

1. In de linkernavigatie, uitgezochte **Webhooks** ![&#x200B; pictogram Webhooks &#x200B;](assets/webhooks-icon.png).
1. Klik op het selectievakje naast de webhaak die u wilt bewerken.
1. In de blauwe banner bij de bodem van het scherm, geeft de klik **&#x200B;**&#x200B;uit.
1. Breng de gewenste wijzigingen in de webhaak aan.
1. Klik **sparen** om Webhaak te bewaren en aan de lijst van Webhaken terug te keren.

