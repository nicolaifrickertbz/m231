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
	Block: Einführung Git/Markdown & LB3 (~35')
  </summary>

→ **[LB3 – Auftrag & Bewertungsraster](lbs/lb3/lb3-auftrag.md)**

### Der Git-Workflow

> 🤖 **Copilot-Agent:** [M231 T02a Git & Markdown](https://m365.cloud.microsoft/chat/?titleId=T_24e32efa-32ba-1462-2a58-03127fa5ff11&source=embedded-builder) — mit dem TBZ-Konto öffnen und **Start** tippen.

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

### Mermaid-Challenge: Spaghetti kochen als Flowchart

> Sozialform: Gruppenarbeit (3–4 Personen)
> Dauer: 10min
> Abgabe: Link zur Datei, Vorstellung/Prämierung im Verlauf des Tages

Das Git-Repository haben Sie bereits an Tag 1 für Ihr Lernjournal erstellt und der Lehrperson freigegeben. Sie haben oben im Git-Workflow-Diagramm gesehen, wie ein Ablauf als Mermaid-Flowchart dargestellt wird – jetzt sind Sie dran!

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
| **Bezug zu Handlungszielen** | Verknüpft Inhalt mit HZ (z. B. «Das betrifft HZ 2.3: MFA») | Kein Bezug zu Lernzielen |
| **Planung** | Konkreter Plan für offene Punkte mit Zeitangabe | Keine oder vage Planung |
| **Eigenständigkeit** | Eigene Gedanken, Fragen, kritische Überlegungen | Zusammenfassung aus Unterlagen |

</details>


<details>
  <summary>
	Block: Datenschutzrecht – Agent & Recherche (~65')
  </summary>

## Datenschutzrecht: revDSG und DSGVO

> 🤖 **Copilot-Agent:** [M231 T02b Datenschutzrecht](https://m365.cloud.microsoft/chat/?titleId=T_140832fa-9dd9-a241-e6ca-c5b466e7a0a3&source=embedded-builder) — mit dem TBZ-Konto öffnen und **Start** tippen.

> Sozialform: Einzelarbeit
> Dauer: ~30min
> Abgabe: keine — der Agent meldet «FERTIG»

Der Agent führt Sie durch das Schweizer Datenschutzgesetz (revDSG) und die DSGVO: Grundsätze,
besonders schützenswerte Personendaten, Betroffenenrechte und die Meldepflicht bei Datenpannen.
Arbeiten Sie ihn durch, **bevor** Sie mit der Recherche beginnen — ohne die Begriffe finden Sie im
Gesetzestext wenig.

---

### Recherche: Datenpanne im Treuhandbüro

> Sozialform: Einzelarbeit
> Dauer: ~35min
> Abgabe: MS-Teams Assignment

**Ausgangslage:** Ein Treuhandbüro in Winterthur betreut rund 400 Kunden. Gestern hat es bemerkt,
dass Unbekannte auf die Kundendatenbank zugegriffen haben. Darin stehen Namen, Adressen,
AHV-Nummern und Steuerunterlagen. Ob die Daten kopiert wurden, ist noch unklar. Etwa 30 Kunden
wohnen in Deutschland, das Büro betreut sie seit Jahren.

Beantworten Sie die vier Fragen. Belegen Sie **jede Antwort mit dem Gesetzesartikel und einem Link
auf die offizielle Quelle**. KI dürfen Sie beim Suchen nutzen. Was zählt, ist der Beleg im
Gesetzestext, nicht die Aussage der KI.

1. Gilt für diesen Fall das **revDSG**? Gilt die **DSGVO**? Begründen Sie beides.
2. Muss das Büro die Panne **melden**? Wem, unter welcher Bedingung und in welcher Frist — nach
   revDSG und nach DSGVO?
3. Müssen die **Kunden informiert** werden? Unter welcher Bedingung — nach revDSG und nach DSGVO?
4. Sind **Steuerunterlagen** besonders schützenswerte Personendaten im Sinne des revDSG? Was folgt
   daraus für die Beurteilung des Risikos?

**Pro Frage:** Antwort in 2–4 Sätzen · Artikel · Link.

**Offizielle Quellen:**

- revDSG (Datenschutzgesetz, SR 235.1): <https://www.fedlex.admin.ch/eli/cc/2022/491/de>
- DSGVO: <https://eur-lex.europa.eu/legal-content/DE/TXT/?uri=CELEX:32016R0679>
- EDÖB: <https://www.edoeb.admin.ch/de>

Einzelne Abgaben werden am Schluss im Plenum besprochen.

*(Die Themen "Datenschutz vs. Datensicherheit" und die Transferaufgabe zum Auskunftsbegehren folgen an Tag 3.)*

</details>


<details>
  <summary>
	Block: Arbeit am Lernjournal (~75')
  </summary>

## Arbeit am Lernjournal

Nach den Qualitäts-Tipps aus dem Git/Markdown-Block (gut vs. schwacher Eintrag) folgt nun betreute Arbeitszeit: Sie schreiben Ihre Lernjournal-Einträge zu Tag 1 und Tag 2, tauschen sich mit einer Partnerin/einem Partner aus und erhalten Feedback anhand der Kriterientabelle.

> Sozialform: Einzelarbeit → Partnerarbeit → Plenum
> Dauer: 75min (10min Repo-/Struktur-Check, 40min Schreibarbeit, 15min Peer-Feedback, 10min Abschlussreflexion)
> Abgabe: Lernjournal-Einträge Tag 1 & Tag 2 im persönlichen Git-Repo committet

---

### Repo- und Struktur-Check (10')

> Sozialform: Einzelarbeit, Lehrperson im Rundgang
> Dauer: 10min

1. Öffnen Sie Ihr persönliches Lernjournal-Repository.
2. Prüfen Sie: Ist die Struktur nachvollziehbar (z. B. eine Datei/ein Abschnitt pro Tag)? Ist die `mermaid-challenge.md` aus dem Vormittag committet?
3. Die Lehrperson geht kurz durch die Reihen und beantwortet offene technische Fragen (Markdown, Git-Befehle).

---

### Schreibarbeit (40')

> Sozialform: Einzelarbeit
> Dauer: 40min

Schreiben oder überarbeiten Sie Ihre Lernjournal-Einträge zu **Tag 1** und **Tag 2**. Orientieren Sie sich an den Qualitäts-Tipps von vorhin:

- Konkrete Konzepte, Befehle und Beispiele statt vager Aussagen
- Reflexion: Was war neu, überraschend oder schwierig – und warum?
- Bezug zu Handlungszielen (HZ) herstellen, wo passend
- Offene Punkte mit konkretem Plan und Zeitangabe festhalten

Nutzen Sie dazu insbesondere die heutigen Themen: Git/Markdown, Datenschutzrecht (Agent und Recherche).

---

### Peer-Feedback (15')

> Sozialform: Partnerarbeit
> Dauer: 15min
> Abgabe: mündliches Feedback an Partner:in

Tauschen Sie Ihr Lernjournal (Bildschirm oder Link) mit einer Sitznachbarin / einem Sitznachbarn:
1. Lesen Sie den Eintrag Ihres Gegenübers.
2. Geben Sie anhand der Kriterientabelle (Konkretheit, Reflexion, Bezug zu HZ, Planung, Eigenständigkeit) mündlich Feedback: Was ist bereits stark? Was könnte vertieft werden?
3. Notieren Sie sich selbst mindestens einen Verbesserungspunkt aus dem erhaltenen Feedback.

---

### Abschlussreflexion (10')

> Sozialform: Einzelarbeit → Plenum
> Dauer: 10min

Ergänzen Sie Ihren Eintrag um den Verbesserungspunkt aus dem Peer-Feedback. Im Plenum: Wer möchte eine besonders gelungene Formulierung oder einen Aha-Moment teilen?

</details>
