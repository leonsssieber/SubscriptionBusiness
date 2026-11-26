# Phase 2 bis 4: Cluster, Deep Dive, Red Team

**Von:** Jive (mit Claude) | **Datum:** 2026-11-26 | Die IDs (P01…) verweisen auf `01-pain-harvest.md`.

## Phase 2: Cluster-Map

Ein Thema zählt nur, wenn mindestens 3 unabhängige Quellen (verschiedene Autoren oder Seiten) denselben Pain zeigen.

| Cluster | Pain | Quellen | Anzahl unabh. Quellen | Zählt? |
|---|---|---|---|---|
| K1 | Handwerker-Software (Field Service) zu aufgebläht, zu teuer, falscher Workflow | P13–P23 | 11 (3 Subreddits + CH) | ✅ |
| K2 | Kleinvermieter: Buchhaltung, Belege, Koordination, Zahlungseingänge | P01–P12 | 12 (r/Landlord, BiggerPockets, CH) | ✅ |
| K3 | CH: QR-Rechnungen für wenige Rechnungen mühsam | P28, P29, P30, P56 | 4 | ✅ |
| K4 | CH: bexio passt nicht / Schweizer Spezialanforderungen | P23, P28, P31, P32 | 4 | ✅ |
| K5 | Shop ↔ Buchhaltung/Auszahlung abgleichen | P33–P38 | 6 | ✅ |
| K6 | Vereinsverwaltung: Mails, Finanzen, Preis, App | P49–P53, P29 | 6 (5 OMR-Autoren + Reddit) | ✅ |
| K7 | Compliance-/Ablauf-Fristen (Zertifikate, Dokumente) | P24–P27 | 4 | ✅ |
| K8 | Lehrpersonen/Tutoren: Planung, Abrechnung, Eltern nachjagen | P43–P48 | 6 (davon 3 UNVERIFIED) | ✅ (knapp) |
| K9 | Daten manuell zwischen Mail, Excel und Tools hin- und herkopieren | P20, P40, P41, P42 | 4 | ✅ (zu generisch) |
| – | Lead-Gen (P55), Stiftungsanträge (P54), Versand (P39) | je 1 | 1 | ❌ |
| – | CH-Stockwerkeigentum, Lehrbetriebe, Fahrlehrer, Kurtaxe | 0 | 0 | ❌ (keine Belege) |

## Phase 3: Deep Dive auf die Top 10 Ideen

Für die DACH-Varianten habe ich K1, K2 und K5 jeweils aufgeteilt, weil der Schweizer Markt anders aussieht als der US-Markt.

### I1: «Light»-Field-Service-Tool für US-Handwerker (K1)
- **Konkurrenz:** Jobber (USD 39–499/Mt., laut einem Vergleichspost in P-Quelle 1s8yd6p, UNVERIFIED), Housecall Pro (USD 49–329/Mt., gleiche Quelle, UNVERIFIED), ServiceTitan, Joist (Free-Tier), QuoteIQ (~USD 49/Mt., UNVERIFIED).
- **Top-Klagen:** Preis und Support (P13, P14), aufgebläht (P15, P17), erzwungener Workflow (P19).
- **Lücke:** «einfach + günstig» wird zwar ständig verlangt, aber Joist und ein Dutzend neue Indie-Tools (Servnox u. a., in den Archiv-Treffern gesehen) bedienen das bereits.

### I2: Handwerker-Software für Schweizer Kleinbetriebe 1–5 MA (K1 + P23)
- **Konkurrenz:** bexio, Programm.io (P23). Weitere Namen wie Smartrapport habe ich nicht geprüft (UNVERIFIED).
- **Top-Klage:** «keine Software hat alles» (P23). Das ist eine Forderung nach Breite, nicht nach Einfachheit.
- **Lücke:** unklar. Handwerker wollen Offerte + Rapport + Material + Rechnung + Lohn aus einem Guss.

### I3: US-Kleinvermieter-Tool (K2)
- **Konkurrenz:** TenantCloud, RentRedi (Forenpost: «flat $40 a month», UNVERIFIED), TurboTenant, Baselane, Buildium, Rentler.
- **Top-Klagen:** zu teuer (P01), Excel bricht (P02), Tools stören die Koordination (P03), Arbeit läuft ausserhalb des Tools (P04).
- **Lücke:** keine echte. Es ist der am stärksten umkämpfte Indie-Markt überhaupt.

