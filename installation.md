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

[Wie erstelle oder clone ich ein Repository?](https://github.com/HSR-Stud/Willkommen/blob/master/HowTo-Create%20a%20Repository.md#create-a-repository)  

## Weitere nützliche Tools

- [excel2latex](https://ctan.org/pkg/excel2latex?lang=de)  
   Konvertiert Excel-Tabellen unter Beibehaltung der Formatierungen und Berechnungen in das LaTeX-Format.  
- [mathpix](https://mathpix.com/)  
   Erstelle einen Screenshot einer Formel und kopiere den daraus erstellten LaTeX-Code in den Editor.  
- [matlab2tikz](https://tomlankhorst.nl/matlab-to-latex-with-matlab2tikz/)  
    Konvertiere Matlab-Plots in ein TikZ/Pgfplots.  
	  
[Home](https://github.com/HSR-Stud/Willkommen)

