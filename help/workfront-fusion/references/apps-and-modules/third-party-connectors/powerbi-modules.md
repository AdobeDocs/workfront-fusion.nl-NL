---
title: Power BI-modules
description: Adobe Workfront Fusion vereist naast een Adobe Workfront-licentie een Adobe Workfront Fusion-licentie.
author: Becky
feature: Workfront Fusion
exl-id: 73eb70e1-3f3d-419d-9cde-3ec3cda224f8
source-git-commit: e0d9d76ab2cbd8bd277514a4291974af4fceba73
workflow-type: tm+mt
source-wordcount: '2195'
ht-degree: 0%

---

# [!DNL Power BI] Modules

[!DNL Power BI] is een toepassing waarmee u gegevens kunt visualiseren en presenteren aan uw belanghebbenden. Het kan gegevens uit een verscheidenheid van bronnen nemen.

>[!NOTE]
>
>Workfront Fusion is geen gegevensbron. Hoewel Workfront Fusion gegevensbronnen kan maken en gebruiken, worden uw gegevens niet opgeslagen.


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
   <td> <p>Nieuw: Standaard</p><p>of</p><p>Huidig: Werk of hoger</p> </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Adobe Workfront Fusion-licentie**</td> 
   <td>
   <p>Huidig: Geen Workfront Fusion-licentievereisten</p>
   <p>of</p>
   <p>Verouderd: Workfront Fusion for Work Automation and Integration </p>
   </td> 
  </tr> 
  <tr> 
   <td role="rowheader">Product</td> 
   <td>
   <p>Nieuw:</p> <ul><li>Select- of Prime Workfront-pakket: uw organisatie moet Adobe Workfront Fusion aanschaffen.</li><li>Ultimate Workfront-pakket: Workfront Fusion is inbegrepen.</li></ul>
   <p>of</p>
   <p>Huidig: Uw organisatie moet Adobe Workfront Fusion aanschaffen.</p>
   </td> 
  </tr>
 </tbody> 
</table>

