# Willkommen 
## Einleitung  
### Was ist der Grundgedanke hinter HSR-Stud?
An der HSR finden jedes Jahr ähnliche Prüfungen zum selben Stoff statt. Warum also immer alle Zusammenfassungen selber schreiben? Es gibt doch sicher Zusammenfassungen von den Vorgänger! Das Projekt HSR-Stud verfolgt genau dieses Ziel: Hier werden LaTeX-Zusammenfassungen gesammelt und zur Verfügung gestellt. Im Gegensatz zum Studentenportal, wo fertige Zusammenfassungen gepostet werden, ist dieses Projekt für die gemeinsame kontinuierliche Arbeit an Zusammenfassungen gedacht.

### Was findest du in diesem Repo?
Dies Repo dient dir dazu einen leichteren Einstieg in Latex, GitHub, Git und SourceTree zu finden.
Du findest hier Informationen zu Fragen wie: 
- [Was ist LaTex?](https://praxistipps.chip.de/was-ist-latex-einfach-erklaert_48193) 
- [Was ist Git?](https://git-scm.com/doc)  
- [Wie funktioniert Git mit dem GUI Sourcetree?](https://confluence.atlassian.com/get-started-with-sourcetree)  
- [Was ist GitHub?](https://t3n.de/news/eigentlich-github-472886/) 

#### Inhaltsverzeichnis
- [Installation](https://github.com/HSR-Stud/Willkommen#installation)  
- [Wie finde ich Repositorys auf HSR-Stud?](https://github.com/HSR-Stud/Willkommen#wie-finde-ich-repositorys-auf-hsr-stud)
- [HSR-Stud Vorgaben für Repositories?](https://github.com/HSR-Stud/Willkommen#hsr-stud-vorgaben-zur-erstellung-und-bearbeitung-von-respositories)
- [Wie bearbeite ich ein bestehendes Repository auf HSR-Stud?](https://github.com/HSR-Stud/Willkommen#wie-bearbeite-ich-ein-bestehendes-repository-auf-hsr-stud) 
- [Wie erstelle ich ein neues Repository auf HSR-Stud?](https://github.com/HSR-Stud/Willkommen#wie-erstelle-ich-ein-neues-repository-auf-hsr-stud) 

- [Travis](https://github.com/HSR-Stud/Willkommen#travis)  

### Werde aktiv
Dieses Projekt ist auf deine Hilfe angewiesen. Damit die Zusammenfassungen aktuell bleiben und Fehler korrigiert werden brauchen wir deine Unterstützung. Willst du eigene Repos erstellen oder bei uns im Admin-Team mithelfen? Dann schreibe ein E-Mail an fachschaft@elektrotechnik-hsr.ch mit deinem GitHub-Username.
Hier findest du weitere Infos, die für dich als aktiver Contributor interessant sein könnten:
- [Wie erstelle oder clone ich ein Repository?](https://github.com/HSR-Stud/Willkommen#wie-erstelle-ich-ein-repository-auf-hsr-stud)
- [Wie nutze ich Travis zur automatischen Erzeugung eines PDF's?](https://github.com/HSR-Stud/Willkommen#travis)  
<!--- Wie kann die Submodules löschen oder Fehler beim Submodule-Link beheben?--->

### Weitersagen
Mache diese Seite möglichst vielen anderen HSR-Studenten bekannt. Denn mehr Mitwisser → mehr Mitmacher → bessere Zusammenfassungen!

### Support
Kein Plan wie das ganze funktioniert? Im [Wiki](http://hsr-stud.github.io/) findest du Anleitungen und viele Tipps.
Wenn du Fragen zu LaTeX hast, gibts zudem hier meistens sehr schnell sehr gute Antworten: http://tex.stackexchange.com/.
Notfalls kannst du dich auch ans Adminteam wenden unter fachschaft@elektrotechnik-hsr.ch. 

---  

 # Installation
 ## LaTeX 
 Damit du Latex nutzen kannst musst du zuerst ein Softwarepaket und dann einen Editor herunterladen.
 
 ### LaTeX Distribution
 Die beliebtesten Latex distributionen sind MikTex und TexLive. Beide Distributionen sind Cross-Platform. Die Installation sollte mit Adminrechten ausgeführt werden.
 
- [MikTex](https://miktex.org/download) 
- [TexLive](https://www.tug.org/texlive/acquire-netinstall.html)
	- [Direct Link für den Windows-Installer](http://mirror.ctan.org/systems/texlive/tlnet/install-tl-windows.exe)
	- [Direct Link für alles andere ausser Windows](http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz)
	- [Direct Link für wenn man sich nicht so ganz sicher ist, welches Betriebssystem man hat](http://mirror.ctan.org/systems/texlive/tlnet/install-tl.zip)

## Editor/IDE
LaTeX Code kann mit jedem beliebigen Editor geschrieben werden, auch mit Notepad++, Vim, Emacs oder ähnlichem. Die beliebtesten Editoren für LaTeX sind 

- [Texstudio](https://www.texstudio.org)
- [Texmaker](http://www.xm1math.net/texmaker/)
- [TexLipse](http://texlipse.sourceforge.net/)

Texstudio und Texmaker sind standalone IDEs, welche spezifisch für LaTeX entwickelt wurden. TexLipse ist ein Eclipse Plugin. Dies bietet den Vorteil, dass kein zusätzliches Tool installiert werden muss. Viele der HSR-Stud Projekte sind mit vorkonfigurierten TexLipse Projekten versehen, die einfach in TexLipse importiert werden können.

### TexLipse Installation und Konfiguration
TexLipse kann wie jedes Eclipse Plugin über `Help/Install New Software` installiert werden. Hier eine [detaillierte Anleitung](http://texlipse.sourceforge.net/manual/installation.html). Nach der Installation muss man nur noch die Pfade zur TeX Distribution angeben, dann kann man loslegen. Dies passiert Projektübergreifend, in den Workspace-Einstellungen. Auch hier [eine Anleitung](http://texlipse.sourceforge.net/manual/configuration.html) dazu. 

Ein kleiner Tipp: gib das `bin` directory der Distribution unten an, damit du nicht jeden einzelnen Pfad eingeben musst.

## Git-Installation mit Sourcetree / GitHub
GitHub basiert auf der Software Git, welche zur Versionskontrolle & -verwaltung eingesetzt wird. Git kann von der Kommandozeile (Git CMD) aus genutzt werden. Dies ist jedoch sehr mühsam, weshalb wir die Nutzung des Git-Guis Sourcetree empfehlen. 
   1. [GitHub Account erstellen](https://www.github.com)
   Dabei solltest du unbedingt deine HSR-Emailadresse verwenden, denn dann hast du direkt Anspruch auf ein Github Student Developer Pack.    Dies erlaubt es dir unlimitierte private Repositories auf Github zu erstellen, Gratis Continuous Integration mit Travis-CI für private    Repositories sowie AWS und Digital Ocean Credits. 
   2. [Github Student Developer Pack beantragen](https://www.openhsr.ch/tipps/github-education-pack/)  
   3. [Sourcetree installieren für ein Git_GUI](https://www.sourcetreeapp.com/)  
   3.1 Atlassin Account erstellen (zwar ist sourcetree gratis, aber dennoch benötigst du eine Lizenz)  
   3.2 Mit GitHub-Account verknüpfen (am Besten bist du dann immernoch im Browser auf GitHub eingeloggt)  
   3.3 Es muss kein globales .gitignore File erstellt werden  
   3.4 Es muss kein SSH-Schlüssel erstellt werden  
   3.5 Sobald du beim Clonen eines Repos angelang bist, kann du den weiteren Setup übersprungen  


## Weitere nützliche Tools

- [excel2latex](https://ctan.org/pkg/excel2latex?lang=de)  
   Konvertiert Excel-Tabellen unter Beibehaltung der Formatierungen und Berechnungen in das LaTeX-Format.  
- [mathpix](https://mathpix.com/)  
   Erstelle einen Screenshot einer Formel und kopiere den daraus erstellten LaTeX-Code in den Editor.  
- [matlab2tikz](https://tomlankhorst.nl/matlab-to-latex-with-matlab2tikz/)  
    Konvertiere Matlab-Plots in ein TikZ/Pgfplots.  
- [JabRef](http://www.jabref.org/)  
    Bibliograpy reference manager für BibTeX.  	  
	  
[Home](https://github.com/HSR-Stud/Willkommen#willkommen)

----

# Wie finde ich Repositorys auf HSR-Stud?
Die Suchfunktion hilft unterhalb der angepinnten Repositories hilft dir dich zurechtzufinden. 
Die Suche funktioniert mit verschiedenen Tags. Dabei gibt es Tags für [latex](https://github.com/search?q=topic%3Alatex+org%3AHSR-Stud&type=Repositories) und [vorlage](https://github.com/search?q=topic%3Avorlage+org%3AHSR-Stud&type=Repositories) sowie Modulname und das Semester (gemäss Musterstudienplan).

#### Vorlagen für Zusammenfassung
[Vorlage](https://github.com/search?q=topic%3Avorlage+org%3AHSR-Stud&type=Repositories)  

#### Mathematik
Alle Repos  [Mathematik](https://github.com/search?q=topic%3Amath+org%3AHSR-Stud&type=Repositories)  

#### Gesellschaft Wirtschaft Recht
Alle Repos [GWR](https://github.com/search?q=topic%3Agwr+org%3AHSR-Stud&type=Repositories)  

#### Naturwissenschaft
Alle Repos [NatWis](https://github.com/search?q=topic%3Anatwis+org%3AHSR-Stud&type=Repositories)

#### Elektrotechnik
Alle Repos [Elektrotechnik](https://github.com/search?q=topic%3Aelektrotechnik+org%3AHSR-Stud&type=Repositories)  
Sortiert nach Semester  
[e-sem1](https://github.com/search?q=topic%3Ae-sem1+org%3AHSR-Stud&type=Repositories)  
[e-sem2](https://github.com/search?q=topic%3Ae-sem2+org%3AHSR-Stud&type=Repositories)  
[e-sem3](https://github.com/search?q=topic%3Ae-sem3+org%3AHSR-Stud&type=Repositories)  
[e-sem4](https://github.com/search?q=topic%3Ae-sem4+org%3AHSR-Stud&type=Repositories)  
[e-sem5](https://github.com/search?q=topic%3Ae-sem5+org%3AHSR-Stud&type=Repositories)  
[e-sem6](https://github.com/search?q=topic%3Ae-sem6+org%3AHSR-Stud&type=Repositories)  

#### Maschinenbau | Innovation
Alle Repos [Maschinenbau](https://github.com/search?q=topic%3Amaschinenbau+org%3AHSR-Stud&type=Repositories)  
Sortiert nach Semester  
[mi-sem5](https://github.com/search?q=topic%3Ami-sem5+org%3AHSR-Stud&type=Repositories)  
[mi-sem6](https://github.com/search?q=topic%3Ami-sem6+org%3AHSR-Stud&type=Repositories)  
#### Bauingenieur
Alle Repos [Bauingenieur](https://github.com/search?q=topic%3Abauingenieur+org%3AHSR-Stud&type=Repositories)  
Sortiert nach Semester  

#### MSE
Alle Repos [MSE](https://github.com/search?q=topic%3Amse+org%3AHSR-Stud&type=Repositories)  

[Home](https://github.com/HSR-Stud/Willkommen#willkommen)

---

# HSR-Stud Vorgaben für Repositories?
Damit ein Dokument in die HSR-Stud Gruppe aufgenommen werden kann, gibt es einige zwingende Vorgaben.
Jedes Repo muss:
-  eine Lizenz enthalten, die klar deklariert, wie man die Zusammenfassung verwenden darf
-  sämtliche Contributoren aufführen
-  mit Tags zu Modulname, Semesternummer, Studiengang versehen sein
-  den richtigen Namen enthalten - also die Namenskonvention erfüllen
-  sauberes Latex enthalten

Ein vorbildliches Repo enthält zudem:
-  ein ReadMe mit generellen Informationen (siehe ReadMe aus Vorlage-Repo)
- "builded" autonom ein PDF bei jedem neuen Release mit Travis

## Lizenz deklarieren 
Die Zusammenfassung muss als Creative Commons oder Public Domain veröffentlicht werden. Die Lizenz muss im README oder in der LICENSE.txt und im Dokument deklariert sein. Die CC-Lizenz welche keine Bearbeitung erlaubt ist dabei nicht zugelassen.

Aktuell muss also eine der folgenden Lizenzen gewählt werden:
- CC by (Namensnennung)
- CC by-sa (Namensnennung, Weitergabe unter gleichen Bedingungen)
- CC by-nc (Namensnennung, nicht kommerziell)
- CC by-nc-sa (Namensnennung, nicht kommerziell, Weitergabe unter gleichen Bedingungen)
- CC0 (Public Domain, keine Einschränkungen)
Weitere Details gibts auf http://creativecommons.org/licenses/.

Einen Wizard, um eine CC Lizenz auszuwählen, gibts auf http://creativecommons.org/choose/.

Um die gewählte Lizenz in dein Projekt zu übernehmen, ist es am Einfachsten, das entsprechende MarkDown-File aus diesem [Ordner](https://github.com/HSR-Stud/Creative-Commons-Markdown/tree/master/4.0) als **LICENSE.txt** in dein Projekt zu kopieren.

Die Lizenz sollte im Header- oder Footer auf jedem Blatt deiner Zusammenfassung anzeigt werden. Schau dazu im "header"-Repo, dort findest du ein Beispiel, wie du die Lizenz einfügen kannst. 

## Beitragende auflisten 
Es ist fair, alle Leute zu erwähnen, die zu einer Zusammenfassung beigetragen haben. Deshalb soll jedes Repository im Hauptverzeichnis eine Datei namens **CONTRIBUTORS.txt** haben, welche alle Mitwirkenden auflistet.

Format:
Vorname Name (HSR-Kürzel)  ...eine Zeile pro Person.

## Tags hinzufügen 
Bitte fügt eurem Repo die entsprechenden Tags in den Settings hinzu. Diese helfen es anderen Studenten die Repos zu finden und trägt zur Ordnung auf HSR-Stud bei. Es sollte mindesten ein Tag haben für:
- Kürzel des Studienfachs und evtl. Studienfach (z.B. IntTra, Integraltransformation) 
- Studiengang (z.B. elektrotechnik, mse, informatik)
- Semester (z.B. e-sem3 - Elektrotechnik Semester 3)
Weitere Hinweise zu häufig verwendeten Tags findet du [hier](https://github.com/HSR-Stud/Willkommen/blob/master/HowTo-Find%20a%20Repository.md= ).

## Namenskonvention
1. ModulName: Bei einem Repo von einem Fach von dem es bisher noch keine Zusammenfassung gab
2. ModulName_Jahr: Bei einem neuen Repo, wo es schon eine erste Zusammenfassung gab
3. Kein neues Repo: Wenn ein bestehendes Repo lediglich leicht abgeändert wurde!
WICHTIG: Es soll kein neues Repo erstellt werden, wenn lediglich kleine Änderungen/Verbesserungen gemacht wurden!

## Sauberes LaTeX schreiben 
Im LATeX 2ε–Sündenregister werden sinnvolle Richtlinien zum Umgang mit LaTeX vorgegeben. Die "[Todsünden](http://dante.ctan.org/tex-archive/info/l2tabu/german/l2tabu.pdf)" sind zwingend zu beachten.
Wenn man das Package nag nutzt, werden l2tabu-Verstösse automatisch als Warnungen auf der Konsole ausgegeben.
<!--- LINK TOT Weitere "Best Practices" zu LaTeX gibts hier: http://stackoverflow.com/questions/193298/best-practices-in-latex --->

[Home](https://github.com/HSR-Stud/Willkommen#willkommen)

---

# Wie bearbeite ich ein bestehendes Repository auf HSR-Stud?

Du hast einen Fehler in einer bestehenden Zusammenfassung gefunden oder eine kleine Verbesserung/Veränderung in einem Rep0 gemacht?
Dann solltest du folgenden Schritten folgen:
1. xxx
2. 
3. 

---
# Wie erstelle ich ein neues Repository auf HSR-Stud?
### Erstelle ein lokales Repository mit Sourcetree
1. Öffne Sourcetree 
2. Klicke auf das + bei den Tabs  
3. Du hast die Auswahl zwischen Clonen, Add und Create.  
4. Um ein neues Repository zu erstellen klicke auf Create.  
4.1 Wähle aus, wo das Repo erstellt werden soll. Achtung nicht in einer Cloud (Google Drive, Dropbox etc.).  
4.2  Gib an, wie das Repo auf deinem Rechner heissen soll.  
4.3 Klicke auf Create  
  
Wenn du nachträglich dein Repo auch auf Github laden willst musst du folgendermassen vorgehen:  
1. Erstelle ein Repository auf Github.  
2. Gehe in Sourcetree auf das Repo welches du auf Github laden willst.  
3. Klicke oben rechts auf Settings.  
3.1 Klicke auf Remotes, hier siehst du die verschiedenen "Server" aufgelistet.  
3.2 Klicke auf add  
3.3 Gib dem remote einen Namen  
3.4 Gehe auf das neu erstellte Github-Repo mit welchem du dein lokales Repo verknüpfen willst und klicke auf Clone or Download.  
3.5 Kopier den Url ins Sourcetree.  
3.6 Sourcetree sollte das Host-Repo selbständig erkennen.  

### Erstelle ein Repository auf Github
1. Gehe auf [Github](www.github.com)  
2. Klicke auf das + oben rechts neben deinem Profilbild.  
3. Klick auf New repository
3.1 Der Name des Repository sollte im Stil von Elo2_FS16 sein.
4. Wähle den Owner  
4.1 Du kannst entweder dein Usernamen auswählen oder ein Repo in HSR-Stud erstellen.  
5. Wähle aus ob das Repo öffentlich oder privat ist.
6. Klicke auf Create repository.

### Clonen eines Repos mit Sourcetree
1. Öffne Sourcetree  
2. Klicke auf das + bei den Tabs  
3. Du hast die Auswahl zwischen Clonen, Add und Create.  
4. Um ein bestehendes Repo zu Clonen, klicke auf Clonen.  
4.1 Gib den Pfad zum Repo ein. Bsp. : https://github.com/HSR-Stud/Willkommen.git  
4.2 Wähle aus, wo das Repo gespeichert werden soll. Achtung nicht in einer Cloud (Google Drive, Dropbox etc.).  
4.3 Gib an, wie die Kopie des Repos auf deinem Rechner heissen soll.  
4.3.1 (!) Wenn das Repo Submodule enthält, musst du unter Advanced Options die Checkbox "Recurse submodules" aktivieren.  
Falls du auf Probleme stösst findest du hier noch die offizielle [Sourcetree Anleitung zum Clonen eines Repos](https://confluence.atlassian.com/bitbucket/clone-a-repository-223217891.html). 

#### Submodule
Submodule sind eigenständige Repos, welche als Inputs in andere Repos gelinkt wurden (oftmals header oder idiotenseite). 
Wurde bei einem Repo mit Submodulen anfänglich vergessen diese hinzuzufügen kannst du folgende Schritte unternehmen:  
1. Gehe auf das Repo in Sourcetree
2. Unten links findest du den Reiter *Submodule*. Dort siehst du die verwendeten Submodules.  
3. Mit einem Rechtsklick auf dem Submodule kannst du auf anzeigen drücken und dann wird es heruntergeladen.

<!---
## Wer sieht was?
### Private and Public

### Lese und Schreibrechte
--->


[Home](https://github.com/HSR-Stud/Willkommen#willkommen)

---

# Travis
     
Travis kann als ein Tool verwendet werden um Repos automatisiert zu "builden". Falls im gewählten Repo ein neuer Tag erstellt wird, dann wird der Build (PDF-File) unter deinem Namen im Projekt released. \
Weitere Infos findest du unter: [Travis README](https://github.com/HSR-Stud/Travis/blob/master/README.md)

[Home](https://github.com/HSR-Stud/Willkommen#willkommen)

---

