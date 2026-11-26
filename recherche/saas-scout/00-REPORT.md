# SaaS-Scout-Report: Ergebnis

**Von:** Jive (mit Claude, Opus) | **Datum:** 2026-11-26 | **Status:** Recherche abgeschlossen, Validierung offen
Details: `01-pain-harvest.md` (56 Pain Points) · `02-cluster-deepdive.md` (Cluster, Top 10, Red Team, Scores) · `preise-konkurrenz.md` (Preistabelle, an Leons Claude delegiert, Stand bei Abschluss: noch nicht geliefert)

## TL;DR (ehrlich)
- **Keine Idee hat den Red Team ohne Bedingungen überlebt.** Zwei überleben **bedingt**, also nur wenn ein 7-Tage-Test positiv ausfällt. Weniger als 3: Ich fülle die Liste bewusst nicht auf.
- **Fast jeder Schweizer Mini-Tool-Markt, den ich geprüft habe, ist schon besetzt oder gratis** (QR-Rechnungen, bexio-Connector, Vereine, Vermieter). Wo Lücken bleiben, sind sie klein.
- Gute Nachricht: Unser «Unfair Advantage» (Schweiz, Deutsch, QR-Rechnung/camt-Know-how) ist echt. Er hilft aber nur in Nischen, die so klein sind, dass grosse Anbieter sie ignorieren.

## Annahmen (bitte korrigieren)
`00-ausgangslage.md` ist noch leer, und im Auftrag standen Platzhalter `[X]`. Ich habe darum Folgendes angenommen:
- Je **5–8 Std./Woche**
- **max. CHF 500 Startkapital, max. CHF 50/Monat laufend**
- Skills: Web (JS/TS, HTML/CSS), etwas C#, einfaches SQL
- **Rechtlich:** Falls einer von euch unter 18 ist: Verträge mit Stripe, Shopify usw. brauchen in der Regel eine volljährige Person (UNVERIFIED pro Anbieter). Das früh mit den Eltern klären, wie es das README schon sagt.

---

## 1. Ranking der überlebenden Ideen

| Rang | Idee | Score (max. 52.5) | Status | Wichtigster offener Punkt |
|---|---|---|---|---|
| 1 | **I10 «Lektionen + QR-Abrechnung» für Schweizer Privatlehrer:innen** | 31.0 | ⚠️ bedingt | Kann **taktjam** die Schweizer QR-Rechnung inkl. Abgleich? Falls ja: aufgeben. |
| 2 | **I6 Shopify → Banana/AbaNinja-Export** für Schweizer Shops mit Banana-/Abacus-Treuhänder | 30.5 | ⚠️ bedingt | Kein einziger Händler hat bisher danach gefragt. Die Nachfrage ist unbelegt. |
| 3 | *bewusst leer* | – | – | Keine weitere Idee hat den Red Team überlebt. |

---

## 2. Opportunity #1: I10 «Lektionen + QR-Abrechnung» für Schweizer Privatlehrer:innen

**1. One-Liner + Zielgruppe:** Stundenplan, Präsenz und Semester- oder Monatsabrechnung mit Schweizer QR-Rechnung und automatischem Zahlungsabgleich, in einem Tool. Zielgruppe: **selbstständige Musik- und Nachhilfelehrer:innen in der Deutschschweiz mit 10–40 Schüler:innen, die Eltern Rechnungen stellen.** Musikschulen mit Angestellten gehören nicht dazu.

