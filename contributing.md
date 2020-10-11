# How to contribute to the project

*You may be interested in the [LaTeX Workshop](https://github.com/openhsr/LaTeX-Workshop) organized by OpenHSR.*

## I have found a typo / error! How can I fix it?

If you *do know how to use LaTeX and Git*, you can fork the repository, fix it, and open a pull request, or open an issue with a patch attached if the fix is short. Tip: You can create a patch by making a commit and then typing

```
$ git format-patch -1 HEAD
```

This will generate a file named something like `0001-The-commit-message.patch`, that can be attached in the issue or directly sent to us.

If you *do know how to use LaTeX* but not Git, you can

  - [Learn to use git](./tutorials/install-git.md) and do the above
  - Open an issue on Github describing how to fix it
  - Ask somebody that knows how to use Git to help you

If you *don't know how to use neither LaTeX nor Git*, the best course of action is to contact the original author and ask them to fix the problem. If the original author cannot fix the issue, then the next best step is to ask somebody from the community, we can find us around in the campus (well, maybe it is not as easy now because of COVID) or at fachschaft@elektrotechnik-hsr.ch .

## I want to write a new cheat sheet for a module

We have [a template](https://github.com/HSR-Stud/VorlageZF) for you to use, to save yourself some work. But wait! Read a bit more below before starting.

### Checklist

You may want to quickly check if

  - I know LaTeX
  - I know how to use Git
  - I have a Github account
  - There is not any previous cheat sheet for `<module name>`
  - Or I am sure that I want to rewrite a new one from scratch

## HSR-Stud Vorgaben für Repositories?
Damit ein Dokument in die HSR-Stud Gruppe aufgenommen werden kann, gibt es einige zwingende Vorgaben.
Jedes Repo muss:
-  eine Lizenz enthalten, die klar deklariert, wie man die Zusammenfassung verwenden darf
-  sämtliche Contributoren/Autoren aufführen
-  mit Tags zu Modulname, Semesternummer, Studiengang versehen sein
-  den richtigen Namen enthalten - also die Namenskonvention erfüllen

Hat folgende Struktur:
- image (Ordner)
- tex 
- license
- .gitignore
- README.md

Wenn du unsere Vorlage [Vorlage](https://github.com/HSR-Stud/VorlageZF) benützt, ist vieles einfacher und schon implementiert.

### Inhalt des README.md
#### DOs
- Name des Repos
- Verwendungszweck (Formelsammlung, Zusammenfassung, Cheatsheet)
- kurze Beschreibung über Inhalt (1-5 Sätze)
- Latex Tool zum kompilieren (zB: xelatex)
- Lizenz

#### Optional
- Seitenzahl oder wie es ausgedruckt werden soll.
- Inhaltsverzeichnis
- woher das Repo kommt

#### Dont's
alles das von Semester zu Semester ändert
- Prüfungsinhalt
- erlaubte Hilfsmittel an Prüfung

### Lizenz deklarieren 
Die Zusammenfassung muss als Creative Commons oder Public Domain veröffentlicht werden. Die Lizenz muss im README.md UND in der LICENSE.txt UND im Dokument deklariert sein. 

Falls nicht trifftige Gründe dagegen sprechen, bitten wir dich folgende Lizenz zu verwenden:
- CC by-nc-sa (Namensnennung, nicht kommerziell, Weitergabe unter gleichen Bedingungen)

Alternativ wären auch folgende Lizenzen möglich:
- CC by (Namensnennung)
- CC by-sa (Namensnennung, Weitergabe unter gleichen Bedingungen)
- CC by-nc (Namensnennung, nicht kommerziell)
- CC0 (Public Domain, keine Einschränkungen)
Die CC-Lizenz welche keine Bearbeitung erlaubt ist dabei *nicht* zugelassen!
Weitere Details gibts auf http://creativecommons.org/licenses/.


### Namenskonvention
Grundsätzlich gilt: Es sollte wieder in das ursprüngliche Git-Projekt zurückgeforkt werden!
(Dies ist der Sinn und Zweck von HSR-Stud, dass sich die Formelsammlungen dem Stoff anpassen.)

Hast du ein **neues** Repo erstellt, gilt folgende Namenskonvention:
1. ModulName: Bei einem Repo von einem Fach von dem es bisher noch keine Zusammenfassung gab.
2. ModulName_Jahr: Bei einem neuen Repo, wo es schon eine erste Zusammenfassung gab.
3. ModulName_Jahr_Nummer: Bei einem neuen Repo, wo es schon eine Zusammenfassung im gleichen Jahr gab.
