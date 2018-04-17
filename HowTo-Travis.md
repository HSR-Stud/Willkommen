# Travis
     
Travis wird die Projekte automatisiert builden, und falls der Commit einen neuen Tag hat diesen unter deinem Namen im Projekt releasen (Bedingungen für den Release können im `.travis.yml` angepasst werden). Dafür brauchst du einen Account in [Travis-CI](https://travis-ci.org/), und einen Token, mit welchem Travis sich bei GitHub authentifizieren und somit die builds releasen kann.

## Installation 
- [Travis anmelden](https://travis-ci.org/) 
- Github-Projekt auf der Profilseite suchen und aktivieren (`https://travis-ci.org/profile/USERNAME`)
- Github Token erstellen: [creating-a-personal-access-token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)  
- Token mit `GITHUB_RELEASE_TOKEN` bennen  
     - Rechte: `public_repo`, `repo_deployment`
- Token lokal sicher abspeichern 
- Token in Travis-CI im Projekt (`https://travis-ci.org/HSR-Stud/PROJECTNAME/settings`) als Environment Variable hinzufügen
     - **ACHTUNG:** Der Token darf im Display Log nicht angezeigt werden: `Display value in build log` muss `OFF` sein!!
     - Name der Variable muss wieder `GITHUB_RELEASE_TOKEN` sein

## Anwendung
 - Travis als Submodul einfügen  
     `git submodule add https://github.com/HSR-Stud/Travis Travis`
 - `.travis.yml` in die oberste Ebene des Repos kopieren.  
 - Das neue `.travis.yml` bearbeiten.  
      - Unter `script` und `file` den aktuellen Dokumentnamen einfügen.  
      - `bibtex` auskommentieren, falls es nicht benötigt wird.

## Build status im Readme anzeigen
- Im Projekt auf den Build Status klicken (rechts neben dem Projektnamen)
- Branch auswählen
- Statt "Image URL" "Markdown" auswählen
- Text kopieren
- In Readme eintragen
- Committen
