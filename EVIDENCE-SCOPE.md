# Ergänzende Nachweisprüfung

Weitere historische Prüfergebnisse werden nur mit dokumentiertem Geltungsbereich veröffentlicht. Private Rohdaten und Implementierungen bleiben geschützt.

## Zusätzliche historische Roundtrip-Nachweise

| ID | Prüfgegenstand | Dokumentiertes positives Ergebnis | Grenze |
|---|---|---|---|
| K26 | Mama Golden Roundtrip | 128 MiB, Cold 67.737.497 Byte, Warm 11.270 Byte; bitidentischer Restore berichtet | Lokaler Golden-Test; Warm mit Wiederverwendung |
| K27 | Kaggle-Datensatz | 698.914 Byte, Restore-SHA-256 identisch, Empfänger-ACK; PASS_LOCAL_ROUNDTRIP | Keine unabhängige Kaggle-Zertifizierung |
| Z01 | Automotive FAST75 | 75/75 Roundtrips, 0 gemeldete Fehler | Öffentliche Beispieldaten, keine Sicherheitszulassung |
| Z21 | Externe GitHub-Runner | 1 GiB und 256 MiB, PASS_REAL_ROUNDTRIP laut Originalberichten | Externe Runner sind kein unabhängiges Prüflabor |

Quelle: Rhodium-Gesamtinventur-2026-10-22.md. Historische positive Berichte, nicht in diesem Commit neu ausgeführte Tests.

## Externe Replays und große Matrixläufe

| ID | Prüfung | Positiv berichtetes Ergebnis | Einschränkung |
|---|---|---|---|
| Z18 | Cross-Runner-Protokoll-Replay | 1 GiB und zwei weitere Größen: PASS_REAL_CROSS_RUNNER_NATIVE_PROTOCOL_REPLAY | Kein gleichzeitiger TCP-Live-Transport |
| Z22 | HTTPS-Echo-Roundtrip | 1 MiB in 16 Paketen; identischer Restore-Hash | Echo-Endpunkt, kein zweiter nativer Rhodium-Empfänger |
| Z23 | 8-GiB Matrix-Roundtrip | 8.589.934.592 Byte; Cold 4.334.824.636 Byte, Warm 696.713 Byte; Hashgleichheit berichtet | Lokale synthetische Daten |
| Z24 | 4-GiB Matrix-Roundtrip | 4.294.967.296 Byte; Cold 2.167.425.223 Byte, Warm 348.553 Byte | Lokale synthetische Daten; frühere Abbrüche nicht als Erfolg gewertet |
| Z25 | Matrixlauf 1 Milliarde Byte | Cold 323.250.554 Byte, Warm 10.592 Byte; Hashgleichheit berichtet | Warm mit vorbefülltem Empfänger |

Quelle: Rhodium-Gesamtinventur-2026-10-22.md, zusätzliche Ergebnispositionen. Kein allgemeiner Kompressions- oder WAN-Leistungsnachweis.

## Weitere positive lokale Prüfungen

| ID | Test | Berichteter Erfolg | Grenze |
|---|---|---|---|
| K28 | Lokaler Vergleich mit MSP360 | 128 MiB Nutzlast; Cold- und Delta-Restore bitidentisch | Unterschiedliche Implementierungs-Messpunkte; keine unabhängige Herstellerzertifizierung |
| K29 | NASA C-MAPSS FD001 Datenpipeline | 495.144 Werte aus 20.631 Zeilen verarbeitet; kein Verlust gemeldet | Keine extern validierte Prognosegenauigkeit, keine NASA-Zertifizierung |
| Z26 | Niagara / USGS | Zwei Originalberichte mit Roundtrip- und Hash-PASS | Kein Nachweis von null physikalischem Rauschen |

Die Inventur enthält mehrere überlappende Registeransichten. Eine Registerzeile ist nicht automatisch ein unabhängiger Benchmark. Fehlversuche und laufende Tests sind nicht als positive Resultate aufgeführt.
