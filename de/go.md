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

Vielleicht ist Go eine Messaging-, Caching-, Datenanalysen-, Kommandozeilenprogramm-, Logging- oder Monitoringsprache. Ich weiss nicht wie man Go genau nennen sollte aber folgendes ist klar: Während meiner ganzen Karriere wurden die Systeme immer komplexer und die Anzahl an nebenläufig ausgeführten Prozessen stieg in die Zehntausende wodurch immer ein grösseres Verlangen nach selbstgebauten Infrasturktursystem entstanden ist. Solche Systeme *kann* man in Ruby oder Python oder in irgendetwas anderem schreiben (und das wird auch häufig getan), aber diese Systeme können von einem etwas statischerem Typsystem und von besserer Performance profitieren. Gleichermassen *kann* man Webseiten in Go programmieren (und das wird auch häufig getan), aber ich bevorzuge trotzdem noch die grosse Ausdruckskraft von Node oder Ruby, wenn ich an einem solchen System arbeite.

Go hat dafür andere Stärken. Zum Beispiel hat ein kompilierte Go-Programm keine Abhängikeiten. Mit Go muss man sich nicht darum kümmern, dass der Nutzer Ruby oder die JVM installiert hat und dann auch noch in der richtigen Version. Deswegen wird Go auch immer belibter als Programmiersprache für Kommandozeilenprogramme und andere Utility-Programme die an einen Nutzer ausgeliefert werden (zum Beispiel einen Log Collector).

Ganz einfach gesagt: Go zu lernen ist effiziente Nutzung der Zeit. Man braucht nicht viele Stunden zu investieren um Go zu lernen und ein Go Experte muss man schon gar nicht sein. Trotzdem kommt am Ende etwas nützliches dabei raus.

## Anmerkung vom Autor

