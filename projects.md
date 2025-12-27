---
layout: default
title: Projekte
---

<nav style="background: #2a2a2a; padding: 1rem; border-radius: 8px; margin-bottom: 2rem;">
  <a href="index.html" style="margin-right: 1rem; color: #3498db;">🏠 Home</a>
  <a href="projects.html" style="color: #3498db;">💼 Projekte</a>
</nav>

# Projekte

Hier findest du eine Übersicht meiner Projekte und Arbeiten.

---

## BulMenu - Digitales Kantinensystem
**Status:** In Entwicklung | **Zeitraum:** Sept 2025 - Juni 2026

Ein vollständiges Vorbestellsystem für die Schulkantine mit QR-Code-Abholung und Wallet-System.

**Highlights:**
- JWT-basierte Authentifizierung
- QR-Code Generierung & Validierung
- Digitales Wallet-System
- Echtzeit-Dashboard für Kantinenpersonal
- SQL 

**Tech Stack:** FastAPI, Vue.js, PostgreSQL, Docker

[→ Zum Repository](https://github.com/BulMenu-Diplomarbeit/bulmenu)

---

## Git Cheat Sheet

Umfassende Dokumentation zu Git, Git Flow und SSH - entstanden während meiner Ausbildung an der Bulme.

### Git Basics

**Repository initialisieren:**
```bash
git init                   # Neues Repo erstellen
git clone <url>            # Repo klonen
```

**Grundlegende Befehle:**
```bash
git status                # Status anzeigen
git add <file>            # Datei stagen
git add .                 # Alle Dateien stagen
git commit -m "message"   # Commit erstellen
git push                  # Zu Remote pushen
git pull                  # Von Remote pullen
```

### Git Flow

**Branch-Struktur:**
```
main                (Production)
  └── develop       (Development)
       ├── feature/login
       ├── feature/dashboard
       └── bugfix/typo
```

**Feature entwickeln:**
```bash
git checkout -b feature/name develop  # Feature-Branch erstellen
# ... entwickeln ...
git add .
git commit -m "feat: add new feature"
git checkout develop
git merge feature/name --no-ff        # Merge mit Commit
```

**Hotfix erstellen:**
```bash
git checkout -b hotfix/bug main      # Von main branchen
# ... fixen ...
git commit -am "fix: critical bug"
git checkout main
git merge hotfix/bug --no-ff         # In main mergen
git checkout develop
git merge hotfix/bug --no-ff         # Auch in develop
```

### Branching & Merging
```bash
git branch                   # Branches anzeigen
git branch <name>            # Neuen Branch erstellen
git checkout <branch>        # Branch wechseln
git checkout -b <branch>     # Erstellen + wechseln
git merge <branch>           # Branch mergen
git branch -d <branch>       # Branch löschen
```

### Remote Operations
```bash
git remote -v                # Remotes anzeigen
git remote add origin <url>  # Remote hinzufügen
git push origin <branch>     # Branch pushen
git push -u origin <branch>  # Pushen + tracking setzen
git fetch                    # Infos vom Remote holen
git pull                     # Fetch + Merge
```

### Undo & Reset
```bash
git reset --soft HEAD~1      # Letzten Commit rückgängig (Änderungen bleiben)
git reset --hard HEAD~1      # Letzten Commit + Änderungen verwerfen
git revert <commit>          # Commit rückgängig (neuer Commit)
git restore <file>           # Datei wiederherstellen
```

### Stash (Zwischenspeichern)
```bash
git stash                    # Änderungen weglegen
git stash list               # Alle Stashes anzeigen
git stash apply              # Letzten Stash zurückholen
git stash pop                # Anwenden + löschen
git stash drop               # Stash löschen
```

### SSH-Key Setup für GitHub

**1. Key erstellen:**
```bash
ssh-keygen -t ed25519 -C "deine.email@example.com"
# Enter bei allen Prompts drücken
```

**2. SSH-Agent starten:**
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

**3. Public Key kopieren:**
```bash
cat ~/.ssh/id_ed25519.pub
# Kompletten Output kopieren
```

**4. Bei GitHub eintragen:**
- GitHub → Settings → SSH and GPG Keys → New SSH Key
- Key einfügen und speichern

**5. Testen:**
```bash
ssh -T git@github.com
# "Hi username!" = funktioniert!
```

### Nützliche Tricks
```bash
git log --oneline --graph    # Schöne History
git log --all --graph        # Alle Branches
git diff                     # Änderungen anzeigen
git blame <file>             # Wer hat was geändert
git clean -fd                # Untracked Dateien löschen
```

### Commit-Nachrichten Konventionen
```bash
feat:       neues Feature
fix:        Bugfix
docs:       Dokumentation
style:      Formatierung
refactor:   Code umstrukturieren
test:       Tests hinzufügen
chore:      Maintenance
```

---

## Weitere Projekte

Hier kommen später weitere Projekte hinzu, die ich während meiner Ausbildung oder privat entwickle.

---

[← Zurück zur Startseite](index.md)