# LB2 — Theorieprüfung 2: Lernziele, Prüfungsrahmen & Spick

## Prüfungsrahmen

| | |
|---|---|
| **Termin** | Tag 10 (02.11.) |
| **Dauer** | 40 Minuten, Einzelarbeit, Stille |
| **Format** | Computer, Safe Exam Browser (SEB) – Moodle |
| **Fragetyp** | Multiple Choice: pro Frage genau **eine** richtige Antwort (vereinzelt Zuordnungsfragen) |
| **Umfang** | 33 Fragen, Reihenfolge der Fragen und Antworten zufällig |
| **Bewertung** | 100 Punkte, Fragen je nach Schwierigkeit 2–4 Punkte, **keine Minuspunkte** bei falschen Antworten, Notenskala wie LB1 |
| **Gewichtung** | 30 % der Modulnote |
| **Stoff** | Schwerpunkt Tag 6–8 (Verschlüsselung inkl. GPG-Praxis, Dateiablage, CIA & Risiko) plus Repetition der Themen aus Tag 1–4 und ~~Grundlagen aus Tag 9 (Backup, RAID, Ransomware, ohne eigenes Lernziel)~~ |
| **Nicht geprüft** | Git/Markdown und Checklisten (→ LB3) |
| **Hilfsmittel** | **Persönlicher Spick**: 1 A4-Blatt, doppelseitig (siehe unten). Keine elektronischen Geräte (Laptop, Tablet, Smartphone, Smartwatch), keine KI |

### Aufbau der Prüfung

| Nr. | Lernziel | Fragen |
|---|---|:---:|
| 1 | Symmetrische Verschlüsselung & Häufigkeitsanalyse | 5 |
| 2 | Asymmetrische Verschlüsselung, Hybrid, PGP & GPG-Praxis | 4 |
| 3 | CIA-Prinzip & Risikomanagement | 6 |
| 4 | Dateiablage & Datenlebenszyklus | 4 |
| 5 | Authentifizierung, Passwörter & Social Engineering (Tag 1) | 4 |
| 6 | Datenschutzrecht, Datenschutz vs. Datensicherheit & Online-Anonymität (Tag 2–3) | 4 |
| 7 | Lizenzmodelle, Privacy-Threats & Dark Patterns (Tag 4) | 6 |
| | **Total** | **33** |

Die Fragen decken die Taxonomiestufen K1 (Wissen), K2 (Verstehen) und K3 (Anwenden an einem Szenario) ab. Etwa die Hälfte der Fragen sind K2/K3-Szenarien – reines Auswendiglernen genügt nicht.

---

## Lernziele

