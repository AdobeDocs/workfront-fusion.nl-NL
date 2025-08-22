---
content-type: reference
title: Fouttypen
description: Soms kan een fout tijdens de uitvoering van een scenario voorkomen. Dit gebeurt gewoonlijk als een service niet beschikbaar is omdat er geen verbinding is met een service of als een validatie mislukt. In dit artikel worden de algemene fouten besproken die u kunt tegenkomen.
author: Becky
feature: Workfront Fusion
exl-id: abf5f844-d13b-416e-a8b8-2d4ee1786262
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# Fouttypen

Soms kan een fout tijdens de uitvoering van een scenario voorkomen. Dit gebeurt gewoonlijk als een service niet beschikbaar is omdat er geen verbinding met de service kan worden gemaakt of als een validatie mislukt.

Adobe Workfront Fusion maakt onderscheid tussen verschillende basistypen fouten. Het type fout bepaalt de volgende acties van uw Fusion-scenario.

## Toegangsvereisten

+++ Breid uit om de toegangseisen voor de functionaliteit in dit artikel weer te geven.

U moet de volgende toegang hebben om de functionaliteit in dit artikel te kunnen gebruiken:

<table style="table-layout:auto">
 <col> 
 <col> 
 <tbody> 
  <tr> 
    <td role="rowheader">Adobe Workfront-pakket</td> 
   <td> <p>Alle</p> </td> 
  </tr> 
  <tr data-mc-conditions=""> 
   <td role="rowheader">Adobe Workfront-licentie</td> 
   <td> Nieuw: Standaard<p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">[!UICONTROL Adobe Workfront Fusion] licentie</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten.</p>
   <p>of</p>
   <p>Verouderd: alle </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>[!UICONTROL Select] of [!UICONTROL Prime] Workfront-abonnement: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>[!UICONTROL Ultimate] Workfront-abonnement: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>


