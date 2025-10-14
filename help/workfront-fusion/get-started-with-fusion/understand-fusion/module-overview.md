---
title: Overzicht van module
description: 'Adobe Workfront Fusion onderscheidt vijf typen modules: actiemodules, zoekmodules, triggermodules, aggregators en iterators. Samenvoegapparatuur en iterators zijn geschikt voor geavanceerde scenario''s.'
author: Becky
feature: Workfront Fusion
exl-id: 4c8fe028-8425-426d-a006-f0c66871b3cd
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# Overzicht van module

Adobe Workfront Fusion onderscheidt vijf typen modules:

* Actiemodules
* Zoeken in modules
* Triggermodules
* Samenvoegapparatuur
* Iteratoren

Samenvoegapparatuur en iterators zijn geschikt voor geavanceerde scenario&#39;s.

## Actiemodules

Modules van de actie zijn het gemeenschappelijkste type van module. Een typische actiemodule voert een actie uit en keert één enkele bundel terug, die dan tot de volgende module voor verwerking overgaat.

In tegenstelling tot triggermodules kunnen actiemodules aan het begin, midden of einde van een scenario worden geplaatst.

Scenario&#39;s kunnen een onbeperkt aantal actiemodules bevatten, hoewel grote aantallen modules (150+) prestaties kunnen beïnvloeden.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **Workfront >[!UICONTROL Upload a file]** verzendt een dossier naar Workfront en keert zijn herkenningsteken terug.
* **[!UICONTROL Image]>[!UICONTROL Resize]** ontvangt een afbeelding, past deze aan de opgegeven afmetingen aan en geeft de gewijzigde afbeelding door aan de volgende actie.

>[!ENDSHADEBOX]

Het type Handeling heeft vier subtypen:

* Maken
* Lezen
* Bijwerken
* Verwijderen

Het subtype Update bevat de volgende drie bewerkingen:

