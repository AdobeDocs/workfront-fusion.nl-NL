---
content-type: overview
title: Stroom uitvoering scenario
description: In dit artikel wordt uitgelegd hoe een scenario wordt uitgevoerd en hoe de gegevens erin stromen. Hier wordt ook uitgelegd waar u informatie kunt vinden over uw verwerkte gegevens en hoe u deze kunt lezen.
author: Becky
feature: Workfront Fusion
exl-id: bd4f05e2-df3c-4848-9a70-3df18ca4461b
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Uitvoeringsstroom van scenario

Dit artikel verklaart hoe een scenario uitvoert en hoe de gegevens door het stromen, en hoe te om de gegevens te bekijken die door elke module worden verwerkt.

Om te bekijken hoe de gegevens door een actief scenario stromen, zie [&#x200B; gegevensstroom van de Mening in een lopend scenario &#x200B;](/help/workfront-fusion/manage-scenarios/view-scenario-data-flow.md).

## Uitvoeringsstroom van scenario

Nadat een scenario opstelling correct en geactiveerd is, voert het volgens zijn bepaald programma uit.

Terwijl het scenario begint, reageert de eerste module op een gebeurtenis waarvoor deze is ingesteld. Wanneer gegevens worden geretourneerd, worden die gegevens in pakketten geplaatst. Het scenario retourneert één bundel voor elke gebeurtenis. Bijvoorbeeld, als een module wordt geplaatst om op kwesties te letten, zal het een bundel gegevens voor elke kwestie terugkeren het vindt.

Als de trekkermodule om het even welke bundels van gegevens terugkeert, gaan die bundels tot de volgende module over en het scenario gaat verder, die de bundels door elke opeenvolgende module, één voor één overgaan.

Als de bundels correct door alle modules verwerken, is het scenario duidelijk als succes in de pagina van de scenariodetails.

### Voorbeeld: [!UICONTROL Workfront Fusion for Work Automation]

>[!BEGINSHADEBOX]

**Voorbeeld:** In dit scenario dat de horloges voor inkomende verzoeken in Workfront en dan hen in de projecten van Workfront omzet, zouden de gegevens als volgt stromen:

De eerste stap van het scenario, die door de eerste module wordt uitgevoerd, moet op verzoeken letten. Elk verzoek dat het vindt wordt beschouwd als één bundel. Als de module zonder enige bundels loopt te vinden, beëindigt het scenario na de eerste module.

Als de eerste module een bundel terugkeert, gaat de bundel door de rest van het scenario. In dit voorbeeld, zou de bundel naar de tweede module gaan, die het verzoek in een project omzet.

![&#x200B; stroom van de Uitvoering van het scenario van Workfront &#x200B;](assets/example-execution-flow-wf-only.png)

>[!ENDSHADEBOX]

### Voorbeeld: [!UICONTROL Workfront Fusion for Work Automation and Integration]

>[!BEGINSHADEBOX]

**Voorbeeld:** In dit scenario dat documenten van Adobe Workfront downloadt en hen naar een omslag in [!DNL Dropbox] verzendt, zouden de gegevens als volgt stromen:

De eerste stap van het scenario, die door de eerste module wordt uitgevoerd, is op documenten in Workfront te letten. Elk document dat het vindt wordt beschouwd als één bundel. Als de module zonder enige bundels loopt te vinden, beëindigt het scenario na de eerste module.

Als een bundel is teruggekeerd, gaat de bundel door de rest van het scenario. In dit voorbeeld bestaat de rest van het scenario uit de tweede module, die de bundel naar de [!DNL Dropbox] -map uploadt.

![&#x200B; stroom van de Uitvoering van integratiescenario &#x200B;](assets/example-execution-flow-wf-dropbox.png)

Als de eerste module meerdere bundels retourneert, wordt de eerste bundel geüpload naar [!DNL Dropbox] voordat de tweede bundel wordt geüpload. Vervolgens uploadt de tweede bundel, vervolgens de derde, enzovoort.

>[!ENDSHADEBOX]

## Informatie over verwerkte pakketten

Voor elke module, gaat de bundel door een proces in vier stappen alvorens naar de volgende module te gaan of zijn definitieve bestemming te bereiken.

* Initialisatie
* Bewerking
* Vastleggen/Terugdraaien
* Voltooiing

>[!NOTE]
>
>Het grotere scenario gaat ook door dit proces. Voor informatie over dit proces op het scenario niveau, zie [&#x200B; uitvoering Scenario, cycli, en fasen &#x200B;](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Nadat een scenario looppas volledig is, toont elke module een pictogram dat het aantal uitgevoerde verrichtingen toont. U kunt op dit pictogram klikken om de gedetailleerde informatie over de verwerkte bundels voor elke stap in het proces weer te geven. U kunt zien welke modulemontages werden gebruikt, en welke bundels door elke module werden teruggekeerd.

![&#x200B; Verwerkte bundels &#x200B;](assets/Info-processed-bundles.png)

In dit voorbeeld ontving de module inputinformatie zoals:

* De id van de uitgave die is gevonden
* Het object waarnaar de uitgave wordt geconverteerd (Project)
* Id van het malplaatje het zal gebruiken om het project tot stand te brengen
* Het recordtype van het gevonden object (OPTASK, een uitgave)

Na verwerking retourneerde de module deze uitvoerinformatie:

* Id van het nieuwe project.

Als de module meer dan één probleem heeft gevonden, wordt de informatie voor elke bundel afzonderlijk vastgelegd. Bewerking 2 heeft dan een gebied met invoer- en uitvoersecties die de tweede bundel beschrijven, enzovoort.

## Fouten bij het uitvoeren van een scenario

Er kan een fout optreden tijdens het uitvoeren van het scenario. Bijvoorbeeld, als u het malplaatje hebt geschrapt dat de module zal gebruiken om het nieuwe project tot stand te brengen, eindigt het scenario met een foutenmelding. Voor meer informatie over hoe te om fouten te behandelen, zie [&#x200B; de types van Fout &#x200B;](/help/workfront-fusion/references/errors/error-processing.md).

## Bronnen

* Voor meer informatie bij vestiging ziet een scenario, [&#x200B; de scenarioredacteur &#x200B;](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-editor.md).
* Voor meer informatie over de pagina van de scenario details, zie {de details van 0} Scenario [.](/help/workfront-fusion/get-started-with-fusion/navigate-fusion/scenario-details.md)
* Voor meer informatie bij het activeren van een scenario, zie [&#x200B; een scenario &#x200B;](/help/workfront-fusion/manage-scenarios/activate-deactivate-scenarios.md) activeren of deactiveren.
* Voor meer informatie bij het plannen van een scenario, zie [&#x200B; Plan een scenario &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).
* Voor meer informatie over modules, zie [&#x200B; Overzicht van de Module &#x200B;](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md).
