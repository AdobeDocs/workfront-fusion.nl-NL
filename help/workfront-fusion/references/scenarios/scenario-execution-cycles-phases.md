---
title: Scenario-uitvoering, cycli en fasen
description: Dit artikel beschrijft gebeurtenissen die voorkomen terwijl een  [!DNL Adobe Workfront Fusion]  scenario, zoals initialisering, verrichtingen, begaat, en terugdraaiversies loopt.
author: Becky
feature: Workfront Fusion
exl-id: abf41be5-df32-4eaf-b3f4-93ddf005bfe3
source-git-commit: fe503c27bc4e3beb5645f0efa7c2097297f19190
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Uitvoering, cycli en fasen van scenario

Elke scenario-uitvoering begint met de initialisatiefase, gaat verder met ten minste één cyclus die bestaat uit de fasen operation en commit/rollback, en eindigt met de eindfase

* Initialisatie
* Cyclus 1
   * Bewerking (lezen of schrijven)
   * Vastleggen of terugdraaien
* Cyclus 2
   * Bewerking (lezen of schrijven)
   * Vastleggen of terugdraaien
* ...
* Cyclus #n
   * Bewerking (lezen of schrijven)
   * Vastleggen of terugdraaien
* Voltooiing

Op kleinere schaal volgt elke module ook deze fasen. De informatie over de modulefasen kan in de verwerkte bundelinformatie worden gevonden, die in de genummerde bel aan het hoogste recht van elke module wordt gevonden nadat het scenario in werking is gesteld. Voor meer informatie bij het lokaliseren van verwerkte bundelinformatie, zie [ Informatie over verwerkte bundels ](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md#information-about-processed-bundles) in de de uitvoeringsstroom van het artikelscenario.

De informatie over de grotere scenario fasen kan in de uitvoeringsdetails worden gevonden.

## Uitvoeringsfasen van scenario

### Initialisatie

Tijdens de initialisatiefase, worden alle noodzakelijke verbindingen (verbinding aan een gegevensbestand, e-maildienst, etc.) gecreeerd en gecontroleerd om ervoor te zorgen dat de module de voorgenomen verrichtingen kan uitvoeren.

### Cycli

Elke cyclus vertegenwoordigt een ondeelbare eenheid van het werk die uit een reeks verrichtingen, elk met wordt samengesteld of terugschroeven van prijzen.

U kunt het maximum aantal cycli instellen in het deelvenster [!UICONTROL scenario settings] . Het standaardnummer is 1.

* [Bewerking](#operation)
* [Vastleggen](#commit)
* [Terugdraaien](#rollback)

#### Bewerking

Tijdens de exploitatiefase wordt een lees- of schrijfbewerking uitgevoerd:

* Een lezingsverrichting bestaat uit het verkrijgen van gegevens van de dienst die dan door andere modules volgens een vooraf bepaald scenario wordt verwerkt. De module [!UICONTROL Workfront] > [!UICONTROL Watch records] retourneert bijvoorbeeld nieuwe bundels (records) die zijn gemaakt sinds de laatste uitvoering van het scenario.
* Een schrijfbewerking bestaat uit het verzenden van gegevens naar een bepaalde dienst voor verdere verwerking. De module [!DNL Workfront] > [!UICONTROL Upload Document] uploadt bijvoorbeeld een bestand naar Workfront.

#### Vastleggen

Als de verrichtingsfase succesvol is, begaat fase waarin alle die verrichtingen door de modules worden uitgevoerd worden begaan. Dit betekent dat [!DNL Workfront Fusion] informatie over het succes van de bewerkingsfase naar alle services stuurt die bij de bewerkingsfase zijn betrokken.

### Terugdraaien

Als een fout tijdens de verrichting voorkomt of fase op om het even welke module begaan, wordt de fase geaborteerd en de terugdraaiingsfase is begonnen, makend alle verrichtingen tijdens de bepaalde cyclusleegte.

>[!IMPORTANT]
>
>Alle [!DNL Workfront Fusion] -modules die rollback (ook wel transactie genoemd) ondersteunen, worden gemarkeerd met de ACID-tag.
>
>![](assets/acid-modules.png)
>
>Modules die niet met deze tag zijn gemarkeerd, kunnen niet worden teruggezet naar de oorspronkelijke status wanneer er fouten optreden in andere modules. Een typisch voorbeeld van een niet-ACID module is de [!UICONTROL Email] > [!UICONTROL Send an Email] actie. Nadat het e-mailbericht is verzonden, kunt u het verzenden niet meer ongedaan maken.

### Voltooiing

Tijdens de afwerkingsfase worden open verbindingen (bijvoorbeeld FTP-verbindingen, databaseverbindingen, enzovoort) gesloten en wordt het scenario voltooid.

## Bronnen

Voor meer informatie, zie [ scenario montages ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen.
