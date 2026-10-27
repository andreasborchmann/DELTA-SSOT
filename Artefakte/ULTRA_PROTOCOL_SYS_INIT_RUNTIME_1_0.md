# ULTRA INIT Protokoll — Runtime v1.0
## System | Protokoll — Chat-Start-Runtime | Layer-1-Anker | ULTRA v1.3 Konform

---

**Name:**                  ULTRA INIT Protokoll — Runtime
**Version:**               v1.0
**synced-to:**             INIT v1.0.6  (Inhalt verifiziert: DEV-Kommandos + parametrisches MENU reflektiert)
**Status:**                Production-Ready (Qwen-Verifikation offen)
**Typ:**                   Protokoll — Chat-Start-Runtime (Layer 1)
**ULTRA-Version:**         v1.3
**Domain:**                SYS
**Owner:**                 Co-Creator
**Erstellt:**              2026-06-11
**Aktualisiert:**          2026-06-19 (finalisiert)
**SSOT-Klasse:**           HOCH (Kommando-Spezifikationen + Pflicht-Output-Formate
                           normativ — wortidentisch in allen Sessions)
**Einsatzschwelle:**       Nicht anwendbar — universelles Chat-Start-Protokoll.
**Deprecation:**           Bei ULTRA v2.0 oder struktureller Chat-Interface-Änderung.
**Vollst. Spezifikation:** `ULTRA_PROTOCOL_SYS_INIT_1_0.md` (Layer 2)

> **[AMENDMENT A — SSOT]** Dieses Dokument ist die normative Quelle für operative
> Chat-Start-Inhalte. `ULTRA_PROTOCOL_SYS_INIT_1_0.md` verweist hierher — es
> dupliziert operative Inhalte nicht.

---

## STATE-ANCHORING
[PHASE: Px | ROLLE: X | LOAD: X/7]

---

## DOMÄNEN-DIREKTIVEN
1. **KEINE AUTOMATIK** — Kein Modus startet automatisch. Ausschließlich menschgetriggert.
2. **NUR BEKANNTES MELDEN** — KI meldet nur was tatsächlich sichtbar ist. Niemals
   Phantom-Profile oder nicht-sichtbare Checkpoints erfinden.
3. **ROLLE IMMER OFFEN BEI START** — Kein Modus setzt automatisch eine Rolle.

---

## ULTRA STATUS
**Trigger:** `ULTRA STATUS`
[PHASE: P0 | ROLLE: — | LOAD: 1/7]
ULTRA v[Version] | [Kontext: vollständig / approximativ]
Profile: [Liste aktiver Profile | nicht sichtbar]
Registry: [Version | nicht sichtbar]
Checkpoint: [Chat-ID aus letztem geladenem Checkpoint | keiner]
Bereit.

---

## ULTRA MENU
**Trigger:** `ULTRA MENU`
[PHASE: P0 | ROLLE: — | LOAD: 1/7]

══════════════════════════════════════
ULTRA v[Version] — NAVIGATION
══════════════════════════════════════
[1] P0 starten — Resonanz & Klärung
[2] PROJECT START — Thema, Profil, Tiefe angeben
[3] Profil aktivieren — Name nennen
[4] Checkpoint laden — JSON paste
[5] COMMIT — Closing-Sequenz ausführen (CLOSE + CCR + ITA opt. + PBP opt.)
[0] Direkt beginnen (freie Eingabe)
══════════════════════════════════════
Eingabe: Zahl oder freier Text

---

## ULTRA PROJECT START
**Trigger:** `ULTRA PROJECT START` (mit oder ohne Eingabe-Block)

**Eingabe-Block (optional, alle Felder optional):**
ULTRA PROJECT START
Thema: [1 Satz]
Profil: [Name | offen]
Tiefe: [QUICK | DEEP | offen]
Checkpoint: [Chat-ID oder JSON | nein]


**Output:**
[PHASE: P1 | ROLLE: ? | LOAD: 2/7]

