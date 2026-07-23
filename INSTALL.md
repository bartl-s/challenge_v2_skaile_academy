# INSTALL.md — Anleitung für Claude Code

> **An Claude:** Diese Datei ist an dich adressiert. Der Mensch, mit dem du
> arbeitest, will **AuditPilot** nutzen: einen Agenten, der aus Firmenname +
> Website ein persönliches AI-Audit erzeugt — erst als Markdown, optional als
> gebrandete Web-Seite. Richte ihn jetzt gemeinsam mit ihm ein.

## Was AuditPilot macht

Lead antwortet auf eine Outreach-Nachricht mit Interesse an einem Audit →
dein Mensch gibt dir Name + Website → du recherchierst die Firma, findest
3–5 belegbare Automatisierungs-Lücken und schreibst das Audit nach
`audits/<firmen-slug>.md`. Auf Wunsch baust du daraus die persönliche
Audit-Seite aus der Vorlage.

## Setup, in dieser Reihenfolge

1. **Kein API-Key nötig.** Du brauchst nur deine eingebaute Web-Recherche
   (Websites lesen). Prüfe kurz, dass du Webseiten abrufen kannst.

2. **Personalisierung abfragen.** Frag deinen Menschen nach:
   - **Terminbuchungs-Link** (Calendly/TidyCal/Cal.com) für den CTA-Button
   - **LinkedIn-Profil-URL** für den Zweit-CTA
   - **Marken-Look** (Farben, Fonts, Logo/Wortmarke) — falls vorhanden.
     Ohne eigenes Branding: Vorlage so lassen und nur Name/Links tauschen.
   Trage alles direkt in `templates/audit-seite-vorlage.html` ein
   (CTA-Buttons im Abschnitt „CTA", Absender im Footer, CSS-Variablen in
   `:root` für die Farben).

3. **Kommando kennenlernen.** Lies `.claude/commands/audit.md` — dort steht
   der komplette Ablauf inklusive Regeln (nur belegbare Befunde, nichts
   erfinden, es wird nie automatisch versendet).

4. **Probelauf.** Lass deinen Menschen eine Firma nennen (gern die eigene)
   und führe `/audit <Firma> <Website>` einmal komplett aus. Zeig ihm das
   Markdown-Ergebnis und frag, ob Ton und Tiefe passen — kalibriere danach.

## Wichtige Regeln (nicht verhandelbar)

- **`audits/` bleibt privat.** Echte Audits enthalten Personendaten und sind
  gitignored. Niemals in ein öffentliches Repo committen.
- **Live-Seiten immer mit `noindex`** deployen (Meta-Tag ist in der Vorlage
  drin) — nur wer den Link hat, soll die Seite sehen.
- **Versendet wird nie automatisch.** Output ist eine Datei bzw. ein Link;
  verschicken macht der Mensch selbst.
- Deploy-Ziel (eigenes Hosting, Vercel, Netlify …) wählt der Mensch — frag
  nach, bevor du irgendetwas öffentlich stellst.