**2. Problem + Zitate:**
- "does it automatically follow up when payments fail, or do you still have to chase parents" (Musiklehrer:in, [reddit.com/comments/1wzi420/_/pfituor](https://www.reddit.com/comments/1wzi420/_/pfituor/), 2026-10-12)
- "I spend $16.95 per month and My Music Staff does it all!" (Beleg für Zahlungsbereitschaft, [reddit.com/comments/1rse814/_/pd9o1x9](https://www.reddit.com/comments/1rse814/_/pd9o1x9/), 2026-10-01)
- "I don't need accounting/accounting export/CRM features — literally just quick PDF QR invoices on phone or laptop." (CH, nennt Tutoren, [reddit.com/comments/1vmm5yf](https://www.reddit.com/comments/1vmm5yf/), 2026-08-12)
- "Expensive, particularly when card processing fees are added." (TutorCruncher-Review, Capterra, **UNVERIFIED**)
- ⚠️ Die Pain-Belege sind **US-lastig**. Für die Schweiz ist der Schmerz nicht direkt belegt, sondern nur abgeleitet: Magic Heidi baut eine eigene Landingpage für «Privatlehrer».

**3. Konkurrenz:**
| Name | Preis | Schwächen |
|---|---|---|
| My Music Staff | USD 16.95/Mt. (Nutzerangabe) | Englisch, USD, Schweizer QR UNVERIFIED |
| taktjam | ~12 EUR (UNVERIFIED) | Zielt auf DACH. Laut Suche SEPA/EPC-QR, Schweizer QR **unbekannt**. **Grösste Gefahr.** |
| Magic Heidi | CHF 24.90/Mt. jährlich, CHF 39/Mt. monatlich (live) | **Kein Stundenplan, keine Präsenz.** Die Seite sagt, gehaltene Stunden muss man «separat» notieren. |
| Pfeffersack | ab CHF 5/Mt. | Buchhaltung für Musiker, kein Stundenplan (UNVERIFIED) |
| TutorBird / TutorCruncher | UNVERIFIED | Englisch, teuer bei mehreren Lehrern (UNVERIFIED) |

**4. Wedge (1 Satz):** «Ein Tool statt Kalender plus Rechnungsprogramm: Stunden abhaken, auf Knopfdruck QR-Rechnungen an alle Eltern schicken, Kontoauszug hochladen, und die Software weiss, wer bezahlt hat. Für weniger Geld als Magic Heidi allein.»

**5. Preis:** **CHF 15/Monat oder CHF 150/Jahr**, 30 Tage gratis testen, kein Freemium.
- Unter Magic Heidi (CHF 24.90–39), obwohl Stundenplanung dabei ist. Etwa auf dem Niveau von My Music Staff.
- Ohne Freemium, weil wir wenig Supportkapazität haben.
- Die Testphase soll zum Semesterstart passen.

**6. Unit Economics (alles ESTIMATE):**
- Brutto CHF 1'000 / CHF 15 = **67 Kund:innen**.
- Zahlungsgebühren ESTIMATE ~2.9 % + CHF 0.30 (Stripe-ähnlich): CHF 15 → ca. CHF 14.27 netto. Dazu ca. CHF 30/Mt. Hosting und Mailversand (ESTIMATE).
- Damit sind es **~72 zahlende Kund:innen für CHF 1'000 netto MRR**.
- **Churn-Annahme 4 %/Monat** (ESTIMATE; Sommerferien, Lehrer hören auf). Bei 72 Kund:innen gehen ca. 3 pro Monat verloren.
- Um in 6–9 Monaten auf 72 zu kommen, braucht es **~10–12 neue Kund:innen pro Monat**.
- **Merchant of Record:** **Nicht nötig, solange nur Schweizer Kund:innen und ein weltweiter Umsatz unter CHF 100'000** (dann keine MWST-Pflicht; ESTIMATE, mit Treuhänder bestätigen). Für Kund:innen aus DE/AT später Paddle oder Lemon Squeezy (MoR, ca. 5 % + Fixgebühr, UNVERIFIED) oder eine eigene EU-Reverse-Charge-Lösung.
- **Wichtig:** Das Geld der Eltern fliesst **direkt aufs Konto der Lehrperson**. Wir berühren keine Zahlungen, also keine Finanzmarkt-Bewilligung.

**7. MVP-Scope (das, wofür man zahlt):**
1. Schüler:innen und Familien, wiederkehrende Lektionen (wöchentlich), **Schulferien pro Kanton werden automatisch übersprungen**
2. Präsenz, Absenzen, Nachholstunden
3. Abrechnungslauf (Monat, Quartal, Semester): **QR-Rechnungs-PDFs mit Referenz (QRR/SCOR)** per Mail an die Eltern
4. **camt.054/camt.053-Upload aus dem E-Banking**: Rechnungen werden automatisch als bezahlt markiert, dazu sanfte Zahlungserinnerung
5. Übersicht «wer hat bezahlt, wer nicht»

**Explizit OUT:** Online-Zahlung/TWINT, native Apps, Buchhaltung/MWST, Musikschulen mit mehreren Lehrern, Übungs-Tracking, Video, Website-Baukasten, Lohn.

**8. Erste 100 Kund:innen:**
- **Kanäle:**
  - Eigenes Netzwerk zuerst (eure eigenen Musik- und Nachhilfelehrer)
  - Regionalsektionen des **Schweizerischen Musikpädagogischen Verbands (SMPV)** (Reichweite UNVERIFIED)
  - Facebook-Gruppen zu Musik- und Nachhilfeunterricht in der Schweiz (Existenz UNVERIFIED, zuerst suchen)
  - Lehrpersonen-Verzeichnisse auf Musikschul-Webseiten (öffentliche Kontaktangaben, nur einzeln anschreiben, **kein automatisiertes Scraping**)
  - Google-Keywords: «QR-Rechnung Nachhilfe», «Rechnung Musikunterricht Vorlage», «Schülerverwaltung Musiklehrer»
  - Später ein kostenloser **«QR-Rechnungs-Vorlagen-Generator für Lehrpersonen»** als SEO-Köder
- **Kaltakquise-Script (3 Sätze):**
  > «Grüezi Frau X, ich habe Ihr Angebot für Klavierunterricht auf [Seite] gesehen. Wir bauen gerade ein kleines Schweizer Tool, das Lektionen, QR-Rechnungen an Eltern und den Zahlungsabgleich mit dem E-Banking in einem macht. Darf ich Ihnen 10 Minuten lang zwei Fragen stellen, wie Sie das heute lösen? Verkaufen will ich nichts.»
- **Launch:**
  - 15–20 Beta-Lehrpersonen machen ein Semester gratis mit und erhalten dafür einen Gründerpreis von CHF 99/Jahr, fix für immer.
  - Mit den ersten 3 Testimonials auf die Verbands-Newsletter und in die FB-Gruppen.

**9. 7-Tage-Validierung (vor dem ersten Code):**
- **Tag 1:** taktjam (und My Music Staff) gratis testen. **Können sie die Schweizer QR-Rechnung mit Referenz und einen camt-Abgleich? Falls ja: sofort stoppen.**
- **Tag 1–2:** Landingpage (Gratis-Baukasten) mit 3 Mockups, Preis und dem Button «Gründerplatz reservieren, CHF 99/Jahr». Entweder als rückerstattbare Vorauszahlung über einen Stripe Payment Link (nur mit volljährigem Kontoinhaber) oder als verbindliche Reservation per Mail.
- **Tag 2–7:** 30 Lehrpersonen direkt kontaktieren, mindestens 15 Gespräche führen.
- **Erfolgsschwelle:**
  - ≥ 8 von 15 sagen, die Abrechnung kostet sie > 1 Std./Monat oder sie jagen Zahlungen nach, **und**
  - **≥ 3 Vorauszahlungen bzw. verbindliche Reservationen**

**10. + 11. Scores:**
- Demand 2 | WTP 4 | Konkurrenz 2 | Bau 4 | Wartung 3 | Reichweite 3 | Vorteil 3
- Rechnung: 2×2 + 4×2 + 2×1.5 + 4×1 + 3×1.5 + 3×1.5 + 3×1 = 4 + 8 + 3 + 4 + 4.5 + 4.5 + 3 = **31.0**

**12. Grösstes Risiko + Kill-Kriterium:**
- **Risiko:** taktjam oder Magic Heidi schliessen die Lücke in wenigen Wochen, und der Schweizer Markt ist zu klein (Anzahl Privatlehrer:innen in der CH: **unbekannt**).
- **Kill, falls eines davon zutrifft:**
  - taktjam kann Schweizer QR + Abgleich schon
  - nach 30 Kontakten **< 3 Vorauszahlungen/Reservationen**
  - weniger als die Hälfte der Gesprächspartner:innen empfindet die Abrechnung als Problem

---

## 3. Opportunity #2: I6 Shopify → Banana/AbaNinja-Export

**1. One-Liner + Zielgruppe:** Eine Shopify-App, die Bestellungen, Rückerstattungen, Gebühren und Auszahlungen monatlich als **fertige Banana-Importdatei mit Schweizer MWST-Codes (8.1/2.6/0 %)** liefert. Zielgruppe: **Schweizer Shopify-Shops mit 20–500 Bestellungen pro Monat, deren Buchhaltung bzw. Treuhänder auf Banana (später AbaNinja/Run my Accounts) läuft.**

**2. Problem + Zitate** (es sind Zitate zu bestehenden Connectoren, **keines zu Banana**):
- "Die Transaktionen werden nicht korrekt abgeglichen und die Synchronisierung mit dem Bexio-Account funktioniert oft nicht." ([apps.shopify.com/bexiosync/reviews](https://apps.shopify.com/bexiosync/reviews), 2021-02-11, alt)
- "Lausiger Support. Schreibt erst nach einer Woche zurück und gibt Shopify die Schuld, obwohl es am App liegt." (ebd., 2024-11-27)
- "Mollie sends payouts separately, with transaction fees and refunds taken into account. So the amounts don't always line up directly." ([reddit.com/comments/1xytbns](https://www.reddit.com/comments/1xytbns/), 2026-11-17)
- Fakt: Laut Pfeffersack-Vergleich (Stand Juli 2026, Anbieter-Quelle) haben **Banana, Abacus/AbaNinja, Run my Accounts, KLARA und MILKEE keine Shopify-Integration**.

**3. Konkurrenz:**
| Name | Preis | Schwächen |
|---|---|---|
| bexio-App (Helvy, offiziell) | USD 12.74–63.76/Mt., 4.6★/38 | nur bexio. Stornos fehlen (Review 2026-10-23). |
| bexioSync | UNVERIFIED (2021: USD 300/Jahr), 3.9★/8 | nur bexio, Support-Klagen |
| Pfeffersack | ab CHF 5/Mt. inkl. Shopify | verlangt einen **Wechsel des Buchhaltungssystems** |
| Magic Heidi | Pro-Plan, Preis UNVERIFIED | ebenfalls Systemwechsel |
| Generische CSV-Exporter (Order Blender u. a.) | UNVERIFIED | ob Banana-Format + CH-MWST dabei ist: UNVERIFIED |

**4. Wedge:** «Behalte Banana und deinen Treuhänder. Die App liefert ihm jeden Monat eine saubere Datei statt Excel-Chaos.»

**5. Preis:** **USD 9 (bis 100 Bestellungen/Mt.) / USD 19 (bis 500)** über die Shopify-Abrechnung, 14 Tage gratis.
- Unter dem bexio-Connector.
- Die Shopify-Abrechnung erspart uns eigene Zahlungsabwicklung und Mahnwesen.

**6. Unit Economics (ESTIMATE):**
- Ø USD 14 ≈ CHF 12 (Kurs ESTIMATE) → **~84 Shops für CHF 1'000 MRR**.
- Shopify-Umsatzbeteiligung laut aktuellen Partner-Bedingungen: ESTIMATE 0 % bis zu einer Umsatzschwelle (UNVERIFIED, prüfen).
- Hosting ~CHF 20/Mt. (ESTIMATE).
- **Churn-Annahme 3 %/Monat** (ESTIMATE; Buchhaltungs-Integrationen sind «sticky»).
- **MoR:** Shopify rechnet mit den Händlern ab. Unsere eigene Steuerpflicht beginnt erst ab CHF 100'000 weltweitem Umsatz (ESTIMATE, mit Treuhänder prüfen).

**7. MVP-Scope:**
1. Shopify-OAuth + Lesezugriff auf Bestellungen, Rückerstattungen und Shopify-Payments-Auszahlungen
2. Mapping auf MWST-Codes und Konten (Vorlage «Kontenplan KMU»)
3. Monatlicher Export im **Banana-Importformat** (Format zuerst prüfen!)
4. Vorschau + Prüfliste: «Auszahlung = Summe Bestellungen – Gebühren – Rückerstattungen»
5. Versand an die Treuhänder-Mail-Adresse

**OUT:** Zwei-Weg-Sync, Lagerbestand, Rechnungsstellung, Mollie/TWINT in v1, Abacus in v1.

**8. Erste 100 Kund:innen:**
- **Kanäle:**
  - Shopify-App-Store-SEO («Banana», «Buchhaltung Schweiz», «Treuhand», «MWST»)
  - **Treuhänder als Multiplikatoren:** Treuhandbüros, die auf ihrer Webseite Banana anbieten, einzeln anschreiben
  - Schweizer Shopify-Agenturen
  - In r/Switzerland gilt: **Eigenwerbung wird entfernt** (P32 zeigt, wie feindselig die Stimmung ist)
- **Script:**
  > «Guten Tag, ich habe gesehen, dass Sie Buchhaltungen mit Banana führen. Bekommen Sie von Kund:innen mit Shopify-Shop die Verkäufe als Excel-Exporte, die Sie von Hand verbuchen müssen? Wir prüfen gerade, ob sich eine kleine App lohnt, die Ihnen jeden Monat eine fertige Banana-Importdatei liefert. Hätten Sie 10 Minuten für zwei Fragen?»

**9. 7-Tage-Validierung:**
- **Tag 1 (1 Stunde):** Banana-Dokumentation lesen. Gibt es schon einen Shopify-Import oder eine Erweiterung, oder liefert ein bestehender CSV-Exporter das Banana-Format? **Falls ja: Kill.**
- **Tag 2–7:** 30 Treuhandbüros mit Banana-Angebot und 15 Schweizer Shopify-Shops anschreiben.
- **Erfolgsschwelle:**
  - **≥ 5 Treuhänder bestätigen, dass Shopify-Kund:innen Daten von Hand liefern**, und ≥ 2 würden die App empfehlen
  - **oder** ≥ 3 Shops reservieren verbindlich

**10. + 11. Scores:**
- Demand 2 | WTP 3 | Konkurrenz 2 | Bau 4 | Wartung 3 | Reichweite 4 | Vorteil 3
- Rechnung: 2×2 + 3×2 + 2×1.5 + 4×1 + 3×1.5 + 4×1.5 + 3×1 = 4 + 6 + 3 + 4 + 4.5 + 6 + 3 = **30.5**

**12. Grösstes Risiko + Kill-Kriterium:**
- **Risiko:** Der Markt «Shopify × Banana» ist winzig und preissensibel. Wer wenig zahlen will, wechselt lieber zu Pfeffersack für CHF 5. Dazu kommt Plattform-Risiko durch Shopify-API-Änderungen.
- **Kill, falls eines davon zutrifft:**
  - Banana hat den Import bereits
  - **< 3 von 30 Treuhändern** bestätigen das Problem

---

## 4. Top-3-Picks mit Begründung
1. **I10 Lehrpersonen:** Die Zahlungsbereitschaft ist am besten belegt (USD 16.95 und CHF 24.90–39 werden heute schon bezahlt). Die Lücke (Stundenplan + Schweizer QR + Abgleich in einem) ist konkret und mit unseren Skills in 4–8 Wochen baubar. Euer eigenes Netzwerk (eigene Lehrpersonen) macht die ersten Gespräche leicht.
2. **I6 Banana-Export:** Ein fertiger Vertriebskanal (App Store), sehr kleiner Bauumfang und wenig Support. Die Nachfrage ist aber reine Hypothese, deshalb Platz 2.
3. **Leer.** Alle anderen Ideen sind im Red Team gestorben (siehe unten). Lieber zwei ehrliche Tests als drei schöne Folien.

Tipp: Die **Kill-Checks an Tag 1 beider Ideen kosten zusammen ca. 2 Stunden.** Macht sie zuerst, parallel: Jive nimmt I10, Leon I6.

---

## 5. Graveyard

| Idee | Warum tot (1 Zeile) |
|---|---|
| Einfaches QR-Rechnungs-Tool CH | Gratis bei codecrete, qr-rechnung.net, PostFinance, UBS und CashCtrl Free. Pfeffersack ab CHF 5/Mt. |
| WooCommerce-Plugin für Schweizer QR | Das Top-Plugin hat nur ~500 Installationen, und **3 neue Konkurrenten wurden diese Woche aktualisiert (0 Installationen)**. Winzig und überlaufen. |
| Shopify-App für QR-Rechnungen | Die 2 bestehenden Apps haben 3–5 Reviews. Der Markt ist zu klein. |
| Shopify↔bexio-Connector | Die offizielle bexio-App (Helvy) hat 4.6★ bei 38 Reviews. Besetzt. |
| Auszahlungs-Abgleich Mollie/Stripe | Recount, Payout Close, Fincile, CONA, Clearfin, Combidesk, Moneybird. Neue Apps haben 0–1 Reviews, eine wurde entfernt. |
| Software für Schweizer Privatvermieter | LIMMOBI (Bankabgleich), Fairwalter, ImmoSync, Bewy, GARAIO. Dazu Haftung bei Fehlern im Mietrecht. |
| US-Kleinvermieter-Tool | Der gesättigtste Indie-Markt (TenantCloud, RentRedi, TurboTenant, Baselane…). |
| Field Service für US-Handwerker | Jobber, HCP, ServiceTitan, Joist, QuoteIQ und eine Flut von Indie-Klonen. |
| Handwerker-Software CH | Die Kundschaft will «alles» (P23): lange Bauzeit, viel Support, Branchenwissen fehlt. |
| Vereinssoftware DACH | ClubDesk, WISO MeinVerein (Ø 4.6), easyVerein, Webling, Fairgate. Saisonaler Support-Peak. |
| E-Rechnung DE für Vereine/Kleinunternehmer | Zum Empfangen gibt es den Gratis-Viewer bei ELSTER. Kleinunternehmer nach §19 müssen keine E-Rechnungen ausstellen. Riesige Platzhirsche. |
| bexio-Alternative (Buchhaltung) | 8+ Schweizer Alternativen (CashCtrl, Klara, Banana, Magic Heidi, Pfeffersack, AbaNinja, RMA, fakturio). Buchhaltung ist zudem heikel. |
| Lerndokumentation für Lehrbetriebe | Läuft über Branchenverbände (time2learn, Kompetenzkompass). Beschaffung statt Self-Service, keine Klagen gefunden. |
| Fristen-/Zertifikats-Tracker (EICR, EPA) | Ausländische Regulierung, teils reguliert, viele generische Tools. |
| Lieferanten-Excel → Shop-Sync | Bestehende Feed-/Sync-Apps (UNVERIFIED welche). Kein Vorteil für uns. |
| Lead-Gen/Outreach | Apollo, Instantly. Die Leute wollen die menschliche Arbeit kaufen (P55), nicht die Software. |
| Stockwerkeigentum selbst verwalten (CH) | **Nicht tot, aber unbelegt:** 0 Pain-Quellen, aber auch kein Schweizer Tool gefunden. Nur testen, wenn ihr selbst STWEG-Eigentümer kennt (5 Gespräche). |

---

## 6. Die nächsten 14 Tage für #1 (I10 Lehrpersonen)

| Tag | Aufgabe | Wer | Ergebnis / Schwelle |
|---|---|---|---|
| 1 | `00-ausgangslage.md` ausfüllen (Zeit, Budget, Alter → Rechtliches mit den Eltern klären) | beide | Annahmen bestätigt oder korrigiert |
| 1 | **Kill-Check:** taktjam + My Music Staff testen (Schweizer QR mit Referenz? camt-Abgleich? Kantonsferien?) | Jive | Falls alles vorhanden: **Stopp**, weiter mit I6 |
| 1 | Kill-Check I6: Banana-Importformat und mögliche Shopify-Erweiterung prüfen | Leon | Falls vorhanden: I6 tot |
| 2 | Liste mit 40 Lehrpersonen (eigenes Umfeld, Musikschul-Seiten, Verbände), Kontakte einzeln von Hand | beide | 40 Kontakte |
| 2–3 | Landingpage + 3 Mockups (Stundenplan, Abrechnungslauf, «bezahlt»-Ansicht) + Gründerpreis CHF 99/Jahr | Jive | Seite online |
| 3–7 | 30 Nachrichten/Anrufe, mindestens 15 Gespräche (Fragen: Wie rechnest du heute ab? Wie viel Zeit kostet es? Was nervt?) | beide | Notizen in `recherche/lehrer-interviews.md` |
| 7 | **Go/No-Go:** ≥ 8 von 15 sehen das Problem **und** ≥ 3 Reservationen/Vorauszahlungen | beide | Go → Tag 8. No-Go → I6 testen oder neu suchen. |
| 8–9 | Technik-Spike: QR-Rechnung mit Referenz erzeugen (Open-Source-Bibliothek, z. B. codecrete «SwissQRBill» für Java/.NET, UNVERIFIED welche Sprachen) + camt.054 parsen | Jive | Ein PDF und ein Abgleich funktionieren |
| 10–12 | Klick-Prototyp oder Mini-MVP: Schüler → Lektionen → Abrechnungslauf | beide | 3 Beta-Lehrpersonen testen live |
| 13 | Datenschutz: Daten von Kindern/Eltern → Hosting CH/EU, Datenschutzerklärung nach nDSG, nur minimale Daten erfassen | Leon | Checkliste |
| 14 | Plan für Woche 3–8 (MVP-Features 1–5), Beta-Vereinbarung mit 10–20 Lehrpersonen | beide | Roadmap in `03-aufgaben.md` |

---

## Methodik und Grenzen
- Reddit ist direkt gesperrt. Ich habe stattdessen das öffentliche Archiv **Arctic Shift** genutzt. Capterra und Mike Holt waren gesperrt (403), solche Zitate sind als UNVERIFIED markiert.
- Shopify App Store und WordPress.org habe ich live geprüft. **Eine Suchmaschinen-Zusammenfassung war falsch:** Sie meldete «bexioSync 4.2★/45 Reviews», live waren es 3.9★/8, und die offizielle bexio-App ist eine andere App. Deshalb: Zahlen nur aus Live-Seiten übernehmen.
- Nicht gefunden bzw. nicht erreichbar: taktjam.com (SSL-Fehler), Marktgrösse «Privatlehrer:innen Schweiz».
