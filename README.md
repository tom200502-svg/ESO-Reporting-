# ESO Reporting Documentation:

# Gesamtpipeline

## Zweck und Aufbau  des Dashboards:
Das Dashboard bietet einen umfassenden Überblick über alle Projekte. Es ist in drei Trichter-Visuals, eine Übersichtstabelle und einen separaten Filterbereich unterteilt. 
Im Filterbereich können Projekte nach bestimmten Attributen gefiltert oder Projektnamen gesucht werden. Die angezeigten Werte und Daten hängen vom ausgewählten "Abzugsdatum" im Filter ab. 
Das Dashboard ist interaktiv: Klicks auf einen Balken oder ein Projekt in einem Visual passen die restliche Dashboard-Ansicht entsprechend an.
 
1. Volumen [MWP] pro Projektstatus: Das erste Visual ist ein Trichter, welcher das Projektvolumen pro Status von L0 bis L5 anzeigt. Rechts daneben steht das Gesamtvolume, welches durch einen Measure berechnet wird (siehe Anhang 1).

2. Anzahl der Projekte pro Status: Das zweite Visual zeigt die Anzahl der Projekte pro Status von L0 bis L5. Rechts danaben sind zwei Kennzahlen angeordnet. Die untere der beiden Kennzahlen ist die summierte Anzahl aller Projekte, welche ebenfalls durch ein Measure berechnet wird (siehe Anhang). Die obere Zahl ist abhängig von der Auswahl des Vergleichsdatumsfilter und berechnet die Differenz der Gesamtzahl der Projekte zwischen den in den Filtern gewählten Daten. Ein Beispiel: Wählt man den 28. Juli (136 Projekte) und den 25. Juni, zeigt ein Delta von -15, dass am 25. Juni 15 Projekte mehr (insgesamt 151) aktiv waren als am 28. Juli. Dies hilft, Trends und Veränderungen schnell zu erkennen.

3. Volumen Gewichtet auf Projekt-Ebene: Das dritte Visual zeigt das Volumen der Projekte pro Status, verrechnet mit der Probability. Es wird angezeigt, welches Volumen wahrscheinlich den Status M6 erreicht.

4. Übersichtstabelle: Das letzte Visual ist eine Übersichtstabelle, die alle Projekte basierend auf den gewählten Filtern anzeigt.

# Filterbereich:
Das ganze Dashboard lässt sich durch die rechts angeordneten Filter bearbeiten, sodass die gewünschten Daten angezeigt werden. 
In diesem Abschnitt sind einmal alle Filter erläutert.

1. Projektname: Hier lässt sich nach jedem Projektnamen in der Gesamtpipeline suchen und filtern, sollten bestimmte Aspekte eines speziellen Projektes von Interesse sein. 

2. Projektleitung: Hier kann nach einer oder mehreren bestimmten Projektleitungen gefiltert werden. Sollten also alle Projekte von Joanna interessant sein, kann hier nach dem Kürzel gesucht und gefiltert werden.

3. Projektstatus: Hier kann nach einem oder mehreren Status gefiltert werden.

4. Potenzial Bucket: Potenzialbuckets sind vordefinierte Buckets, welche auf einem Measure basieren (Siehe Anhang). Diese beinhalten Projekte eines bestimmten Status. Das Potenzialbucket L3 enthält alle Projekte, welche zum Abzugsdatum den Status L2 und so führt sich die Logik fort. Hier wollen wir Fokus auf Projekt legen, die möglicherweise interessant für die OKR-Auswertung werden könnten.

5. Flächenkategorie: Hier lassen sich alle Visuals und Tabellen nach der jeweiligen Flächenkategorie (privilegiert etc.) filtern.

6. Priorität: Hier lassen sich alle Projekte nach ihrer Priorität filtern. Diese ist von 0-4 angegeben.

7. Abzugsdatum: Dieser Filter setzt die Grundlage für alle anderen Filter. Das gewählte Datum stellt das Abzugsdatum dar, d.h. es werden immer die Daten zum hier gewählten Datum angezeigt.

8. Vergleichsdatum: Dieser Filter bezieht sich lediglich auf die Kennzahl “Delta zum Vergleichsdatum” und bestimmt zu welchem Abzugsdatum das Delta berechnet wird (Siehe Beispiel im oberen Teil)


# OKRs auf Lead Ebene

## Zweck und Aufbau  des Dashboards
Das Dashboard dient die quartärlichen OKRs der Akquise nachzuverfolgen. Hierbei handelt es sich um eine Darstellung aller LEADs welche sich neu in den Status L3 oder L4 bewegt haben. 
Generell ist das Dashboard ähnlich zur Gesamtpipeline aufgebaut und besteht aus einem Balkendiagramm, einer Übersichtstabelle, einer Kennzahl und einem eigenen Filterbereich, welcher im unteren Teil der Dokumentation noch erläutert wird.

1. OKR - Übersicht auf Lead Ebene: Das Diagramm zeigt basiert auf der unten erläuterten Logik und zeigt die Flächengröße der Leads, welche neu in den Status L3 oder L4 sind. Auch dieses ist interaktiv, d.h. wenn auf die verschiedenen Balken geklickt wird, passt sich die Gesamtfläche an und die Tabelle zeigt nur das ausgewählte Projekt.

