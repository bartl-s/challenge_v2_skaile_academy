# AuditPilot — SKAILE Building Challenge

> Diese Datei füllst du im Laufe der Challenge aus. Die Platzhalter in eckigen
> Klammern ersetzt du durch deine Inhalte — dein Claude Code hilft dir dabei
> (siehe START.md).

## Das Problem

Mein LinkedIn-Outreach verspricht interessierten Leads ein persönliches
AI-Audit — bisher hieß das: pro Lead ein Loom-Video aufnehmen. Das kostet
mich jedes Mal 20–30 Minuten, die ich neben Festanstellung und Kundenprojekten
nicht habe, und wird so zum Flaschenhals meiner Akquise.

## Was der Agent macht

Ich gebe dem Agenten Name und Website (oder LinkedIn) eines Leads. Er
recherchiert die Firma, findet 3–5 konkrete Automatisierungs-Lücken und baut
daraus eine persönliche Audit-Web-Seite in meinem Marken-Look — inklusive
Handlungsempfehlungen und Link zum Erstgespräch. Am Ende bekomme ich einen
fertigen Link, den ich dem Lead einfach per DM schicke. Statt 30 Minuten
Video: ein Befehl, wenige Minuten, hochwertigeres Ergebnis.

## Stack

- [x] Claude Code (Agent / Skills)
- [ ] n8n
- [ ] Sonstiges: [was?]

**Vorarbeit (existierte schon vor der Challenge, wird ehrlich genannt):**
LinkedIn-Outreach mit AUDIT-Keyword läuft bereits (SendPilot), Marken-Design
(Sovreta) und ein HTML-Design-Skill existieren in meinem Workspace. Der
AuditPilot-Agent selbst (Recherche → Audit → Seite → Link) entsteht komplett
während der Challenge.

## Setup

Siehe **[INSTALL.md](INSTALL.md)** — sie ist an Claude adressiert. Repo
clonen, Claude Code darin öffnen und sagen: „Lies die INSTALL.md und richte
AuditPilot für mich ein." Claude führt dich durch alles (dauert ~5 Minuten,
kein API-Key nötig).

## Was während der Challenge entstanden ist

**Vorher schon da (ehrlich benannt):** LinkedIn-Outreach mit AUDIT-Keyword
(SendPilot), Sovreta-Markendesign, ein HTML-Design-Skill im Workspace.

**Neu in der Challenge gebaut:**
- Das `/audit`-Kommando: Firmenname + Website rein → belegbasiertes
  Markdown-Audit raus (Lücken mit Befund/Kosten/Empfehlung + Quick Win)
- Die Audit-Seiten-Vorlage im Marken-Look (`templates/`) inklusive
  Termin-Buchung und LinkedIn-CTA
- Der komplette Loop lief an Tag 1 schon einmal echt durch: realer Lead →
  Audit → persönliche Web-Seite, live deployt und per DM verschickt

## Learnings

1. **Scroll-Animationen brauchen ein Sicherheitsnetz.** Die
   Einblende-Effekte (IntersectionObserver) ließen Inhalte in manchen
   Browsern unsichtbar. Fix: Nach 2,5 Sekunden wird alles eingeblendet,
   egal was der Observer tut. Gefunden, weil der Agent seine eigene Seite
   per Screenshot geprüft hat.
2. **Öffentliches Repo und Kundendaten von Anfang an trennen.** Echte
   Audits enthalten Personendaten — der Ordner `audits/` ist deshalb
   gitignored, ins Repo kommt nur die anonymisierte Vorlage. Die
   Live-Seiten stehen auf `noindex`: nur wer den Link hat, sieht sie.
3. **Die Seite schlägt das Video.** Statt pro Lead ~30 Minuten Loom
   aufzunehmen, entsteht in wenigen Minuten eine persönliche Audit-Seite,
   die hochwertiger wirkt und einen buchbaren Termin gleich mitbringt.

---

**Demo-Video:** https://www.berrycast.com/conversations/f6182316-9edf-5183-bc22-223d84d70b00 — ein Durchlauf, ungeschnitten

*SKAILE Academy Building Challenge — Juli 2026*