Nach der Vorbereitung können Sie (Bezug zur [Kompetenzmatrix M231](https://kompetenzmatrix.ch/informatiker/cluster-data/m231/) in Klammern):

**1. Symmetrische Verschlüsselung & Häufigkeitsanalyse** *(C1B/C1I · HZ 2.1, 2.4)*
- das Prinzip der Verschlüsselung (Klartext, Schlüssel, Chiffrat) erklären sowie Caesar, Vigenère und AES einordnen und das Schlüsselverteilungsproblem benennen (K1/K2)
- ein Chiffrat mit Häufigkeitsanalyse bzw. Kasiski-Test angreifen und beurteilen, wann ein Verfahren dagegen geschützt ist (K3)

**2. Asymmetrische Verschlüsselung, PGP & GPG-Praxis** *(C1B/C1I/C1A · HZ 2.1)*
- erklären, wer welchen Schlüssel (Public/Private) für Verschlüsselung und Signatur verwendet, und Hybridverschlüsselung (TLS, PGP) beschreiben (K1/K2)
- clientseitige und serverseitige Verschlüsselung (z. B. E2EE) an einem Beispiel unterscheiden und eine eingesetzte Lösung beurteilen (K2/K3)
- die GPG-Schritte in der richtigen Reihenfolge und mit den passenden Schlüsseln beschreiben (Schlüsselpaar erstellen, Public Key exportieren/importieren, verschlüsseln, entschlüsseln, signieren, Signatur prüfen, Fingerprint vergleichen) und Fehler in einem Szenario erkennen (K2/K3)

**3. CIA-Prinzip & Risikomanagement** *(Datensicherheit der Infrastruktur · HZ 3.1, 5.1, 5.2)*
- für einen Vorfall das primär verletzte CIA-Ziel bestimmen und je Ziel typische Bedrohungen, Massnahmen und Kontrollen nennen (K2/K3)
- Risiko als Eintrittswahrscheinlichkeit × Schadensausmass bewerten, in einer Risikomatrix einordnen und eine passende Strategie (vermeiden, vermindern, übertragen, akzeptieren) wählen (K3)

**4. Dateiablage & Datenlebenszyklus** *(B1B/B1I, B2B · HZ 5.1, 5.2)*
- Ordnungsprinzipien und Namenskonventionen anwenden, Daten und Applikationen trennen und lokale von cloudbasierter Ablage abgrenzen (K1/K2)
- für ein Szenario Aufbewahrungsfristen (CH) und eine sichere Löschmethode wählen und begründen (K3)

**5. Authentifizierung, Passwörter & Social Engineering (Repetition Tag 1)** *(E1B · HZ 2.3, 2.4, 5.1)*
- Authentifizierung und Autorisierung unterscheiden, die drei Faktorenkategorien nennen und MFA sowie Least Privilege erklären (K1/K2)
- Social-Engineering-Methoden (Phishing, Vishing, Pretexting, Baiting) erkennen, Prinzipien guter Passwörter und Passwortmanager begründen und für ein Fallbeispiel eine angemessene Reaktion ableiten (K2/K3)

**6. Datenschutzrecht, Datenschutz vs. Datensicherheit & Online-Anonymität (Repetition Tag 2–3)** *(A1B, F1B · HZ 1.1–1.4, 2.3, 3.1)*
- revDSG und DSGVO (Geltungsbereich, Marktortprinzip, besonders schützenswerte Daten, Meldepflicht) nennen und Datenschutz von Datensicherheit abgrenzen (K1/K2)
- für ein Szenario beurteilen, ob Datenschutz, Datensicherheit oder beides betroffen ist, und die Funktionsweise sowie Grenzen von VPN und Tor erklären (K3)

**7. Lizenzmodelle, Privacy-Threats & Dark Patterns (Repetition Tag 4)** *(D1B/D1I, F2B · HZ 6.1, 5.2, 4.1)*
- permissive und Copyleft-Lizenzen sowie die Creative-Commons-Kürzel (BY, SA, NC, ND) unterscheiden und Cookie-Typen, Tracking und Fingerprinting erklären (K1/K2)
- für ein Szenario die passende Lizenz begründen, die verwendete Tracking-Methode identifizieren und ein Dark Pattern samt Manipulationswirkung erkennen (K3)

---

## Spick (persönliche Zusammenfassung)

| | |
|---|---|
| **Umfang** | **1 A4-Blatt**, doppelseitig beschrieben bzw. bedruckt |
| **Persönlich** | Selbst erstellt, handschriftlich oder am Computer gesetzt und ausgedruckt. Kein Kopieren von Mitlernenden, keine gemeinsame Vorlage, kein KI-generierter Text ohne eigene Überarbeitung |
| **Beschriftung** | Name und Klasse oben auf dem Blatt |
| **Abgabe** | Der Spick wird mit der Prüfung abgegeben. Er wird **nicht** bewertet |
| **Nicht erlaubt** | Mehrere Blätter, aufgeklebte Zusatzblätter, Bücher, Ausdrucke der Folien oder des Skripts |

**Tipps für einen guten Spick:**
- Nach den 7 Lernzielen gliedern, pro Lernziel ein Block
- Stichwörter, Tabellen und kleine Skizzen statt ganzer Sätze (z. B. Risikomatrix, Ablauf Hybridverschlüsselung)
- Begriffe, die Sie verwechseln (Public/Private Key, symmetrisch/asymmetrisch, Signatur/Verschlüsselung), nebeneinander stellen
- Eigene Beispiele eintragen – sie helfen beim Erinnern
- Die Erstellung selbst ist die beste Vorbereitung: Wer den Spick gut schreibt, braucht ihn kaum noch

---

## Vorbereitung

1. Tag-Unterlagen 6–8 durchgehen: [Tag 6](../../tag-06.md), [Tag 7](../../tag-07.md), [Tag 8](../../tag-08.md). Für Lernziele 5–7: [Tag 1](../../tag-01.md)–[Tag 4](../../tag-04.md) und [LB1-Repetition](../lb1/lb1-lernziele.md)
2. Lernziele oben als Checkliste verwenden: Kann ich es erklären (K2) und auf ein Beispiel anwenden (K3)?
3. Spick erstellen und damit die Aufgaben der Transferaufgaben (Tage 1–8) wiederholen
4. An Tag 10 ist am Morgen Zeit für Repetition und offene Fragen
