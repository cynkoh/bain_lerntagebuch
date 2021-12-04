---
title: "6. Lerneinheit: Metadaten modellieren und Schnittstellen nutzen 1/2"
date: 2021-12-02
---

<h1>Metadaten harvesten</h1>

<p>In dieser Lerneinheit haben wir uns mit Crosswalks und VuFindHarvest auseinandergesetzt.<br></p>

<p>Wie in der <a href="https://github.com/melakae/bain_lerntagebuch/blob/4bd4d1bc03848d44cbe44f3f70eb815fa1348609/_posts/2021-09-15-lerneinheit_1.md">1. Lerneinheit</a> beschrieben, sind Crosswalks Brückenbauer zwischen den Metadaten-Standards. D.h. mit Crosswalks können Metadaten von einem Standard in einen anderen überführt werden. Es handelt sich dabei um einen Prozess, wobei es eigentlich ein Mapping ist, um zuzuordnen, welcher Wert wohin überführt wird. So ist je nach Metadatenstandard der Titel eines Werkes in einem anderen «Feld». Nun muss definiert werden, dass 24Xa mit den verschiedenen möglichen Ausprägungen für X aus dem Metadatenstandard MARC bei Dublin Core bspw. das Feld «Title» ist. Die <a href="https://www.getty.edu/research/publications/electronic_publications/intrometadata/crosswalks.html">Webseite des Kulturinstituts Getty in Los Angeles</a> gibt einen Überblick, welche die Komplexität ihres Crosswalks aufzeigt durch die Matrix mit den verschiedenen Metadatenstandards. Mit solchen Crosswalks können grosse Datensätze maschinell transformiert werden.<br></p>

<p>Über Schnittstellen wie z.B. OAI-PMH (s. <a href="https://github.com/melakae/bain_lerntagebuch/blob/4bd4d1bc03848d44cbe44f3f70eb815fa1348609/_posts/2021-11-19-lerneinheit_5.md">Lerneinheit 5</a>) können mittels Harvesting-Tools vorhandene Metadaten zusammengetragen werden – man «erntet» also verfügbare Daten. In der Fachsprache wird dazu der englische Ausdruck «harvest» genutzt. Die <a href="https://guides.lib.utexas.edu/metadata-basics/harvesting">Universität von Texas</a> erläutert das «Metadata harvesting» als das automatische Sammeln von Metadaten aus unterschiedlichen Quellen. Diese werden dann zusammengeführt (aggregiert) und anderen Anwendungen zur Verfügung gestellt. Kurz und prägnant erklären es <a href"https://guides.ucf.edu/metadata/metaHarvesting">University of Central Florida Libraries</a>: «Metadata Harvesting refers to gathering metadata from multiple places or archives and storing it in a central database.»<br></p>

<p>Im Unterricht haben wir Metadaten mit dem Tool VueFindHarvest zusammengetragen. Dazu haben wir die Beispieldatensätze aus Koha und ArchivesSpace mittels VueFindHarvest via Schnittstelle geladen und lokal abgespeichert. VueFindHarvest hat keine grafische Oberfläche, sondern wird nur via Terminal auf der virtuellen Maschine bedient. Der Vorgang ist schnell und einfach. Es benötigt einen Befehl im richtigen Verzeichnis und schon kann man die Daten «harvesten». Wichtig ist, dass man im Konsolenbefehl unterschiedliche Ordnernamen vergibt, die Daten nicht laufend direkt wieder überschreibt. Zu Beginn des Unterrichts habe ich nicht genau verstanden, was durch den eher unspektakulär wirkenden Vorgang wirklich ausgelöst wird. Nachdem ich mich nochmals mit dem Harvesting auseinandergesetzt habe, verstehe ich das besser. Bevor wir das Harvesting über VueFindHarvest gestartet haben, mussten wir sicherstellen, dass die Schnittstellen von Koha und ArchivesSpace erreichbar sind. Über VueFindHarvest haben wir dann die URL der Schnittstelle angegeben sowie den Zielordner, wo die Daten abgelegt werden sollen. Dieser Befehl wurde einmal für Koha und einmal für ArchivesSpace ausgeführt. Danach standen am definierten Zielort zwei Ordner mit den exportierten Metadaten zur Verfügung. Diese können nun weiterverarbeitet werden. Die Weiterverarbeitung bedeutet, dass die Daten via Crosswalks in den Ziel-Metadatenstandard transformiert werden. Denn die Applikation bzw. Datenbank, in welche die Daten integriert werden sollen, nutzen allenfalls einen anderen Standard. Wenn der Metadatenstandard nicht ändert, so ist die Überführung nicht nötig. Ist eine Transformation nötig, so können Werkzeuge wie z.B. MarcEdit7 genutzt werden. Je nach Metadatenstandard kann es sogar nötig sein, die Transformation in mehreren Schritten vorzunehmen. So müssen bspw. EAD-Daten erst in Marc konvertiert und von MARC21 dann zu MARC21XML transformiert werden. Dies birgt Risiken, da es durch die Transformation zu Informationsverlusten kommen kann. Durch das definierte Mapping in den Crosswalks sollte das grundsätzlich nicht geschehen, lässt sich aber nicht immer komplett vermeiden, da die Standards so unterschiedlich sind.</p>