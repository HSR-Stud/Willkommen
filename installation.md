 # Installation
 ### Latex 
 Damit du Latex nutzen kannst musst du zuerst ein Softwarepaket (MikTex) und dann einen Editor (Texstudio) herunterladen.
 Nach der Installation von MikTex und Texstudio soltest du kurz deinen Computer neu starten, damit alle Konfigurationen automatisch korrekt sind.
   1. [MikTex installieren](https://miktex.org/download) (mit Adminrechten)
   2. [Texstudio installieren](https://www.texstudio.org) (mit Adminrechten) 

### Git-Installation mit Sourcetree / GitHub
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
