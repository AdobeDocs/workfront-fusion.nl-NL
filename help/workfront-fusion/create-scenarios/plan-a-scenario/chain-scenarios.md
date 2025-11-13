---
title: Meerdere scenario's met ketens samenvoegen
description: U kunt scenario's samen ketenen, toestaand één scenario om een ander teweeg te brengen, en de gegevensoutput door het tweede scenario aan het eerste terug te keren.
author: Becky
feature: Workfront Fusion
exl-id: def8d4c1-fc20-4b93-b1fd-be2f60300464
source-git-commit: 7f73007e219714c38dd0cf29d2a1e3a4c8f6f3cc
workflow-type: tm+mt
source-wordcount: '1247'
ht-degree: 0%

---

# Meerdere scenario&#39;s samenvoegen

>[!NOTE]
>
>Deze functie is momenteel in Beta.

U kunt scenario&#39;s samen ketenen, toestaand één scenario om een ander teweeg te brengen, en de gegevensoutput door het tweede scenario aan het eerste terug te keren. Dit staat meer modulaire scenario verwezenlijking toe, waar u geen scenario secties in veelvoudige scenario&#39;s moet dupliceren.

U kunt veelvoudige kindscenario&#39;s van een ouderscenario roepen, en u kunt een kindscenario van veelvoudige ouderscenario&#39;s roepen. U kunt kindscenario&#39;s ook nesten, roepend één van een andere.

Wanneer een ouderscenario op een kindscenario wacht om gegevens terug te keren, telt die tijd niet tegen de onderbreking van het ouderscenario. Bijvoorbeeld, roept een ouderscenario 5 kindscenario&#39;s, elk waarvan 10 minuten om vergt te lopen, voor een totaal van 50 minuten. De modules in het ouderscenario zelf vergen 15 minuten om te lopen. Het bovenliggende scenario heeft geen time-out, ook al is er in totaal 65 minuten verstreken, wat meer is dan de time-outlimiet van 40 minuten.

Voor meer informatie over de prestatiesbegeleiding van Fusion, met inbegrip van onderbrekingen, zie [ de prestatiesgidsen van de Fusie ](/help/workfront-fusion/references/scenarios/fusion-performance-guardrails.md).

