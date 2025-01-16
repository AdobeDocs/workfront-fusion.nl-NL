---
title: Veelgestelde vragen over scenario-planning
description: De informatie in dit artikel kan handig zijn wanneer u scenario's begint te maken in Workfront Fusion.
author: Becky
feature: Workfront Fusion
exl-id: 6a1d672d-0bd7-4a3a-b96d-6d8b4c97522d
source-git-commit: 77ec3c007ce7c49ff760145fafcd7f62b273a18f
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Veelgestelde vragen over scenario-planning

De informatie in dit artikel kan handig zijn wanneer u scenario&#39;s begint te maken in Workfront Fusion.

## Wat is een scenario?

### Antwoord

Een scenario definieert een reeks stappen die door Adobe Workfront Fusion moet worden uitgevoerd. Voor elk scenario, specificeert u de gegevensbron, welke te gebruiken gegevens, en hoe de gegevens moeten worden verwerkt. Met Fusion kunt u eenvoudige of complexe scenario&#39;s maken die voldoen aan de gebruiksscenario&#39;s voor uw organisatie.

Voor meer informatie over scenario&#39;s, zie [ Overzicht Scenario ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/scenario-overview.md).

## Hoeveel modules kan ik in een scenario gebruiken?

### Antwoord

U kunt zoveel modules gebruiken als u in een scenario wilt. U kunt modules in routes scheiden, en kunt specificeren welke gegevens door elke route zouden moeten stromen. U kunt de output van één module als input aan een andere module ook gebruiken.

Hoewel er geen grens aan het aantal modules in een scenario is, kunnen meer dan 150 modules scenario prestaties beïnvloeden.

Voor meer informatie over modules, zie [ Overzicht van de Module ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).

## Kan [!DNL Workfront Fusion] werken met bestanden?

### Antwoord

Ja. Workfront Fusion kan bestanden ontvangen, opslaan, transformeren, converteren en versleutelen. Fusion biedt ook een groot aantal ingebouwde functies die zijn ontworpen om gebruikers in staat te stellen effectief en creatief te werken met de gegevens in de bestanden.

Voor meer informatie bij het werken met dossiers in Fusion, zie [ een dossier tussen modules ](/help/workfront-fusion/create-scenarios/map-data/map-files.md) in kaart brengen.

## Bij sommige triggers kunnen scenario&#39;s direct worden uitgevoerd. Wat betekent &#39;onmiddellijk&#39;?

### Antwoord

Scenario&#39;s kunnen met intervallen volgens het programma lopen u, zoals elk uur of om de 5 minuten specificeert. Er zijn speciale triggers, ook wel &#39;instant triggers&#39; genoemd, die uw scenario direct kunnen starten nadat ze gegevens van een bepaalde service ontvangen. De fusie verwerkt de ontvangen gegevens onmiddellijk, zonder op de volgende geplande looppas te wachten.

Voor meer informatie over het verschil tussen gepolled en onmiddellijke trekkers, zie {de modules van de Trigger ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#trigger-modules) in het overzicht van de artikelmodule.[

## Wat is een operatie?

### Antwoord

Een verrichting is om het even welke die taak door een module wordt uitgevoerd. Een bewerking vindt bijvoorbeeld altijd plaats wanneer een trigger wordt uitgevoerd en telkens wanneer een handeling een taak uitvoert.

Sommige plannen van de Fusie zijn gebaseerd op het aantal verrichtingen uw organisatie gebruikt.

Voor meer informatie over verrichtingen, zie [ Verrichtingen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/operations-in-workfront-fusion.md).

## Wat is gegevensoverdracht?

### Antwoord

De overdracht van gegevens verwijst naar de hoeveelheid gegevens die door uw scenario wordt overgebracht. Bijvoorbeeld, een scenario dat een beeld 100KB van Workfront terugwint, dan uploadt het beeld aan een leverancier van de documentopslag. De hoeveelheid gegevens die in dit scenario wordt gebruikt, is 200 kB.

## Wat is een verbinding?

### Antwoord

Een verbinding is de koppeling tussen uw [!DNL Workfront Fusion] -account en de service van derden die u wilt gebruiken. De verbinding kan worden tot stand gebracht wanneer het uitgeven van een scenario.

Voor meer informatie, zie [ Overzicht van de Verbinding ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/connection-overview.md).

## Wat zijn aggregators?

### Antwoord

Met een [!UICONTROL Aggregator] worden gegevens samengevoegd in één verzameling. Een voorbeeld hiervan zijn bestanden die worden gecomprimeerd in een zip-archief en als e-mailbijlage worden verzonden.

Zie [[!UICONTROL Aggregator] module ](/help/workfront-fusion/references/modules/aggregator-module.md) voor meer informatie.

## Wat gebeurt er als ik [!DNL Workfront Fusion] een e-mailbericht met meerdere bijlagen laat verwerken?

### Antwoord

Als u de [!UICONTROL Email] module [!UICONTROL Retrieve attachments] gebruikt, wordt elke gehechtheid verzonden individueel door de rest modules in het scenario. Soortgelijke modules zijn ook beschikbaar in andere apps die meerdere bestanden tegelijk ontvangen.
