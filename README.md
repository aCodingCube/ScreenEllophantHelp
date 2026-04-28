# Tauri Präsentations-App Dokumentation

Dieses Projekt ist eine Tauri-basierte Anwendung zur Steuerung und Verwaltung von Medieninhalten (Videos, Bilder, Farben) für Präsentationen. Die Benutzeroberfläche ist in drei Hauptbereiche unterteilt: **Hauptsteuerung**, **Szenen-Modus** und **Asset-Management**.

## Benutzeroberfläche & Funktionen

### 1. Haupt-Navigationsleiste (Top-Box Left)
Diese Knöpfe steuern die grundlegende Navigation und den Modus der Anwendung.

| Button-ID | Icon | Beschreibung |
|:---|:---:|:---|
| `closeBtn` | ✖ | **Schließen:** Beendet die Anwendung. |
| `assetToggle` | ◫ | **Asset-Panel:** Öffnet oder schließt die Seitenleiste für die Medienauswahl. |
| `editToggle` | ✎ | **Edit-Modus:** Schaltet zwischen dem **PRÄSENTIEREN**-Modus (Sicherheitsmodus) und dem **BEARBEITEN**-Modus (Löschen/Umbenennen) um. |

---

### 2. Präsentations-Einstellungen (Display-Menu)
Diese Knöpfe sind aktiv, wenn der Modus auf **PRÄSENTIEREN** steht.

| Button-ID | Icon | Beschreibung |
|:---|:---:|:---|
| `launchBtn` | 🖥️↗ | **Präsentation Starten:** Öffnet das externe Projektionsfenster. |
| `endBtn` | 🖥️✖ | **Präsentation Beenden:** Schließt das externe Projektionsfenster. |
| `visibilityToggle`| 👁️‍🗨 | **Vorschau umschalten:** Blendet die Anzeige auf dem Projektionsfenster ein oder aus (Stummschaltung des Bildsignals). |
| `blackoutBtn` | ⏻ | **Blackout:** Schaltet die Ausgabe sofort auf Schwarz. |
| `transitionToggle`| ▤ | **Übergänge:** Wechselt den Übergangs-Modus zwischen **CUT** (harter Schnitt) und **FADE** (weiche Blende). |
| `loopBtn` | ↻ | **Loop:** Aktiviert oder deaktiviert die Endlosschleife für das aktuell gewählte Video. |

---

### 3. Editier-Werkzeuge (Edit-Menu)
Diese Knöpfe erscheinen, wenn der **BEARBEITEN**-Modus aktiviert ist.

| Button-ID | Icon | Beschreibung |
|:---|:---:|:---|
| `deleteBtn` | 📄✖ | **Löschen:** Entfernt das ausgewählte Asset aus der Liste. |
| `templateDeleteBtn`| 🧹 | **Bereinigen:** Löscht ungenutzte Vorlagen oder leert den aktuellen Auswahlbereich. |
| `renameBtn` | ✎＿ | **Umbenennen:** Ermöglicht das Ändern des Anzeigenamens eines Assets. |
| `templateBtn` | ➕ | **Hinzufügen:** Erstellt einen neuen Slot oder eine neue Vorlage. |

---

### 4. Asset- & Ordnersteuerung (Bottom-Area Left)
Diese Steuerelemente befinden sich über der linken Asset-Liste.

| Button-ID | Icon | Beschreibung |
|:---|:---:|:---|
| `projectFolderBtn`| 📁🔍 | **Ordner wählen:** Öffnet den System-Dialog, um einen Ordner mit Mediendateien zu importieren. |
| `loadBtn` | ↻ | **Neu laden:** Aktualisiert den Inhalt des gewählten Projektordners. |
| `colorBtn` | ➕ | **Farbe hinzufügen:** Erstellt ein neues Asset basierend auf der gewählten Farbe im Color-Picker. |
| `colorInput` | 🎨 | **Farbauswahl:** Ein natives Farbauswahl-Feld (Color Picker) zur Definition von Hintergrundfarben. |

## Bedienungshinweis
- **Links (`container-left`):** Hier werden die verfügbaren Assets (Videos/Bilder/Farben) angezeigt.
- **Rechts (`container-right`):** Dient zur Verwaltung der aktiven Playlist oder Szenenstruktur.
- Der aktuelle Modus wird jederzeit durch das Label neben dem Pencil-Icon (z.B. "PRÄSENTIEREN") angezeigt.