Voor instructies bij het vormen van de modules van de Keten, zie [ modules van de Keten ](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

## Bovenliggende en onderliggende scenario&#39;s

* Het **ouder** scenario roept een ander scenario, gebruikend de **Keten** > **Vraag een van het kindscenario** module. Het ontvangt de output van het kindscenario, dat het in recentere scenario modules kan verwerken.
* Het **kind** scenario wordt geroepen door het ouderscenario. Zijn trekkermodule ontvangt gegevens van het ouderscenario, en keert output aan het ouderscenario terug.

Het ouderscenario vereist een reactie van het kindscenario. De scenario&#39;s van het kind die geen gegevens terugkeren worden momenteel niet gesteund.

## Gegevensstructuren in kettingscenario&#39;s

Workfront Fusion gebruikt gegevensstructuren om informatie van het ouderscenario naar het kindscenario over te brengen. De gegevensstructuur wordt gevormd in het kindscenario. Wanneer het kindscenario van het ouderscenario wordt geselecteerd, verschijnen de gebieden voor de gegevensstructuur die als input van het kindscenario wordt gebruikt in het ouderscenario. U kunt waarden toewijzen aan deze velden, die worden doorgegeven aan het onderliggende scenario wanneer dit wordt geactiveerd.

Voor informatie over de modules om in de ouder en kindscenario&#39;s te vormen, zie [ modules van de Keten ](/help/workfront-fusion/references/apps-and-modules/tools-and-transformers/chain-modules.md).

Voor informatie over gegevensstructuren, zie [ structuren van Gegevens ](/help/workfront-fusion/references/mapping-panel/data-types/data-structures.md).

## Gegevensstroom

1. De gegevens stromen door het ouderscenario.
1. De gegevens bereiken de Vraag een module van het kindscenario. De gegevens worden in kaart gebracht aan de gebieden in Vraag een module van het kindscenario, die de gebieden in de gegevensstructuur aanpassen die in de de trekkermodule van het kindscenario wordt gebruikt.
1. De gegevens van Vraag een kindscenario worden overgegaan tot het kindscenario.
1. Het kindscenario verwerkt gegevens en voert acties uit.
1. Het kindscenario beëindigt met de reactie van de Terugkeer op oudermodule.
1. De output van de reactie van de Terugkeer op oudermodule wordt overgegaan tot het ouderscenario.
1. De output van Vraag een kindscenario is de output van het kindscenario. Deze output kan later in het ouderscenario worden verwerkt.

## Gebruik hoofdletters

Overweeg de volgende voorbeelden gebruiksgevallen voor het ketenen van scenario&#39;s:

* **Herbruikbare logica**: U kunt scenario voor herhaalde acties ketenen die over veelvoudige scenario&#39;s worden gebruikt. Bijvoorbeeld, als u veelvoudige scenario&#39;s hebt die inhoud archiveren, kunt u één enkel kindscenario tot stand brengen genoemd &quot;inhoud van het Archief&quot;die u als kindscenario voor om het even welke werkschema&#39;s kunt dan gebruiken die inhoud archiveren.

* **Fout die** behandelt: Het is gemeenschappelijk voor organisaties om de zelfde fout behandelende acties over veelvoudige scenario&#39;s, zoals een fout behandelende route te hebben die een foutenlogboek naar een gegevensopslag verzendt en tot een slack bericht leidt. U kunt een kindscenario met deze acties en ketting tot stand brengen dat scenario in fout behandelende routes in veelvoudige scenario&#39;s.

* **Uitbreidende tijd**: U kunt het ketenen voor grote partijverrichtingen met lange lopende acties, zoals gebruiken wanneer u om dossiers uit te voeren en in te voeren. Deze bewerking duurt even als er veel bestanden zijn. Omdat de kindscenario&#39;s niet tegen de onderbreking van het ouderscenario tellen, kunt u uitvoeringstijd overschrijden door veelvoudige kindscenario&#39;s te gebruiken om de dossiers uit te voeren of in te voeren.

* **die iterators** vervangt iterators met kindscenario&#39;s kan geheugengebruik, zoals in complexe verrichtingen in een herhaling verminderen die uit de fout van het Geheugen veroorzaakt. U kunt een afzonderlijk scenario voor de complexe verrichting tot stand brengen en de iterator met Vraag een module van het kindscenario vervangen

* **Onderzoek naar en creeer een verslag**: Bijvoorbeeld, kon u een scenario tot stand brengen dat naar een gebruiker zoekt. Als zij bestaan, voegt het scenario hen als fiatteur met toegang toe zij moeten herzien en goedkeuren. Als zij niet bestaan, leidt het scenario tot een verzoek om admin aan boord een nieuwe gebruiker.

## Uitvoeringshistorie weergeven voor kettingscenario&#39;s

U kunt uitvoeringshistorie voor geketende scenario&#39;s bekijken door de geschiedenis van elk scenario te bekijken inbegrepen in de ketting. Bijvoorbeeld, zou de de uitvoeringsgeschiedenis van het ouderscenario informatie over modules en gegevens omvatten die direct in het ouderscenario worden verwerkt. Om uitvoeringsgeschiedenis voor modules en gegevens te bekijken die in een kindscenario worden verwerkt, open het kindscenario en bekijk de uitvoeringsgeschiedenis daar.

Wij adviseren gebruikend **ga naar de knoop van het kindscenario** in Vraag een module van het kindscenario om snel naar het kindscenario te gaan, waar u zijn uitvoeringsgeschiedenis kunt bekijken. Het kindscenario opent in een ander browser venster, dat u toestaat om ouder en kindscenario&#39;s tezelfdertijd te zien.

![ ga naar de knoop van het kindscenario ](assets/go-to-the-child-button.png)

## Fouten en onvolledige uitvoering

### Foutafhandeling

Als de fouten van het kindscenario uit, dat het krijgen van gegevens terug naar uw ouder kan beïnvloeden.

Wij adviseren vormend fout behandeling in het kindscenario om ervoor te zorgen dat als iets in het kindscenario verkeerd gaat, het ouderscenario niet geplakt wachtend op de reactie van het kindscenario.

## Aanbevolen procedures

Overweeg de volgende beste praktijken wanneer het ketenen van een scenario.

### Vermijd herhaling bij kettingscenario&#39;s

Recursie treedt op wanneer een scenario een nieuwe uitvoering van zich teweegbrengt, die een nieuwe uitvoering, etc. in een oneindige lijn teweegbrengt.

De recursie kan prestatieskwesties voor zowel de organisatie veroorzaken die het recursieve scenario, als aan andere organisaties bezit.

Wanneer het ketenen van scenario&#39;s, volg deze praktijken om recursie te vermijden:

* Zorg ervoor dat **kindscenario&#39;s niet het ouderscenario** kunnen teweegbrengen. Bijvoorbeeld, als een ouderscenario wordt teweeggebracht wanneer een verzoek wordt gecreeerd, zorg ervoor dat de kindscenario&#39;s geen verzoeken creëren.
* Zorg ervoor dat **kindscenario&#39;s elkaar** niet roepen. Bijvoorbeeld, als kindscenario A kindscenario B roept, zorg ervoor dat kindscenario B geen kindscenario A roept.
* Zorg ervoor dat **een scenario zich** niet kan roepen. Bijvoorbeeld, wordt een scenario teweeggebracht wanneer een taak wordt gecreeerd, en dat scenario leidt tot twee taken. De nieuw gecreëerde taken allebei teweegbrengen opnieuw het scenario teweeg, dat vier nieuwe taken creeert. Telkens als een taak wordt gecreeerd, wordt het scenario teweeggebracht, en telkens als het scenario loopt, verdubbelt het aantal taken. Het aantal taken groeit exponentieel.

>[!IMPORTANT]
>
>* **wanneer een scenario recursie veroorzaakt, wordt het gedeactiveerd door het technische team van de Fusie om verdere prestatieskwesties te verhinderen.**
>* Omdat de recursie een resultaat van scenario ontwerp is, moet u uw scenario&#39;s op een manier ontwerpen die ervoor zorgt dat het scenario geen acties omvat die het scenario teweegbrengen.

### Foutafhandeling gebruiken om een reactie te garanderen

Omdat het ouderscenario op een reactie van het kindscenario wacht alvorens het kan verdergaan, moet u ervoor zorgen dat het kindscenario wordt gebouwd zodat het een reactie zal verstrekken zelfs als het een fout ontmoet.
