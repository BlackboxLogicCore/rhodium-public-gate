# Rhodium Germany – kontrollierte Kundenprüfung

Status: Dokumentation veröffentlicht; **kein öffentlicher Kundentest-Endpunkt freigegeben oder extern erfolgreich geprüft**. Diese Seite ist keine Einladung, ungeprüfte Zugangsdaten oder sensible Daten zu senden.

## Freigabe für individuelle Pilotkunden

Ein Kundentest wird erst als **AKTIV** bezeichnet, wenn ein ausschließlich für den jeweiligen Kunden autorisierter Arbeiterbox-Endpunkt vorhanden ist und folgende Abnahme protokolliert wurde:

1. Eindeutige Kunden- und Testumgebungskennung, begrenzte Gültigkeit, widerrufbare Berechtigung; keine gemeinsamen oder öffentlichen Zugangsschlüssel.
2. Getrennte Arbeiterbox-Instanz mit Ressourcen- und Datenisolation. Kein Zugang zur privaten Mama- oder Forschungsbox.
3. Verschlüsselte Verbindung, definierte Größen- und Ratenlimits, dokumentierte Zustimmung zum Testdateneinsatz.
4. Echte Ende-zu-Ende-Prüfung mit vereinbarter Original-Testdatei: Eingangs-SHA-256, Übertragung, Wiederherstellung, Ausgangs-SHA-256, Byte-für-Byte-Vergleich und vollständige Transferbilanz.
5. Negativtest: nicht autorisierter Zugriff wird abgewiesen. Nachweis, dass andere Kundeninstanzen nicht erreichbar sind.
6. Unabhängiger Abruf über eine zweite Verbindung außerhalb des lokalen Host-Netzes; Zeitstempel und anonymisierte Prüfprotokolle.
7. Abschlussbericht mit PASS oder FAIL, Testumfang, Version, Empfänger-Vorbelegung, Reproduktionsanleitung und SHA-256-Siegel.

**Freigabekriterium:** Nur wenn sämtliche Kriterien erfüllt und dokumentiert sind, wird der kundenspezifische Zugang direkt an die autorisierte Kontaktperson übermittelt. Zugangsdaten gehören niemals in dieses öffentliche Repository.

## Kundenkommunikation

Rhodium Germany bietet auf Anfrage individuell vereinbarte, isolierte technische Pilotprüfungen an. Veröffentlichte historische Ergebnisse sind im [Nachweisregister](EVIDENCE.md) beschrieben. Ein konkreter Kundentest-Zugang wird erst nach technischer Abnahme und individueller Freigabe bereitgestellt. Es gibt derzeit keinen hier nachgewiesenen öffentlichen Selbsttest-Zugang.

## Datenschutz und Architektur

Testdaten werden nach vereinbarter Zweckbindung behandelt. Private Originale, Implementierungsdetails, interne Boxen und Schlüssel werden nicht veröffentlicht. Der vorgesehene Datenpfad ist Streaming; dauerhafte Zwischenspeicherung ist kein Standardmerkmal. Eine Speicherung von Prüfbelegen wird separat geregelt.

## Kostenfreier Ablauf ohne neues Abonnement

**Weg A – Testpaket des Kunden:** Der Kunde erhält zunächst die Prüfspezifikation und ein vereinbartes Limit. Eine autorisierte Kontaktperson stellt nur freigegebene, nicht vertrauliche Testdaten über einen zuvor verifizierten Übertragungsweg bereit. Rhodium prüft Eingangs-Hash, Datenumfang, Wiederherstellung, Ausgangs-Hash und vollständige Übertragungsbilanz. Ein öffentlicher Upload-Endpunkt ist derzeit **nicht** nachgewiesen und wird nicht vorgetäuscht.

**Weg B – Prüfung beim Kunden:** Nach schriftlicher technischer Freigabe wird ein isolierter Arbeiterbox-Prüfpfad in der vom Kunden kontrollierten Umgebung getestet. Es gibt keinen Fernzugriff auf die private Mama- oder Forschungsbox. Die Daten bleiben nach Vereinbarung beim Kunden; Rhodium erhält nur den freigegebenen Prüfbericht.

**Kostenregel:** Kein neues kostenpflichtiges Hosting, keine bezahlte Testplattform und keine automatische Fremddienstbuchung. Kostenlos nutzbare vorhandene Infrastruktur ist zulässig, soweit technisch und vertraglich geeignet. Etwaige Netz-, Geräte- und Personalkosten werden vor dem Pilot individuell geklärt; eine kostenlose Durchführung kann erst nach bestätigter Kapazität zugesagt werden.

**Versandfertige Unterlagen:** Für jeden Interessenten kann dieser öffentliche Link gemeinsam mit [EVIDENCE.md](EVIDENCE.md) und [EVIDENCE-SCOPE.md](EVIDENCE-SCOPE.md) geteilt werden. Er ist eine Prüfspezifikation, **kein Zugangstoken**. Kundenspezifische Zugangsdaten werden erst nach erfolgreichem Authentifizierungs-, Isolations- und Netztest ausgestellt.
