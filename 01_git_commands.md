# Grundlegende Dokumentation über die Versionskontrolle mit Git / Basic Documentation on Version Control with Git

## Einführung / Introduction
Git ist ein verteiltes Versionskontrollsystem, das von Linus Torvalds entwickelt wurde, um die Entwicklung des Linux-Kernels zu unterstützen. Es ermöglicht Entwicklern, den Verlauf von Änderungen in ihren Projekten zu verfolgen, verschiedene Versionen zu verwalten und effizient zusammenzuarbeiten.

Git is a distributed version control system developed by Linus Torvalds to support the development of the Linux kernel. It allows developers to track changes in their projects, manage different versions, and collaborate efficiently.

## Installation
### Auf Windows / On Windows:
1. Gehe zur [Git-Website](https://git-scm.com/) und lade den Windows Installer herunter.
2. Führe den Installer aus und folge den Anweisungen.

Go to the [Git website](https://git-scm.com/) and download the Windows installer. Run the installer and follow the instructions.

### Auf macOS / On macOS:
1. Verwende Homebrew: `brew install git`
2. Alternativ, lade den Installer von der [Git-Website](https://git-scm.com/) herunter und folge den Anweisungen.

Use Homebrew: `brew install git`. Alternatively, download the installer from the [Git website](https://git-scm.com/) and follow the instructions.

### Auf Linux / On Linux:
1. Verwende den Paketmanager deiner Distribution:
   - Debian/Ubuntu: `sudo apt-get install git`
   - Fedora: `sudo dnf install git`
   - Arch: `sudo pacman -S git`

Use the package manager of your distribution:
- Debian/Ubuntu: `sudo apt-get install git`
- Fedora: `sudo dnf install git`
- Arch: `sudo pacman -S git`

## Grundlegende Konzepte / Basic Concepts
### Repository
Ein Repository (Repo) ist ein Speicherort, der den gesamten Verlauf der Projektdateien und die Metadaten zur Versionsverwaltung enthält. Es gibt zwei Arten von Repositories:
- **Lokales Repository**: Befindet sich auf deinem lokalen Computer.
- **Remote Repository**: Befindet sich auf einem Server, z.B. auf GitHub, GitLab oder Bitbucket.

A repository (repo) is a storage location that contains the entire history of project files and version control metadata. There are two types of repositories:
- **Local Repository**: Located on your local computer.
- **Remote Repository**: Located on a server, such as GitHub, GitLab, or Bitbucket.

### Commit
Ein Commit ist eine Momentaufnahme des Projekts zu einem bestimmten Zeitpunkt. Jeder Commit hat eine eindeutige ID (SHA-1 Hash) und enthält eine Nachricht, die die vorgenommenen Änderungen beschreibt.

A commit is a snapshot of the project at a specific point in time. Each commit has a unique ID (SHA-1 hash) and contains a message describing the changes made.

### Branch
Ein Branch ist ein Zeiger auf einen Commit und wird verwendet, um parallele Entwicklungsstränge zu erstellen. Der Hauptbranch in den meisten Repositories heißt `main` oder `master`.

A branch is a pointer to a commit and is used to create parallel development lines. The main branch in most repositories is called `main` or `master`.

### Merge
Ein Merge kombiniert Änderungen aus verschiedenen Branches. Ein häufiger Anwendungsfall ist das Zusammenführen eines Feature-Branches in den `main`-Branch.

A merge combines changes from different branches. A common use case is merging a feature branch into the `main` branch.

## Grundlegende Befehle / Basic Commands
### Repository erstellen / Creating a Repository
```sh
git init
```
Initialisiert ein neues Git-Repository im aktuellen Verzeichnis.
Initializes a new Git repository in the current directory.

### Repository klonen / Cloning a Repository
```sh
git clone <repository-url>
```
Kopiert ein bestehendes Repository aus einer Remote-Quelle.
Copies an existing repository from a remote source.

### Änderungen verfolgen / Tracking Changes
1. Dateien zum Staging-Bereich hinzufügen / Adding files to the staging area:
    ```sh
    git add <datei>
    git add <file>
    ```

2. Änderungen committen / Committing changes:
    ```sh
    git commit -m "Commit-Nachricht"
    git commit -m "Commit message"
    ```

### Branches verwalten / Managing Branches
1. Neuen Branch erstellen / Creating a new branch:
    ```sh
    git branch <branch-name>
    ```

2. Zu einem Branch wechseln / Switching to a branch:
    ```sh
    git checkout <branch-name>
    ```

3. Branch erstellen und wechseln / Creating and switching to a branch:
    ```sh
    git checkout -b <branch-name>
    ```

4. Zu einem Branch wechseln (alternativ zu `checkout`) / Switching to a branch (alternative to `checkout`):
    ```sh
    git switch <branch-name>
    ```

### Änderungen zusammenführen / Merging Changes
1. Änderungen von einem Branch in den aktuellen Branch mergen / Merging changes from one branch to the current branch:
    ```sh
    git merge <branch-name>
    ```

### Remote-Repositories verwalten / Managing Remote Repositories
1. Remote-Repository hinzufügen / Adding a remote repository:
    ```sh
    git remote add origin <repository-url>
    ```

2. Änderungen pushen / Pushing changes:
    ```sh
    git push origin <branch-name>
    ```

3. Änderungen pullen / Pulling changes:
    ```sh
    git pull origin <branch-name>
    ```

4. Einen lokalen Branch zu einem Remote-Branch machen / Making a local branch a remote branch:
    ```sh
    git push -u origin <branch-name>
    ```

## Nützliche Befehle / Useful Commands
### Status anzeigen / Displaying status
```sh
git status
```
Zeigt den aktuellen Status des Repositories an.
Shows the current status of the repository.

### Verlauf anzeigen / Viewing the log
```sh
git log
```
Zeigt die Commit-Historie an.
Displays the commit history.

### Unterschied zwischen Dateien anzeigen / Showing the difference between files
```sh
git diff
```
Zeigt die Unterschiede zwischen dem Arbeitsverzeichnis und dem Staging-Bereich an.
Shows the differences between the working directory and the staging area.

### Änderungen rückgängig machen / Undoing changes
1. Staging-Bereich leeren / Unstaging files:
    ```sh
    git reset HEAD <datei>
    git reset HEAD <file>
    ```

2. Letzten Commit zurücksetzen / Resetting the last commit:
    ```sh
    git reset --soft HEAD~1
    ```

### Tags erstellen / Creating Tags
Tags werden verwendet, um bestimmte Punkte in der Git-Historie zu markieren, z.B. Versionsveröffentlichungen.
Tags are used to mark specific points in the Git history, such as version releases.

1. Tag erstellen / Creating a tag:
    ```sh
    git tag -a v1.0 -m "Version 1.0"
    ```

2. Tag pushen / Pushing a tag:
    ```sh
    git push origin v1.0
    ```

### Remote Branches verwalten / Managing Remote Branches
1. Liste aller Remote-Branches anzeigen / Listing all remote branches:
    ```sh
    git branch -r
    ```

2. Remote-Branch löschen / Deleting a remote branch:
    ```sh
    git push origin --delete <branch-name>
    ```

### Rebase
Rebase wird verwendet, um Änderungen von einem Branch an der Spitze eines anderen Branches anzuwenden.
Rebase is used to apply changes from one branch on top of another branch.

```sh
git rebase <branch-name>
```

### Stash
Stash wird verwendet, um vorübergehend nicht committe Änderungen zu speichern und den Arbeitsbereich zu bereinigen.
Stash is used to temporarily save uncommitted changes and clean the working directory.

1. Änderungen stashen / Stashing changes:
    ```sh
    git stash
    ```

2. Gespeicherte Änderungen anwenden / Applying stashed changes:
    ```sh
    git stash apply
    ```

## Beispiel für das Mergen von Branches / Example of Merging Branches

Angenommen, du arbeitest an einem Feature in einem Branch namens `dev` und möchtest die neuesten Änderungen aus dem `main`-Branch in deinen `dev`-Branch übernehmen. Hier ist, wie du das machst:

Let's assume you are working on a feature in a branch called `dev` and you want to incorporate the latest changes from the `main` branch into your `dev` branch. Here’s how you do it:

1. Wechsel zum `main`-Branch / Switch to the `main` branch:
    ```sh
    git checkout main
    ```

2. Hole die neuesten Änderungen aus dem Remote-Repository / Pull the latest changes from the remote repository:
    ```sh
    git pull origin main
    ```

3. Wechsel zurück zu deinem `dev`-Branch / Switch back to your `dev` branch:
    ```sh
    git checkout dev
    ```

4. Merg die Änderungen vom `main`-Branch in deinen `dev`-Branch / Merge the changes from the `main` branch into your `dev` branch:
    ```sh
    git merge main
    ```

Falls es Merge-Konflikte gibt, wirst du diese manuell lösen müssen. Nachdem die Konflikte gelöst sind, markierst du sie als gelöst und commitest die Änderungen.

If there are merge conflicts,

 you will need to resolve them manually. After resolving the conflicts, mark them as resolved and commit the changes.

```sh
git add <datei-mit-konflikt>
git commit -m "Konflikte gelöst zwischen dev und main"
git commit -m "Resolved conflicts between dev and main"
```

## Fazit / Conclusion
Git ist ein mächtiges Werkzeug, das die Zusammenarbeit und das Versionsmanagement in Softwareprojekten erheblich erleichtert. Diese grundlegende Dokumentation bietet einen Einstieg in die wichtigsten Konzepte und Befehle. Für eine tiefere Einarbeitung empfiehlt es sich, die [offizielle Git-Dokumentation](https://git-scm.com/doc) zu konsultieren.

Git is a powerful tool that significantly facilitates collaboration and version management in software projects. This basic documentation provides an introduction to the key concepts and commands. For deeper understanding, it is recommended to consult the [official Git documentation](https://git-scm.com/doc).

</br>
</br>

------------
------------
# Änderungen von `main` in den `dev` Branch mergen, während man sich im `dev` Branch befindet / Merging changes from `main` into the `dev` branch while staying in the `dev` branch

## Anleitung / Instructions

### Schritt-für-Schritt-Anleitung / Step-by-step Instructions

1. Stelle sicher, dass du dich im `dev` Branch befindest:
   Ensure that you are in the `dev` branch:
   ```sh
   git branch
   ```

   Der aktuelle Branch wird mit einem Sternchen (*) markiert. Falls `dev` nicht der aktuelle Branch ist, wechsle zu `dev`:
   The current branch is marked with an asterisk (*). If `dev` is not the current branch, switch to `dev`:
   ```sh
   git switch dev
   ```

2. Hole die neuesten Änderungen aus dem `main` Branch, ohne den `dev` Branch zu verlassen:
   Fetch the latest changes from the `main` branch without leaving the `dev` branch:
   ```sh
   git fetch origin main
   ```

3. Merg die Änderungen vom `main` Branch in den `dev` Branch:
   Merge the changes from the `main` branch into the `dev` branch:
   ```sh
   git merge origin/main
   ```

Falls es Merge-Konflikte gibt, wirst du diese manuell lösen müssen. Nachdem die Konflikte gelöst sind, markierst du sie als gelöst und commitest die Änderungen.

If there are merge conflicts, you will need to resolve them manually. After resolving the conflicts, mark them as resolved and commit the changes.

```sh
git add <datei-mit-konflikt>
git commit -m "Konflikte gelöst zwischen dev und main"
git commit -m "Resolved conflicts between dev and main"
```

</br>
</br>

------------
------------
# Anleitung zum Ändern einer Commit-Mitteilung

Es kann vorkommen, dass eine Commit-Nachricht unklare, falsche oder vertrauliche Informationen enthält. In solchen Fällen kannst du die Nachricht lokal ändern und den Commit mit einer neuen Nachricht zu GitHub pushen. Hier ist eine detaillierte Anleitung für verschiedene Szenarien.

## Die letzte Commit-Mitteilung ändern

### Schritt-für-Schritt-Anleitung

1. **Navigiere in der Befehlszeile zu dem Repository, das den Commit enthält, den du ändern möchtest:**
   ```sh
   cd /pfad/zu/deinem/repository
   ```

2. **Ändere die Commit-Nachricht mit dem Befehl `git commit --amend`:**
   ```sh
   git commit --amend
   ```
   Dies öffnet den Standard-Texteditor, in dem du die Commit-Mitteilung bearbeiten kannst.

3. **Bearbeite die Commit-Nachricht, speichere die Datei und schließe den Editor.**

4. **Falls der Commit noch nicht online veröffentlicht wurde, kannst du einfach die Änderungen pushen:**
   ```sh
   git push origin branch-name
   ```

5. **Falls der Commit bereits veröffentlicht wurde, musst du den Push erzwingen:**
   ```sh
   git push --force-with-lease origin branch-name
   ```

### Beispiel:
```sh
cd /pfad/zu/deinem/repository
git commit --amend
# Bearbeite die Commit-Nachricht im Editor
# Speichere und schließe den Editor
git push --force-with-lease origin branch-name
```

## Ältere oder mehrere Commit-Mitteilungen ändern

### Schritt-für-Schritt-Anleitung

1. **Navigiere in der Befehlszeile zu dem Repository, das den Commit enthält, den du ändern möchtest:**
   ```sh
   cd /pfad/zu/deinem/repository
   ```

2. **Verwende den Befehl `git rebase -i HEAD~n`, um eine Liste der letzten n Commits anzuzeigen:**
   ```sh
   git rebase -i HEAD~3
   ```
   Dies zeigt die letzten 3 Commits im Standard-Texteditor an.

3. **Ersetze vor jeder Commit-Nachricht, die du ändern möchtest, `pick` durch `reword`:**
   ```
   pick e499d89 Delete CNAME
   reword 0c39034 Better README
   reword f7fde4a Change the commit message but push the same commit.
   ```

4. **Speichere die Datei und schließe den Editor.**

5. **Bearbeite in den resultierenden Commit-Dateien die Commit-Mitteilungen, speichere die Dateien und schließe den Editor.**

6. **Erzwinge den Push der Änderungen zu GitHub:**
   ```sh
   git push --force origin branch-name
   ```

### Beispiel:
```sh
cd /pfad/zu/deinem/repository
git rebase -i HEAD~3
# Ersetze `pick` durch `reword` bei den zu ändernden Commits
# Speichere und schließe den Editor
# Bearbeite die Commit-Nachrichten in den resultierenden Dateien
git push --force origin branch-name
```

## Hinweise

- **Erzwungener Push:** Beim Erzwingen eines Pushs (`--force` oder `--force-with-lease`) wird der Verlauf des Repositorys geändert, was dazu führen kann, dass andere Entwickler, die das Repository bereits geklont haben, ihre lokalen Kopien manuell korrigieren müssen.
- **Interaktives Rebase:** Ein interaktives Rebase ermöglicht das Ändern der Commit-Nachrichten mehrerer Commits. Weitere Informationen dazu findest du im Git-Handbuch unter [Interaktiver Modus](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History).

Diese Anleitung hilft dir, Commit-Nachrichten sowohl für den letzten als auch für ältere Commits zu ändern und diese Änderungen korrekt zu GitHub zu pushen.

</br>
</br>

------------
------------

# Anleitung: Wie man den Git-Commit-Editor schließt

Wenn du den Befehl `git commit` ausführst, öffnet sich ein Editor, in dem du die Commit-Nachricht eingeben kannst. Um diesen Editor zu schließen und den Commit abzuschließen, folge den untenstehenden Schritten. Diese Anleitung umfasst gängige Editoren wie Vim und Nano, die häufig als Standard-Editoren für Git konfiguriert sind.

## Schließen des Git-Commit-Editors in verschiedenen Editoren

### Vim
Vim ist ein weit verbreiteter Texteditor in Unix-ähnlichen Systemen. Hier ist, wie du ihn schließen kannst:

1. **Bearbeiten der Commit-Nachricht beenden**:
   - Drücke `Esc`, um den Bearbeitungsmodus zu verlassen.

2. **Datei speichern und Editor schließen**:
   - Gib `:wq` ein und drücke `Enter`.
     - `:w` speichert die Datei.
     - `:q` schließt den Editor.

### Nano
Nano ist ein einfach zu bedienender Editor, der ebenfalls häufig verwendet wird.

1. **Bearbeiten der Commit-Nachricht beenden und Datei speichern**:
   - Drücke `Ctrl + O` (das O steht für "Write Out", also speichern).
   - Drücke `Enter`, um den Dateinamen zu bestätigen.

2. **Editor schließen**:
   - Drücke `Ctrl + X`.

### Emacs
Emacs ist ein weiterer weit verbreiteter Editor, besonders in der Unix- und Linux-Welt.

1. **Bearbeiten der Commit-Nachricht beenden und Datei speichern**:
   - Drücke `Ctrl + X` gefolgt von `Ctrl + S` (speichern).

2. **Editor schließen**:
   - Drücke `Ctrl + X` gefolgt von `Ctrl + C`.

## Vermeiden des Editors mit `-m` Option
Wenn du den Editor komplett vermeiden möchtest, kannst du die Commit-Nachricht direkt im Commit-Befehl angeben:

```sh
git commit -m "Meine Commit-Nachricht"
```

### Beispiel:
```sh
git add .
git commit -m "Füge neue Funktionen hinzu"
```

## Zusammenfassung

- **Vim**: `Esc` → `:wq` → `Enter`
- **Nano**: `Ctrl + O` → `Enter` → `Ctrl + X`
- **Emacs**: `Ctrl + X` `Ctrl + S` → `Ctrl + X` `Ctrl + C`
- **Vermeiden des Editors**: `git commit -m "Meine Commit-Nachricht"`

Mit diesen Anweisungen solltest du in der Lage sein, den Git-Commit-Editor erfolgreich zu schließen und deine Commit-Nachricht zu speichern.