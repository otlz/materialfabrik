<p align="center">
  <img src="https://beta.materialfabrik.de/materialfabrik-icon.svg" alt="materialfabrik Logo" width="80">
</p>

<h1 align="center">materialfabrik</h1>

<p align="center">
  <em>Das KI-Werkzeug für Unterrichtsmaterial</em>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white" alt="Prisma">
  <img src="https://img.shields.io/badge/Typst-239DAD?style=flat-square&logo=typst&logoColor=white" alt="Typst">
  <img src="https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI">
  <img src="https://img.shields.io/badge/Google_Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white" alt="Google Gemini">
  <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis">
</p>

<p align="center">
  <a href="https://beta.materialfabrik.de">🔗 Live-Demo</a>
</p>

---

## Über das Projekt

**materialfabrik** ist eine Webanwendung für Lehrkräfte, mit der Arbeitsblätter, Tests, Klausuren, Quizze, Audiokonversationen und Karteikarten erstellt werden können — unterstützt durch KI-Generierung und Live-Vorschau direkt im Browser.

Die Plattform richtet sich an alle Schulformen (Gymnasium, Realschule, Berufsschule, Gesamtschule u.a.) und wird aktiv im Unterricht eingesetzt.

> **Hinweis:** Dieses Repository dient als Projektvorstellung. Der Quellcode ist nicht öffentlich verfügbar.

---

## Features

### 📄 Dokumente

Drag-and-Drop-Editor mit Live-PDF-Vorschau. Die PDF-Erzeugung läuft vollständig im Browser über den Typst-WASM-Compiler — kein Server nötig.

**Blocktypen:** Überschriften, Absätze, Aufgaben mit Punkten und Musterlösung, Alertboxen, Antwortzeilen, Antwortboxen, Lückentext, Karopapier, Bilder mit Beschriftung, Spalten-Layout, Seitenumbruch

**Export & Teilen:** PDF-Download, öffentliche Ansicht über Short-Link (`/v/{id}`), PDF-Direktlink (`/api/v/{id}/pdf`), QR-Code zum Verteilen im Unterricht

<p align="center">
  <img src="screenshots/document.png" alt="Dokument-Editor" width="800">
</p>

### ❓ Quizze

Interaktive Quizze mit 11 Fragetypen und automatischer Bewertung.

**Fragetypen:** Single-Choice, Multiple-Choice, Sortierung, Kategorisierung, Kurzantwort, Langtext, Drag-and-Drop, Wörter ziehen (Text), Wörter ziehen (Bild), Lückentext, Text auf Bild

**Prüfungsmodus:** Beaufsichtigte Klausuren mit Zugangscode, Anti-Cheat (Tab-Erkennung, Vollbild-Pflicht, Rechtsklick-Sperre), Echtzeit-Monitoring, verschlüsselte Schülerdaten (AES-256), Wiederherstellungscodes und automatische Bewertung mit Notenskalen

**Teilen:** Öffentlicher Quiz-Link (`/q/{id}`) mit gemischten Antwortoptionen

<p align="center">
  <img src="screenshots/quizzes.png" alt="Quiz-Editor" width="800">
</p>

### 🎧 Audio

Audiokonversationen mit mehreren Stimmen über Text-to-Speech — ideal für Hörverstehensübungen und Dialoge.

**Stimmen:** 2–4 Stimmen mit eigenen Namen und Farben, 13 Sprachen über Chatterbox API

**Export:** WAV-Audio, Transkript (Text/HTML), SRT-Untertitel, JSON

**Teilen:** Öffentliche Wiedergabe mit synchronisiertem Transkript (`/a/{id}`)

<p align="center">
  <img src="screenshots/audio.png" alt="Audio-Editor" width="800">
</p>

### 🃏 Karteikarten

Lernsets mit Text- und Bildkarten für Vokabeln, Prüfungsvorbereitung und Wiederholung.

**Funktionen:** Kategorien, Hinweise, Tastatursteuerung (Pfeiltasten, Leertaste zum Umdrehen), KI-Generierung ganzer Kartensets

<p align="center">
  <img src="screenshots/flashcards.png" alt="Karteikarten-Editor" width="800">
</p>

---

## Übergreifende Funktionen

- **KI-Generierung** — Dokumente, Quizze, Audiokonversationen und Karteikarten können per KI erstellt werden (OpenAI, Gemini, Perplexity). Zweistufig: erst Planung, dann parallele Generierung aller Blöcke.
- **Echtzeit-Kollaboration** — Mehrere Lehrkräfte bearbeiten gleichzeitig über Redis Pub/Sub und Server-Sent Events mit automatischem Polling-Fallback.
- **QR-Codes & Short-Links** — Jedes Dokument, Quiz und Audio bekommt einen 8-Zeichen Short-Link zum direkten Teilen im Unterricht.
- **Schulverwaltung** — Schulen mit Rollen (Admin/Lehrkraft), gemeinsame Bibliothek, Microsoft-OAuth-Login.
- **DSGVO-konform** — Cookieless Analytics (PostHog), verschlüsselte Prüfungsdaten, kein Tracking ohne Einwilligung.

---

## Autor

**Navin Dass** — Studienrat für Mathematik, Informatik, Wirtschaft und Verwaltung an der Karl Kübel Schule, Bensheim.

- Website: [trivial.xyz](https://trivial.xyz)
- GitHub: [@otlz](https://github.com/otlz)

---

<p align="center">
  <sub>Dieses Repository enthält keinen Quellcode. Alle Rechte vorbehalten. © 2025 Navin Dass</sub>
</p>
