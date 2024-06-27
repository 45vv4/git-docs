### Grundlegende Schreib- und Formatierungssyntax für GitHub Markdown

#### 1. Überschriften
```markdown
# Überschrift 1
## Überschrift 2
### Überschrift 3
#### Überschrift 4
##### Überschrift 5
###### Überschrift 6
```

#### 2. Textformatierung
```markdown
**Fett**
*Kursiv*
***Fett und Kursiv***
```

#### 3. Listen
- **Ungeordnete Listen**
```markdown
- Ein Punkt
* Ein anderer Punkt
+ Noch ein Punkt
```

- **Geordnete Listen**
```markdown
1. Erster Punkt
2. Zweiter Punkt
3. Dritter Punkt
```

#### 4. Links
```markdown
[GitHub](https://github.com)
```

#### 5. Bilder
```markdown
![Alternativtext](https://example.com/image.png)
```

#### 6. Zitate
```markdown
> Dies ist ein Zitat.
```

#### 7. Code
- **Inline-Code**
```markdown
`inline code`
```

- **Codeblöcke**
```markdown
```
Mehrzeiliger Codeblock
```
```

- **Syntaxhervorhebung**
```markdown
```python
def hello_world():
    print("Hello, world!")
```
```

#### 8. Tabellen
```markdown
| Spalte 1 | Spalte 2 |
|----------|----------|
| Inhalt 1 | Inhalt 2 |
| Inhalt 3 | Inhalt 4 |
```

#### 9. Horizontale Linien
```markdown
---
***
___
```

#### 10. Aufgabenlisten
```markdown
- [ ] Aufgabe 1
- [x] Aufgabe 2 (erledigt)
```

#### 11. Emojis
```markdown
:smile: :heart: :thumbsup:
```

#### 12. Fußnoten
```markdown
Dies ist ein Beispieltext mit einer Fußnote.[^1]

[^1]: Dies ist die Fußnote.
```

### Erweiterte Schreib- und Formatierungssyntax für GitHub Markdown

#### 1. Alerts (Hinweiskästen)
##### Hinweis (Note)
```html
<div style="padding: 10px; background-color: #e7f3fe; border-left: 5px solid #2196F3; color: black;">
  <strong>NOTE:</strong> Useful information that users should know, even when skimming content.
</div>
```

##### Tipp (Tip)
```html
<div style="padding: 10px; background-color: #e8f5e9; border-left: 5px solid #4CAF50; color: black;">
  <strong>TIP:</strong> Helpful advice for doing things better or more easily.
</div>
```

##### Wichtig (Important)
```html
<div style="padding: 10px; background-color: #fff3cd; border-left: 5px solid #ffeb3b; color: black;">
  <strong>IMPORTANT:</strong> Key information users need to know to achieve their goal.
</div>
```

##### Warnung (Warning)
```html
<div style="padding: 10px; background-color: #fff3cd; border-left: 5px solid #ffc107; color: black;">
  <strong>WARNING:</strong> Urgent info that needs immediate user attention to avoid problems.
</div>
```

##### Fehler (Danger)
```html
<div style="padding: 10px; background-color: #f8d7da; border-left: 5px solid #dc3545; color: black;">
  <strong>Danger!</strong> This is a danger alert.
</div>
```

##### Vorsicht (Caution)
```html
<div style="padding: 10px; background-color: #fff3e0; border-left: 5px solid #ff9800; color: black;">
  <strong>CAUTION:</strong> Advises about risks or negative outcomes of certain actions.
</div>
```

#### 2. Definition Lists
```html
<dl>
  <dt>Begriff</dt>
  <dd>Definition des Begriffs.</dd>
</dl>
```

#### 3. Task List mit Details
```markdown
- [ ] Aufgabe 1
  - Details zu Aufgabe 1
- [x] Aufgabe 2 (erledigt)
  - Details zu Aufgabe 2
```

#### 4. Collapse (Zusammenklappbare Abschnitte)
```html
<details>
  <summary>Mehr erfahren</summary>
  Hier sind die zusätzlichen Informationen, die zuerst versteckt sind.
</details>
```

#### 5. Mentions
```markdown
@username
```

