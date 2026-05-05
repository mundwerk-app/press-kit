# Press Release Boilerplate (English)

> All texts below can be reproduced verbatim, shortened, or rephrased. If used verbatim, please credit „Bjoern Kindler / mundwerkapp.de" as the source.

## Headline Options

- *Mundwerk: Local dictation for macOS — fully offline, no subscription*
- *Dictate on Mac without your audio ever leaving the device: Mundwerk ships v1.0*
- *GDPR-friendly speech-to-text for Apple Silicon: Mundwerk brings Whisper to macOS, on-device*

## Lead Paragraph (3–4 sentences)

Mundwerk is a new dictation app for macOS that turns speech at your cursor into text — entirely on-device on Apple Silicon, without any cloud processing. The app uses OpenAI Whisper via the open-source C++ implementation whisper.cpp, optimised for seamless switching between German and English technical terms. Mundwerk is a one-time purchase (14.99 €, introductory 8.99 € until 2026-06-19), no subscription, no account. The app positions itself as a privacy-respecting alternative to cloud dictation for developers, medical professionals, lawyers, and researchers in the German-speaking market.

## Mid-Paragraph (Tech / USP)

Unlike Apple Dictation (cloud component for larger models, "Enhanced Dictation" features) and commercial Whisper frontends with cloud backends (such as SaaS products built on the OpenAI API), Mundwerk processes audio strictly on-device. The Whisper model file (default `large-v3`, ~3 GB) is downloaded once and stored locally; transcription runs via Metal GPU with low latency. Voice Activity Detection is handled by Silero VAD v5 (ONNX). A local correction history (SQLite) and domain-specific vocabulary hints improve recognition of jargon over time.

## Tech-Spec Box

| Field | Value |
|-------|-------|
| Platform | macOS 26.0+, Apple Silicon |
| Speech model | OpenAI Whisper (large-v3 default, smaller sizes selectable) |
| Backend | whisper.cpp with Metal GPU acceleration |
| VAD | Silero VAD v5 |
| Data processing | 100 % on-device |
| UI | Menu-bar app, push-to-talk via Fn key or custom hotkey |
| Auto-update | Sparkle (EdDSA-signed) |
| Price | 14.99 € one-time (introductory 8.99 € with code `LAUNCH` until 2026-06-19) |
| Trial | 7 days free, full feature set |
| Maker | Bjoern Kindler, Unterhaching, Germany |
| Website | <https://mundwerkapp.de> |

## Closing Paragraph (Maker boilerplate)

Mundwerk is developed by **Bjoern Kindler**, an independent software developer based in Unterhaching near Munich, Germany. His work focuses on privacy-respecting software for the German-speaking indie Mac scene. Mundwerk reflects his conviction that productive AI tools need not be coupled to cloud backends — Apple Silicon provides enough compute for demanding models directly on the Mac. Contact: <info@kindler-dev.de>.

## Press Contact

**Bjoern Kindler** · <info@kindler-dev.de> · Phone +49 89 66598360 · <https://mundwerkapp.de>
