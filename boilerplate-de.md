# Pressemitteilung — Bausteine (Deutsch)

> Alle folgenden Texte können wortgetreu übernommen, gekürzt oder umformuliert werden. Bei wörtlicher Übernahme bitte „Bjoern Kindler / mundwerkapp.de" als Quelle nennen.

## Headline-Optionen

- *Mundwerk: Lokale Diktiersoftware für macOS — komplett offline, ohne Abo*
- *Diktieren am Mac, ohne dass Audio den Rechner verlässt: Mundwerk veröffentlicht Version 1.0*
- *DSGVO-Diktat für Apple Silicon: Mundwerk bringt Whisper-Spracherkennung lokal auf macOS*

## Lead-Absatz (3–4 Sätze)

Mundwerk ist eine neue Diktiersoftware für macOS, die Sprache am Cursor in Text verwandelt — komplett lokal auf Apple Silicon, ohne Cloud-Verarbeitung. Die App nutzt OpenAI Whisper über die quelloffene C++-Implementierung whisper.cpp und ist auf nahtlosen Wechsel zwischen Deutsch und englischen Fachbegriffen optimiert. Mundwerk wird einmalig verkauft (14,99 €, Einführungspreis 8,99 € bis 19.06.2026), kein Abo, kein Account. Damit positioniert sich Mundwerk als datenschutzfreundliche Alternative zu Cloud-Diktatlösungen für Entwickler, Mediziner, Juristen und Wissenschaftler im DACH-Raum.

## Mittlerer Absatz (Tech / USP)

Im Unterschied zu Apple Diktat (Cloud-Anteil bei großen Modellen, „Erweiterte Diktat"-Funktionen) und kommerziellen Whisper-Frontends mit Cloud-Backend (z. B. SaaS-Angebote auf API-Basis) verarbeitet Mundwerk Audio ausschließlich auf dem Gerät. Die Whisper-Modelldatei (Standard `large-v3`, ca. 3 GB) liegt nach einmaligem Download lokal; die Transkription läuft via Metal GPU mit niedriger Latenz. Voice Activity Detection übernimmt Silero VAD v5 (ONNX). Eine Korrektur-Historie (lokal in SQLite gespeichert) und domänen-spezifische Vokabular-Hints verbessern die Erkennung von Fachjargon über die Zeit.

## Tech-Spec-Box (für Tabellen)

| Feld | Wert |
|------|------|
| Plattform | macOS 26.0+, Apple Silicon |
| Sprachmodell | OpenAI Whisper (large-v3 Standard, alternative Größen wählbar) |
| Backend | whisper.cpp mit Metal-GPU-Beschleunigung |
| VAD | Silero VAD v5 |
| Datenverarbeitung | 100 % lokal auf dem Gerät |
| UI | Menüleisten-App, Push-to-Talk via Fn-Taste oder Custom-Hotkey |
| Auto-Update | Sparkle (EdDSA-signiert) |
| Preis | 14,99 € einmalig (Einführungsangebot 8,99 € mit Code `LAUNCH` bis 19.06.2026) |
| Trial | 7 Tage kostenlos, voller Funktionsumfang |
| Hersteller | Bjoern Kindler, Unterhaching |
| Website | <https://mundwerkapp.de> |

## Schluss-Absatz (Hersteller-Boilerplate)

Mundwerk wurde von **Bjoern Kindler** entwickelt, freiberuflicher Software-Entwickler aus Unterhaching bei München. Schwerpunkt seiner Arbeit ist datenschutzfreundliche Software für die deutschsprachige Indie-Mac-Szene. Mundwerk steht in direkter Linie zu seiner Überzeugung, dass produktive KI-Werkzeuge nicht zwingend an Cloud-Backends gekoppelt sein müssen — Apple Silicon liefert genug Rechenleistung für anspruchsvolle Modelle direkt auf dem Mac. Kontakt: <info@kindler-dev.de>.

## Pressekontakt

**Bjoern Kindler** · <info@kindler-dev.de> · Tel. +49 89 66598360 · <https://mundwerkapp.de>
