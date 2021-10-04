# How to contribute to the project

*You may be interested in the [LaTeX Workshop](https://github.com/openhsr/LaTeX-Workshop) organized by OpenHSR.*

## I have found a typo / error! How can I fix it?

If you **do know how to use LaTeX and Git**, you can fork the repository, fix it, and open a pull request, or open an issue with a patch attached if the fix is short. Tip: You can create a patch by making a commit and then typing

```
$ git format-patch -1 HEAD
```

This will generate a file named something like `0001-The-commit-message.patch`, that can be attached in the issue or directly sent to us.

If you **do know how to use LaTeX but not Git**, you can

  - [Learn to use git](./tutorials/install-git.md) and do the above
  - Open an issue on Github describing how to fix it
  - Ask somebody that knows how to use Git to help you

If you **don't know how to use neither LaTeX nor Git**, the best course of action is to contact the original author and ask them to fix the problem. If the original author cannot fix the issue, then the next best step is to ask somebody from the community, we can find us around in the campus (well, maybe it is not as easy now because of COVID) or at fachschaft@elektrotechnik-hsr.ch .

## I want to write a new cheat sheet for a module

We have [a template](https://github.com/HSR-Stud/VorlageZF) for you to use, to save yourself some work. But wait! Read a bit more below before starting.

### Checklist

You may want to quickly check if

  - I know LaTeX
  - I know how to use Git
  - I have a Github account
  - There is not any previous cheat sheet for `<module name>`
  - Or I am sure that I want to rewrite a new one from scratch

Next you should take a look at our [LaTeX Guidelines](./Guidelines), to avoid committing typesetting crimes.

### Requirements

For a repository to be approved in the HSR-Stud organization, it needs to have the following:

  - Name according to the current naming convention
  - License (see below) with a copy of it in a `LICENSE.txt` file
  - Name of all authors and contributors to the document(s)
  - Correct Github tags to make it discoverable

To avoid having to set it up yourself we have a [Template](https://github.com/HSR-Stud/VorlageZF) that already does everything for you.

### License

Documents of the HSR-Stud must have an open license, that allows for future modification or adaptations of your work. Some good license for that are:

  - Public domain (with CC0 license)
  - [Creative Commons (CC)](https://creativecommons.org/choose) and its variants, we recommend (CC BY-NC-SA)

### What to put in README.md

Do's:

  - Name of the module
  - Purpose (Formelsammlung, Zusammenfassung, Cheatsheet)
  - Short description  (1 - 5 sentences)
  - Latex Tool(s) needed to compile (Ex: `xelatex`, `lualatex`)
  - License deed (not the whole thing!)

Optional:

  - Page count, suggestions on how to print
  - Table of contents
  - Sources

Dont's: what changes every semester

  - What will be / was in the exam
  - What you can take to the exam

### Naming convention

For new repositories the name shall be given as follows:

  1. `<ModuleName>`: If there were no previous documents of `Module`
  2. `<ModuleName>_<Year>`: If there was already a document for said module
  3. `<ModuleName>_<Year>_<Nr>`: If there is already one of the same year (how did that happen?)
