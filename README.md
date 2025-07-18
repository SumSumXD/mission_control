**WICHTIG:**
Dieses Repository ist urheberrechtlich geschützt. Jegliches Kopieren, Forken, Klonen oder die Nutzung des Codes ist ohne ausdrückliche schriftliche Erlaubnis untersagt.

# Mission Control (Web)

**Mission Control** ist eine Web-App zur Verwaltung von Mitarbeitern ("Mitarbeiter") mit Rollen, Urlaubsverwaltung, Bürozeiten und Supervisoren. Die App nutzt Firebase für Authentifizierung und Firestore als Datenbank.

## Features
- **Login für Admins** (nur Admins können Mitarbeiterdaten verwalten)
- **Mitarbeiterliste** mit Such- und Auswahlfunktion
- **Bearbeiten von Mitarbeiterdaten**: Name, E-Mail, Telefon, Bürozeiten, Urlaubszeiten, Supervisoren
- **Urlaubsverwaltung**: Checkbox mit Datumsfeldern "Urlaub von" und "Urlaub bis"
- **Bürozeiten**: Für jeden Wochentag einzeln einstellbar
- **Supervisoren**: Dynamisch hinzufügbar/entfernbar (nur für Supervisor-Rolle)
- **Modernes, responsives UI**
- **Status-Overlay** für Lade- und Fehlermeldungen

## Technologie
- **Frontend**: HTML, CSS, Vanilla JavaScript (ES6+)
- **Backend**: [Firebase](https://firebase.google.com/) (Authentication, Firestore)
- **Hosting**: Empfohlen auf [GitHub Pages](https://pages.github.com/)

## Einrichtung & Deployment

### 1. Repository klonen
```bash
git clone https://github.com/DEIN-USERNAME/DEIN-REPO.git
cd DEIN-REPO
```

### 2. Firebase-Projekt anpassen (optional)
Die Firebase-Konfiguration findest du in der `index.html`. Für eigene Projekte ersetze die Werte durch deine eigenen aus der [Firebase Console](https://console.firebase.google.com/).

### 3. Deployment auf GitHub Pages
- Repository auf GitHub hochladen
- Unter **Settings → Pages** den Branch (z.B. `main`) und das Root-Verzeichnis (`/`) auswählen
- Nach wenigen Minuten ist die App unter `https://DEIN-USERNAME.github.io/DEIN-REPO/` erreichbar

## Sicherheitshinweise
- Die **Firebase-Konfiguration** (API Key etc.) ist **öffentlich** und dient nur zur Projekt-Identifikation, nicht als Geheimnis.
- **Echte Sicherheit** kommt durch die [Firestore Security Rules](https://firebase.google.com/docs/firestore/security/get-started) und die Authentifizierung.
- **Passwörter** werden nie im Code gespeichert.
- **Nur Admins** (laut Firestore-Datenbank) können Mitarbeiterdaten bearbeiten.

## Anpassungen
- Für eigene Rollen, Felder oder Logik kann die `index.html` direkt angepasst werden.
- Die App ist komplett clientseitig und benötigt keinen eigenen Server.

## Lizenz
MIT License 