Voor meer detail over de informatie in deze lijst, zie [&#x200B; vereisten van de Toegang in documentatie &#x200B;](/help/workfront-fusion/references/licenses-and-roles/access-level-requirements-in-documentation.md).

Voor informatie over de vergunningen van de Fusie van Adobe Workfront, zie [&#x200B; de Fusie van Adobe Workfront vergunningen &#x200B;](/help/workfront-fusion/set-up-and-manage-workfront-fusion/licensing-operations-overview/license-automation-vs-integration.md).

+++

## Microsoft Power BI API-informatie

De Microsoft Power BI-connector gebruikt het volgende:

<table style="table-layout:auto"> 
 <col> 
 <col> 
 <tbody> 
  <tr> 
   <td role="rowheader">Basis-URL</td> 
   <td> https://api.powerbi.com/v1.0</td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-versie</td> 
   <td> v1.0 </td> 
  </tr> 
  <tr> 
   <td role="rowheader">API-tag</td> 
   <td>v1.0.2</td> 
  </tr>
 </tbody> 
 </table>

## [!DNL Power BI] modules en hun velden

Wanneer u [!DNL Power BI] configureert, geeft Workfront Fusion de onderstaande velden weer. Afhankelijk van factoren zoals uw toegangsniveau in de app of service, kunnen er naast deze velden mogelijk extra velden worden weergegeven. Een vetgedrukte titel in een module geeft een verplicht veld aan.

Als u de kaartknoop boven een gebied of een functie ziet, kunt u het gebruiken om variabelen en functies voor dat gebied te plaatsen. Voor meer informatie, zie [&#x200B; informatie van de Kaart van één module aan een andere in de Fusie van Adobe Workfront &#x200B;](/help/workfront-fusion/create-scenarios/map-data/map-data-from-one-to-another.md).

![&#x200B; Kaart knevel &#x200B;](/help/workfront-fusion/references/apps-and-modules/assets/map-toggle-350x74.png)

* [Dashboards](#dashboards)
* [Rapporten](#reports)
* [Gegevensset](#dataset)
* [Apps](#apps)
* [Overige](#other)

### Dashboards

* [Een dashboard maken](#create-a-dashboard)
* [Een dashboard ophalen](#get-a-dashboard)
* [Een dashboardtegel ophalen](#get-a-dashboard-tile)
* [Lijstdashboardblokken](#list-dashboard-tiles)
* [Lijstdashboards](#list-dashboards)

#### [!UICONTROL Create a Dashboard]

Deze actiemodule maakt een nieuw dashboard.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Voer een naam voor het dashboard in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het nieuwe dashboard zal bezitten.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard]

Deze actiemodule wint meta-gegevens van een gespecificeerd dashboard terug.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Selecteer of wijs de optie toe om het dashboard te kiezen waarvoor u meta-gegevens wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Voer de id van het dashboard in of wijs deze toe waarvoor u metagegevens wilt ophalen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het dashboard bezit dat u meta-gegevens voor wilt terugwinnen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dashboard Tile]

Deze actiemodule wint meta-gegevens van een gespecificeerde dashboardtegel terug.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
      <td>
        <p>Selecteer of wijs de optie toe om de dashboarddetails te kiezen u wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dashboard ID]</td>
      <td>
        <p>Voer de id van het dashboard in of wijs deze toe waarvoor u details wilt ophalen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tile ID]</td>
      <td>Voer de id in van het element [!DNL Power BI] waarvoor u details wilt ophalen of wijs dit toe.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die de tegel bezit u wilt terugwinnen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Dashboard Tiles]

Deze zoekmodule haalt een lijst met dashboardtegels op.

<table>
<col/>
<col/>
<tbody>
  <tr>
    <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Enter a Dashboard ID]</td>
    <td>
      <p>Selecteer of wijs de optie toe om het dashboard te kiezen waarvan de tegels u wilt vermelden.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Dashboard ID]</td>
    <td>
      <p>Voer de id van het dashboard in of wijs deze toe met de tegels die u wilt weergeven.</p>
    </td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Group ID]  </td>
    <td>Selecteer of wijs identiteitskaart van de Groep toe die de dashboards bezit die de tegels bevat u wilt een lijst maken.</td>
  </tr>
  <tr>
    <td role="rowheader">[!UICONTROL Limit]  </td>
    <td>
      <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
    </td>
  </tr>
</tbody>
</table>

#### [!UICONTROL List Dashboards]

Deze zoekmodule haalt een lijst met dashboards op.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Selecteer of wijs identiteitskaart van de Groep toe die de dashboards bezit u wilt een lijst maken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

### Rapporten

* [Een rapport kopiëren](#copy-a-report)
* [Een rapport verwijderen](#delete-a-report)
* [Een rapport ophalen](#get-a-report)
* [Rapporten weergeven](#list-reports)

#### [!UICONTROL Copy a Report]

Deze actiemodule kopieert een bestaand rapport.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Selecteer of wijs de optie in kaart om het rapport te kiezen dat u wilt kopiëren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Ga of kaart identiteitskaart van het rapport in dat u wilt kopiëren.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het rapport bezit dat u wilt kopiëren.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL New Copied Report Name]</td>
      <td>Ga of kaart een naam voor het nieuwe rapport in.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Report]

Deze actiemodule verwijdert een rapport.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Selecteer of wijs de optie in kaart om het rapport te kiezen dat u wilt schrappen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Ga of kaart identiteitskaart van het rapport in dat u wilt schrappen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het rapport bezit dat u wilt schrappen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Report]

Deze actiemodule wint meta-gegevens van een gespecificeerd rapport terug.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Selecteer of wijs de optie in kaart om het rapport te kiezen waarvoor u meta-gegevens wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Ga of kaart identiteitskaart van het rapport in dat u meta-gegevens voor wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het rapport bezit dat u meta-gegevens voor wilt terugwinnen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Reports]

Deze zoekmodule haalt een lijst met rapporten op.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>
        <p>Selecteer of wijs identiteitskaart van de Groep toe die de rapporten bezit u wilt een lijst maken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>


### Gegevensset

* [Rijen toevoegen/verwijderen in een tabel met gegevenssets](#add-or-delete-rows-in-a-dataset-table)
* [Een gegevensset maken](#create-a-dataset)
* [Een gegevensset verwijderen](#delete-a-dataset)
* [Een gegevensset ophalen](#get-a-dataset)
* [Lijstgegevens](#list-datasets)
* [Een gegevensset vernieuwen](#refresh-a-dataset)

#### [!UICONTROL Add or Delete Rows in a Dataset Table]

Deze actiemodule voegt rijen van een gespecificeerde lijst van duwdataset toe of schrapt.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a table]</td>
      <td>Selecteer of wijs de optie toe om de dataset te selecteren die de lijst bevat u wilt aanpassen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Ga of kaart identiteitskaart van de dataset in die de rijen bevat u wilt toevoegen of schrappen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Typ of wijs de naam toe van de tabel die de rijen bevat die u wilt toevoegen of verwijderen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Ga of kaart identiteitskaart van de groep in die de dataset bezit.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Select the Action]</td>
      <td>
        <p>Selecteer of wijs de actie toe die u wilt uitvoeren.</p>
        <ul>
          <li>
            <p>[!UICONTROL Add rows]</p>
          </li>
          <li>
            <p>[!UICONTROL Delete All Rows]</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>
        <p>Voeg de rijvelden toe.</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Key]</b>
            </p>
            <p>Voer de sleutelnaam in of wijs deze toe.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Field Type]</b>
            </p>
            <p>Selecteer of wijs het veldtype toe:</p>
            <ul>
              <li>
                <p>Boolean</p>
              </li>
              <li>
                <p>Datum</p>
              </li>
              <li>
                <p>Tekst</p>
              </li>
              <li>
                <p>Getal</p>
              </li>
            </ul>
          </li>
          <li>
            <p>[!UICONTROL Value]</p>
            <p>Voer de sleutelwaarde in of wijs deze toe.</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Create a Dataset]

Deze actiemodule leidt tot een nieuwe dataset.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>Ga of kaart een naam voor de dataset in.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of kaart identiteitskaart van de Groep die de nieuwe dataset zal bezitten.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Default Mode]</td>
      <td>
        <p>Selecteer of wijs de standaardwijze voor de dataset toe:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL As Azure]</b>: Een dataset met een live verbinding met [!DNL Azure Analysis Service]</p>
          </li>
          <li>
            <p><b>[!UICONTROL As on Prem]</b>: Een dataset met een live verbinding met [!DNL On-premise Analysis] Service</p>
          </li>
          <li>
            <p><b>[!DNL Push]</b>: Een dataset die programmatic toegang voor het duwen van gegevens in toestaat [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Push Streaming]</b>: Een dataset die gegevens het stromen steunt en programmatic toegang toestaat voor het duwen van gegevens in [!DNL Power BI]</p>
          </li>
          <li>
            <p><b>[!DNL Streaming]</b>: Een dataset die gegevens het stromen steunt</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Tables]</td>
      <td>Voeg lijsten aan de dataset toe. Voor gebieden, zie {de gebieden van 0} Lijst <a href="#Table" class="MCXref_0"></a></td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Data sources]</td>
      <td>Voeg de gegevensbronnen toe. Voor gebieden, zie <a href="#Data" class="MCXref_0"> gegevensbrongebieden </a>.</td>
    </tr>
    <tr>
      <td role="rowheader">[!DNL Default Retention Policy]  </td>
      <td>
        <p>Selecteer of wijs het opzettelijke beleid voor de dataset toe:</p>
        <ul>
          <li>
            <p>[!UICONTROL None]</p>
          </li>
          <li>
            <p>[!UICONTROL Basic FIFO]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

##### Tabelvelden

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Name]</td>
      <td>
        <p>  Voer een naam voor de tabel in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Columns]</td>
      <td>
        <p>Voeg de kolommen toe:</p>
        <ul>
          <li>
            <p><b>[!UICONTROL Name]</b>
            </p>
            <p>Voer (kaart) een kolomnaam in.</p>
          </li>
          <li>
            <p><b>[!UICONTROL Data Type]</b>
            </p>
            <p>Selecteer of wijs het gegevenstype toe:</p>
            <ul>
              <li>
                <p>[!UICONTROL String]</p>
              </li>
              <li>
                <p>[!UICONTROL Integer]</p>
              </li>
              <li>
                <p>[!UICONTROL Boolean]</p>
              </li>
              <li>
                <p>[!UICONTROL Date Time]</p>
              </li>
            </ul>
          </li>
          <li>
            <p><b>[!UICONTROL Format String]</b>
            </p>
            <p>Voer de indelingstekenreeks in (kaart).</p>
          </li>
        </ul>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Rows]</td>
      <td>Voer rijdetails in of wijs deze toe.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Measures]</td>
      <td>Voeg de maatregel voor de lijsten toe.</td>
    </tr>
  </tbody>