#### 6. Referenzen und Verweise
```markdown
#123  // Referenz zu Issue oder Pull Request Nummer 123
commit 1a2b3c4d5e  // Referenz zu einem Commit
```

### Beispiel-Dokument
Hier ist ein Beispiel-Dokument, das alle grundlegenden und erweiterten Elemente kombiniert:
```markdown
# Beispiel-Dokument für GitHub Markdown

## Grundlegende Syntax

### Überschriften
# Überschrift 1
## Überschrift 2
### Überschrift 3

### Textformatierung
**Fett**
*Kursiv*
***Fett und Kursiv***

### Listen
- Ein Punkt
* Ein anderer Punkt
+ Noch ein Punkt

1. Erster Punkt
2. Zweiter Punkt
3. Dritter Punkt

### Links
[GitHub](https://github.com)

### Bilder
![Alternativtext](https://example.com/image.png)

### Zitate
> Dies ist ein Zitat.

### Code
`inline code`

```
Mehrzeiliger Codeblock
```

```python
def hello_world():
    print("Hello, world!")
```

### Tabellen
| Spalte 1 | Spalte 2 |
|----------|----------|
| Inhalt 1 | Inhalt 2 |
| Inhalt 3 | Inhalt 4 |

### Horizontale Linien
---
***
___

### Aufgabenlisten
- [ ] Aufgabe 1
- [x] Aufgabe 2 (erledigt)

### Emojis
:smile: :heart: :thumbsup:

### Fußnoten
Dies ist ein Beispieltext mit einer Fußnote.[^1]

[^1]: Dies ist die Fußnote.

## Erweiterte Syntax

### Alerts
#### Hinweis (Note)
<div style="padding: 10px; background-color: #BBDEFB; border-left: 5px solid #2196F3; color: black;">
  <strong>NOTE:</strong> Useful information that users should know, even when skimming content.
</div>

#### Tipp (Tip)
<div style="padding: 10px; background-color: #e8f5e9; border-left: 5px solid #4CAF50; color: black;">
  <strong>TIP:</strong> Helpful advice for doing things better or more easily.
</div>

#### Wichtig (Important)
<div style="padding: 10px; background-color: #e7d0f2; border-left: 5px solid #8253de; color: black;">
  <strong>IMPORTANT:</strong> Key information users need to know to achieve their goal.
</div>

#### Warnung (Warning)
<div style="padding: 10px; background-color: #ffe0cc; border-left: 5px solid #ff9800; color: black;">
  <strong>WARNING:</strong> Urgent info that needs immediate user attention to avoid problems.
</div>

#### Vorsicht (Caution)
<div style="padding: 10px; background-color: #f5aeb0; border-left: 5px solid #dc3545; color: black;">
  <strong>CAUTION:</strong> Advises about risks or negative outcomes of certain actions.
</div>

#### Fehler (Danger)
<div style="padding: 10px; background-color: #f5aeb0; border-left: 5px solid #dc3545; color: black;">
  <strong>Danger!</strong> This is a danger alert.
</div>



## Simple alerts
> [!NOTE]
> This is a note.

> [!TIP]
> This is a tip. (Supported since 14 Nov 2023)

> [!IMPORTANT]
> Crutial information comes here.

> [!CAUTION]
> Negative potential consequences of an action. (Supported since 14 Nov 2023)

> [!WARNING]
> Critical content comes here.


### Definition Lists
<dl>
  <dt>Begriff</dt>
  <dd>Definition des Begriffs.</dd>
</dl>

### Task List mit Details
- [ ] Aufgabe 1
  - Details zu Aufgabe 1
- [x] Aufgabe 2 (erledigt)
  - Details zu Aufgabe 2

### Collapse (Zusammenklappbare Abschnitte)
<details>
  <summary>Mehr erfahren</summary>
  Hier sind die zusätzlichen Informationen, die zuerst versteckt sind.
</details>

### Mentions
@username

### Referenzen und Verweise
#123
commit 1a2b3c4d5e
```

Dieses Dokument enthält alle grundlegenden und erweiterten Elemente, die Sie in GitHub Markdown verwenden können, um Ihre Dokumentation umfassend und ansprechend zu gestalten.