Ich habe gezögert, bevor ich dieses Buch geschrieben habe, aus mehreren Gründen: Erstens wegen der offiziellen Go-Dokumentation, vor allem das Kapitel [Effective Go](https://golang.org/doc/effective_go.html) ist sehr gut.

Zweitens, weil es mir unangenehm ist, ein Buch über eine Programmiersprache zu schreiben. Als ich "The Little MongoDB Book" geschrieben habe, konnte ich sicher sein, dass die meisten Leser schon ein Grundverständnis für relatinoale Datenbanken und deren Modeling hatten. Beim "The Little Redis Book" konnte ich von Grundkenntnissen von Key- Valuestores ausgehen und darauf aufbauen.

Wenn ich an die Absätze und Kapitel denke, die vor mir liegen, weiß ich, dass ich nicht in der Lage sein werde, dieselben Annahmen zu treffen. Wie viel Zeit sollte man damit verbringen, über Interfaces zu sprechen, wenn man weiss, dass für einige das Konzept komplett neu sein wird, während es für andere reicht, zu sagen:*Go hat Interfaces*? Letztendlich fasse ich Mut daraus, zu wissen, dass die Leser mich es wissen lassen werden, wenn einige Teile zu flach oder andere zu detailliert sind. Dies ist der Preis für dieses Buch.

# Der Einstieg

Wenn Sie ein wenig mit Go rumspielen möchten, sollten Sie sich die Seite[Go Playground](https://play.golang.org/) ansehen, auf der Sie Code online ausführen können, ohne irgendetwas installieren zu müssen. Dies ist auch die gebräuchlichste Art, Go-Code zu teilen, wenn man Hilfe im[Go Diskussionsforum](https://groups.google.com/forum/#!forum/golang-nuts) und Orten wie StackOverflow sucht.

Die Installation von Go ist einfach und schnell erledigt. Man kann Go aus dem Quellcode Kompilieren und installieren, aber ich empfehle, eine der vorkompilierten Go Binaries zu verwenden. Wenn man auf die Download-Seite (https://golang.org/dl/) geht, sieht man Installer für verschiedene Plattformen. Wir verzichten auf einen solchen Installer und lernen anstatt dessen, wie wir Go selbst installieren und konfigurieren können. Es ist wirklich nicht schwer.

Abgesehen von einfachen Beispielen ist Go so konzipiert, dass davon ausgegangen wird, dass der Code sich in einem Workspace befindet. Der Workspace ist ein Verzeichnis, das aus den Unterordnern `bin`, `pkg` und `src` besteht. Man ist versucht, Go zu zwingen, dem eigenen Stil zu folgen, was keine gute Idee ist.

Normalerweise lege ich alle meine Projekte unter `~/code` ab. Mein Blog befindet sich zum Beispiel im Verzeichnis `~/code/blog`. Bei Go-Projekten ist mein Workspace `~/code/go`. Wenn ich einen Blog in Go schreiben würde, befände sich dieser unter `~/code/go/src/blog`.

Kurz gesagt, sollte man einen `go`-Ordner mit einem `src`-Unterordner erstellen, wo auch immer man seine Projekte normalerweise ablegt.

## OSX / Linux

Laden Sie die `tar.gz` für Ihre Plattform herunter. Für OSX werden Sie sich höchstwahrscheinlich für `go#.#.#.#.darwin-amd64-osx10.8.tar.gz` interessieren, wobei `#.#.#` die neueste Version von Go ist.

Entpacken Sie die Datei nach `/usr/local` mittels `tar -C /usr/local -xzf go#.#.#.#.darwin-amd64-osx10.8.tar.gz`.

Richten Sie zwei Umgebungsvariablen ein:

  1. `GOPATH` zeigt auf den Workspace, bei mir ist das `$HOME/code/go`.
  2. Wir müssen Go's Binary an unseren `PATH` anhängen.

Man kann diese Variabeln von der Kommandozeile aus ausführen:

    echo 'export GOPATH=$HOME/code/go' >> $HOME/.profile
    echo 'export PATH=$PATH:/usr/local/go/bin' >> $HOME/.profile

Um die Variabeln zu aktivieren, kann man entweder die Kommandozeile neustarten oder man kann folgendes Kommando ausführen: `source $HOME/.profile`.

Geben Sie `go version` ein, was hoffentlich in einer ähnlichen Anzeige wie dieser resultiert: `go version go1.3.3.3 darwin/amd64`

## Windows

Laden sie sich die neuste ZIP-Datei herunter. Wenn sie auf einem x64 System arbeiten, brauchen Sie die Datei `go#.#.#.windows-amd64.zip`, wobei `#.#.#` der neusten Go-Version entspricht.

Entpacken sie die ZIP-Datei in einen Ordner Ihrer Wahl. Mit `c:\Go` ist man gut beraten.

Setzen Sie zwei Umgebungsvariabeln:

1. `GOPATH` zeigt auf Ihren Workspace. Der Wert dieser Umgebungsvariable könnte zum Beispiel `c:\users\goku\work\go` sein.
2. Fügen Sie `c:\Go\bin` zu Ihrer `PATH` Umgebungsvariable hinzu.

Umgebungsvariablen können gesetzt werden, indem man den `Umgebungsvariabeln`-Knopf in der `Erweitert` Schaltfläche des `System` Menupunktes in der Systemsteuerung drückt. Gewisse Versionen von Windows bieten diese Einstellung die `Erweiterte Systemeinstellungen` Option des `System` Menupunktes in der Systemsteuerung.

Öffnen Sie eine Kommandozeile und geben Sie `go version` ein. Jetzt sehen Sie hoffentlich in der Ausgabe etwas ähnliches wie das: `go version go1.3.3 windows/amd64`.

# Kapitel 1 - Die Basics

Go ist eine kompilierte und statisch-typisierte Programmiersprache mit ein C-ähnlichen Syntax und mit Garbage Collection. Was bedeuted das?

## Kompilierung

Die Kompilierung ist der Prozess des Übersetzens des Sourcecodes in eine tiefere Sprache - entweder Assembly (wie bei Go), oder in eine Zwischensprache (wie bei Java und C#).

Kompilierte sprachen können mühsam sein, da die Kompilierung langsam sein kann. Es ist schwierig Änderungen auszuprobieren, wenn man bei jeder Kompilierung Minuten oder gar Stunden warten muss. Die Kompilierungsgeschwindigkeit ist eines der Hauptziele von Go. Das ist eine gute Nachricht für Leute, die an einem grossen Projekt arbeiten oder auch für diejenigen, die es gewöhnt sind mit einem schnellen Feedback-Zyklus zu arbeiten, so wie man es von interpretierten Sprachen kennt.

Kompilierte Sprachen neigen dazu etwas schneller zu laufen und funktionieren ohne zusätzliche Abhängigkeiten (zumindest bei Sprachen wie C, C++ oder Go, die direkt zu Assembly kompilieren).

## Statische Typisierung

Wenn eine Sprache statisch typisiert ist, bedeutet das, dass Variablen von einem bestimmten Typ sein müssen (int, string, bool, []byte, etc.). Dies wird entweder durch die Angabe des Typs bei der Deklaration der Variable erreicht oder in vielen Fällen durch Ableitung des Typs durch den Compiler (wir werden uns in Kürze Beispiele ansehen).

Es gibt noch viel mehr, was man über statische Typisierung sagen kann, aber ich glaube, statische Typisierung ist etwas, das man besser versteht, wenn man sich Code ansieht. Wenn Sie es gewohnt sind, dynamisch typisierte Sprachen zu verwenden, kann es sein, dass Sie statische Typisierung etwas umständlich finden. Damit liegen Sie nicht falsch, aber es gibt Vorteile, besonders wenn man statische Typisierung mit Kompilierung verbindet. Die beiden sind oft verschmolzen. Es ist wahr, dass, wenn man das eine hat, normalerweise auch das andere hat, aber das ist keine harte Regel. Mit einem statischen Typsystem ist ein Compiler in der Lage, Probleme über syntaktische Fehler hinaus zu erkennen und weiter zu optimieren.

Wenn eine Programmiersprache eine C-ähnliche Syntax hat, bedeutet das, dass wenn Sie an andere C-ähnliche Sprachen wie C, C++, Java, JavaScript und C# gewöhnt sind, dann Ihnen auch diese Sprache bekannt vorkommen wird - zumindest oberflächlich. Es bedeutet zum Beispiel, dass `&&` als boolesches UND verwendet wird, `==` zum Vergleich der Gleichheit verwendet wird, `{` und `}` einen Scope starten und beenden, und Array-Indizes bei null beginnen.

C-ähnliche Syntax bedeutet auch, Semikolons beenden eine Zeile und Klammern finden sich um Bedingungen. Go macht Schluss mit beidem, obwohl Klammern immer noch verwendet werden, um Priorität zu kontrollieren. Zum Beispiel sieht eine `if`-Anweisung so aus:

```go
if name == "Leto" {
  print("the spice must flow")
}
```

In etwas komplizierteren Fällen sind Klammern immer noch nützlich:

```go
if (name == "Goku" && power > 9000) || (name == "gohan" && power < 4000)  {
  print("super Saiyan")
}
```

Abgesehen davon ist Go viel näher an C als C# oder Java - nicht nur in Bezug auf die Syntax, sondern auch in Bezug auf den Zweck. Das spiegelt sich in der Knappheit und Einfachheit der Sprache wider, die hoffentlich offensichtlich wird, wenn man sie lernt.

## Garbage Collection

Einige Variablen, wenn sie erstellt werden, haben eine leicht zu definierende Lebensdauer. Eine Variable, die sich lokal zu einer Funktion befindet, verschwindet beispielsweise, wenn die Funktion beendet wird. In anderen Fällen ist es nicht so offensichtlich - zumindest für einen Compiler. Beispielsweise kann die Lebensdauer einer Variablen, die von einer Funktion zurückgegeben oder von anderen Variablen und Objekten referenziert wird, schwierig zu bestimmen sein. Ohne Garbage Collection liegt es an den Entwicklern, den mit solchen Variablen verbundenen Speicher an einem Punkt wieder freizugeben, an dem der Entwickler weiß, dass die Variable nicht benötigt wird. Wie? In C würden Sie die Variable mittls `free(str);` wieder freigeben.

Sprachen mit Garbage Collection (z.B. Ruby, Python, Java, JavaScript, C#, Go) können Variabeln im Augen behalten und schliesslich freigeben, wenn sie nicht mehr verwendet werden. Die Garbage Collection bringt Mehraufwand, beseitigt aber auch eine Reihe von verheerenden Bugs.

## Go-Code ausführen

Lassen sie uns für den Anfang ein einfaches Programm erstellen um zu lernen, wie man es Kompilieren und Ausführen kann. Öffnen Sie ihren Lieblingseditor und geben Sie folgenden Code ein:

```go
package main

func main() {
  println("it's over 9000!")
}
```

Speichern Sie die Datei als `main.go`. Momentan ist es noch egal wo Sie die Datei Speichern. Wir brauchen die Datei nicht im Go-Workspace für solche trivialen Beispiele.

Als nächstes, öffnen Sie die Kommandozeile und wechseln Sie zum Verzeichnis, wo Sie die Datei gespeichert haben. Bei mir resultiert das im Kommando `cd ~/code`.

Schliesslich können Sie das Programam ausführen, indem Sie folgendes eingeben: 

```
go run main.go
```

Wenn alles funktioniert hat, sollten Sie die Ausgabe *it's over 9000!* sehen.

Einen Moment, was ist mit dem Kompilierungsschritt? `go run` ist ein praktisches Kommando, welches das Programm Kompiliert und sogleich ausführt. Das Kommando nutzt ein temporäres Verzeichnis um das Programm zu kompilieren und anschliessend auszuführen. Danach wird das temporäre Verzeichnis bereinigt. Das temporäre Verzeichnis wird sichtbar, wenn man folgendes Kommando ausführt.

```
go run --work main.go
```

Um explizit Code zu kompilieren, brauchen Sie `go build`:

```
go build main.go
```

Dieses Kommando generiert eine ausführbare Datei namens `main`, welche Sie ausführen können. Auf Linux und OSX ist zu beachten, dass die `./`-Prefix benötigt ist. Geben Sie also `./main` ein.

Während der Entwicklung können Sie entweder `go run` oder `go build` verwenden. Wenn Sie Ihren Code jedoch ausliefern, ist es zu empfehlen, ein Binary über `go build` zu bereitstellen.