### I4: Software für Schweizer Privatvermieter mit 2–15 Wohnungen (K2 + P11, P12)
- **Konkurrenz (CH):** LIMMOBI (Bankabgleich für Mietzinseingänge, für Selbstverwalter), Bewy, GARAIO REM, Fairwalter (Zürich, «über 1'500 Nutzende» laut CB-Insights-Vergleich, UNVERIFIED), ImmoSync (laut Capterra für Privatvermieter), Weka-Rechner für Stockwerkeigentum. Die Preise prüft Leons Claude (`preise-konkurrenz.md`).
- **Top-Klagen:** Software überdimensioniert, Mieteingänge von Hand prüfen (P11). Nebenkostenabrechnung bleibt liegen (P12, Mieter-Sicht).
- **Lücke:** Bankabgleich, das stärkste Feature, bietet LIMMOBI bereits an.

### I5: Minimal-Tool für Schweizer QR-Rechnungen (K3, K4)
- **Konkurrenz:** **gratis:** codecrete.net/qrbill (Open Source), qr-rechnung.net, PostFinance-Generator, UBS-QR-Portal, CashCtrl Free, Banana. **Günstig:** Pfeffersack (laut eigener Seite «Ab CHF 5/Monat im Jahresabo»), Kimai Cloud (~CHF 3/Mt., laut Reddit-Kommentar, UNVERIFIED), fakturio, Magic Heidi.
- **Lücke:** keine. Die Kernfunktion ist ein Gratis-Produkt.

### I6: Shopify/WooCommerce → Banana / AbaNinja / Run my Accounts / KLARA (K5)
- **Konkurrenz:**
  - Shopify↔bexio ist abgedeckt: Die **offizielle bexio-App von Helvy** hat 4.6★ bei 38 Reviews und kostet USD 12.74–63.76/Mt. (live geprüft). Dazu kommt bexioSync mit 3.9★ bei 8 Reviews.
  - Pfeffersack und Magic Heidi haben eine **native** Shopify-Anbindung, Pfeffersack ab CHF 5/Mt.
  - Laut Pfeffersack-Vergleich (Stand Juli 2026, Anbieter-Quelle) haben **Abacus/AbaNinja, Run my Accounts, KLARA, MILKEE und Banana keine Shopify-Integration**.
  - Generische Exporter (Order Blender, CSV Exporter Orders) erzeugen CSV-Dateien «für Buchhaltungssysteme». Ob Banana-Formate dabei sind, ist UNVERIFIED.
  - In WordPress gibt es für bexio/AbaNinja nur frische Plugins mit 0 Installationen (pingvin-sync-for-bexio, strainovic-it-shop-invoices-for-abaninja).
- **Zahlungsbereitschaft belegt:** «DATEV > Buchhaltungsexport Pro» (das deutsche Pendant) hat 4.8★ bei 115 Reviews (live gesehen). bexio-Connector-Kunden zahlen USD 12.74–63.76/Mt.
- **Top-Klagen bei bestehenden Connectoren:** falscher Abgleich (P34), langsamer Support (P35), Einrichtung nur mit Support möglich (P36), Stornos fehlen (P37).
- **Lücke:** Händler, deren **Treuhänder Banana oder Abacus verlangt**, haben keinen sauberen Weg. Das ist eine Hypothese. Es gibt **kein einziges Zitat eines Händlers, der danach fragt**.

### I7: Auszahlungs-Abgleich Mollie/PSP ↔ Shopify (K5)
- **Konkurrenz:** Recount (USD 29–49/Mt., **gestartet 12.10.2026, 1 Review**), Payout Close (nur Shopify Payments), Fincile, CONA, Clearfin, Moneybird-App, Combidesk (Mollie↔Buchhaltung), A2X (UNVERIFIED ob mit Mollie). «Payout Match» ist aus dem App Store **entfernt**.
- **Lücke:** Mollie-spezifisch vielleicht. Aber viele neue Einsteiger mit fast null Reviews sind ein schlechtes Zeichen für die Zahlungsbereitschaft.

### I8: Vereinssoftware DACH (K6)
- **Konkurrenz:** ClubDesk (trusted.de-Test Note 1.4), WISO MeinVerein (117 Reviews, Ø 4.6 auf OMR), easyVerein, Webling, Fairgate, Campai, Vereinsflieger. Preise holt Leons Claude.
- **Top-Klagen:** Mailzustellung (P49), Finanzteil zu kompliziert (P50), Preis (P51), App (P52).
- **Lücke:** keine strukturelle. Die Kunden sind zufrieden genug (Ø 4.6).

### I9: Tracker für Fristen und Zertifikate (K7)
- **Konkurrenz:** viele generische Tools für ablaufende Dokumente und Verträge. Bei UK-Zertifikats-Software sind Erinnerungen vermutlich eingebaut (UNVERIFIED).
- **Lücke:** Regeln sind länderspezifisch (UK-EICR, US-EPA). Das ist nicht unser Markt und teils reguliert.

### I10: Unterrichtsplanung + Schweizer QR-Abrechnung für Privatlehrer:innen (Musik, Nachhilfe) (K8)
- **Konkurrenz:**
  - **My Music Staff:** USD 16.95/Mt. laut Nutzer (P44). Planung, Abrechnung und Autopay sind drin, die Schweizer QR-Rechnung **UNVERIFIED**.
  - **taktjam:** für Musiklehrer in AT/DE/CH, Planung + Nachholstunden + Rechnungen, angeblich ~12 EUR (UNVERIFIED, Seite war nicht erreichbar). Laut Suchergebnis erzeugt es SEPA/EPC-QR. **Ob es die Schweizer QR-Rechnung kann, ist offen. Das ist der entscheidende Punkt.**
  - **Magic Heidi:** CHF 24.90/Mt. (Jahresabo) bzw. CHF 39/Mt. Serienrechnungen, Pakete, Reminder und QR sind drin, aber **keine Stundenplanung und keine Präsenz** (live geprüft).
  - **Pfeffersack:** Lösung für Musiker, ab CHF 5/Mt.
  - **TutorBird, TutorCruncher, Teachworks:** englisch, ohne CH-Fokus.
- **Top-Klagen:** Eltern nachjagen (P43), Kosten mit Kartengebühren (P46), Preis bei mehreren Lehrern (P48), keine App (P47).
- **Lücke (Hypothese):** «Stundenplan + Präsenz + Semester-Abrechnung mit Schweizer QR + automatischer Zahlungsabgleich (camt.054) + Schulferien pro Kanton». Für eine Person kostet das heute **zwei Tools** (z. B. Kalender + Magic Heidi = CHF 25–39/Mt. nur für die Rechnungen).

## Phase 4: Red Team

| Idee | Stärkstes Argument, warum sie scheitert | Gewinnt das Argument? | Urteil |
|---|---|---|---|
| I1 US-Handwerker light | Jobber/HCP/Joist + Dutzende Indie-Klone. In jedem Trade-Subreddit stehen Gründer-«Umfragen». Wir sind weder Handwerker noch Amerikaner. | **Ja** | ❌ Graveyard |
| I2 CH-Handwerker | Die Nachfrage verlangt Breite («hat alles»), nicht Einfachheit. Das sind 12+ Monate Bauzeit, viel Support und Branchenwissen, das wir nicht haben. | **Ja** | ❌ Graveyard |
| I3 US-Vermieter | Gesättigtster Indie-Markt, kein Vorteil für uns, US-Recht in 50 Staaten. | **Ja** | ❌ Graveyard |
| I4 CH-Privatvermieter | LIMMOBI hat schon Bankabgleich, dazu Fairwalter, ImmoSync und Bewy. Bei Fehlern im Mietrecht (Mietzinsanpassung, amtliches Formular, Nebenkosten-Ausweis) entsteht Haftung. Zielgruppe eher älter und offline, Verkauf über HEV ist schwer. | **Ja** | ❌ Graveyard |
| I5 QR-Rechnungs-Tool | Gratis-Alternativen von Banken und Open Source. Pfeffersack kostet CHF 5/Mt. inkl. Buchhaltung. | **Ja, klar** | ❌ Graveyard |
| I6 Shop → Banana/Abacus/RMA | (a) Es gibt kein Zitat eines Händlers, der danach fragt. (b) Pfeffersack für CHF 5/Mt. mit nativem Shopify ist eine billige Ausweichlösung. (c) Banana oder ein Exporter könnte es selbst bauen. (d) Kleiner Markt. **Gegenargument:** Den Treuhänder wechselt man nicht, und Banana/Abacus sind bei Treuhändern verbreitet (UNVERIFIED). Der App Store ist ein fertiger Vertriebskanal. | **Unentschieden** | ⚠️ überlebt nur **bedingt**, braucht einen 7-Tage-Test |
| I7 Payout-Abgleich | Viele neue Apps mit 0–1 Reviews, eine schon entfernt. Shopify oder Mollie können das jederzeit selbst bauen. | **Ja** | ❌ Graveyard |
| I8 Vereinssoftware | Ø-Bewertungen von 4.6 zeigen zufriedene Kunden. ClubDesk ist in der Schweiz stark. Viel Support in der Saison (GV, Beiträge). | **Ja** | ❌ Graveyard |
| I9 Fristen-Tracker | Generisch, viele Gratis-Alternativen, länderspezifische Regeln, kein Vorteil für uns. | **Ja** | ❌ Graveyard |
| I10 CH-Privatlehrer | (a) taktjam zielt genau auf DACH-Musiklehrer. (b) Magic Heidi deckt die Rechnungen ab. (c) Für die Schweiz gibt es nur dünne Belege (die Pain-Zitate sind US-lastig). (d) Lehrer sind preissensibel, und es gibt Churn in den Sommerferien. **Gegenargument:** Zahlungsbereitschaft ist belegt (USD 16.95, CHF 24.90–39). Wenn taktjam keine CH-QR-Rechnung und keinen Abgleich hat, ist die Lücke konkret und klein genug für uns. | **Unentschieden** | ⚠️ überlebt nur **bedingt** |

**Ergebnis: Keine Idee überlebt bedingungslos. Zwei überleben bedingt (I10, I6).** Das sind weniger als 3, und ich fülle die Liste bewusst nicht künstlich auf.

## Scores (alle 10, Formel: D×2 + WTP×2 + K×1.5 + Bau×1 + Wartung×1.5 + Reichweite×1.5 + Vorteil×1, max. 52.5)

Ein hoher Score rettet keine Idee, die im Red Team gestorben ist. Die Scores sind meine Schätzungen (ESTIMATE).

| Idee | D | WTP | K (5=wenig) | Bau | Wartung (5=wenig) | Reichw. | Vorteil | Rechnung | Total | Urteil |
|---|---|---|---|---|---|---|---|---|---|---|
| I1 | 5 | 4 | 1 | 3 | 2 | 3 | 1 | 10+8+1.5+3+3+4.5+1 | 31.0 | ❌ |
| I3 | 5 | 4 | 1 | 3 | 2 | 3 | 1 | 10+8+1.5+3+3+4.5+1 | 31.0 | ❌ |
| **I10** | 2 | 4 | 2 | 4 | 3 | 3 | 3 | 4+8+3+4+4.5+4.5+3 | **31.0** | ⚠️ |
| **I6** | 2 | 3 | 2 | 4 | 3 | 4 | 3 | 4+6+3+4+4.5+6+3 | **30.5** | ⚠️ |
| I4 | 3 | 4 | 2 | 3 | 2 | 2 | 4 | 6+8+3+3+3+3+4 | 30.0 | ❌ |
| I8 | 4 | 4 | 1 | 3 | 2 | 3 | 2 | 8+8+1.5+3+3+4.5+2 | 30.0 | ❌ |
| I5 | 3 | 1 | 1 | 5 | 4 | 3 | 4 | 6+2+1.5+5+6+4.5+4 | 29.0 | ❌ |
| I2 | 3 | 4 | 2 | 2 | 1 | 3 | 3 | 6+8+3+2+1.5+4.5+3 | 28.0 | ❌ |
| I7 | 3 | 3 | 1 | 3 | 3 | 4 | 1 | 6+6+1.5+3+4.5+6+1 | 28.0 | ❌ |
| I9 | 3 | 3 | 2 | 4 | 3 | 2 | 1 | 6+6+3+4+4.5+3+1 | 27.5 | ❌ |