* **Wis de inhoud van een gebied**. Deze bewerking vindt plaats wanneer de inhoud van het veld wordt geëvalueerd naar het trefwoord `erase` (niet te verwarren met `empty` ).

  ![&#x200B; Wis sleutelwoord &#x200B;](assets/erase-content-of-field.png)

* **verlaat de inhoud van een gebied onveranderd**. Deze bewerking vindt plaats wanneer het veld leeg blijft of wanneer de inhoud van het veld wordt geëvalueerd naar leeg (weergegeven als null in JSON).

  ![&#x200B; Lege bundel &#x200B;](assets/leave-content-field-unchanged.png)

* **vervangt de inhoud van een gebied**. Deze operatie vindt plaats in alle andere gevallen dan de twee hierboven beschreven gevallen.

>[!NOTE]
>
>* Als u het trefwoord `erase` niet ziet in het deelvenster Toewijzing, is de module geen updatemodule of is deze niet bijgewerkt naar de meest recente specificaties voor de app.
>* `Empty` wijzigt de inhoud van het veld niet. Als u het veld moet wissen, gebruikt u de volgende formule:
>
>   ![&#x200B; als leeg &#x200B;](assets/formula-ifempty-name-erase.png)
>
>* Het ongewijzigd laten van een veld wanneer de inhoud ervan als leeg wordt beschouwd, wordt momenteel niet ondersteund.

## Zoeken in modules

De modules van het onderzoek keren nul, één, of meerdere bundels terug, die dan tot de volgende module voor verwerking overgaan.

U kunt de modules van het Onderzoek aan het begin, het midden, of het eind van een scenario plaatsen.

Scenario&#39;s kunnen een onbeperkt aantal modules van het Onderzoek bevatten, hoewel de grote aantallen modules (150+) prestaties kunnen beïnvloeden.

>[!BEGINSHADEBOX]

**Voorbeeld:**

**Workfront >[!UICONTROL Read Related Records]** leest verslagen die de onderzoeksvraag aanpassen u, in een bepaald oudervoorwerp specificeert.

>[!ENDSHADEBOX]

## Triggermodules

Triggers genereren bundels wanneer er een wijziging is opgetreden in een bepaalde service, zoals het maken of bijwerken van een record.

Triggers retourneren nul, een of meer bundels, die vervolgens worden doorgegeven aan de volgende module voor verwerking.

Omdat de Trekkers scenario&#39;s veroorzaken om met uitvoering te beginnen, kunnen zij slechts aan het begin van een scenario worden geplaatst.

Elk scenario kan slechts één trekker bevatten.

Workfront Fusion gebruikt twee typen triggers: opiniepeilingtriggers en Instant-triggers.

### Opiniepeilingtriggers

De opiniepeilingen brengen regelmatig opiniepeilingen een bepaalde dienst zelfs als er geen verandering sinds de vorige scenario looppas is geweest. Wij adviseren dat u een scenario plant dat een opiniepeilingtrekker bevat om met regelmatige intervallen te lopen. Als er een verandering is die de configuratie van de trekker aanpast, keert de trekker bundels terug die informatie over de verandering bevatten. Als er geen verandering is die de configuratie aanpast, voert de trekker geen bundels uit.

Voor instructies bij het plannen van een scenario, zie [&#x200B; Plan een scenario &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Met opiniepeilingtriggers kunt u de eerste bundel selecteren die wordt uitgevoerd via een deelvenster dat automatisch wordt weergegeven nadat u een trigger hebt opgeslagen of de triggerinstellingen hebt gewijzigd. Deze selectie heeft alleen invloed op de eerste uitvoering van de module. Nadat de module eenmaal is uitgevoerd, worden de volgende uitvoeringen alleen gecontroleerd op wijzigingen die zich na de meest recente uitvoering voordoen.

Voor meer informatie, zie [&#x200B; kiezen waar een trekkermodule &#x200B;](/help/workfront-fusion/create-scenarios/add-modules/choose-where-trigger-module-starts.md) begint.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **Workfront >[!UICONTROL Watch records]** keert verslagen terug die onlangs na de laatste tijd werden toegevoegd het scenario in werking gesteld.

* **[!DNL Google Sheets]>[!UICONTROL Watch Rows]** retourneert nieuwe rijen die zijn toegevoegd na de laatste keer dat het scenario werd uitgevoerd.

>[!ENDSHADEBOX]

### Instant triggers

Met instant-triggers kan een service Workfront Fusion direct na een wijziging op de hoogte stellen. Wij adviseren dat u een scenario plant dat een onmiddellijke trekker bevat om onmiddellijk te lopen.

Voor instructies, zie [&#x200B; Plan een scenario &#x200B;](/help/workfront-fusion/create-scenarios/config-scenarios-settings/schedule-a-scenario.md).

Voor details op hoe de inkomende gegevens door een onmiddellijke trekker worden behandeld, zie [&#x200B; Onmiddellijke trekkers (webhooks) &#x200B;](/help/workfront-fusion/references/modules/webhooks-reference.md).

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **Workfront >[!UICONTROL Watch Events]** keert informatie terug wanneer een bepaald type van gebeurtenis in Workfront, zoals de verwezenlijking van een taak voorkomt.
* **[!DNL Google Sheets]>[!UICONTROL Watch Changes]** geeft informatie wanneer een cel wordt bijgewerkt.

>[!ENDSHADEBOX]

## Samenvoegapparatuur

Een aggregatormodule accumuleert meerdere bundels tot één bundel.

De aggregators keren slechts één bundel terug, die dan tot de volgende module voor verdere verwerking overgaat.

U kunt aggregators slechts in het midden van een scenario plaatsen.

Scenario&#39;s kunnen een onbeperkt aantal aggregators bevatten, hoewel grote aantallen modules (150+) prestaties kunnen beïnvloeden.

>[!BEGINSHADEBOX]

**Voorbeelden:**

* **[!UICONTROL Archive]>[!UICONTROL Create an archive]** comprimeert meerdere bestanden tot een ZIP-archief.
* **[!UICONTROL CSV]>[!UICONTROL Aggregate to CSV]** voegt meerdere tekenreeksen van een CSV-bestand samen tot één rij.
* **[!UICONTROL Tools]>[!UICONTROL Text aggregator]** combineert meerdere tekenreeksen tot één tekenreeks.

>[!ENDSHADEBOX]

Voor meer informatie, zie [&#x200B; de module van de Samenvoegaar &#x200B;](/help/workfront-fusion/references/modules/aggregator-module.md).

## Iteratoren

Een iterator is een type module dat arrays splitst in afzonderlijke bundels.

Iterators retourneren een of meer bundels, die vervolgens worden doorgegeven aan de volgende module voor verwerking.

U kunt Iterators slechts in het midden van een scenario plaatsen.

Scenario&#39;s kunnen een onbeperkt aantal iterators bevatten, hoewel grote aantallen modules (150+) prestaties kunnen beïnvloeden.

>[!BEGINSHADEBOX]

**Voorbeeld:**

**[!UICONTROL Email]>[!UICONTROL Retrieve attachments]** breekt een array met bijlagen in afzonderlijke bundels.

>[!ENDSHADEBOX]

Voor meer informatie, zie [&#x200B; de module van de Teller 0&rbrace; en &#x200B;](/help/workfront-fusion/references/modules/iterator-module.md) Kaart een serie [.](/help/workfront-fusion/create-scenarios/map-data/map-an-array.md)
