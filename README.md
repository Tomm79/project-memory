# Projektgedächtnis für Codex-Projekte mit lokalem Arbeitsordner

*Für Menschen, die mit Codex im Dialog über längere Zeit zusammenhängende Texte, Vorlagen, Konzepte oder Software entwickeln und für die nächste Aufgabe frühere Überlegungen wieder brauchen – weil der **aktuelle Arbeitsstand allein die Vorgeschichte oft nicht mehr erklärt**.*

Erschließt und pflegt wichtige Originalstellen in Gesprächen und Dokumenten, damit spätere Chats auf dem entstandenen Projektwissen aufbauen können. Besonders sinnvoll für länger laufende Ausarbeitungen und Projekte, in denen eine gemeinsame Grundlage entwickelt, wiederholt angewendet und weiter verbessert wird.

> [!Schnellstart: Installation und Einrichtung]
>
> Den Skill einmal installieren, anschließend das Gedächtnis im gewünschten Projekt einrichten:
>
> **1. Installieren.** Diese Anweisung in einem lokalen Codex-Chat der ChatGPT-App senden, in dem `skill-installer` verfügbar ist:
>
> ```text
> $skill-installer install https://github.com/Tomm79/project-memory/tree/main/project-memory
> ```
>
> **2. Im Projekt einrichten.** Nach erfolgreicher Installation das gewünschte Codex-Projekt mit lokalem Arbeitsordner öffnen und dort diese Anweisung senden:
>
> ```text
> $project-memory Richte das Projektgedächtnis im aktuellen Projekt-Arbeitsordner ein.
> ```
>
> Danach gelten die Gedächtnisregeln auch in weiteren Chats dieses Projekts. [Ausführliche Anleitung](#installation-und-erste-einrichtung).

Eine typische Situation: „Die Ergebnisse sind vorhanden, aber für die nächste Aufgabe brauche ich auch wieder die Überlegungen dahinter.“ Vielleicht ist eine Gliederung bereits ausgearbeitet oder eine Vorlage fertig, doch für ihre Weiterentwicklung werden eine frühere Begründung, ein Einwand oder ein zurückgestellter Entwurf wieder wichtig. Kurze Gedächtniseinträge erklären, welche Originalstellen dafür relevant sind, und führen zum passenden Zusammenhang.

Der Skill richtet das Gedächtnis auf ausdrücklichen Auftrag ein und regelt anschließend Aufnahme, Abruf und laufende Pflege. Auch relevante Inhalte, die noch keinen Platz in einer ausgearbeiteten Projektdokumentation gefunden haben, werden erschlossen. Das Gedächtnis soll zur Quelle führen, statt ganze Gespräche oder Ausarbeitungen nochmals zusammenzufassen.

Das Gedächtnis gehört zum jeweiligen Projekt. Ein für mehrere Projekte verfügbarer Skill führt deren Inhalte nicht zusammen. Der Bestand liegt im Arbeitsordner unter `project-memory/`; die Projektanweisungen binden den Skill ein. Normale Dateiwerkzeuge und gegebenenfalls lokales Git genügen. Der Skill installiert keine Software.

Der technische Skillname ist `project-memory`; mit diesem Namen wird der Skill installiert und aufgerufen. Der Anzeigename in Codex ist „Projektgedächtnis für Projekte im Dialog – mit lokalem Arbeitsordner“.

## Voraussetzungen und Einsatzbereich

Für den Betrieb gelten folgende Voraussetzungen und Empfehlungen:

| Bereich | Voraussetzung oder Empfehlung |
| --- | --- |
| App | Empfohlen ist eine aktuelle Version der ChatGPT-Desktop-App mit Codex und Unterstützung für [lokale Skills](https://learn.chatgpt.com/docs/build-skills). Für die beschriebene Installation muss `skill-installer` verfügbar sein. |
| Projekt | Ein [lokales Codex-Projekt](https://learn.chatgpt.com/docs/projects) mit dauerhaft verfügbarem Arbeitsordner. |
| Zugriffsrechte | Codex muss die Projektdateien lesen und bearbeiten, gewöhnliche lokale Dateioperationen ausführen und die Projektanweisungen in `AGENTS.md` verwenden können. |
| Betriebssystem | Windows ist praktisch erprobt. Die macOS-Erprobung steht noch aus. |
| Modell und Denkaufwand | **Empfohlen und praktisch erprobt: GPT-6.1 Sol mit Denkaufwand `high`.** |
| Git – optional | Ohne Git im Arbeitsordner werden Kopiensicherungen verwendet. Ist der Arbeitsordner bereits mit Git versioniert, muss Git für lokale Sicherungscommits nutzbar sein. [Details zur Git-Nutzung](#git-im-projekt-arbeitsordner). |
| Originalquellen | Dokumente und frühere Chats müssen für Codex erreichbar sein. Der Skill nutzt vorhandene Chatzugänge; bei fehlendem Zugang kann ein begrenzter Originalauszug die benötigte Stelle erhalten. |
| Regelmäßiger Check – optional | Benötigt eine verfügbare Automatisierungsfunktion für einen eigenen lokalen Projektchat und deine Freigabe. Für [lokale automatische Läufe](https://learn.chatgpt.com/docs/automations?surface=app) müssen Rechner und App laufen. Die gewöhnliche Nutzung funktioniert auch ohne diesen Check. |

GPT-6.1 Sol mit `high` ist die erprobte Empfehlung; ein technisches Modell-Minimum ist nicht festgelegt. GPT-6 Luna mit `medium` wird nach den bisherigen Vergleichstests für selbstständige Quellenkuratierung und Pflege nicht empfohlen.

Für den normalen Betrieb sind keine zusätzlichen Hilfsprogramme oder Datenbanken erforderlich. Andere Agenten und Cloud-Arbeitsumgebungen gehören nicht zum derzeit entwickelten Einsatzbereich.

## Wofür eignet sich das Projektgedächtnis?

Besonders hilfreich ist das Verfahren, wenn ein Ergebnis über mehrere Chats entsteht und später weiterbearbeitet oder als Grundlage für weitere Dokumente verwendet wird. Im fertigen Dokument steht häufig das Ergebnis; die Gründe, verworfenen Varianten und noch offenen Überlegungen liegen dagegen in früheren Gesprächen oder Ausarbeitungen.

| Anwendungsfall | Was ein späterer Chat wiederfinden soll |
| --- | --- |
| Essays, Bücher und Veröffentlichungsreihen | Argumentative Absicht, frühere Gliederungen und Formulierungen sowie zurückgestellte Gedanken, an denen die nächste Überarbeitung anknüpft. |
| Vertragsvorlagen und konkrete Verträge | Die Überlegungen hinter der Vorlage, ihre Weiterentwicklung und die Gründe für Anpassungen, die ausschließlich zu einem bestimmten Fall gehören. |
| Angebote und Leistungsbeschreibungen | Die gemeinsame Leistungsgrundlage, ihre Abgrenzungen und die ursprünglichen Anforderungen hinter kundenspezifischen Varianten. |
| Rechercheberichte und Konzeptbewertungen | Relevante Quellenpassagen, Gegenargumente und noch offene Interpretationen samt dem Zusammenhang ihrer bisherigen Bewertung. |
| Schulungen und Unterrichtsmaterialien | Didaktische Gründe für Aufbau und Beispiele sowie Rückmeldungen, die eine Überarbeitung oder Zielgruppenvariante ausgelöst haben. |
| Produkt-, Kommunikations- und Organisationskonzepte | Die Abwägungen hinter gemeinsamen Vorgaben, auf denen Website-Texte, Präsentationen, Handbücher oder weitere Ausarbeitungen aufbauen. |
| Softwareentwicklung | Architekturentscheidungen, frühere Lösungsversuche und Einschränkungen, deren Begründung für eine spätere Änderung wichtig ist. |

Ein typischer Ablauf: Eine Vorlage wird im Dialog entwickelt, in zwei unterschiedlichen Fällen angewendet und danach in einem neuen Chat überarbeitet. Das Gedächtnis erschließt die ursprünglichen Gründe und die fallbezogenen Abweichungen. Der neue Chat kann dadurch prüfen, welche Erkenntnis zur allgemeinen Vorlage gehört und welche Besonderheit nur für einen Einzelfall gilt.

Die Beispiele zeigen, für welche Arbeitsmuster der Skill gedacht ist. Die bisherigen Praxisprüfungen betreffen vor allem Essayarbeit und Quellenabruf; die weiteren Anwendungsfälle sind noch zu erproben.

## Wie erschließt das Projektgedächtnis den Zusammenhang hinter den Ergebnissen?

Entscheidungsjournale, Konzepte und Bewertungen halten fachliche Inhalte und häufig auch ihre Begründungen fest. Diese Dokumente können selbst die maßgeblichen Quellen sein. Das Projektgedächtnis erschließt die für eine spätere Aufgabe wichtigen Stellen darin; eine zusätzliche ausführliche Kopie der Bewertung oder des Konzepts ist dafür nicht nötig.

Manchmal wird eine Überlegung wieder gebraucht, die im fertigen Ergebnis keinen Platz gefunden hat: Warum wurde eine Alternative verworfen? Welche Frage blieb offen? Galt eine Anpassung nur für einen bestimmten Fall? Wenn der passende Zusammenhang in einem früheren Gespräch oder einer weiteren Ausarbeitung liegt, führt der Gedächtniseintrag auch dorthin.

Der zusätzliche Nutzen liegt in der laufenden Auswahl und Pflege dieser Zugänge über die verschiedenen Quellen hinweg. Aktuelle Arbeitsdateien bleiben die Grundlage der Ausarbeitung. Ein Eintrag kann auch einen unbestätigten Entwurf erschließen; seine Aufnahme bedeutet keine Zustimmung des Nutzers.

## Wann ist der Zusatznutzen geringer?

Bei kurzen Einzelaufgaben oder einem kleinen, gut gegliederten und aktuell gehaltenen Dokumentbestand reicht oft die vorhandene Dokumentation. Gedächtnisabruf, Pflege und Sicherung verursachen ebenfalls Aufwand. Je seltener frühere Gespräche oder verteilte Quellen wieder benötigt werden, desto geringer ist der erwartbare Nutzen.

Wichtige Originalquellen müssen tatsächlich erreichbar sein. Der Skill nutzt vorhandene Chatzugänge; er stellt selbst keinen zusätzlichen Zugang bereit. Bei fehlendem Zugang kann ein begrenzter Originalauszug helfen. Das Verfahren bietet keine automatische Synchronisierung zwischen Rechnern und keine technisch erzwungene Projektisolierung. Weniger wiederholte Erklärung und gezieltere Suche sind Ziele; eine allgemeine Zeit- oder Tokenersparnis ist bislang nicht gemessen.

## Installation und erste Einrichtung

Die Installation macht den Skill für lokale Codex-Chats verfügbar. Erst ein weiterer Auftrag richtet das Gedächtnis in einem bestimmten Projekt ein. Eine Installation allein verändert keine Projekt-Arbeitsordner und führt keine Projektinhalte zusammen.

### 1. Skill installieren

Verwende einen lokalen Codex-Chat in der ChatGPT-App, in dem `skill-installer` verfügbar ist. Sende diese Anweisung:

```text
$skill-installer install https://github.com/Tomm79/project-memory/tree/main/project-memory
```

Der Auftrag installiert den aktuellen Stand aus dem Branch `main`. Nach erfolgreicher Installation steht der Skill im nächsten Chat-Turn zur Verfügung.

### 2. Gedächtnis im Zielprojekt einrichten

Öffne das gewünschte Codex-Projekt mit seinem Arbeitsordner. Beauftrage dort die Einrichtung:

```text
$project-memory Richte das Projektgedächtnis im aktuellen Projekt-Arbeitsordner ein.
```

Der Skill richtet den Gedächtnisordner und die passende Sicherung ein und ergänzt die Projektanweisungen in `AGENTS.md`. Bestehende Anweisungen bleiben erhalten; ein vorhandenes, eindeutig zugeordnetes Gedächtnis wird weiterverwendet. Bei der Sicherung durch Kopien wird die Aufbewahrungsregel erklärt und zur Freigabe vorgelegt.

Nach erfolgreicher Einrichtung gelten die Gedächtnisregeln auch in weiteren Chats des Projekts. Vor Änderungen an den Projektregeln müssen andere laufende Chats abgeschlossen oder ihre Gedächtniszugriffe geklärt sein. Bei gewöhnlicher Projektarbeit musst du `$project-memory` anschließend nicht jedes Mal ausdrücklich nennen.

## Nutzung und Pflege

Codex hält kurze Einträge mit Hinweisen auf wichtige Gesprächs- und Dokumentstellen aktuell und greift bei späteren Aufgaben auf diese Quellen zurück. Dafür ist keine zusätzliche vollständige Belegablage nötig. Ist ein Originalchat nicht erreichbar, kann ein begrenzter Originalauszug die benötigte Stelle erhalten.

Laufende Inhaltspflege gehört zur normalen Arbeit: Einträge und Index verbessern, Doppelungen beheben und Fundstellen prüfen. Änderungen an Funktion, vereinbartem Aufbau oder Regeln werden dagegen erklärt und erst im konkret freigegebenen Umfang umgesetzt.

Direkt nach der Einrichtung wird ein optionaler regelmäßiger Check angeboten. Er startet einen eigenen Projektchat und prüft besonders Funktion, Struktur und Eignung der Regeln. Zeitplan und Einstellungen werden erklärt und erst nach deiner Freigabe eingerichtet. Die gewöhnliche Nutzung funktioniert auch ohne diesen automatisierten Check.

Mehrere Chats koordinieren ihre Zugriffe auf das Gedächtnis über gemeinsame Arbeitsregeln. Die Koordination funktioniert nur, wenn die beteiligten Chats diese Regeln befolgen.

Du kannst das Projektgedächtnis auf Wunsch:

- **Deaktivieren und archivieren:** Inhalte und zugehörige Nutzungsanweisungen sichern, aus dem laufenden Projekt entfernen und einen Deaktivierungshinweis hinterlassen. Eine spätere Reaktivierung stellt das Gedächtnis wieder her.
- **Aus dem Projekt entfernen:** Gedächtnis, zugehörige Sicherungen, Gedächtnisregeln und Pflegeautomatisierung entfernen.

Diese Schritte betreffen nur das jeweilige Projekt. Die globale Skillinstallation und andere Projekte bleiben erhalten. Eine Wiederaufnahme erfolgt auf ausdrücklichen Auftrag. Einzelheiten stehen in der [Lebenszyklus-Anleitung](project-memory/references/lifecycle.md).

## Git im Projekt-Arbeitsordner

Git kann die Entwicklung der eigentlichen Arbeitsdateien nachvollziehbar erhalten. Das ist auch für Essays, Konzepte, Recherchen und andere Textprojekte nützlich: Gesicherte Fassungen lassen sich vergleichen, Änderungen einem Arbeitsstand zuordnen und frühere Versionen gezielt wiederherstellen. Die Arbeit mit dem Gedächtnis ersetzt diese Versionierung der Originaldateien nicht.

Wer sowohl die Arbeitsdateien als auch das Projektgedächtnis mit Git sichern möchte, sollte den Projekt-Arbeitsordner vor der Gedächtniseinrichtung als Git-Arbeitskopie vorbereiten beziehungsweise eine bestehende Arbeitskopie verwenden. Auch die Zugehörigkeit zu einem übergeordneten Repository zählt. **Die bloße Installation der Git-Software genügt dafür nicht.** Ein Repository entsteht erst durch die Einrichtung der Versionierung oder durch Übernahme einer bestehenden Git-Arbeitskopie. [Git: Ein Repository anlegen oder übernehmen](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository).

Der Skill prüft den tatsächlichen Stand und richtet kein Git für den übrigen Arbeitsordner ein. Die Versionierung der Arbeitsdateien folgt dem dort vereinbarten Verfahren. Sie läuft nicht automatisch allein deshalb, weil ein Repository vorhanden ist: Gewünschte Änderungen müssen als Git-Commit gesichert werden. Originalchats werden durch Git im Arbeitsordner ebenfalls nicht automatisch gespeichert.

Für die Gedächtniseinrichtung gelten diese beiden Wege:

| Stand des Arbeitsordners | Sicherung des Projektgedächtnisses |
| --- | --- |
| Der Arbeitsordner gehört bereits zu einer Git-Arbeitskopie. | Der Skill richtet ein eigenes, vom übrigen Projekt abgegrenztes Git in `project-memory/` ein. Git muss dafür ausführbar und für lokale Commits nutzbar sein. |
| Der Arbeitsordner gehört zu keiner Git-Arbeitskopie. | Das Gedächtnis wird durch vollständige, geprüfte Kopien in `.project-memory-archive/` gesichert. Das gilt auch dann, wenn Git auf dem Rechner installiert ist. |

Kann die vorgesehene Git-Sicherung nicht eingerichtet werden oder ist die Zuordnung unklar, erklärt der Skill das Hindernis. Er wechselt das Sicherungsverfahren nicht ohne Rücksprache.

## Zwei Repositorys mit getrennten Aufgaben

Bei der Git-Variante bleiben Arbeitsdateien und Gedächtnis im selben Projektordner, haben aber getrennte Versionsgeschichten. Für ein Projekt mit Git unmittelbar in seiner Wurzel sieht der Aufbau beispielsweise so aus:

```text
project-root/
├── .git/                    Git des übrigen Projekts
├── .gitignore               Abgrenzung des Gedächtnisses
├── AGENTS.md                Projektanweisungen und Skillverweis
├── draft.md                 Eine normale Arbeitsdatei
└── project-memory/
    ├── .git/                Eigenes Git des Gedächtnisses
    ├── PROFILE.md           Projektzuordnung und örtliches Verfahren
    ├── INDEX.md             Kurzer thematischer Einstieg
    └── entries/             Einträge mit Quellenzugängen
```

Das äußere Repository versioniert die dafür vorgesehenen Arbeitsdateien und Projektanweisungen. Das innere Repository sichert ausschließlich den zugehörigen Gedächtnisbestand. Ein Gedächtnis-Commit enthält deshalb keine außerhalb liegenden Arbeitsdateien oder Originalchats. Beide Geschichten können unabhängig voneinander nachvollzogen und wiederhergestellt werden.

Codex sichert zusammengehörige Gedächtnisänderungen und erhält vor dem Ersetzen oder Neuordnen von Inhalten den bisherigen Stand. Die Sicherung der übrigen Arbeitsdateien folgt dem vereinbarten Projektverfahren. Einzelheiten beschreibt die [Sicherungsanleitung](project-memory/references/backup.md).

Git bewahrt die Versionsgeschichte des Gedächtnisses. Frühere Stände können bei Bedarf ausdrücklich wiederhergestellt werden.

## Wie die Abgrenzung sichergestellt wird

Die Einrichtung ergänzt in der `.gitignore` des Projekt-Arbeitsordners drei örtlich verankerte Ausschlüsse:

```gitignore
/project-memory/
/.project-memory-archive/
/.project-memory.lock
```

Dadurch werden der Gedächtnisordner, ein vorhandenes Kopienarchiv und die vorübergehende Datei zur Zugriffskoordination bei der üblichen Aufnahme neuer Dateien ins äußere Git ausgeschlossen. Der Skill legt keinen Submodul-Verweis an und nimmt das innere Repository nicht als Bestandteil des äußeren Repositorys auf. Die Archivregel ist auch in der Git-Variante Vorsorge; sie verlangt dort keinen zusätzlichen Archivordner.

Der Skill prüft die tatsächliche Abgrenzung. **Bereits im äußeren Git verfolgte Dateien werden durch eine neue Ignore-Regel nicht entfernt.** Ein solcher Altbestand muss gezielt geklärt werden; die Einrichtung darf ihn nicht als korrekt getrennt melden oder ungefragt aus der bisherigen Geschichte entfernen. Vorhandene fremde Regeln und vorgemerkte Änderungen bleiben erhalten. [Git: Wirkung von Ignore-Regeln](https://git-scm.com/docs/gitignore).

Für laufende Aufgaben wird nur der aktive Gedächtnisbestand genutzt. Frühere Stände im Git und Kopien im Archiv dienen der Sicherung und einer ausdrücklich beauftragten Wiederherstellung. Diese Trennung wird durch die Projektregeln gesteuert.

## Spätere Versionierung und Übernahme des Projekts

Auch ohne äußeres Git legt die Einrichtung die Ignore-Regeln vorsorglich an. Wird der Arbeitsordner später versioniert, sind Gedächtnis und Archiv deshalb bereits für die Abgrenzung vorgesehen. Beauftrage den Wechsel von Kopiensicherung zu einem eigenen Gedächtnis-Git ausdrücklich. Die bisherige Sicherung bleibt erhalten, bis das neue Verfahren geprüft ist.

Ein Clone oder neuer Worktree des äußeren Repositorys enthält das ausgeschlossene Gedächtnis nicht automatisch. Dasselbe gilt für die Übertragung des äußeren Repositorys an einen Git-Server. Eine gewünschte Übernahme des Gedächtnisses einschließlich seiner eigenen Historie muss gesondert beauftragt und geprüft werden. Der Skill führt keinen automatischen Push aus. Beide örtlichen Sicherungsverfahren erhalten Versionen im lokalen Arbeitsumfeld; eine zusätzliche Sicherung außerhalb dieses Umfelds ist eine eigene Aufgabe.

## Aktualisierung des Skills

Der Installationsauftrag aktualisiert einen bereits installierten Skill nicht automatisch. Beauftrage ein Update ausdrücklich; vorhandene örtliche Anpassungen müssen dabei abgeglichen werden. Gedächtnisbestände, ihre Projektzuordnung und Sicherungen bleiben erhalten.

Wird die Skillinstallation verschoben, müssen die Verweise in bestehenden Projekten angepasst werden. Ein Update ändert die vereinbarten Projekteinstellungen und Pflegeautomatisierungen nicht automatisch.

## Weiterführende Anleitungen

Die verbindlichen Modellanweisungen stehen in [SKILL.md](project-memory/SKILL.md). Die Referenzen erläutern [Einrichtung](project-memory/references/setup.md), [Zugriffskoordination](project-memory/references/coordination.md), [Sicherung](project-memory/references/backup.md), [Wiederherstellung](project-memory/references/restore.md), [regelmäßigen Check](project-memory/references/automation.md) sowie [Pause, Archivierung, Entfernung und Reaktivierung](project-memory/references/lifecycle.md).

## Lizenz

Der Skill und die zugehörige Dokumentation stehen unter der [MIT-Lizenz](LICENSE).

Copyright (c) 2026 Salestracks.
