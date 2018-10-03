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

Laden sie sich die neuste ZIP-Datei herunter. Wenn sie auf einem x64 System arbeiten, brauchen Sie die Datei `go#.#.#.windows-amd64.zip`, wobei `#.#.#` der neusten Go-Version entspricht.