# Travis
## Anwendung
 Travis als Submodul einfügen  
 
     git submodule add https://github.com/HSR-Stud/Travis Travis

 .travis.yml in die oberste Ebene des Repos kopieren.  
 Das neue .travis.yml bearbeiten.  
      - Unter skript und file den aktuellen Dokumentnamen einfügen.  
      -  (bibtex auskommentieren)  
      
## Installation
 Zur Nutzung von Travis musst du dich für das [Github Student Developer Pack](https://education.github.com/pack) registriert haben.  
 [Travis anmelden](https://travis-ci.org/)  
 Github Token erstellen: [creating-a-personal-access-token](https://help.github.com/articles/creating-a-personal-access-token-for-the-command-line/)  
 Als GITHUB_RELEASE_TOKEN bennen  
     - Rechte: public_repo, repo_deployment  
     - Token lokal sicher abspeichern und bei Travis hinzufügen.