</table>

##### Gegevensbronvelden

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Database]  </td>
      <td>
        <p>Voer de database die u wilt gebruiken in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Server]  </td>
      <td>
        <p>Voer de naam in of wijs de naam toe van de server die u wilt gebruiken.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL URL]  </td>
      <td>
        <p>Voer de gewenste URL in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source ID]</td>
      <td>
        <p>  Voer de id van de gegevensbron in of wijs deze toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Data source Type]  </td>
      <td>
        <p>Selecteer of wijs het gegevenstype van de gegevensbron in kaart. Voorbeeld: SQL.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Gateway ID]  </td>
      <td>Ga of kaart identiteitskaart van de gateway in u wilt gebruiken.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Delete a Dataset]

Deze actiemodule schrapt een dataset.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Selecteer of wijs de optie in kaart om de dataset te kiezen die u wilt schrappen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Ga of kaart identiteitskaart van de dataset in die u wilt schrappen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die de dataset bezit die u wilt schrappen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get a Dataset]

Deze actiemodule wint meta-gegevens van een gespecificeerde dataset terug.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a Report ID]</td>
      <td>
        <p>Selecteer of wijs de optie in kaart om het rapport te kiezen waarvoor u meta-gegevens wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>Ga of kaart identiteitskaart van de dataset in die u meta-gegevens voor wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die de dataset bezit die u meta-gegevens voor wilt terugwinnen.</td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Datasets]

