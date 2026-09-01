<div align="center">
  <img src="logo.png" alt="Briefly Logo" width="160" />

  # Briefly

  **Deine Post, automatisch sortiert — komplett lokal auf deinem PC.**

  ![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-7C3AED)
  ![Local First](https://img.shields.io/badge/verarbeitung-100%25%20lokal-16a34a)
  ![Status](https://img.shields.io/badge/status-aktiv%20in%20Entwicklung-8B5CF6)
</div>

---

Briefly ist eine Desktop-Anwendung für Windows, die Fotos und Scans deiner
Briefe automatisch ausliest, sinnvoll umbenennt, in einer sauberen
Ordnerstruktur ablegt und dich rechtzeitig an Fristen erinnert — Rechnungen,
Bescheide, Kündigungsfristen, Widersprüche und mehr, ohne dass du selbst den
Überblick behalten musst.

## Warum Briefly?

- 📥 **Automatische Erkennung** — leg ein Foto/Scan in einen Ordner, Briefly
  erkennt Absender, Datum, Betreff, Kategorie und eventuelle Fristen
- ✅ **Nie blind übernommen** — jede Ablage läuft über einen
  Bestätigungs-Dialog, besonders bei Fristen wird nichts automatisch
  akzeptiert, wenn die Erkennung unsicher ist
- 🗂️ **Saubere Ablage** — automatische Ordnerstruktur nach Jahr/Absender,
  erkennt sogar ähnlich benannte Absender wieder, um Chaos zu vermeiden
- ⏰ **Fristen im Blick** — eigener Fristen-Bereich mit Farbcodierung
  (überfällig/bald fällig/später) und Kalender-Export (.ics)
- ✂️ **Manuelles Zuschneiden** — falls ein Foto mal schräg ist: Rechteck
  verschieben oder 4 Eckpunkte setzen (wie bei einer Handy-Scanner-App)
- 🔍 **Duplikat-Erkennung** — warnt, falls dasselbe Dokument versehentlich
  zweimal eingelesen wird

## Datenschutz zuerst

Briefly läuft standardmäßig **komplett lokal** über [Ollama](https://ollama.com)
mit einem lokalen Vision-Modell. Deine Dokumente verlassen dabei **nie**
deinen Rechner — keine Cloud, kein Upload, kein Tracking. Eine optionale
Cloud-Anbindung (für PDF-Verarbeitung) ist verfügbar, aber bewusst abgeschaltet,
bis du sie selbst aktivierst.

## Screenshots

<table>
  <tr>
    <td align="center"><b>Neue Dokumente</b><br/><img src="screenshots/neue-dokumente.png" width="380" /></td>
    <td align="center"><b>Fristen</b><br/><img src="screenshots/fristen.png" width="380" /></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><b>Archiv</b><br/><img src="screenshots/archiv.png" width="380" /></td>
  </tr>
</table>

## Voraussetzungen

- Windows 10/11
- Für gute Geschwindigkeit: eine NVIDIA-Grafikkarte mit mind. 8 GB VRAM
  (ohne GPU läuft es auf der CPU, aber deutlich langsamer)

## Installation

Fertige Version unter **[Releases](../../releases)** herunterladen, entpacken,
`Briefly.exe` starten — keine Installation nötig, kein Python-Setup, alles
in einer eigenständigen `.exe`. Briefly richtet sich beim ersten Start
selbst ein (inkl. automatischem Herunterladen des KI-Modells).

## Technischer Unterbau

Briefly ist in Python geschrieben und nutzt u. a.:

- [Ollama](https://ollama.com) — lokales Vision-Language-Modell
- [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) — Oberfläche
- [OpenCV](https://opencv.org) — Bildvorverarbeitung (Perspektivkorrektur,
  Belichtungsausgleich)
- [PyInstaller](https://pyinstaller.org) — Packaging als eigenständige `.exe`

Die genaue Paketliste steht in [`requirements.txt`](requirements.txt),
Beispiel-Konfiguration in [`.env.example`](.env.example).

## Lizenz

Copyright © 2026 DanteDi. Alle Rechte vorbehalten — siehe [LICENSE](LICENSE).
Der Quellcode dieses Projekts ist nicht Teil dieses Repositories.
