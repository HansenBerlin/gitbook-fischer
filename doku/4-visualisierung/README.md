# 4 Visualisierung

Die Visualisierung der Daten war aus mehreren Gründen komplexer als zunächst angenommen:

* geographische Daten werden teils als eigenes Format (.geojson) gespeichert
* Postleitzahlen sind für ein Mapping auf Regionen weniger geeignet, dafür werden die amtlichen Gemeindeschlüssel (AGS) verwendet, welche auch in den Geojsons zum Einsatz kommen.&#x20;
* eine rein zweidimensionale Betrachtung der Daten lieferte oft keine befriedigenden Ergebnisse. Die Darstellung von mehr als zwei Dimensionen kann hingegen schnell unübersichtlich werden. Beispiel: wie verhält sich das durchschnittliche Haushaltseinkommen in einer Region zu den Kaltmieten der Wohnungen in dieser Region? Die Dimensionen Einkommen und Kaltmiete sind je mit geografischen Dimensionen verknüpft (AGS bzw Längen- und Breitengrad).
* Tools wie Tableau bieten durch den NoCode Ansatz einen schnellen Einstieg, stoßen aber hinsichtlich Konfiguration und erweiterter Anforderungen wie der o.g. an ihre Grenzen. Wir  haben uns deshalb für eine eigene Lösung entschieden



Die Anwendung wurde als Webapplikation mit .NET Blazor umgesetzt. Durch die Verwendung eines Komponentenframeworks (MudBlazor), welches für viele Standardfälle bereits Templates anbietet, sowie eine gute Portierung der Plotly Library als nuget Paket, konnten bereits bekannte Workflows der Plotlylibrary in Python übernommen werden.&#x20;

Zusätzlich wurden für die Anbindung an die Datenbank und eine einfachere Aufbereitung der Daten für den Client zwei REST API's gebaut (eine als Layer zwischen Client und Datawarehouse, eine für die ML- Vorhersagen).

### Features

* a
* b

### Architekturübersicht

ggf Anhang



### Aufbau

Die folgenden Kapitel sind immer nach demselben, kommentierten Schema aufgebaut. Der jeweilige Teil wird nur dann weiter erläutert, wenn die Komplexität über ein normales Maß hinausgeht oder Entscheidungen getroffen wurden, die dies aus unserer Sicht erforderlich machen:

* kurze Einleitung
* Screenshot der Umsetzung in der Anwendung
* verwendetes Datenmodell
* Datenabfrage (Aggregationen, Transformationen)
* exemplarischer Codeausschnitt der Dashboardanwendung (Client), sofern für den BIA Kontext relevant