Deze onderzoeksmodule wint een lijst van datasets terug.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Selecteer of wijs identiteitskaart van de Groep toe die het rapport bezit dat u meta-gegevens voor wilt terugwinnen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]</td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Refresh a Dataset]

Deze actiemodule vernieuwt een gespecificeerde dataset.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Enter a dataset]</td>
      <td>Selecteer of wijs de optie in kaart om de dataset te selecteren die u wilt verfrissen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Dataset ID]</td>
      <td>Ga of kaart identiteitskaart van de dataset in die u wilt verfrissen.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Table Name]  </td>
      <td>
        <p>Typ of wijs de naam toe van de tabel die de rijen bevat die u wilt toevoegen of verwijderen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Group ID]  </td>
      <td>Ga of kaart identiteitskaart van de groep in die de dataset bezit.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Notify Option]  </td>
      <td>
        <p>Selecteer of wijs de optie toe om op de hoogte te brengen:</p>
        <ul>
          <li>
            <p>[!UICONTROL Mail on Completion]</p>
          </li>
          <li>
            <p>[!UICONTROL Mail on Failure]</p>
          </li>
          <li>
            <p>[!UICONTROL No Notification]</p>
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

### Apps

* [Een app ophalen](#get-an-app)
* [Het dashboard van een app ophalen](#get-an-apps-dashboard)
* [App-rapport ophalen](#get-an-apps-report)
* [De dashboards van de app van de lijst](#list-apps-dashboards)
* [App-rapporten weergeven](#list-apps-reports)
* [Lijsttoepassingen](#list-apps)
* [Apps controleren](#watch-apps)

#### [!UICONTROL Get an App]

Deze actiemodule haalt metagegevens van een opgegeven toepassing op.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Selecteer of wijs de id toe van de app die u wilt ophalen.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Dashboard]

Deze actiemodule haalt metagegevens op van het dashboard van een opgegeven app.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Selecteer of wijs de id van de app toe die het dashboard bevat dat u wilt ophalen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Selecteer of wijs identiteitskaart van het dashboard toe u wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Get an App's Report]

Met deze actiemodule worden metagegevens opgehaald van het rapport van een opgegeven app.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]  </td>
      <td>
        <p>Selecteer of wijs identiteitskaart van app toe die het rapport bevat u wilt terugwinnen.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Report ID]</td>
      <td>
        <p>  Selecteer of wijs identiteitskaart van het rapport toe u wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List Apps]

Deze zoekmodule haalt een lijst op met alle geïnstalleerde apps.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Dashboards]

Deze zoekmodule haalt een lijst met dashboards op uit een opgegeven app.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Selecteer of wijs de id van de app toe waaruit u de dashboards wilt weergeven.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL List App's Reports]

Deze zoekmodule haalt een lijst op met alle rapporten in de opgegeven app.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL App ID]</td>
      <td>Selecteer of wijs de id van de app toe waaruit u rapporten wilt weergeven.</td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

#### [!UICONTROL Watch Apps]

Deze triggermodule start een scenario wanneer een app wordt bijgewerkt.

<table>
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Limit]  </td>
      <td>
        <p>Ga of kaart het maximumaantal verslagen in u de module tijdens elke cyclus van de scenariouitvoering wilt terugkeren.</p>
      </td>
    </tr>
  </tbody>
