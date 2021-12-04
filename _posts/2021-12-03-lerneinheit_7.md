---
title: "7. Lerneinheit: Metadaten modellieren und Schnittstellen nutzen"
date: 2021-12-03
---

<h1>OpenRefine</h1>

<p>Diese Lerneinheit stand ganz im Zeichen des OpenSource Tools von OpenRefine. Mit diesem Tool können Metadaten transformiert und editiert werden.<br></p>

<p>Die Oberfläche zeigt in Tabellenform die geladenen Metadaten, welche nun gesamthaft oder auch spaltenweise geprüft, bereinigt und auch angereichert werden können. Wo sinnvoll können Ähnlichkeiten gefunden und Daten entsprechend geclustert werden. Dies ist bspw. bei Autoren sinnvoll. Gibt es mehrere Schreibweisen, kann diese mit wenig Aufwand vereinheitlicht werden. Dazu wird die Funktion Cluster in der entsprechenden Spalte aufgerufen. Das Tool macht Vorschläge, wo Ähnlichkeiten gefunden wurden. Der User entscheidet, ob er diese annimmt und wenn ja mit welcher der gefunden Schreibweisen.<br></p>

<p><img src="https://user-images.githubusercontent.com/83494929/144718420-d13e81ba-2a02-4d62-bce1-bc1278c543b0.png" alt=" Ansicht: Cluster-Funktion in OpenRefine" width="100%"><br>
<i>Cluster-Funktion in der Spalte Authors in OpenRefine</i><br></p>

<p>Ebenfalls spannend ist die Funktion Reconsiliation. Damit können die Metadaten mit Daten aus anderen Datenbanken wie z.B. Wikidata angereichert werden. Dies macht bspw. für Journals Sinn. Über die ISSN können die entsprechenden Einträge gefunden und zugeordnet werden. Die Journals können in eine neu erstellte Spalte den Einträgen zugeordnet werden. Im Unterricht verwenden wir dazu die Datenbank Wikidata. Es handelt sich dabei um eine frei verfügbare Datenbank mit 96'093'698 Datenelemente (Stand 4.12.2021). Die Wissensdatenbank kann von Maschinen wie auch von Menschen genutzt werden. Der Inhalt ist über eine freie Lizenz verfügbar und die Inhalte können über Standardformate exportiert werden. Die Datenbank enthält strukturierte, mehrsprachige Daten von den Schwesterprojekten Wikipedia, Wikivoyage, Wikionary, Wikisource und weiteren (<a href="https://www.wikidata.org/wiki/Wikidata:Main_Page">Wikidata MainPage</a>). <br></p>

<p>Die Inhalte von Wikidata werden kollaborativ gesammelt (<a href="https://www.wikidata.org/wiki/Wikidata:Introduction">Wikidata: Instroduction</a>). Jede/r – auch Organisationen –  können mit machen und die Datenbank weiter anreichern. Die Daten können bspw. über ein SPARQL Endpoint oder auch über URL-Schnittstellen in Formaten wie Jason, RDF und weiteren genutzt werden. Weitere Informationen sind auf <a href="https://www.wikidata.org/wiki/Wikidata:Data_access">Wikidata: Data access</a> verfügbar.<br></p>

<p><img src="https://user-images.githubusercontent.com/83494929/144718443-8583a7d2-5d83-4da6-868f-c34edaf8be77.png" alt=" Ansicht: Neue Spalte hinzufügen in OpenRefine" width="100%"><br>
<i>Neue Spalte hinzufügen für Journals in OpenRefine.</i><br></p>

<p>Weiter kann über die Scriptsprache GREL ein Mapping vorgenommen werden, welche Spalte wo und wie im Export ausgegeben werden soll. So können nicht benötigte Daten weggeschnitten oder auch Inhalte gesplittet werden. Es ist auch möglich, die Reihenfolge zu ändern, so dass der Hauptautor am Anfang des Records erscheint und weitere Autoren aber am Ende des Datensatzes zu dem Werk. <br></p>

<p>GREL steht für General Refine Expression Language und ist ähnlich wie Javascript konzipiert (<a href="https://docs.openrefine.org/manual/grel">docs.openrefine.org/manual/grel</a>). Die Syntax kann zwei Formen aufweisen – entweder functionName (arg0, arg2, …) oder arg0.funktionName(arg1, …), wobei arg für Argument steht. Zweitere Form ist die Kurzfrom (dot notation), wohingegen die erstere die volle Notation (full notation) ist. So können die Ausdrücke unterschiedlich aussehen – je nach dem, ob jemand die dot oder full Notation verwendet. Es sind auch Steuerelemente (controls) verfügbar, womit Schleifenabfragen mit if und for möglich sind (<a href="https://docs.openrefine.org/manual/grel">docs.openrefine.org/manual/grel</a>). Es sind auch Funktionen verfügbar, bspw. für Boolean, Strings aber auch format-based Funktionen. Die Scriptsprache verfügt auch über Arrays, Datums-, Mathematik- und weitere Funktionen (<a href="https://docs.openrefine.org/manual/grelfunctions">docs.openrefine.org/manual/grelfunctions</a>). <br></p>

<p>Weiterführende Infos zu OpenRefine sind in der Dokumentation verfügbar unter <a href="https://docs.openrefine.org/manual/expressions">openrefine.org/manual</a>.</p>

