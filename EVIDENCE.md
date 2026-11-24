# Rhodium Germany — Technische Nachweise

Dieses Register enthält ausschließlich positiv dokumentierte Prüfungen mit klar begrenztem Aussageumfang. Es ist keine unabhängige Zertifizierung und keine allgemeine Leistungszusage.

## Lokal dokumentierter Doppel-Replay (12.10.2026)

- Prüfdaten: `enwik9-first-128MiB.bin`, 134.217.728 Byte (128 MiB).
- Zwei XZ-Pakete: 34.429.224 Byte und 35.314.196 Byte.
- Beide Pakete wurden laut lokalem Abschlussbericht jeweils mit zwei getrennten lokalen Validierungsprogrammen (A und B) rekonstruiert.
- Dokumentiertes Ergebnis: SHA-256 von Original und Rekonstruktion jeweils identisch; rekonstruierte Länge jeweils 134.217.728 Byte.
- Geltungsbereich: lokaler Replay unter den dokumentierten Bedingungen. Der Vergleich der Nutzlastgrößen ist kein Nachweis der gesamten Übertragungskosten.
- Interne Belegreferenzen: `13_LOKALER_DOPPEL_REPLAY` und `14_LOKALER_DOPPEL_REPLAY_BASELINE`, jeweils mit SHA-256-Manifest, laut `15_ABSCHLUSS_STATUS_20261012.txt`.

## Weitere dokumentierte Benchmark-Familien (historische Best-Evidence)

Die folgenden positiven Resultate sind in der vorhandenen Rhodium-Gesamtinventur und der Kunden-Evidence-Dokumentation mit Run-IDs erfasst. Sie sind **historische interne Ergebnisnachweise**, keine hier neu ausgeführten Tests oder unabhängig zertifizierten Messungen. Die Angaben zu kleinen Übertragungswerten beziehen sich auf den jeweiligen Warm-/Recognition-Testaufbau und dürfen nicht als universelle verlustfreie Kompression beliebiger Daten verstanden werden.

| Benchmark-Familie | Referenzumfang | Dokumentiertes Ergebnis | Nachweisreferenz |
|---|---:|---|---|
| Fingerprint Recognition 32 (32 Worker) | 1.000.000.000 Byte | 81.481 Byte Warm-Recognition-Wert; SHA-256 match; bitidentisch gemeldet | Run `36869981648` |
| Foreign Recognition 32 (32 Worker) | 134.728.520 Byte | 11.354 Byte Recognition-Wert; SHA-256 match; bitidentisch gemeldet | Run `36869283513` |
| Fingerprint Pure One-File | 1.048.576 Byte | 7.151 Byte Ergebnis; Restore-SHA-256 identisch; ca. 62 ms Restore | Run `36993722643` |

Die beiden 32-Worker-Familien sind **zwei Testfamilien mit je 32 Workern**, nicht automatisch 64 unabhängig abgenommene Benchmarks. Der historische Quellenbezug ist `Rhodium-Gesamtinventur-2026-10-22.md` sowie `Rhodium_Germany_Kunden_Evidence_Praesentation_V1.pptx`. Die Rohprotokolle und der vollständige Empfängerzustand sind nicht Bestandteil dieser öffentlichen Kurzfassung.

## Dokumentations- und Prüfstatus

Der lokale Registerstand vom 12.10.2026 enthält 10.083 Berichtseinträge, 8.308 eindeutige Berichtsdatei-SHA-256 und 1.737 Testgruppen. Diese Zahlen sind **keine** Zahl unabhängig bestätigter Benchmarks. Insbesondere werden 1.438 nur als PASS gemeldete Gruppen nicht pauschal als verifiziert veröffentlicht.

Weitere positive Prüfungen werden erst mit zugeordnetem Originalbeleg, Prüfumfang, Ergebnis und Integritätswert aufgenommen. Fehlversuche und unbestätigte Aussagen gehören nicht in die Erfolgsübersicht. Interne Rohdaten und geschützte Box-Implementierungen werden nicht veröffentlicht.

Quelle für den hier beschriebenen lokalen Prüfstand: `D:\rhodiumgermany\BEWEISE-ZENTRAL-20261011\00_BENCHMARKS_ZUSAMMENGEFUEHRT\15_ABSCHLUSS_STATUS_20261012.txt` und `08_ZUSAMMENFUEHRUNG_STATUS.json` (lokale Prüfprotokolle, nicht extern zertifiziert).

## Prüfsummen des lokal dokumentierten Doppel-Replays

Die folgenden SHA-256-Werte sind aus den vorhandenen lokalen Prüfmanifesten vom 12.10.2026 übernommen. Sie ermöglichen den gezielten Abgleich mit den privaten Originalen, ohne Quelldaten oder Implementierungsdetails zu veröffentlichen.

| Prüfobjekt | SHA-256 | Ergebnis |
|---|---|---|
| Originaldatensatz (128 MiB) | `17aab1a22a35df5b125d456910a8d5e0345fedd78e0bf32c177c9dcc0eb02d5c` | Referenz |
| Paket A (34.429.224 B) | `bb0e77a321053be60dfb54abef907fe207ea294f9f28a2d5e1c4f6487cebedbe` | Lokaler Restore PASS in Validator A und B |
| Vergleichspaket (35.314.196 B) | `572386ce4a8f4c2ae71587c8f2a843c3f8fbab96851ef99c16ae544d552842fa` | Lokaler Restore PASS in Validator A und B |

