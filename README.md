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

Drag-and-Drop-Editor mit über 10 Blocktypen (Überschriften, Aufgaben, Alertboxen, Antwortzeilen, Bilder u.v.m.) und Live-PDF-Vorschau. Die PDF-Erzeugung läuft vollständig im Browser über den Typst-WASM-Compiler.

<p align="center">
  <img src="screenshots/document.png" alt="Dokument-Editor" width="800">
</p>

### ❓ Quizze

Interaktive Quizze mit 11 Fragetypen — von Single-/Multiple-Choice über Zuordnung und Sortierung bis hin zu Lückentexten und Drag-and-Drop. Mit automatischer Bewertung, Prüfungsmodus (beaufsichtigte Klausuren mit Anti-Cheat) und Echtzeit-Monitoring.

<p align="center">
  <img src="screenshots/quizzes.png" alt="Quiz-Editor" width="800">
</p>

### 🎧 Audio

Audiokonversationen mit mehreren Stimmen über Text-to-Speech (13 Sprachen). Erstellte Gespräche können als WAV, Transkript, HTML oder SRT-Untertitel exportiert werden — ideal für Hörverstehensübungen.

<p align="center">
  <img src="screenshots/audio.png" alt="Audio-Editor" width="800">
</p>

### 🃏 Karteikarten

Lernsets mit Text- und Bildkarten, Kategorien und Hinweisen. Interaktive Vorschau mit Tastatursteuerung und KI-gestützter Generierung ganzer Kartensets.

<p align="center">
  <img src="screenshots/flashcards.png" alt="Karteikarten-Editor" width="800">
</p>

---

## Technologie-Stack

| Kategorie | Technologie |
|-----------|-------------|
| Framework | Next.js 16, React 19, TypeScript |
| Styling | Tailwind CSS, shadcn/ui |
| Datenbank | PostgreSQL, Prisma, Redis |
| PDF-Engine | Typst WASM (clientseitig) |
| KI | Vercel AI SDK (OpenAI, Gemini, Perplexity) |
| Echtzeit | Redis Pub/Sub + Server-Sent Events |
| Testing | Vitest, Playwright |

---

## Architektur

```
Blöcke bearbeiten → Typst-Code generieren → WASM-Compiler → SVG/PDF → Live-Vorschau
```

Die gesamte PDF-Kompilierung findet clientseitig im Browser statt. Dokumente werden als strukturierte JSON-Blöcke gespeichert und über einen Converter in Typst-Quellcode umgewandelt — unter Nutzung des eigenen `typ-notes`-Pakets für erweiterte Typografie (Alertboxen, Badges, Baumdiagramme, Spielkarten u.v.m.).

Echtzeit-Kollaboration läuft über Redis Pub/Sub mit SSE-Streaming und automatischem Polling-Fallback.

---

## Autor

**Navin Dass** — Studienrat für Mathematik, Informatik, Wirtschaft und Verwaltung an der Karl Kübel Schule, Bensheim.

- Website: [trivial.xyz](https://trivial.xyz)
- GitHub: [@otlz](https://github.com/otlz)

---

<p align="center">
  <sub>Dieses Repository enthält keinen Quellcode. Alle Rechte vorbehalten. © 2025 Navin Dass</sub>
</p>