2. Übersichtstabelle: Die Übersichtstabelle zeigt die LeadID, den Projektnamen und den aktuellen Status der Leads, welche im Balkendiagramm visuell veranschaulicht werden.

3. Gesamtfläche [ha]:  Zeigt die Gesamtfläche der Leads aus dem Balkendiagramm und der Tabelle an. Auch diese passt sich nach dem gewählten Filterkontext an.

## Logik der Analyse
Diese Logik/Rechnung berechnet die Gesamtfläche von Projekten, die innerhalb eines von Ihnen gewählten Zeitraums wirklich neu in eine hohe Status-Stufe aufgestiegen sind.
Sie legen mit einem Referenzdatum und einem aktuellen Datum den Analysezeitraum fest. Die Logik prüft dann für jedes Projekt dessen gesamte Historie bis zum Referenzdatum zurück.
Ein Projekt wird nur dann als "neu" gezählt, wenn es diesen hohen Status vor dem Referenzdatum noch nie zuvor erreicht hatte. So wird sichergestellt, dass nur echte Aufsteiger und brandneue Projekte in die Berechnung einfließen, aber keine "Veteranen", die nur zu einem alten Top-Status zurückkehren.

## Filterbereich
1. Status: Filtert die Visuals, um nur die Projekte zu zeigen, die in der gewählten Stufe (Neu in L3 oder Neu in L4) neu sind.

2. Flächenkategorie: Zeigt nur Projekte an, die der ausgewählten Flächenkategorie zugeordnet sind.

3. Ansprechpartner: Schränkt die Ansicht auf die Projekte des gewählten Ansprechpartners ein.

4. Priorität: Filtert die Projekte nach der zugewiesenen Priorität. (Leer) zeigt Projekte ohne gesetzte Priorität.

5. Referenzdatum: Setzt den Startpunkt für die Analyse. Dient als Stichtag, bis zu dem die Projekthistorie geprüft wird.

6. Aktuelles Datum: Setzt den Endpunkt für die Analyse. Der Projektstatus an diesem Datum wird für den Vergleich verwendet.

# OKRs auf Projekt Ebene

## Zweck und Aufbau  des Dashboards
Das Dashboard dient dazu, die OKRs der Akquise darzustellen und nachzuverfolgen. Hierbei handelt es sich um eine Darstellung aller Projekte, welche sich neu in den Status L5 bewegt haben. 
Generell ist das Dashboard ähnlich zur Gesamtpipeline aufgebaut und besteht aus einem Balkendiagramm, einer Übersichtstabelle, einer Kennzahl und einem eigenen Filterbereich, welcher im unteren Teil der Dokumentation noch erläutert wird.

1. OKR - Übersicht auf Projekt Ebene: Das Diagramm zeigt basiert auf der unten erläuterten Logik und zeigt die Flächengröße der Projekte, welche neu in den Status L5 sind. Auch dieses ist interaktiv, d.h. wenn auf die verschiedenen Balken geklickt wird, passt sich die Gesamtfläche an und die Tabelle zeigt nur das ausgewählte Projekt.

2. Übersichtstabelle: Die Übersichtstabelle zeigt die ProjektID, den Projektnamen und den aktuellen Status der Projekte, welche im Balkendiagramm visuell veranschaulicht werden.

3. Gesamtfläche [ha]:  Zeigt die Gesamtfläche des Projekts aus dem Balkendiagramm und der Tabelle an. Auch diese passt sich nach dem gewählten Filterkontext an.

## Logik der Analyse
Diese Logik/Rechnung berechnet die Gesamtfläche von Projekten, die innerhalb eines von Ihnen gewählten Zeitraums wirklich neu in eine hohe Status-Stufe aufgestiegen sind.
Sie legen mit einem Referenzdatum und einem aktuellen Datum den Analysezeitraum fest. Die Logik prüft dann für jedes Projekt dessen gesamte Historie bis zum Referenzdatum zurück.
Ein Projekt wird nur dann als "neu" gezählt, wenn es diesen hohen Status vor dem Referenzdatum noch nie zuvor erreicht hatte. So wird sichergestellt, dass nur echte Aufsteiger und brandneue Projekte in die Berechnung einfließen, aber keine "Veteranen", die nur zu einem alten Top-Status zurückkehren.
## Filterbereich
1. Status: Filtert die Visuals, um nur die Projekte zu zeigen, die in der gewählten Stufe (Neu in L3 oder Neu in L4) neu sind.

2. Flächenkategorie: Zeigt nur Projekte an, die der ausgewählten Flächenkategorie zugeordnet sind.

3. Ansprechpartner: Schränkt die Ansicht auf die Projekte des gewählten Ansprechpartners ein.

4. Priorität: Filtert die Projekte nach der zugewiesenen Priorität. (Leer) zeigt Projekte ohne gesetzte Priorität.

5. Referenzdatum: Setzt den Startpunkt für die Analyse. Dient als Stichtag, bis zu dem die Projekthistorie geprüft wird.

6. Aktuelles Datum: Setzt den Endpunkt für die Analyse. Der Projektstatus an diesem Datum wird für den Vergleich verwendet.
