---
title: Methoden van HTTP-aanvragen
description: Wanneer u een API vraag in een module vormt, moet u de HTTP- verzoekmethode selecteren. In dit artikel worden de beschikbare methoden beschreven en wordt uitgelegd waarom u elke methode wilt selecteren.
author: Becky
feature: Workfront Fusion
exl-id: 481131c9-356a-4c62-a653-d6bba9be5be8
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Methoden van HTTP-aanvragen

Wanneer u een API vraag in een module vormt, moet u de HTTP- verzoekmethode selecteren. In dit artikel worden de beschikbare methoden beschreven en wordt uitgelegd waarom u elke methode wilt selecteren.

## HTTP-methoden

Gebruik een van de volgende HTTP-methoden.

* **[!UICONTROL GET]**: haalt gegevens op van een webserver op basis van uw parameters. [!UICONTROL GET] vraagt om een representatie van de opgegeven bron en ontvangt een [!UICONTROL 200 OK] -antwoordbericht met de aangevraagde inhoud als dit gelukt is.
* **[!UICONTROL POST]**: verzendt gegevens naar een webserver op basis van uw parameters. [!UICONTROL POST] -aanvragen bevatten handelingen zoals het uploaden van een bestand. Meerdere [!UICONTROL POST]&#39;s kunnen resulteren in een ander resultaat dan één [!UICONTROL POST] . Wees daarom voorzichtig met het onbedoeld verzenden van meerdere [!UICONTROL POST] s. Als een [!UICONTROL POST] is gelukt, ontvangt u een [!UICONTROL 200 OK] antwoordbericht.
* **[!UICONTROL PUT]**: verzendt gegevens naar een locatie op de webserver op basis van uw parameters. [!UICONTROL PUT] -aanvragen bevatten handelingen zoals het uploaden van een bestand. Het verschil tussen a [!UICONTROL PUT] en [!UICONTROL POST] is dat PUT epidemisch is, wat betekent dat het resultaat van één succesvolle [!UICONTROL PUT] hetzelfde is als veel identieke [!UICONTROL PUT] s. Als een PUT succesvol is, ontvangt u een 200 reactiebericht (gewoonlijk 201 of 204).
* **[!UICONTROL PATCH]**: (Niet beschikbaar voor sommige API-callmodules) Hiermee past u op basis van uw parameters gedeeltelijke wijzigingen toe op een bron op een webserver. [!UICONTROL PATCH] is niet dekkend, wat betekent dat het resultaat van meerdere [!UICONTROL PATCH] &#39;&#39;s onbedoelde gevolgen kan hebben. Als een [!UICONTROL PATCH] is gelukt, ontvangt u een 200-antwoordbericht (meestal 204).
* **[!UICONTROL DELETE]**: verwijdert de opgegeven bron van de webserver op basis van uw parameters (als de bron bestaat). Als een [!UICONTROL DELETE] is gelukt, ontvangt u een 200 OK-antwoordbericht.