Neem contact op met uw Workfront-beheerder om te weten te komen welk plan, licentietype of toegang u hebt.

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [ de Fusie van Adobe Workfront vergunningen ](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Verbindingsfout

`ConnectionError`

Verbindingsfouten zijn een van de meest voorkomende fouten. Zij worden gewoonlijk veroorzaakt door onbeschikbaarheid van de derdedienst om diverse redenen, zoals overbelasting, onderhoud, of stroomonderbreking. De standaardafhandeling van deze fout is afhankelijk van de module die de fout heeft aangetroffen.

* Als de fout op de eerste module voorkomt, wordt de uitvoering van het scenario geëindigd met een waarschuwingsbericht. Vervolgens probeert Workfront Fusion herhaaldelijk het scenario opnieuw uit te voeren met toenemende tijdsintervallen. Als alle pogingen mislukken, deactiveert Workfront Fusion het scenario.
* Als de verbindingsfout op een andere module dan de eerste voorkomt, hangen de verdere stappen van Toestaan af het opslaan van onvolledige uitvoeringen optie in de scenario geavanceerde montages:

   * Als deze optie is ingeschakeld, wordt de uitvoering van het scenario verplaatst naar de map [!UICONTROL Incomplete executions] waar Workfront Fusion herhaaldelijk probeert het scenario opnieuw uit te voeren met toenemende tijdsintervallen. Als alle pogingen mislukken, blijft de uitvoering in de map Onvolledige uitvoeringen staan, in afwachting van handmatige oplossing door de gebruiker.

     Voor meer informatie over onvolledige uitvoeringen, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.
   * Als deze optie is uitgeschakeld, eindigt de uitvoering van het scenario met een fout gevolgd door een terugdraaifase. Vervolgens probeert Workfront Fusion herhaaldelijk het scenario opnieuw uit te voeren met toenemende tijdsintervallen. Als alle pogingen mislukken, deactiveert Workfront Fusion het scenario.

  Voor meer informatie over toestaan het opslaan van onvolledige uitvoeringen die plaatsen, zie [ toestaan het opslaan van onvolledige uitvoeringen ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#allow-storing-incomplete-executions) in artikel vormt scenario montages.

### Tijdintervallen vergroten

Het algoritme voor het verhogen van tijdintervallen tussen pogingen wanneer een fout voorkomt is genoemd exponentiële backoff. De steeds langere tijdsintervallen worden als volgt ingesteld:

1. 10 minuten
1. 1 uur
1. 3 uur
1. 12 uur
1. 24 uur

De stijgende tijdintervallen helpen vaak uitgevoerde scenario&#39;s verhinderen verrichtingen bij herhaaldelijk het ontbreken pogingen te gebruiken.

>[!BEGINSHADEBOX]

**Voorbeeld:**

Een scenario bevat de [!DNL Google Sheets] trigger [!UICONTROL Watch Rows] . [!DNL Google Sheets] is 30 minuten niet beschikbaar vanwege onderhoud wanneer Workfront Fusion het scenario start, zodat het geen nieuwe rijen kan ophalen. Het scenario stopt en probeert het over 10 minuten opnieuw. Omdat [!DNL Google Sheets] nog steeds niet beschikbaar is, kan Workfront Fusion nog steeds geen informatie over nieuwe rijen ophalen. De volgende looppas van het scenario is gepland in 1 uur. [!DNL Google Sheets] is op dit moment weer beschikbaar en het scenario wordt uitgevoerd.

>[!ENDSHADEBOX]

## Gegevensfout

`DataError`

Er wordt een gegevensfout gegenereerd wanneer een item onjuist is toegewezen en niet voldoet aan de validatie die aan de Workfront Fusion-zijde of aan de zijkant van de service van derden wordt uitgevoerd.

Als deze fout voorkomt, wordt het scenario, tot waar de module ontbrak, verplaatst naar de onvolledige uitvoeringsomslag, waar u de kwestie kunt problemen oplossen. Nochtans, houdt het scenario niet op, en blijft lopen volgens zijn programma. Als u de uitvoering van het scenario wilt stoppen wanneer er een gegevensfout optreedt, schakelt u de optie Opeenvolgende verwerking in het instellingenvenster Scenario in.

Als u de optie [!UICONTROL Allow storing incomplete executions] niet hebt ingeschakeld in de scenario-instellingen, wordt de uitvoering van het scenario beëindigd met de fout en wordt een terugdraaiactie uitgevoerd.

## Gegevensfout dupliceren

`DuplicateDataError`

Als Workfront Fusion twee keer probeert dezelfde bundel in te voegen in een service die dubbele gegevens niet toestaat, wordt een dubbele gegevensfout gegenereerd. Als deze fout optreedt, gaat Workfront Fusion op dezelfde manier te werk als de gegevensfout.

Voor meer informatie, zie [ Fout van Gegevens ](#data-error) in dit artikel.


## Fout: toegang tot token

`InvalidAccessTokenError`

Er treedt een ongeldige toegangstoken-fout op wanneer Workfront Fusion geen toegang heeft tot uw account die bij een service van derden is geregistreerd. Dit gebeurt gewoonlijk wanneer u toegangsrechten voor Workfront Fusion in het beleid van een bepaalde dienst intrekt, maar de scenario&#39;s die die dienst gebruiken blijven lopend volgens programma.

Als deze fout optreedt, wordt de uitvoering van het scenario onmiddellijk gestopt. De rest van het scenario die van de module begint waar de fout voorkwam beweegt zich aan de onvolledige uitvoeringenomslag.

## Fout tarieflimiet

`RateLimitError`

Als een door een bepaalde dienst vastgestelde grens wordt overschreden, wordt een fout van de tariefgrens geproduceerd. Als deze fout optreedt, gaat Workfront Fusion op dezelfde manier te werk als bij de verbindingsfout.

Voor meer informatie, zie [ Fout van de Verbinding ](#connection-error) in dit artikel.

## Onvolledige gegevensfout

`IncompleteDataError`

Een onvolledige gegevensfout treedt alleen op bij triggers. Deze fout wordt gegenereerd als een trigger vereiste gegevens niet kan downloaden van een bepaalde service.

Als een scenario met `IncompleteDataError` eindigt, zal zijn verder gedrag van zijn het plaatsen van [!UICONTROL Max number of consecutive errors] afhangen.

Voor meer informatie, zie [ Aantal opeenvolgende fouten ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) in het artikel scenario montages vormt.

>[!BEGINSHADEBOX]

**Voorbeeld:**

Voor een scenario is de Workfront-trigger [!UICONTROL Watch Record] ingesteld op controleren voor documenten. Het scenario wordt uitgevoerd terwijl u een groot document uploadt, zoals een lange video. Aangezien [!UICONTROL Workfront Fusion] de video probeert te downloaden terwijl deze nog steeds naar Workfront wordt geüpload, wordt het scenario afgesloten met de instructie `IncompleteDataError` .

>[!ENDSHADEBOX]

## Runtime-fout

`RuntimeError`

Elke fout die tijdens de uitvoering van het scenario wordt weergegeven en niet een van deze fouttypen is, wordt gerapporteerd als een `RunTimeError` .

Als een scenario met `RuntimeError` eindigt, hangt zijn verdere gedrag van het [!UICONTROL Max number of consecutive errors] plaatsen af.

Voor meer informatie, zie [ Aantal opeenvolgende fouten ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#number-of-consecutive-errors) in het artikel scenario montages vormt.


>[!NOTE]
>
>Als een scenario begint met een onmiddellijke trigger en deze fout aantreft, wordt de instelling van [!UICONTROL Max number of consecutive errors] genegeerd en wordt het scenario onmiddellijk gedeactiveerd.
>&#x200B;>Voor meer informatie, zie [ Onmiddellijke trekkers ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/module-overview.md#instant-triggers) in het overzicht van de artikelmodules.

## Inconsistentiefout

`InconsistencyError`

Als om het even welk van deze fouten tijdens begaat of het terugschroeven van prijzen zich fase voordoet, eindigt het scenario met een Fout van de Inconsistentie.

Als deze fout in een scenario verschijnt, wordt de uitvoering van het scenario onmiddellijk gestopt.

## Waarschuwing

Tijdens het uitvoeren van een scenario, kunt u een waarschuwing ontvangen die u over een probleem op de hoogte brengt. Een waarschuwing verhindert niet het scenario met succes te voltooien.

Er kan bijvoorbeeld een waarschuwing verschijnen wanneer de maximaal toegestane bestandsgrootte wordt overschreden en de optie [!UICONTROL Enable data loss] is uitgeschakeld.

## Bronnen

Voor meer informatie bij afbeelding, zie [ Overzicht van de Afbeelding ](/help/workfront-fusion/get-started-with-fusion/understand-fusion/mapping-overview.md).

Voor informatie over onvolledige uitvoeringen, zie [ Mening en los onvolledige uitvoeringen ](/help/workfront-fusion/manage-scenarios/view-and-resolve-incomplete-executions.md) op.

Voor informatie over het paneel van de scenario montages, zie [ scenario montages ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md) vormen.

Voor informatie over programma&#39;s, zie [ Plan een scenario ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Voor informatie over scenario fasen, zie [ uitvoering Scenario, cycli, en fasen ](/help/workfront-fusion/references/scenarios/scenario-execution-cycles-phases.md).

Voor informatie over de Enable optie van het gegevensverlies, zie [ gegevensverlies ](/help/workfront-fusion/create-scenarios/config-scenarios-settings/configure-scenario-settings.md#enable-data-loss) in artikel toelaten vormt scenario montages.