</table>

### Overige

#### [!UICONTROL Make an API Call]

Deze actiemodule voert een API-aanroep uit naar de [!DNL Power BI] API.

<table style="table-layout:auto"> 
  <col/>
  <col/>
  <tbody>
    <tr>
      <td role="rowheader">[!UICONTROL Connection]</td>
   <td> <p>Voor instructies over het aansluiten van uw [!DNL Power BI] rekening aan de Fusie van Workfront, zie <a href="/help/workfront-fusion/create-scenarios/connect-to-apps/connect-to-fusion-general.md" class="MCXref xref" data-mc-variable-override=""> een verbinding aan de Fusie van Adobe Workfront tot stand brengen - Basisinstructies </a></p> </td> 
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Path]</p>
      </td>
      <td>
        <p>Voer een pad in dat relatief is ten opzichte van <code>https://api.powerbi.com</code> . Voorbeeld: <code>/v1.0/myorg/datasets</code> .</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">
        <p>[!UICONTROL Method]</p>
      </td>
      <td>
        <p>Selecteer de aanvraagmethode [!UICONTROL HTTP] die u nodig hebt om de API-aanroep te configureren. Zie [!UICONTROL HTTP] aanvraagmethoden voor meer informatie.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Headers]</td>
      <td>
        <p>Voeg de kopteksten van het verzoek toe in de vorm van een standaard JSON-object.</p>
        <p>Bijvoorbeeld: <code>{"Content-type":"application/json"}</code></p>
        <p>Workfront Fusion voegt automatisch machtigingsheaders en x-api-sleutelkopballen toe.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Query String]  </td>
      <td>
        <p>Voer de queryreeks voor de aanvraag in.</p>
      </td>
    </tr>
    <tr>
      <td role="rowheader">[!UICONTROL Body]</td>
   <td> <p>Voeg de inhoud van de hoofdtekst voor de API-aanroep toe in de vorm van een standaard JSON-object.</p> <p>Opmerking:  <p>Wanneer u voorwaardelijke instructies gebruikt, zoals <code>if</code> in uw JSON, plaatst u de aanhalingstekens buiten de voorwaardelijke instructie.</p> 
     <div class="example" data-mc-autonum="<b>Example: </b>"> 
      <p> <img src="/help/workfront-fusion/references/apps-and-modules/assets/quotes-in-json-350x120.png" style="width: 350;height: 120;"> </p> 
     </div> </p> </td>     </tr>
  </tbody>
</table>
