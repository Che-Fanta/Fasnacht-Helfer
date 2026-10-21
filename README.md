# Fasnacht Ebnat-Kappel – Helfer-Tool

Helfer tragen sich ohne Login für Einsätze ein, das OK sieht alles und teilt ein.
Live über GitHub Pages; Daten in Firebase Firestore. Alles in `index.html`.

- Helfer: Startseite → "Ich will helfen"
- OK: Startseite → "OK-Login" (oder Link mit `#ok`)

## Einrichtung Firebase (einmalig)
1. console.firebase.google.com → Projekt hinzufügen (z.B. `fasnacht-ek`), Analytics aus.
2. Build → Firestore Database → Datenbank erstellen (Standort `eur3`/Zürich, Produktionsmodus).
3. Firestore → Regeln: Inhalt von `firestore.rules` einfügen → Veröffentlichen.
4. Sicherheit → Authentication → Jetzt starten → Anmeldemethode → **E-Mail/Passwort** aktivieren.
   Zusätzlich Anbieter **Anonym** aktivieren (Geräte-Login der Helfer für "Meine Einsätze" / Abmelden).
   Unter "Users" für jedes OK-Mitglied einen Benutzer anlegen.
5. Projekteinstellungen → Web-App hinzufügen → `firebaseConfig` in `index.html` einsetzen.
6. Authentication → Settings → Autorisierte Domains: `che-fanta.github.io` hinzufügen.
7. Als OK einloggen → Tab "Einsätze verwalten" → Vorlage importieren, Bedarf pro Einsatz prüfen.

## Neues Jahr
In `index.html` `JAHR`, `TAGE` und `VORLAGE` anpassen. Daten früherer Jahre bleiben in eigenen Sammlungen.
