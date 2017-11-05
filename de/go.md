# Über dieses Buch

## Lizenz

"The Little Go Book" ist unter der "Attribution-NonCommercial-ShareAlike 4.0 International license" lizenziert. Du solltest für dieses Buch nichts bezahlt haben.

Es ist dir erlaubt dieses Buch zu kopieren, zu vertreiben, zu verändern oder zur Schau zu stellen. Allerdings bitte ich dich, dass du das Buch immer mir, Karl Seguin, zuschreibst und das Buch nicht für kommerzielle Zwecke benutzt.

Du kannst den ganzen, englischen Lizenztext unter dieser Adresse einsehen:

<https://creativecommons.org/licenses/by-nc-sa/4.0/>

## Neuste Version

Die neusten Quelldateien für dieses Buch sind unter dieser Adresse abrufbar:
<https://github.com/karlseguin/the-little-go-book>

## Vorwort

Ich habe schon immer eine Hassliebe für das Lernen neuer Programmiersprachen gehabt. Auf der einen Seite sind Programmiersprachen so fundamental für unsere Tätigkeit, dass sogar kleinste Veränderungen einen signifikanten Einfluss haben. Dieses *aha*-Erlebnis, welches man erfährt, wenn man etwas Neues kapiert, kann eine andauernde Auswirkung darauf haben, wie man programmiert. Dieses Erlebnis kann sogar die eigenen Erwartungen an andere Programmiersprachen neu setzen. Auf der anderen Seite ist Programmiersprachen-Design etwas ziemlich inkrementelles. Es ist viel Arbeit sich neue Keywords, Typ-Systeme, Coding Stile, neue Programmierbibliotheken, Communities und Programmierparadigmen anzueignen. Diese Arbeit scheint schwierig zu rechtfertigen sein. Verglichen mit allem anderem, was wir so erlernen müssen, erscheint das Lernen einer neuen Programmiersprache als eine schlechte Investition unserer Zeit.

Trotz all dem *müssen* wir uns weiterentwickeln. Wir *müssen* bereit sein weiterzuziehen, denn wie schon gesagt sind Programmiersprachen das Fundament dessen, was wir tun. Die Veränderungen sind aber oft inkrementell, sie neigen dazu ein großes Feld abzudecken und beeinflussen die Produktivität, Lesbarkeit, Performance, Testbarkeit, Dependency Management, Error Handling, Dokumentation, Profiling, Communities, Standardprogrammierbibliotheken und so weiter. Gibt es eine positive Art *Tot durch tausend Schnitte* zu sagen?

Nun bleibt uns eine wichtige Frage: **Warum Go?** Für mich gibt es zwei zwingende Gründe. Der erste ist, dass Go eine relativ einfache Sprache mit einer relativ einfachen Standardbibliothek ist. In vielerlei Hinsicht vereinfacht der inkrementelle Charakter Go's die Komplexität, die in den letzten paar Jahrzehnten zu anderen Programmiersprachen hinzugekommen ist. Der zweite Grund ist, dass Go das Arsenal vieler Programmierer vervollständigen kann.

Go wurde als eine System-Sprache (z. B. Betriebssysteme oder Gerätetreiber) geschaffen. Somit richtet sich Go an C und C++ Entwickler. Gemäß dem Go Team wird Go vor allem von Applikationsentwicklern, wie zum Beispiel ich einer bin, und nicht von Systementwicklern genutzt. Wieso? Ich kann zwar nicht für Systementwickler sprechen, für Applikationsentwickler jedoch schon. Für uns Applikationsentwickler ist ein ausschlaggebender Grund, dass wir ein Klassensystem brauchen, welches sich irgendwo zwischen low-level Systemanwendungen und high-level Anwendungen befindet.

