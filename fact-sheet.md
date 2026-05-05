# Fact Sheet — Mundwerk

## Produkt

| Feld | Wert |
|------|------|
| Name | Mundwerk |
| Kategorie | Diktiersoftware (Speech-to-Text) |
| Plattform | macOS 26.0+ |
| Architektur | Apple Silicon (M1, M2, M3, M4 oder neuer) — Intel nicht unterstützt |
| Sprache (UI) | Deutsch (English in Vorbereitung) |
| Erkennungssprachen | Deutsch primär, Englisch (gemischt im Code-Switching), weitere Whisper-Sprachen optional |
| Verarbeitung | 100 % lokal, keine Cloud, keine Telemetrie |

## Tech

| Komponente | Implementierung |
|------------|-----------------|
| Sprachmodell | OpenAI Whisper (large-v3, medium, small, base, tiny — wählbar) |
| Inference-Backend | whisper.cpp (C++, Metal-GPU-beschleunigt) |
| VAD | Silero VAD v5 (ONNX) + RMS-Fallback |
| App-Sprache | Swift 6 (strict concurrency) |
| UI-Framework | SwiftUI |
| Datenbank (lokal) | SQLite via GRDB |
| Hotkey-Detection | NSEvent.addGlobalMonitorForEvents (kein CGEventTap) |
| Text-Injection | CGEvent.post (mit Accessibility-Permission) |
| Auto-Update | Sparkle (EdDSA-signiert) |
| Code-Signierung | Apple Developer ID, hardened runtime, notarisiert + gestapelt |
| Build-Tooling | Xcode 16, xcodegen, fastlane |

## Distribution & Preise

| Feld | Wert |
|------|------|
| Distribution | Direct Download (DMG), nicht im Mac App Store |
| Trial | 7 Tage kostenlos, voller Funktionsumfang, keine Kreditkarte |
| Preis (regulär) | 14,99 € einmalig |
| Einführungspreis | 8,99 € mit Code `LAUNCH` bis 19.06.2026 |
| Lizenzmodell | Einmalkauf, dauerhafte Updates innerhalb der gekauften Hauptversion |
| Zahlungsabwicklung | Lemon Squeezy (Merchant of Record für USt-Abwicklung) |
| USt-Status Hersteller | Kleinunternehmer §19 UStG |

## Hersteller

| Feld | Wert |
|------|------|
| Name | Bjoern Kindler |
| Rechtsform | Freiberufler nach §18 EStG |
| Anschrift | Bischofshofener Str. 9, 82008 Unterhaching, Deutschland |
| Telefon | +49 89 66598360 |
| E-Mail | <info@kindler-dev.de> |
| Website | <https://mundwerkapp.de> |
| Veröffentlichung v1.0.0 | 2026-05-04 |

## Datenschutz-Highlights (für DSGVO-Reviews)

- Audio verlässt das Gerät niemals
- Keine Telemetrie, keine Crash-Analytics, keine Werbe-IDs
- Lizenzaktivierung via Lemon Squeezy einmalig (Email-Identifier), danach komplett offline
- Auto-Update prüft nur `appcast.xml` (Standard-HTTP-Logs auf Server, 7-Tage-Rotation)
- Quelltext-Audit auf Anfrage für seriöse Rezensenten möglich

## Vergleich mit anderen Lösungen (Stand 2026-05-05)

| Eigenschaft | Mundwerk | Apple Diktat | Cloud-Whisper-SaaS |
|-------------|----------|--------------|--------------------|
| 100 % offline | ✅ | ⚠️ Teilweise (Cloud bei großen Modellen) | ❌ |
| Einmalkauf | ✅ | n/a (im OS enthalten) | ❌ Abo |
| DE+EN Code-Switch | ✅ | ⚠️ Eingeschränkt | ✅ |
| Eigene Vokabular-Injection | ✅ | ❌ | Teilweise |
| Korrektur-Speicher | ✅ lokal | ❌ | meist Cloud |
| DSGVO-konform per Architektur | ✅ | ⚠️ Cloud-Anteil prüfen | ⚠️ AVV nötig |
| Apple Silicon optimiert | ✅ Metal-GPU | ✅ | meist Server-GPU |

## Verwendete Open-Source-Komponenten

- [whisper.cpp](https://github.com/ggerganov/whisper.cpp) — MIT
- [Silero VAD](https://github.com/snakers4/silero-vad) — MIT
- [GRDB.swift](https://github.com/groue/GRDB.swift) — MIT
- [Sparkle](https://github.com/sparkle-project/Sparkle) — MIT-Lizenzteil

---

**Stand:** 2026-05-05 · Aktuelle Version: 1.0.0
