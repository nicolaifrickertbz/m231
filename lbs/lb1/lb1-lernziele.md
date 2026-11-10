# LB1 — Theorieprüfung 1: Lernziele & Vorbereitung

## Prüfungsinformationen

| | |
|---|---|
| **Termin** | Tag 5 (22.09.2025) |
| **Dauer** | 45 Minuten |
| **Format** | Computer, Safe Exam Browser (SEB) – Moodle |
| **Erlaubte Hilfsmittel** | Keine |
| **Stoff** | Tag 1–4 |

> Die Vorbereitung erfolgt **im Selbststudium** anhand dieses Dokuments – in Tag 5 selbst ist keine Vorbereitungszeit mehr eingeplant, es findet direkt die Prüfung statt. Zur Übung steht ausserdem eine **Moodle-Probeprüfung** (9 Fragen, gleicher Stil) zur Verfügung.

---

## Lernziele

Nach der Vorbereitung können Sie:

**Authentifizierung & Autorisierung**
- Authentifizierung und Autorisierung unterscheiden, die drei Faktorenkategorien erklären und MFA korrekt abgrenzen (K1/K2)
- anhand eines Praxisbeispiels beurteilen, ob eine Anmeldung MFA-Anforderungen bzw. dem Least-Privilege-Prinzip entspricht (K3)

**Social Engineering & Passwortsicherheit**
- mindestens drei Social-Engineering-Methoden benennen und erklären, weshalb eine Passphrase sicherer ist als ein kurzes komplexes Passwort (K1/K2)
- für ein Fallbeispiel eine angemessene Reaktion auf einen Social-Engineering-Versuch ableiten (K3)

**Datenschutzrecht (revDSG & DSGVO)**
- Inkrafttretensdatum des revDSG und Geltungsbereich der DSGVO (Marktortprinzip) nennen und erklären (K1/K2)
- für ein Szenario mit Datenpanne die korrekten gesetzlichen Meldepflichten ableiten (K3)

**CIA-Triade**
- die drei Ziele der CIA-Triade benennen (K1)
- einem konkreten Vorfall das primär verletzte CIA-Ziel zuordnen und begründen (K2/K3)

**Datenschutz vs. Datensicherheit**
- erklären, wodurch Datenschutz und wodurch Datensicherheit primär geregelt werden (K1/K2)
- ein Szenario beurteilen, ob Datenschutz, Datensicherheit oder beides verletzt ist (K3)

**Online-Anonymität & Datenschutztools**
- die Funktionsweise von VPN und Tor beschreiben (K1/K2)
- die Grenzen dieser Tools (z. B. Exit-Node, VPN-Anbieter selbst) an einem Beispiel erklären (K3)

**Lizenzmodelle & Urheberrecht/Creative Commons**
- die Bedeutung der CC-Kürzel BY, SA, NC, ND nennen und permissive von Copyleft-Lizenzen unterscheiden (K1/K2)
- für ein gegebenes Szenario die passende Lizenz auswählen und begründen (K3)

**Privacy-Threats (Cookies, Tracking, Fingerprinting)**
- Cookie-Typen unterscheiden und erklären, weshalb Fingerprinting schwerer zu blockieren ist als Cookies (K1/K2)
- in einem Szenario die verwendete Tracking-Methode identifizieren (K3)

**Dark Patterns**
- mindestens drei Dark Patterns benennen und beschreiben (K1)
- ein UI-Beispiel einem Dark Pattern zuordnen und die Manipulationswirkung erklären (K2/K3)

> Symmetrische/asymmetrische Verschlüsselung, PKI und Häufigkeitsanalyse (Tag 6/7) sind **nicht** Teil von LB1 – dieser Stoff wird bei **LB2** geprüft. Git/Markdown (Tag 2) ist ebenfalls **nicht** Teil von LB1 – es wird über LB3 bewertet.

---

## Kurzrepetition der Kernbegriffe

#### Authentifizierung & Autorisierung (Tag 1)
Authentifizierung = Wer bist du? / Autorisierung = Was darfst du? · Faktoren: Wissen, Besitz, Biometrie · MFA = mind. 2 **verschiedene** Faktoren · Least Privilege = nur die Rechte, die für die Aufgabe nötig sind

#### Social Engineering & Passwortsicherheit (Tag 1)
Phishing, Spear Phishing, Vishing, Pretexting, Baiting · gutes Passwort: ≥12 Zeichen, einzigartig · Passphrasen: lang & merkbar

#### Datenschutzrecht (Tag 2)
revDSG (CH) seit 01.09.2023 · DSGVO (EU) gilt via Marktortprinzip auch für CH-Firmen · besonders schützenswerte Daten (Gesundheit, Religion, Biometrie, …) · Meldepflicht Datenpanne: 72h an EDÖB

#### CIA-Triade & Datenschutz vs. Datensicherheit (Tag 3)
Confidentiality/Integrity/Availability · Datenschutz = rechtlich/ethisch (Gesetze) · Datensicherheit = technisch/organisatorisch (Massnahmen) · Datensicherheit ist Voraussetzung, aber kein Ersatz für Datenschutz

#### Online-Anonymität & Datenschutztools (Tag 3)
VPN: verschlüsselt zum VPN-Server, Anbieter selbst sieht Traffic · Tor: 3 Knoten, Exit-Node sieht Klartext ohne HTTPS · Fingerprinting: Tracking ohne Cookies

#### Lizenzmodelle & Urheberrecht (Tag 4)
Proprietär vs. Open Source · Copyleft (GPL) vs. permissiv (MIT, Apache) · CC: BY (Namensnennung), SA (Share Alike), NC (nicht-kommerziell), ND (keine Bearbeitung)

#### Privacy-Threats & Dark Patterns (Tag 4)
Third-Party-Cookies = Tracking über Seiten hinweg · Fingerprinting = Kombination Browser-Merkmale · Dark Patterns: Roach Motel, Confirmshaming, Hidden Costs, Urgency/Scarcity

---

## Selbsttest

Beantworten Sie die folgenden Fragen ohne Unterlagen und vergleichen Sie danach mit der Kurzrepetition oben.

1. Was prüft die Authentifizierung, was die Autorisierung? Nennen Sie je ein Beispiel.
2. Was bedeutet «Least Privilege» und warum ist es wichtig?
3. Nennen Sie drei Social-Engineering-Methoden und je eine konkrete Schutzmassnahme.
4. Was macht eine Passphrase gegenüber einem kurzen, komplexen Passwort sicherer?
5. Was ist der zentrale Unterschied im Geltungsbereich zwischen revDSG und DSGVO?
6. Nennen Sie die drei Ziele der CIA-Triade und je ein Beispiel für eine Verletzung.
7. Erklären Sie den Unterschied zwischen Datenschutz und Datensicherheit an einem Beispiel.
8. Warum schützt ein VPN nicht vor dem VPN-Anbieter selbst?
9. Was bedeutet «Copyleft» bei einer Open-Source-Lizenz wie der GPL v3?
10. Nennen Sie zwei Dark Patterns und beschreiben Sie kurz, wie sie Nutzer:innen manipulieren.