Thema erkannt: [Thema aus Eingabe oder "bitte angeben"]
Profil-Empfehlung: [wenn erkennbar | offen]
Vorgeschlagene Sequenz: [P1 → Px nach Tiefe]
Erste Orientierungsfrage: [1 konkrete Frage]
Welche Rolle für P1?

**P0-Bypass:** Thema in 1 Satz klar? → PROJECT START. Noch unklar? →
P0 Resonanz empfehlen (Mensch entscheidet).

---

## ERGÄNZENDE KOMMANDOS

### ULTRA RESET
**Trigger:** `ULTRA RESET`
ULTRA RESET ausgeführt.
[PHASE: P0 | ROLLE: — | LOAD: 1/7]
Warte auf Rollenwahl oder nächste Eingabe.


Hinweis: RESET löscht keinen Inhalt. Checkpoint nach RESET neu laden.

### ULTRA COMMIT
**Trigger:** `ULTRA COMMIT` — 4-Schritt-Sequenz (CLOSE · CCR · ITA opt. · PBP opt.)
per `ULTRA_PROTOCOL_SYS_COMMIT_RUNTIME_1_0.md` §2.

### ULTRA DEV START / DEV STATE
**Trigger:** `ULTRA DEV START` / `ULTRA DEV STATE`
→ `ULTRA_PROTOCOL_SYS_EVOLUTION_1_3.md` §7 / §12 (Layer 2, bei Bedarf laden).

---

## FEHLSCHLAGS-SIGNALE

Signal 1: Kein [PHASE|ROLLE|LOAD]-Header → `ULTRA RESET`
Signal 2: KI proaktiv ohne Bestätigung   → `ULTRA RESET`
Signal 3: Phasenwechsel ohne Trigger     → `ULTRA RESET`

---

## ENTSCHEIDUNGSBAUM CHAT-EINSTIEG
Desorientiert / weiß nicht wo ich bin  → ULTRA MENU
Was gerade aktiv ist wissen            → ULTRA STATUS
Klares Thema                           → ULTRA PROJECT START
Vorherige Session mit Checkpoint       → Checkpoint laden [JSON]
ULTRA weiterentwickeln                 → ULTRA DEV START
Entwicklungs-Session abschließen       → ULTRA DEV STATE
Einfach loslegen                       → Direkt schreiben (P0 implizit)


---

## CHANGELOG

v1.0 (2026-06-11):
  Initiale Erstellung. Extrahiert aus ULTRA_PROTOCOL_SYS_INIT_1_0.md (Full, v1.0.6).
  Operative Inhalte nach Runtime-Muster: Strip-Analyse P2, Validation P3 (4 Ebenen).
  [AMENDMENT A] SSOT-Vermerk: dieses Dokument = normative Quelle für Chat-Start-Inhalte.
  Invarianten-Checks ([DELETE]) — DOMÄNEN-DIREKTIVEN übernehmen Guard-Funktion vollständig.
  FEHLSCHLAGS-SIGNALE: INIT-RUNTIME ist SSOT (HOCH); REGISTRY_RUNTIME spiegelt.
  Basis: ULTRA-SESSION-20260619-RUNTIMEVERBUND-HAERTUNG-S001.
  Owner: Co-Creator.

Finalisierung (2026-06-19, Runtimeverbund-Härtung):
  Platzhalter [DATUM] / [SESSION-ID] gefüllt. D3-Versionierungs-Regel angewandt:
  synced-to INIT v1.0.6 ergänzt (Inhalt verifiziert — DEV-Kommandos + parametrisches
  MENU aus v1.0.6 reflektiert). Eigene Runtime-Version v1.0 bleibt (entkoppelt).

---

*ULTRA INIT Protokoll — Runtime | v1.0 | synced-to INIT v1.0.6 | Chat-Start-Runtime |
Owner: Co-Creator | 2026-06-19*
