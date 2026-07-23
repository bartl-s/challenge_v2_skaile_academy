# /audit — AuditPilot

Erzeuge ein persönliches AI-Audit für einen Lead.

**Input:** `$ARGUMENTS` = Firmenname + Website-URL (optional: LinkedIn-Profil, Notizen aus der DM).

## Schritte

1. **Website lesen:** Startseite plus die relevanten Unterseiten (Angebot/Kurse, Preise, Kontakt, Über uns). Nur was wirklich existiert — nichts erfinden.
2. **Geschäftsmodell erfassen:** In 2–3 Sätzen — was verkaufen sie, an wen, wie kommt heute Umsatz rein.
3. **3–5 Automatisierungs-Lücken finden:** Nur Befunde, die aus der Website belegbar sind. Typische Kandidaten: Terminbuchung per Mail statt Kalender-Tool, kein Lead-Magnet/keine E-Mail-Liste, händische Angebots-/Rechnungserstellung, Support nur per Mail, keine Follow-up-Sequenzen, Onboarding manuell. Keine generischen Floskeln — jede Lücke muss einen konkreten Beleg von der Website haben.
4. **Audit schreiben** nach `audits/<firmen-slug>.md` mit dieser Struktur:
   - `# AI-Audit für <Firma>` + Datum
   - **Kurzeinschätzung** (3 Sätze: wo steht die Firma, wo liegt das größte Potenzial)
   - **Die Lücken** — pro Lücke: *Befund* (was ist heute, mit Beleg), *Was es kostet* (grobe Zeit-/Geld-Schätzung pro Monat), *Empfehlung* (konkrete Automatisierung, mit Tool-Beispiel)
   - **Quick Win** — die eine Sache mit dem besten Aufwand-Nutzen-Verhältnis, umsetzbar in unter einer Woche
   - **Nächster Schritt** — CTA mit Erstgespräch-Link (Platzhalter `[CALL-LINK]`)
5. **Ton:** Deutsch, per Du (LinkedIn-Kontext), Klartext, konkret. Keine KI-Floskeln, keine Dreiergruppen-Rhetorik, kein Buzzword-Bingo. Es soll klingen wie eine ehrliche Einschätzung von einem Profi, nicht wie ein Verkaufsprospekt.

## Grenzen

- Nichts behaupten, was die Website nicht hergibt. Wenn unklar: als offene Frage ins Audit schreiben („Wie macht ihr heute X?").
- Es wird NICHTS versendet — Output ist nur die Markdown-Datei.
