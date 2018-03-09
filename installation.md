 # Installation
 ### Latex 
   1. [MikTex installieren](https://miktex.org/download) (mit Adminrechten)   
   2. [Texstudio mit Adminrecht) installieren](https://www.texstudio.org) (mit Adminrechten) 
   2.1 (MikTex Package aktualisieren mit MikTex Package Manager)  


### Git-Installation mit Sourcetree / GitHub  
   1. [GitHub Account erstellen](https://www.github.com)
   Dabei solltest du unbedingt deine HSR-Emailadresse verwenden, denn dann hast du direkt Anspruch auf ein Github Student Developer Pack. Dies erlaubt es dir unlimitierte private Repositories auf Github zu erstellen, Gratis Continuous Integration mit Travis-CI für private Repositories sowie AWS und Digital Ocean Credits. 
   2. [Github Student Developer Pack beantragen](https://www.openhsr.ch/tipps/github-education-pack/)
   3. [Sourcetree installieren für ein Git_GUI](https://www.sourcetreeapp.com/)  
   3.1 Atlassin Account erstellen (zwar ist es gratis, aber dennoch benötigst du eine Lizenz)
   3.2 Mit GitHub-Account verknüpfen (am Besten bist du im Browser auf GitHub eingeloggt)
   3.3 Es muss kein globales .gitignore File erstellt werden  
   3.4 Es muss kein SSH-Schlüssel erstellt werden
   3.5 Sobald du beim Clonen eines Repos angelang bist, kann du den weiteren Setup übersprungen

### Clonen eines Repos mit Sourcetree
[Anleitung: Clonen eins Repos](https://confluence.atlassian.com/bitbucket/clone-a-repository-223217891.html)  
1. Öffne Sourcetree  
2. Klicke auf das + bei den Tabs  
3. Du hast die Auswahl zwischen Clonen, Add und Create.  
4. Um ein bestehendes Repo zu Clonen, klicke auf Clonen.  
4.1 Gib den Pfad zum Repo ein. Bsp. : https://github.com/HSR-Stud/Willkommen.git  
4.2 Wähle aus, wo das Repo gespeichert werden soll. Achtung nicht in einer Cloud (Google Drive, Dropbox etc.).  
4.3 Gib an, wie die Kopie des Repos auf deinem Rechner heissen soll.  
4.3.1 (!) Wenn das Repo Submodule enthält, musst du unter Advanced Options die Checkbox "Recurse submodules" aktivieren.  

#### Submodule
Submodule sind eigenständige Repos, welche als Inputs ein anderes Repo gelinkt wurde (oftmals header oder idiotenseite). 
Wurde bei einem Repo mit Submodulen anfänglich vergessen diese hinzuzufügen kannst du folgende Schritte unternehmen:  
1. Gehe auf das Repo in Sourcetree
2. Unten links findest du den Reiter *Submodule*. Dort siehst du die verwendeten Submodules.  
3. Mit einem Rechtsklick auf dem Submodule kannst du auf anzeigen drücken und dann wird es heruntergeladen.
