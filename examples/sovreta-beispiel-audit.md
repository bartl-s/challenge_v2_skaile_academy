# AI-Audit für Sovreta (Beispiel-Audit)

*Erstellt am 25.07.2026 · Basis: www.sovreta.com · Demo-Lauf von AuditPilot
gegen die Website des eigenen Erbauers — ehrlicher geht Dogfooding nicht.*

## Kurzeinschätzung

Die Positionierung sitzt: Revenue Operating System für Coaches und Berater,
klare 5-Phasen-Struktur, echte Cases, ein Gesicht dahinter. Aber die Seite
kennt nur einen Conversion-Weg, und der endet in einem Formular mit
„Antwort innerhalb von 48 Stunden". Für eine Marke, die Automatisierung
verkauft, bleibt hier sichtbar Automatisierung liegen.

## Die Lücken

### 1. Kein Terminbuchungs-Link auf der ganzen Seite

**Befund:** Alle CTAs führen zum Funnel-Check-Formular. Ein buchbarer
Kalender-Slot fehlt, obwohl ein TidyCal-Konto mit öffentlicher
Buchungsseite existiert.
**Was es kostet:** Wer bereit für ein Gespräch ist, muss ein Formular
ausfüllen und bis zu 48 Stunden warten. Ein Teil dieser heißen Besucher
springt in der Wartezeit ab.
**Empfehlung:** Zweiter CTA „Gespräch buchen" direkt neben dem Formular,
verlinkt auf den bestehenden TidyCal-Slot. Aufwand: eine Zeile HTML.

### 2. Kein Lead-Magnet, kein Newsletter

**Befund:** Außer dem Funnel-Check gibt es kein Angebot gegen
E-Mail-Adresse — kein Freebie, keine Newsletter-Anmeldung.
**Was es kostet:** Besucher, die noch nicht anfrage-bereit sind,
verschwinden ohne Spur. Genau die Zielgruppe, die später kauft.
**Empfehlung:** Ein bestehendes Asset (z. B. eine Funnel-Checkliste) als
Download gegen E-Mail, dahinter eine kurze automatische Mail-Strecke.

### 3. Der Ablauf-Text verkauft noch den alten manuellen Prozess

**Befund:** Schritt 1 der Zusammenarbeit verspricht „einen kurzen Loom" —
dabei liefert der Betreiber Audits inzwischen als persönliche Web-Seite
unter /audit/, automatisiert erstellt.
**Was es kostet:** Die Seite untertreibt das eigene Produkt. Der stärkste
Beweis („so eine Seite bekommst du") wird nicht gezeigt.
**Empfehlung:** Ablauf-Text aktualisieren und ein anonymisiertes
Beispiel-Audit als Live-Demo verlinken.

### 4. Nach dem Formular: Funkstille bis zur Handarbeit

**Befund:** Nach dem Absenden gibt es nur „Antwort innerhalb von 48
Stunden". Von außen ist keine automatische Bestätigungs- oder
Warmhalte-Mail erkennbar — ehrlich als offene Frage markiert.
**Empfehlung:** Automatische Antwort-Mail mit nächstem Schritt (z. B.
direkt der Buchungslink), damit die 48 Stunden keine tote Zeit sind.

## Quick Win

**Lücke 1: der Buchungs-Button.** Eine Zeile HTML, null Kosten, und der
heißeste Besucher-Typ bekommt sofort einen Weg zum Gespräch.

## Nächster Schritt

Dieses Audit ist der Demo-Durchlauf von AuditPilot. Für echte Leads endet
die Seite hier mit einem Buchungs-Button — siehe
`templates/audit-seite-vorlage.html`.
