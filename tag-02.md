# Tag 02 - Werkzeuge & Datenschutzrecht

<details>
  <summary>
	Block: Repetition Tag 1 (~10')
  </summary>

## Repetitionsblock: Was ist von Tag 1 hängen geblieben?

> Sozialform: Einzelarbeit im Plenum (Fragen werden gemeinsam vorgelesen/gezeigt, jede:r beantwortet für sich)
> Dauer: 10min (ca. 6min stilles Beantworten, 4min gemeinsame Auswertung)
> Abgabe: mündlich im Plenum

Beantworten Sie die folgenden 6 Fragen still für sich (auf Papier oder im Lernjournal-Entwurf). Anschliessend werden die Fragen im Plenum reihum aufgelöst.

**Frage 1:** Was ist der Unterschied zwischen Authentifizierung und Autorisierung? Nennen Sie je ein Beispiel.

<details>
  <summary>Lösungshinweis</summary>

Authentifizierung prüft, *wer* jemand ist (z. B. Login mit Passwort). Autorisierung legt fest, *was* diese Person darf (z. B. Zugriff auf bestimmte Ordner). Authentifizierung kommt immer zuerst.

</details>

**Frage 2:** Nennen Sie die drei Faktorenkategorien der Authentifizierung und je ein Beispiel dazu.

<details>
  <summary>Lösungshinweis</summary>

Wissen (z. B. Passwort), Besitz (z. B. Hardware-Token, Smartphone), Biometrie (z. B. Fingerabdruck). MFA kombiniert mindestens zwei *verschiedene* Kategorien.

</details>

**Frage 3:** Was bedeutet das Prinzip "Least Privilege" und warum ist es wichtig?

<details>
  <summary>Lösungshinweis</summary>

Nutzer:innen erhalten nur genau die Rechte, die sie für ihre Aufgabe brauchen – nicht mehr. Das begrenzt den Schaden, falls ein Konto kompromittiert wird oder jemand fahrlässig/böswillig handelt.

</details>

**Frage 4:** Nennen Sie zwei Methoden des Social Engineering und worin sie sich unterscheiden.

<details>
  <summary>Lösungshinweis</summary>

Z. B. Phishing (E-Mail mit gefälschtem Absender/Link) vs. Vishing (Voice Phishing, telefonisch). Beide zielen auf Manipulation und Vertrauensmissbrauch, unterscheiden sich aber im Kanal.

</details>

**Frage 5:** Was macht ein sicheres Passwort aus, und wofür braucht man einen Passwort-Manager?

<details>
  <summary>Lösungshinweis</summary>

Sicher = lang (Passphrase statt kurzes komplexes Passwort), einzigartig pro Dienst, keine offensichtlichen Muster. Ein Passwort-Manager generiert und speichert einzigartige, komplexe Passwörter pro Dienst, sodass man sich nur ein Master-Passwort merken muss.

</details>

**Frage 6:** Wie darf KI gemäss dem KI-Nutzungsrahmen in diesem Modul genutzt werden? Nennen Sie ein Beispiel für "erlaubt" und eines für "nicht erlaubt".

<details>
  <summary>Lösungshinweis</summary>

Erlaubt: Erklärungen einfordern, Rückfragen stellen, Prompt-Übungen/Testdaten generieren lassen. Nicht erlaubt: Lernjournal-Reflexionen von der KI schreiben lassen, KI bei LB1/LB2 nutzen, eigenleistungspflichtige Kernaufgaben durch KI ersetzen.

</details>

</details>


<details>
  <summary>
	Block: Einführung Git/Markdown & LB3 (~55')
  </summary>

→ **[LB3 – Auftrag & Bewertungsraster](lbs/lb3/lb3-auftrag.md)**

### Der Git-Workflow

> 🤖 **Copilot-Agent:** [M231 T02a Git](https://m365.cloud.microsoft/chat/?titleId=T_24e32efa-32ba-1462-2a58-03127fa5ff11&source=embedded-builder) — mit dem TBZ-Konto öffnen und **Start** tippen.

Git verwaltet Änderungen an Dateien in mehreren Schichten. Das folgende Diagramm zeigt den grundlegenden Arbeitsablauf:

```mermaid
flowchart LR
  WD["Working Directory\n(lokale Dateien)"]
  SA["Staging Area\n(Index)"]
  LR["Local Repository\n(.git Ordner)"]
  RR["Remote Repository\n(GitHub / GitLab)"]

  WD -- "git add" --> SA
  SA -- "git commit" --> LR
  LR -- "git push" --> RR
  RR -- "git pull / git clone" --> WD
  LR -- "git checkout" --> WD
```

**Wichtigste Git-Befehle im Überblick:**

| Befehl | Wirkung |
|---|---|
| `git init` | Neues Repository initialisieren |
| `git status` | Zeigt den aktuellen Zustand (geänderte, gestagete Dateien) |
| `git add <datei>` | Datei zur Staging Area hinzufügen |
| `git commit -m "Nachricht"` | Änderungen als Snapshot speichern |
| `git push` | Lokale Commits ins Remote-Repo hochladen |
| `git pull` | Änderungen vom Remote-Repo herunterladen |
| `git log` | Commit-Historie anzeigen |

---

### Markdown-Grundlagen

Markdown ist eine leichtgewichtige Auszeichnungssprache, die in Git-Repositories, Wikis und vielen weiteren Systemen verwendet wird. Die Syntax ist bewusst einfach und lesbar.

**Wichtigste Elemente:**

| Element | Syntax | Darstellung |
|---|---|---|
| Überschrift 1 | `# Titel` | Grösste Überschrift |
| Überschrift 2 | `## Abschnitt` | Zweite Ebene |
| Fett | `**text**` | **text** |
| Kursiv | `*text*` | *text* |
| Link | `[Beschriftung](URL)` | Klickbarer Link |
| Bild | `![Alternativtext](Pfad)` | Eingebettetes Bild |
| Ungeordnete Liste | `- Punkt` | Aufzählungsliste |
| Geordnete Liste | `1. Punkt` | Nummerierte Liste |
| Inline-Code | `` `code` `` | `code` |
| Codeblock | ` ```sprache ` | Syntaxhervorhebung |
| Tabelle | `\| Spalte \| Spalte \|` | Tabelle |
| Zitat | `> Text` | Eingerücktes Zitat |
| Horizontale Linie | `---` | Trennstrich |

**Beispiel einer gut strukturierten Markdown-Datei:**

```markdown
# Mein Lernportfolio M231

## Tag 1 – Zusammenfassung

Heute habe ich gelernt:
- Was Authentifizierung und Autorisierung bedeutet
- Wie Social Engineering funktioniert
- Grundlegende Git-Befehle

### Reflexion

> Was würde ich beim nächsten Mal anders machen?

Ich würde früher mit dem Lernjournal beginnen und Notizen
während der Lektionen strukturierter festhalten.

| Thema | Verstanden? | Offene Fragen |
|---|---|---|
| Auth & Authz | Ja | — |
| Social Engineering | Teilweise | Unterschied Vishing/Pretexting |
```

---

### Qualitäts-Tipps für das Lernjournal

Das Lernjournal ist ein zentrales Bewertungskriterium bei LB3 (8 von 32 Punkten). Es geht nicht um Länge, sondern um **Tiefe der Reflexion** – ein guter Zeitpunkt, das jetzt zu wissen, bevor Sie viele Einträge schreiben.

**Guter Lernjournal-Eintrag (Beispiel):**
> «Heute habe ich verstanden, weshalb MFA mindestens zwei *verschiedene* Faktoren braucht: Zwei Passwörter wären beide „Wissen" und würden bei Phishing gleichzeitig kompromittiert. Praktisch überraschte mich, wie günstig ein Passwort-Manager mit MFA-Schutz bereits ausreicht. Für LB3 möchte ich als nächstes zwei Passwort-Manager vergleichen. Plan: bis Tag 7 Bitwarden und KeePassXC testen.»

**Schwacher Lernjournal-Eintrag (Beispiel):**
> «Heute haben wir Auth und Git gelernt. War interessant. Mache ich morgen weiter.»

**Unterschied – woran erkenne ich einen guten Eintrag?**

| Merkmal | Guter Eintrag | Schwacher Eintrag |
|---|---|---|
| **Konkretheit** | Nennt spezifische Konzepte, Befehle, Beispiele | Bleibt vage und allgemein |
| **Reflexion** | Erklärt, was überraschend/neu/schwierig war und warum | Beschreibt nur, was gemacht wurde |
| **Bezug zur Kompetenzmatrix** | Verknüpft Inhalt mit einer Kompetenz der [Kompetenzmatrix M231](https://www.modulbaukasten.ch/module/231/1/de-DE?title=Datenschutz-und-Datensicherheit-anwenden&tab=2&degree=13d8d40b-6d82-eb11-a812-0022486f6f83) (z. B. «Das betrifft E1I: Passwort-Manager einsetzen») | Kein Bezug zu Lernzielen |
| **Planung** | Konkreter Plan für offene Punkte mit Zeitangabe | Keine oder vage Planung |
| **Eigenständigkeit** | Eigene Gedanken, Fragen, kritische Überlegungen | Zusammenfassung aus Unterlagen |

---

### Mermaid-Challenge: Spaghetti kochen als Flowchart

> Sozialform: Gruppenarbeit (3–4 Personen)
> Dauer: 20min
> Abgabe: Link zur Datei, Vorstellung/Prämierung im Verlauf des Tages

Das Git-Repository haben Sie bereits an Tag 1 für Ihr Lernjournal erstellt und der Lehrperson freigegeben. Sie haben oben im Git-Workflow-Diagramm gesehen, wie ein Ablauf als Mermaid-Flowchart dargestellt wird – jetzt sind Sie dran!

> 📘 **Tutorial:** [Mermaid – Flowchart-Syntax](https://mermaid.js.org/syntax/flowchart.html) (offizielle Dokumentation, Englisch) — die Abschnitte zu Richtung, Formen und Pfeilen genügen; jedes Beispiel lässt sich mit «Run» ausprobieren. Auf Deutsch: [GitHub Docs – Erstellen von Diagrammen](https://docs.github.com/de/get-started/writing-on-github/working-with-advanced-formatting/creating-diagrams).

**Mermaid-Flowchart – die wichtigsten Elemente:**

| Element | Syntax | Bedeutung |
|---|---|---|
| Diagrammblock | ` ```mermaid ` … ` ``` ` | Kennzeichnet den Diagrammcode |
| Richtung | `flowchart TD` / `flowchart LR` | Top-Down bzw. Left-Right |
| Schritt (Rechteck) | `A["Text"]` | normaler Prozessschritt |
| Entscheidung (Raute) | `B{"Frage?"}` | Verzweigung |
| Pfeil | `A --> B` | Ablauf |
| Beschrifteter Pfeil | `A -- "Ja" --> C` | Ablauf mit Bedingung |

1. Bilden Sie eine Gruppe von 3–4 Personen (nach Sitzordnung).
2. Modellieren Sie gemeinsam den Prozess **«Spaghetti kochen»** als Flowchart – mit **mindestens einer Entscheidung/Verzweigung** (z. B. «Wasser am Kochen?», «Spaghetti al dente?», «Sauce fertig?»). Alle Gruppen bearbeiten denselben Prozess – das macht die Diagramme direkt vergleichbar.
3. Entwerft und prüft euer Diagramm im Online-Editor **[mermaid.live](https://mermaid.live/)** – dort seht ihr die Grafik live, ohne committen zu müssen.
4. Legt in **eurem persönlichen Git-Repository** (aus Tag 1) eine neue Datei `mermaid-challenge.md` an und fügt den fertigen Code aus mermaid.live ein – am schnellsten direkt über «Add file» im Browser auf GitHub/GitLab, ohne lokales Klonen.
5. Committet die Datei und gebt den Link im Klassen-Chat/MS Teams ab.

> 🏆 **Prämierung:** Die Lehrperson wählt das kreativste bzw. klarste Diagramm – die Gewinner-Gruppe erhält einen kleinen Preis. Auflösung im Verlauf des Tages.

</details>


<details>
  <summary>
	Block: Datenschutzrecht – Gruppenrecherche & Präsentation (~55')
  </summary>

## Datenschutzrecht: revDSG und DSGVO

### Gruppenrecherche mit Präsentation

> Sozialform: Gruppenarbeit (4 Teams à 4 Personen) → Plenum
> Dauer: 30min Vorbereitung, 25min Präsentationen (5min pro Team)
> Abgabe: keine

Jedes Team erhält eines der Themen A–D und präsentiert es der Klasse in **5 Minuten**.

1. Lesen Sie den Text zu Ihrem Thema.
2. Informieren Sie sich über das Thema. Der Text nennt nur Stichworte; die **Leitfragen** unter
   Ihrem Thema zeigen, was in die Präsentation gehört. Womit Sie sich informieren, entscheiden Sie.
3. Prüfen Sie jede Aussage in der offiziellen Quelle und notieren Sie den **Artikel**.
4. Bereiten Sie die Präsentation vor: die wichtigsten Punkte, ein eigenes Beispiel, zu jeder
   Kernaussage **Artikel und Link** auf die offizielle Quelle.

Weicht der Text von der Quelle ab, gilt die Quelle. Sagen Sie das in der Präsentation.
Präsentiert wird in der Reihenfolge A–D.

**Offizielle Quellen:**

- revDSG (Datenschutzgesetz, SR 235.1): <https://www.fedlex.admin.ch/eli/cc/2022/491/de>
- DSGVO: <https://eur-lex.europa.eu/legal-content/DE/TXT/?uri=CELEX:32016R0679>
- EDÖB: <https://www.edoeb.admin.ch/de>

#### Thema A: Schweizer Datenschutzgesetz (revDSG) – Grundsätze

Das revidierte **Datenschutzgesetz (revDSG)** ist seit dem 1. September 2023 in Kraft.

| Grundsatz | Bedeutung |
|---|---|
| **Rechtmässigkeit** | Datenbearbeitung braucht eine Rechtsgrundlage oder Einwilligung |
| **Verhältnismässigkeit** | Nur so viele Daten erheben wie nötig (Datensparsamkeit) |
| **Zweckbindung** | Daten nur für den angegebenen Zweck verwenden |
| **Richtigkeit** | Daten müssen korrekt und aktuell sein |
| **Datensicherheit** | Angemessene technische und organisatorische Massnahmen |
| **Transparenz** | Betroffene müssen informiert werden |

**Leitfragen:**

- In welchem Artikel stehen die Grundsätze, und stimmen sie mit der Tabelle überein?
- Was bedeuten Verhältnismässigkeit und Zweckbindung, wenn Ihr Lehrbetrieb ein Kontaktformular
  für Kundinnen und Kunden erstellt?
- Braucht ein privates Unternehmen für jede Datenbearbeitung eine Einwilligung?

#### Thema B: Besonders schützenswerte Personendaten

**Besonders schützenswerte Personendaten (Art. 5 lit. c revDSG):**

- Religiöse, weltanschauliche, politische oder gewerkschaftliche Ansichten oder Tätigkeiten
- Gesundheit, Intimsphäre, Zugehörigkeit zu einer Rasse oder Ethnie
- Genetische Daten
- Biometrische Daten, die eine Person eindeutig identifizieren
- Daten über verwaltungs- und strafrechtliche Verfolgungen oder Sanktionen
- Daten über Massnahmen der sozialen Hilfe

Für diese Datenkategorien gelten strengere Anforderungen (z. B. ausdrückliche Einwilligung,
höheres Schutzniveau) als für gewöhnliche Personendaten.

**Leitfragen:**

- Was gilt für besonders schützenswerte Personendaten anders als für gewöhnliche Personendaten?
- Welche Daten in Ihrem Lehrbetrieb gehören dazu, zum Beispiel in der Personalabteilung?
- Wann muss eine Einwilligung ausdrücklich sein?

#### Thema C: DSGVO-Betroffenenrechte & Vergleich revDSG/DSGVO

Die **DSGVO** gilt auch für Unternehmen ausserhalb der EU, wenn sie **Personen in der EU** Waren oder
Dienstleistungen anbieten oder deren Verhalten beobachten (Marktortprinzip). Massgebend ist, wo sich
die Person befindet, nicht ihre Staatsangehörigkeit.

**Betroffenenrechte (Auswahl):**

| Recht | Bedeutung |
|---|---|
| Auskunftsrecht | Ich kann fragen, welche Daten über mich gespeichert sind |
| Recht auf Berichtigung | Falsche Daten müssen korrigiert werden |
| Recht auf Löschung | «Recht auf Vergessenwerden» |
| Recht auf Datenübertragbarkeit | Daten in maschinenlesbarem Format herausgeben |
| Widerspruchsrecht | Gegen bestimmte Datenbearbeitungen widersprechen |

**Vergleich revDSG vs. DSGVO:**

| Aspekt | revDSG (CH) | DSGVO (EU) |
|---|---|---|
| Geltungsbereich | Schweiz | EU / EWR |
| In Kraft | 01.09.2023 | 25.05.2018 |
| Bussen | bis CHF 250'000, gegen die verantwortliche natürliche Person | bis € 20 Mio. oder 4 % des weltweiten Jahresumsatzes, gegen das Unternehmen |
| Datenschutzberater/-beauftragter | für private Unternehmen freiwillig (Datenschutzberater) | Pflicht für Behörden und für Unternehmen, deren Kerntätigkeit umfangreiche Überwachung oder die umfangreiche Bearbeitung besonders sensibler Daten ist |
| Auskunftsrecht | Ja | Ja |

**Leitfragen:**

- Wann gilt die DSGVO für ein Unternehmen in der Schweiz? Nennen Sie ein Beispiel.
- Welche der Betroffenenrechte gibt es auch im revDSG, und in welchem Artikel?
- Wen trifft eine Busse nach revDSG, wen nach DSGVO, und was bedeutet das für Mitarbeitende?

#### Thema D: Meldepflicht bei Datenpannen – der Prozess

Wenn Personendaten unbefugt offenbart, verändert, gelöscht werden oder verloren gehen, liegt eine
Verletzung der Datensicherheit vor. Der folgende Prozess zeigt, was zu tun ist:

```mermaid
flowchart TD
  A["Datenpanne erkannt\n(Verlust, Zugriff, Veröffentlichung\nvon Personendaten)"]
  B{"Ist die Panne\nmeldepflichtig?\nrevDSG: voraussichtlich hohes Risiko\nDSGVO: ausser voraussichtlich kein Risiko"}
  C["Meldung\nrevDSG: an den EDÖB so rasch als möglich\nDSGVO: an die Aufsichtsbehörde\nmöglichst innert 72 Stunden"]
  D["Betroffene informieren\nrevDSG: wenn zu ihrem Schutz erforderlich\noder vom EDÖB verlangt\nDSGVO: bei voraussichtlich hohem Risiko"]
  E["Massnahmen ergreifen\nLücke schliessen, Schäden\nbegrenzen, Forensik"]
  F["Intern dokumentieren\nVorfall aufzeichnen,\nkeine externe Meldung nötig"]
  G["Nachkontrolle\nMassnahmen prüfen,\nWiederholung verhindern"]

  A --> B
  B -- "Ja" --> C
  C --> D
  D --> E
  E --> G
  B -- "Nein" --> F
  F --> G
```

> **EDÖB** = Eidgenössischer Datenschutz- und Öffentlichkeitsbeauftragter (www.edoeb.admin.ch)

**Leitfragen:**

- Wann ist eine Datenpanne nach revDSG meldepflichtig, wann nach DSGVO?
- Wem muss gemeldet werden, und bis wann?
- Wann müssen die betroffenen Personen selbst informiert werden?

---

**Zum Nachlernen (LB1):** 🤖 Copilot-Agent [M231 T02c Datenschutzrecht](https://m365.cloud.microsoft/chat/?titleId=T_140832fa-9dd9-a241-e6ca-c5b466e7a0a3&source=embedded-builder) — mit dem TBZ-Konto öffnen und **Start** tippen. Er führt Schritt für Schritt durch revDSG und DSGVO.

*(Die Themen "Datenschutz vs. Datensicherheit" und die Transferaufgabe zum Auskunftsbegehren folgen an Tag 3.)*

</details>


<details>
  <summary>
	Block: Arbeit am Lernjournal (~45')
  </summary>

## Arbeit am Lernjournal

Nach den Qualitäts-Tipps aus dem Block «Einführung Git/Markdown & LB3» (gut vs. schwacher Eintrag) folgt nun betreute Arbeitszeit: Sie schreiben/überarbeiten Ihre Lernjournal-Einträge zu Tag 1 und Tag 2, tauschen sich mit einer Partnerin/einem Partner aus und erhalten Feedback anhand der Kriterientabelle.

> Sozialform: Einzelarbeit → Partnerarbeit → Plenum
> Dauer: ~45min, restliche Zeit (5min Repo-/Struktur-Check, 25min Schreibarbeit, 10min Peer-Feedback, 5min Abschlussreflexion)
> Abgabe: Lernjournal-Einträge Tag 1 & Tag 2 im persönlichen Git-Repo committet

---

### Repo- und Struktur-Check (5')

> Sozialform: Einzelarbeit, Lehrperson im Rundgang
> Dauer: 5min

1. Öffnen Sie Ihr persönliches Lernjournal-Repository.
2. Prüfen Sie: Ist die Struktur nachvollziehbar (z. B. eine Datei/ein Abschnitt pro Tag)? Ist die `mermaid-challenge.md` aus dem Vormittag committet?
3. Die Lehrperson geht kurz durch die Reihen und beantwortet offene technische Fragen (Markdown, Git-Befehle).

---

### Schreibarbeit (25')

> Sozialform: Einzelarbeit
> Dauer: 25min

Schreiben oder überarbeiten Sie Ihre Lernjournal-Einträge zu **Tag 1** und **Tag 2**. Orientieren Sie sich an den Qualitäts-Tipps von vorhin:

- Konkrete Konzepte, Befehle und Beispiele statt vager Aussagen
- Reflexion: Was war neu, überraschend oder schwierig – und warum?
- Bezug zur [Kompetenzmatrix M231](https://www.modulbaukasten.ch/module/231/1/de-DE?title=Datenschutz-und-Datensicherheit-anwenden&tab=2&degree=13d8d40b-6d82-eb11-a812-0022486f6f83) herstellen (z. B. A1B, E1I), wo passend
- Offene Punkte mit konkretem Plan und Zeitangabe festhalten

Nutzen Sie dazu insbesondere die heutigen Themen: Git/Markdown, Datenschutzrecht (Gruppenrecherche und Präsentationen).

---

### Peer-Feedback (10')

> Sozialform: Partnerarbeit
> Dauer: 10min
> Abgabe: mündliches Feedback an Partner:in

Tauschen Sie Ihr Lernjournal (Bildschirm oder Link) mit einer Sitznachbarin / einem Sitznachbarn:
1. Lesen Sie den Eintrag Ihres Gegenübers.
2. Geben Sie anhand der Kriterientabelle (Konkretheit, Reflexion, Bezug zur Kompetenzmatrix, Planung, Eigenständigkeit) mündlich Feedback: Was ist bereits stark? Was könnte vertieft werden?
3. Notieren Sie sich selbst mindestens einen Verbesserungspunkt aus dem erhaltenen Feedback.

---

### Abschlussreflexion (5')

> Sozialform: Einzelarbeit → Plenum
> Dauer: 5min

Ergänzen Sie Ihren Eintrag um den Verbesserungspunkt aus dem Peer-Feedback. Im Plenum: Wer möchte eine besonders gelungene Formulierung oder einen Aha-Moment teilen?

</details>
