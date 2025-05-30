---
title: De uitvoeringsgeschiedenis van een scenario weergeven
description: U kunt informatie over de gebeurtenissen of de uitvoeringen van een scenario tonen, of u kunt alle uitvoeringen van het scenario voor specifieke gegevens zoeken.
author: Becky
feature: Workfront Fusion
exl-id: 974b32b4-d86a-48cd-a8d4-1ae2cf309b9b
source-git-commit: cc7c05614390e20d4051635c605e12dfa65493a1
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# De uitvoeringsgeschiedenis van een scenario weergeven

U kunt informatie over de gebeurtenissen of de uitvoeringen van een scenario tonen, of u kunt alle uitvoeringen van het scenario voor specifieke gegevens zoeken.

De uitvoering van een scenario vertegenwoordigt één uitvoering van het scenario.

Een scenario-gebeurtenis is een wijziging in het scenario, zoals bewerken, activeren of deactiveren.

>[!NOTE]
>
>De geschiedenis van een scenario toont alle gebeurtenissen en executies van een scenario voor de laatste 30 dagen.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront] package</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">[!DNL Adobe Workfront] licentie</td> 
   <td> <p>Nieuw: [!UICONTROL Standard]</p><p>of</p><p>Huidig: [!UICONTROL Work] of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!DNL Adobe Workfront Fusion] licentie**</td> 
   <td>
   <p>Huidig: Geen [!DNL Workfront Fusion] vereiste licentie.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] [!DNL Workfront] -abonnement: uw organisatie moet het abonnement aanschaffen [!DNL Adobe Workfront Fusion] .</li><li>[!UICONTROL Ultimate] [!DNL Workfront] abonnement: [!DNL Workfront Fusion] is opgenomen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet [!DNL Adobe Workfront Fusion] aanschaffen.</p>
   </td> 
  </tr>
  <tr data-mc-conditions=""> 
   <td role="rowheader">Configuraties op toegangsniveau*</td> 
   <td> 
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw organisatie zijn.</p>
     <p>U moet een [!DNL Workfront Fusion] beheerder voor uw team zijn.</p>
   </td> 
  </tr> 
   </td> 
  </tr> 
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [ vereisten van de Toegang in documentatie ](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over [!DNL Adobe Workfront Fusion] vergunningen, zie [[!DNL Adobe Workfront Fusion]  vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Geschiedenis van scenario&#39;s weergeven


### De scenario-geschiedenis van de mening op het lusje van de Geschiedenis

Het tabblad [!UICONTROL History] bevat meer details dan beschikbaar zijn op de pagina van [!UICONTROL Scenario detail] . U kunt de uitvoeringen ook filteren en sorteren op het tabblad [!UICONTROL History] .

1. Klik op de tab **[!UICONTROL Scenario]** in het linkerdeelvenster en klik vervolgens op het scenario.

   of

   Als u aan het scenario in de redacteur van het Scenario werkt, klik de linkerpijl ![ Uitgang die pijl ](assets/exit-editing-arrow.png) dichtbij de upper-left hoek van het venster uitgeeft.

1. Klik **Geschiedenis** dichtbij de naam van het scenario.
   ![ geschiedenislusje ](assets/history-tab.png)

   De volgende details zijn vermeld voor elke uitvoering van het scenario:

   * Datum waarop de bewerking is uitgevoerd **[!UICONTROL Started]**
   * Uitvoerings-id
   * **[!UICONTROL Status]** (geslaagd of mislukt)
   * Uitvoeren **[!UICONTROL Duration]**
   * Aantal **[!UICONTROL Operations]**
   * Grootte van **[!UICONTROL Data Transfer]**

   >[!NOTE]
   >
   >De scenario-geschiedenis toont a **badge van de a** Verwerking naast scenario&#39;s die onlangs hebben uitgevoerd, terwijl de uitvoeringsdetails aan opslag worden geschreven. De verwerking vindt onmiddellijk plaats nadat het scenario wordt uitgevoerd. en mag niet langer duren dan een paar minuten. Details van de uitvoering van het scenario zijn mogelijk niet zichtbaar terwijl de uitvoering wordt verwerkt.

1. Om details voor een specifieke scenario uitvoering te bekijken, klik **Details** in uiterst rechts. De koppeling [!UICONTROL details] is alleen zichtbaar als er details beschikbaar zijn voor de uitvoering.

   Voor meer informatie bij het bekijken van de details van de scenariouitvoering, zie [ Mening een specifieke scenario uitvoering ](/help/workfront-fusion/manage-scenarios/view-a-specific-scenario-execution.md).
1. Om gebeurtenissen te bekijken, knevel **gebeurtenissen** tonen aan.


### De de scenariogeschiedenis van de mening op de pagina van het Detail van het Scenario


1. Klik op de tab **[!UICONTROL Scenario]** in het linkerdeelvenster en klik vervolgens op het scenario.

   of

   Als u aan het scenario in de redacteur van het Scenario werkt, klik de linkerpijl ![ Uitgang die pijl ](assets/exit-editing-arrow.png) dichtbij de upper-left hoek van het venster uitgeeft.

1. Klik op de tab **[!UICONTROL History]** in het rechterdeelvenster.
1. (Optioneel) Klik op de uitvoering in het rechterdeelvenster voor gedetailleerde informatie over een geselecteerd scenario.

   Voor meer informatie bij verwerkingsbundels, zie [ de uitvoeringsstroom van het Scenario ](/help/workfront-fusion/references/scenarios/scenario-execution-flow.md)

   >[!NOTE]
   >
   >* De de geschiedenisvertoningen van het scenario a **Verwerkingsgeschiedenis** badge naast scenario&#39;s die onlangs hebben uitgevoerd, terwijl de uitvoeringsdetails aan opslag worden geschreven. De verwerking vindt onmiddellijk plaats nadat het scenario wordt uitgevoerd. en mag niet langer duren dan een paar minuten. Details van de uitvoering van het scenario zijn mogelijk niet zichtbaar terwijl de uitvoering wordt verwerkt.

1. Om gebeurtenissen te bekijken, klik de **Gebeurtenissen** tabel.

## De uitvoeringshistorie van het scenario filteren

U kunt de uitvoeringshistorie filteren om alleen uitvoeringen met de opgegeven waarden weer te geven.

1. Open de full-page geschiedenis voor een scenario zoals die in [ de uitvoeringshistorie van het scenario van de Mening op het [!UICONTROL History] lusje ](#view-scenario-history-on-the-history-tab) in dit artikel wordt beschreven.
1. Klik het [!UICONTROL filter] pictogram van de het filterfilter van het pictogram ![ Scenario ](assets/fusion-scenario-filter-icon.png) in de kopbal van de kolom u wilt filtreren door.
1. Voer in het dialoogvenster [!UICONTROL filter] de waarden in waarop u wilt filteren.
1. Klik op **[!UICONTROL Save]**.

Het filterpictogram is oranje in kolommen met een actief filter.

<!-- don't see how to do this
## Sort the scenario execution history

You can sort the scenario execution history.

1. Open the full-page history for a scenario as described in [View scenario execution history on the [!UICONTROL History] tab](#view-scenario-execution-history-on-the-history-tab) in this article.
1. Click the [!UICONTROL Sort] icon in the header of the column you want to filter by.
1. Optional: To reverse the order of the sort, click the [!UICONTROL Sort] icon again.
-->

## Alle uitvoeringen van een scenario doorzoeken

1. Open de full-page geschiedenis voor een scenario zoals die in [ de uitvoeringshistorie van het scenario van de Mening op het [!UICONTROL History] lusje ](#view-scenario-history-on-the-history-tab) in dit artikel wordt beschreven.
1. Klik op **[!UICONTROL Fulltext search]** boven aan de lijst met uitvoeringen.

   of

   Het type **Ctrl+Shift+F** (Vensters) of **Cmd+Shift+F** (Mac)
Het venster [!UICONTROL Search in history] wordt geopend.

1. (Optioneel) Als u wilt zoeken naar uitvoeringen die specifieke tekst bevatten, voert u de tekst in de zoekbalk van het venster **[!UICONTROL Search in history]** in.

   Als u naar exacte tekst wilt zoeken, plaatst u dubbele aanhalingstekens in de tekst (&quot;voorbeeld&quot;).

   >[!INFO]
   >
   >**Voorbeeld:** als u de uitvoering wilt vinden die tot een specifiek project leidde, ga projectidentiteitskaart in de [!UICONTROL Fulltext search] bar in.
   >
   >&quot;625ef2ef006036bd1794b6e52d737c5&quot;

1. (Optioneel) Als u uw zoekopdracht wilt beperken tot een datumbereik, selecteert u de begin- en einddatum van de gewenste zoekopdracht in het gebied [!UICONTROL By date range] .

   >[!NOTE]
   >
   >* Uitvoeringen zijn alleen beschikbaar gedurende de afgelopen 30 dagen.
   >
   >* In [!DNL Workfront Fusion] worden de payloads van de webhaak 30 dagen opgeslagen. De toegang tot van een Web-haaklading meer dan 30 dagen nadat het werd gecreeerd resulteert in de fout &quot;[!UICONTROL Failed to read file from storage.]&quot;


1. (Optioneel) Als u uw zoekopdracht wilt beperken tot status, selecteert u de gewenste status in het vervolgkeuzemenu **[!UICONTROL By status]** .


   Beschikbare statussen zijn:

   * [!UICONTROL All]

   * [!UICONTROL Error]

   * [!UICONTROL Warning]

   * [!UICONTROL Success]

1. (Optioneel) Wijzig de volgorde die wordt weergegeven in de vervolgkeuzelijst **[!UICONTROL Sort by dates]** .

1. (Optioneel) Klik op het pictogram **[!UICONTROL Copy execution ID]** om een scenario-uitvoerings-id te kopiëren <img src="assets/copy-fusion-execution-id-icon.png"> in de rij van de gewenste uitvoering.

1. (Optioneel) Klik op een resultaat van de [!UICONTROL Fulltext search] om de uitvoerbundel van de scenariomodule met de informatie te bekijken.