Für beide Pakete dokumentieren die Prüfmanifeste den identischen SHA-256-Wert von Original und Rekonstruktion. Die Paketdifferenz beträgt **884.972 Byte** zugunsten von Paket A. Das ist ein Vergleich der gespeicherten Pakete, keine Aussage über vollständige Netzwerk- oder Protokollkosten. Der Test ist **lokal dokumentiert**, nicht extern zertifiziert.

## Weitere historische positive Prüfpositionen (Inventur 22.10.2026)

Diese Positionen stammen aus der vorhandenen internen Gesamtinventur. **PASS** bezeichnet den dort dokumentierten Ergebnisstatus, nicht eine von dieser GitHub-Seite neu vorgenommene unabhängige Verifikation. Ergebnisse verschiedener Testaufbauten sind nicht direkt vergleichbar; Warm-/Recognition-Werte sind keine universellen Kompressionsraten.

| Inventur-ID | Prüfung | Dokumentiertes positives Ergebnis | Aussagegrenze |
|---|---|---|---|
| K01 | NASA Juno WAVES Datensatz, 62 Dateien | 5.443.001.419 Byte; Wiederherstellung mit identischem SHA-256, gemeldete verlustfreie Reduktion 85,54 % | Prüfung auf öffentlich verfügbaren Daten; keine Bestätigung durch NASA |
| K03 | Evidence Gateway | 250.000 Ereignisse auf 1.842 Ausgaben reduziert; Precision 1,0, Recall 1,0 laut Inventur | Definierter Filtertest, kein allgemeines Leistungsversprechen |
| K04 | 100 GiB Scale/Recovery | 107.374.182.400 Byte Testumfang; zwei Wiederherstellungsprüfungen als PASS dokumentiert | Historischer interner Skalierungstest |
| K05 | Signatur-/Manipulationsprüfung | 3/3 Signaturprüfungen und 3/3 Manipulationsabweisungen PASS | Prüfungsbezogener Integritätsnachweis |
| K06 | World Blind Proof | Run `34779963182`; 4/4 + 2/2 PASS laut Inventur | Historische Blind-/Integritätsprüfung; kein externer Prüfbericht hier beigefügt |
| K07 | External Matrix Proof | Run `33840634749`; 1 GiB; bitidentisch PASS laut Inventur | Historischer, konfigurationsabhängiger Test |
| K11 | Live Source | 64 MiB; Wiederherstellung PASS; 6.950 Byte Cold / 5.838 Byte Warm gemeldet | Gleiche Nutzlast; kein symmetrischer Internetpfad-Vergleich |
| K19 | 32-Point Validation | 32 dokumentierte Validierungspositionen | **Eine** Validierungsfamilie, nicht 32 separat bestätigte Benchmarks |
| K20 | Metrica Sports Sample | 33.554.432 Byte; 128 Blöcke; Restore-Hash identisch; P0 PASS gemeldet | Benchmark auf Beispieldaten |
| K22 | Mirror-Restore | 6 MiB A/B; bitidentischer Restore PASS | Begrenzter Wiederherstellungstest |
| K23 | Verify-Relay | End-to-End-Relay mit SHA-256-Siegel als verifiziert protokolliert | Historischer Relay-/Integritätsnachweis |
| K24 | WAN TRUE-COLD | Session `TRUE-COLD-20260929-141308`; 64 MiB; PASS gemeldet | Gilt ausschließlich für die dokumentierte Sitzung |
| K25 | 64 MiB Blackbox | 64 MiB; Cold/Warm-Durchläufe mit bitidentischer Wiederherstellung laut Inventur | Konfigurationsabhängiger lokaler Blackbox-Test |

**Quellenverweis:** `Rhodium-Gesamtinventur-2026-10-22.md`, Katalogpositionen K01–K25. Die zugrunde liegenden Rohberichte verbleiben in den geschützten Archiven. Externe Zertifizierung oder Herstellerendorsement wird nicht behauptet. Die Katalogpositionen sind nicht mit der Anzahl eindeutig verifizierter Benchmark-Läufe gleichzusetzen.


## Ergänzende historische Prüffamilien

Weitere dokumentierte Roundtrip-, Runner-, Matrix- und Pipeline-Ergebnisse mit ihren jeweiligen Aussagegrenzen sind in [Ergänzende Nachweise](EVIDENCE-SCOPE.md) aufgeführt. Die Einträge sind historische interne Prüfberichte, keine neu ausgeführten oder extern zertifizierten Tests.

## Zuordnung zu externen Verbindungsprüfungen

Im ergänzenden Register sind Z18 (Cross-Runner-Replay), Z21 (externe Runner mit 1 GiB und 256 MiB) und Z22 (1 MiB HTTPS-Echo) ausdrücklich ausgewiesen. Diese historischen PASS-Berichte belegen jeweils den dort beschriebenen Pfad. Ein separater Nachweis **Mobilfunk-Handy → WLAN-Laptop → kundenseitig authentifizierte Arbeiterbox** wurde bisher nicht als Originalprotokoll identifiziert und wird nicht als zusätzlicher bestandener Benchmark gezählt. Die Kundenzugangsabnahme ist unter [CUSTOMER-PILOT-ACCESS.md](CUSTOMER-PILOT-ACCESS.md) dokumentiert.
