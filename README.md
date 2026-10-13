# Projektgedächtnis für Codex-Projekte mit lokalem Arbeitsordner

*Für Menschen, die mit Codex im Dialog über längere Zeit zusammenhängende Texte, Vorlagen, Konzepte oder Software entwickeln und für die nächste Aufgabe frühere Überlegungen wieder brauchen – weil der **aktuelle Arbeitsstand allein die Vorgeschichte oft nicht mehr erklärt**.*

Erschließt und pflegt wichtige Originalstellen in Gesprächen und Dokumenten, damit spätere Chats auf dem entstandenen Projektwissen aufbauen können. Besonders sinnvoll für länger laufende Ausarbeitungen und Projekte, in denen eine gemeinsame Grundlage entwickelt, wiederholt angewendet und weiter verbessert wird.

Eine typische Situation: „Die Ergebnisse sind vorhanden, aber für die nächste Aufgabe brauche ich auch wieder die Überlegungen dahinter.“ Vielleicht ist eine Gliederung bereits ausgearbeitet oder eine Vorlage fertig, doch für ihre Weiterentwicklung werden eine frühere Begründung, ein Einwand oder ein zurückgestellter Entwurf wieder wichtig. Kurze Gedächtniseinträge erklären, welche Originalstellen dafür relevant sind, und führen zum passenden Zusammenhang.

Der Skill richtet das Gedächtnis auf ausdrücklichen Auftrag ein und regelt anschließend Aufnahme, Abruf und laufende Pflege. Auch relevante Inhalte, die noch keinen Platz in einer ausgearbeiteten Projektdokumentation gefunden haben, werden erschlossen. Das Gedächtnis soll zur Quelle führen, statt ganze Gespräche oder Ausarbeitungen nochmals zusammenzufassen.

Das Gedächtnis gehört zum jeweiligen Projekt. Ein für mehrere Projekte verfügbarer Skill führt deren Inhalte nicht zusammen. Der Bestand liegt im Arbeitsordner unter `project-memory/`; die Projektanweisungen binden den Skill ein. Normale Dateiwerkzeuge und gegebenenfalls lokales Git genügen. Der Skill installiert keine Software.

Der technische Skillname ist `project-memory`; mit diesem Namen wird der Skill installiert und aufgerufen. Der Anzeigename in Codex ist „Projektgedächtnis für Projekte im Dialog – mit lokalem Arbeitsordner“.

## Voraussetzungen und Einsatzbereich

Vorgesehene Zielumgebung ist ein Codex-Projekt mit einem dauerhaft verfügbaren lokalen Arbeitsordner, in dem Codex die Projektdateien lesen und schreiben kann. Einrichtung, Pflege, Sicherung und Zugriffskoordination verwenden diesen örtlichen Bestand. Die Projektanweisungen müssen wirksam eingebunden sein, und die gewöhnlichen Datei-/Ausführungswerkzeuge müssen die beschriebenen Operationen erlauben.

Der vorhandene Chatzugang bestimmt, welche Originalgespräche tatsächlich gelesen werden können; der Skill stellt diesen Zugang selbst nicht bereit. Der regelmäßige Pflegechat benötigt zusätzlich eine passende native Automatisierungsfunktion und ausdrückliche Freigabe. Diese optionale Funktion ist keine Voraussetzung für die gewöhnliche Nutzung.

Die grundlegenden Markdown- und Dateiabläufe sind nicht prinzipiell auf Codex beschränkt. Ihre vollständige Einbindung in andere Agenten, reine Chats ohne lokalen Dateizugriff oder Cloud-Arbeitsumgebungen gehört jedoch nicht zum derzeit entwickelten und erprobten Einsatzbereich. Die bisherigen Ausführungsprüfungen erfolgten unter Windows; eine praktische macOS-Erprobung steht noch aus.

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

Die Beispiele zeigen, für welche Arbeitsmuster der Skill gedacht ist. Die bisherigen Praxisprüfungen betreffen vor allem Essayarbeit und Quellenabruf; die weiteren Anwendungsfälle sind noch zu erproben. Einzelheiten stehen unter „Prüfstand“.

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

Verwende einen lokalen Codex-Chat innerhalb der ChatGPT-App, in dem `skill-installer` verfügbar ist und auf den lokalen Skillordner zugreifen kann. Ein beliebiger Cloudchat genügt dafür nicht. Der vorgesehene Copy-&-Paste-Auftrag lautet:

```text
$skill-installer install https://github.com/OWNER/REPOSITORY/tree/main/project-memory
```

**`OWNER` und `REPOSITORY` sind Platzhalter.** Eine tatsächliche öffentliche Repository-Adresse steht noch nicht fest; diese Vorlage ist derzeit keine funktionierende Installationsadresse. Vor Veröffentlichung werden die Platzhalter ersetzt und der konkrete Installationsauftrag erprobt.

Der Installer übernimmt den Unterordner `project-memory/` einschließlich `SKILL.md`, `references/`, `agents/openai.yaml` und `LICENSE` in den lokalen Skillbestand. Die Anzeigemetadaten geben dem installierten Skill den Namen „Projektgedächtnis für Projekte im Dialog – mit lokalem Arbeitsordner“ und eine kurze Beschreibung seines Nutzens. README und Repository-Verwaltung werden nicht als Skillinhalt benötigt. Nach erfolgreicher Installation ist der Skill im nächsten Chat-Turn verfügbar.

### 2. Gedächtnis im Zielprojekt einrichten

Öffne das gewünschte Codex-Projekt mit seinem Arbeitsordner. Beauftrage dort die Einrichtung:

```text
$project-memory Richte das Projektgedächtnis im aktuellen Projekt-Arbeitsordner ein.
```

Der Skill prüft vorhandene Projektregeln und den Sicherungsweg, legt den örtlichen Bestand an und ergänzt einen Verweis in `AGENTS.md`. Bestehende Projektanweisungen bleiben erhalten. Ein erneuter Auftrag verwendet einen eindeutig zugeordneten Bestand weiter; er setzt ihn nicht auf einen leeren Anfang zurück. Im Kopienverfahren wird die Aufbewahrungsregel vor ihrer Aktivierung erklärt und zur Freigabe vorgelegt.

Nach erfolgreicher Einrichtung greifen die Projektregeln auch in weiteren Chats auf den Skill zurück. Alte, noch laufende Chats müssen vor einem Regelübergang abgeschlossen oder ihre Gedächtniszugriffe geklärt sein. Danach ist die ausdrückliche Nennung `$project-memory` bei gewöhnlicher Projektarbeit nicht jedes Mal erforderlich.

## Nutzung und Pflege

Das Modell erschließt relevante neue Inhalte und folgt bei Bedarf den Hinweisen zu ihren Originalstellen. Eintragsdateien enthalten nur die verpflichtenden Kennzeichnungen `id` und `project_id`; der übrige Text gibt knappe Orientierung und Quellenzugänge. Der Skill verlangt keine zusätzliche routinemäßige Belegablage. Ist ein Originalchat nicht erreichbar, kann ein begrenzter Originalauszug dessen benötigten Wortlaut erhalten; eine erfundene Fundstelle ersetzt den fehlenden Zugang nicht.

Laufende Inhaltspflege gehört zur normalen Arbeit: Einträge und Index verbessern, Doppelungen beheben und Fundstellen prüfen. Änderungen an Funktion, vereinbartem Aufbau oder Regeln werden dagegen erklärt und erst im konkret freigegebenen Umfang umgesetzt.

Direkt nach der Einrichtung wird ein optionaler regelmäßiger Check angeboten. Er startet einen eigenen lokalen Projektchat und prüft besonders Funktion, Struktur und Eignung der Regeln. Zeitplan, Projekt, Modell und Denkaufwand werden vor der Einrichtung zur Freigabe vorgelegt. Ohne Freigabe oder passenden nativen Automatisierungszugang bleibt es beim Angebot; das Gedächtnis kann trotzdem genutzt werden.

Mehrere regelkonforme Chats koordinieren zusammengehörige Gedächtniszugriffe über die temporäre Datei `.project-memory.lock`. Die Reservierung wird vor Quellenlektüre und fachlicher Arbeit wieder freigegeben. Sie ist eine kooperative Arbeitsregel und keine technische Sperre aller möglichen Dateizugriffe.

Für Lebenszyklusaufträge stehen drei Optionen zur Verfügung: Pausieren erhält aktive Dateien und Sicherungen; Deaktivieren und Archivieren ersetzt den aktiven Bestand durch einen Hinweis und hält einen Wiederherstellungsstand; vollständiges Entfernen beseitigt ausschließlich die örtliche Implementierung einschließlich ihrer zugeordneten Sicherungen und Pflegeautomatisierung. Reaktivierung erfolgt ausdrücklich. Globale Skillinstallation und andere Projekte bleiben bei der örtlichen Entfernung erhalten. Einzelheiten stehen in der [Lebenszyklus-Anleitung](project-memory/references/lifecycle.md).

## Git im Projekt-Arbeitsordner

Git kann die Entwicklung der eigentlichen Arbeitsdateien nachvollziehbar erhalten. Das ist auch für Essays, Konzepte, Recherchen und andere Textprojekte nützlich: Gesicherte Fassungen lassen sich vergleichen, Änderungen einem Arbeitsstand zuordnen und frühere Versionen gezielt wiederherstellen. Die Arbeit mit dem Gedächtnis ersetzt diese Versionierung der Originaldateien nicht.

Wer sowohl die Arbeitsdateien als auch das Projektgedächtnis mit Git sichern möchte, sollte den Projekt-Arbeitsordner vor der Gedächtniseinrichtung als Git-Arbeitskopie vorbereiten beziehungsweise eine bestehende Arbeitskopie verwenden. Auch die Zugehörigkeit zu einem übergeordneten Repository zählt. **Die bloße Installation der Git-Software genügt dafür nicht.** Ein Repository entsteht erst durch die Einrichtung der Versionierung oder durch Übernahme einer bestehenden Git-Arbeitskopie. [Git: Ein Repository anlegen oder übernehmen](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository).

Der Skill prüft den tatsächlichen Stand und richtet kein Git für den übrigen Arbeitsordner ein. Die Versionierung der Arbeitsdateien folgt dem dort vereinbarten Verfahren. Sie läuft nicht automatisch allein deshalb, weil ein Repository vorhanden ist: Gewünschte Änderungen müssen als Git-Commit gesichert werden. Originalchats werden durch Git im Arbeitsordner ebenfalls nicht automatisch gespeichert.

Für die Gedächtniseinrichtung gelten diese beiden Wege:

| Stand des Arbeitsordners | Sicherung des Projektgedächtnisses |
| --- | --- |
| Der Arbeitsordner gehört bereits zu einer Git-Arbeitskopie. | Der Skill richtet ein eigenes, vom übrigen Projekt abgegrenztes Git in `project-memory/` ein. Git muss dafür ausführbar und für lokale Commits nutzbar sein. |
| Der Arbeitsordner gehört zu keiner Git-Arbeitskopie. | Das Gedächtnis wird durch vollständige, geprüfte Kopien in `.project-memory-archive/` gesichert. Das gilt auch dann, wenn Git auf dem Rechner installiert ist. |

Git im Arbeitsordner ist damit eine bewusste Wahl für die Versionierung des Projekts und ermöglicht zusätzlich die Git-Sicherung des Gedächtnisses. Ein Projekt ohne Git kann das Gedächtnis mit Kopiensicherung nutzen. Bei vorhandener Git-Zuordnung und fehlendem nutzbarem Git oder unklarer Zuordnung meldet der Skill das Hindernis; er behauptet keine Gitfreiheit und wechselt nicht stillschweigend das Verfahren.

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

Für das Gedächtnis sichert das Modell geprüfte zusammenhängende Änderungspakete. Vor einer ersetzenden Überarbeitung wird ein noch ungesicherter Ausgangsstand zusätzlich gesichert; ein bereits gesicherter identischer Stand braucht keinen weiteren Commit. Einzelne Dateischreibvorgänge verlangen keine getrennten Sicherungen. Das betrifft die Gedächtnispflege, nicht automatisch jeden Arbeitsschritt im übrigen Projekt.

Git erhält die Gedächtnishistorie ohne die Generationenbegrenzung der Kopiensicherung. Bei „Deaktivieren und archivieren“ bleiben Ordner und inneres Git bestehen: Der letzte aktive Stand wird als Rückkehrpunkt bezeichnet, die aktiven Inhalte durch einen Hinweis ersetzt und der Übergang committed. Eine Reaktivierung stellt den Bestand auf dem erhaltenen Verlauf wieder her. Damit bleiben auch frühere Pflege- und Deaktivierungsschritte nachvollziehbar.

## Wie die Abgrenzung sichergestellt wird

Die Einrichtung ergänzt in der `.gitignore` des Projekt-Arbeitsordners drei örtlich verankerte Ausschlüsse:

```gitignore
/project-memory/
/.project-memory-archive/
/.project-memory.lock
```

Dadurch werden der Gedächtnisordner, ein vorhandenes Kopienarchiv und die vorübergehende Datei zur Zugriffskoordination bei der üblichen Aufnahme neuer Dateien ins äußere Git ausgeschlossen. Der Skill legt keinen Submodul-Verweis an und nimmt das innere Repository nicht als Bestandteil des äußeren Repositorys auf. Die Archivregel ist auch in der Git-Variante Vorsorge; sie verlangt dort keinen zusätzlichen Archivordner.

Der Skill prüft die tatsächliche Abgrenzung. **Bereits im äußeren Git verfolgte Dateien werden durch eine neue Ignore-Regel nicht entfernt.** Ein solcher Altbestand muss gezielt geklärt werden; die Einrichtung darf ihn nicht als korrekt getrennt melden oder ungefragt aus der bisherigen Geschichte entfernen. Vorhandene fremde Regeln und vorgemerkte Änderungen bleiben erhalten. [Git: Wirkung von Ignore-Regeln](https://git-scm.com/docs/gitignore).

Gedächtnis-Git-Aktionen richten sich ausdrücklich auf dessen eigenen Ordner. Die Repository-Zuordnung wird geprüft, damit eine Sicherung nicht versehentlich das übergeordnete Projekt betrifft. Bei einem Worktree kann die äußere Git-Verwaltung durch eine `.git`-Datei eingebunden sein; auch diese gültige Zuordnung wird berücksichtigt.

Die Abgrenzung regelt außerdem die Inhaltsnutzung: Frühere Gedächtnisstände im Git und Kopien im Archiv dienen technischer Sicherung und ausdrücklich beauftragter Wiederherstellung. Das Modell verwendet sie nicht als Ersatzgedächtnis oder zusätzlichen Kontext für laufende Aufgaben. Normale Suche schließt Git-Verwaltung, Archiv und Reservierungsdatei aus. Das sind verbindliche Arbeitsregeln und keine technische Lesesperre. Änderungen am aktiven Gedächtnis werden zwischen regelkonformen Chats kooperativ koordiniert.

## Spätere Versionierung und Übernahme des Projekts

Auch ohne äußeres Git legt die Einrichtung die Ignore-Regeln vorsorglich an. Wird der Arbeitsordner später versioniert, sind Gedächtnis und Archiv deshalb bereits für die Abgrenzung vorgesehen. Der Wechsel von Kopiensicherung zu einem eigenen Gedächtnis-Git benötigt einen ausdrücklichen Einrichtungsabgleich. Die bisherige funktionierende Sicherung bleibt erhalten, bis das neue Verfahren geprüft ist. Alte Kopien werden nicht automatisch in Git-Commits umgewandelt und bleiben aus gewöhnlichen Inhaltsabrufen ausgeschlossen.

Ein Clone oder neuer Worktree des äußeren Repositorys enthält das ausgeschlossene Gedächtnis nicht automatisch. Dasselbe gilt für die Übertragung des äußeren Repositorys an einen Git-Server. Eine gewünschte Übernahme des Gedächtnisses einschließlich seiner eigenen Historie muss gesondert beauftragt und geprüft werden. Der Skill führt keinen automatischen Push aus. Beide örtlichen Sicherungsverfahren erhalten Versionen im lokalen Arbeitsumfeld; eine zusätzliche Sicherung außerhalb dieses Umfelds ist eine eigene Aufgabe.

Beim vollständigen Entfernen des Projektgedächtnisses wird nur dessen örtliche Implementierung samt zugeordneten Sicherungen entfernt. Das äußere Projekt-Git, die Git-Software, ein gemeinsam verwendeter Skill und andere Projekte bleiben erhalten.

## Aktualisierung des Skills

Der `skill-installer` bricht ab, wenn der Zielordner des Skills bereits vorhanden ist; derselbe Installationsauftrag ist deshalb kein automatisches Update. Eine Aktualisierung muss ausdrücklich beauftragt werden und darf nur die zugeordnete Skillinstallation betreffen. Vorhandene örtliche Anpassungen werden dabei geprüft und erhalten beziehungsweise gezielt abgeglichen. Gedächtnisbestände, ihre Projektkennungen und ihre Sicherungen werden dadurch nicht ersetzt.

Projektregeln verweisen auf die tatsächliche installierte `SKILL.md`. Bleibt die Skillinstallation am selben Pfad, bleibt dieser Verweis verwendbar. Bei einem Umzug der Installation müssen betroffene Projektverweise ausdrücklich abgeglichen werden. Eine neue Skillfassung ändert vereinbarte örtliche Konfigurationen oder bestehende Pflegeautomatisierungen nicht selbstständig.

## Prüfstand

Die Einrichtung und wesentliche Quellen- und Pflegeabläufe wurden unter Windows in Testprojekten erprobt. Technische Prüfungen decken außerdem Sicherungen, kooperative parallele Zugriffe sowie Pause, Archivierung, Wiederherstellung und örtliche Entfernung ab. Das belegt die jeweils geprüften Abläufe und keine zuverlässige Befolgung jeder Regel durch jedes Modell.

Offen sind insbesondere die Ausführung unter macOS, die tatsächliche Einrichtung und Verwaltung nativer Pflegeautomatisierungen sowie ein erfolgreicher selbstständiger Modelllauf durch die neu ergänzten Lebenszyklusverfahren. Auch die vorgesehene GitHub-Installation wird erst mit der tatsächlichen Veröffentlichungsadresse erprobt. Weniger Tokens sind ein Ziel der Quellenkuratierung, keine bereits allgemein nachgewiesene Ersparnis.

## Struktur und Verfahrensbeschreibung

```text
README.md
LICENSE
CHANGELOG.md
project-memory/
├── SKILL.md
├── LICENSE
├── agents/
│   └── openai.yaml
└── references/
    ├── setup.md
    ├── coordination.md
    ├── backup.md
    ├── restore.md
    ├── automation.md
    └── lifecycle.md
```

Die verbindlichen Modellanweisungen stehen in [SKILL.md](project-memory/SKILL.md). Die Referenzen erläutern [Einrichtung](project-memory/references/setup.md), [Zugriffskoordination](project-memory/references/coordination.md), [Sicherung](project-memory/references/backup.md), [Wiederherstellung](project-memory/references/restore.md), [regelmäßigen Check](project-memory/references/automation.md) sowie [Pause, Archivierung, Entfernung und Reaktivierung](project-memory/references/lifecycle.md).

## Lizenz und Veröffentlichung

Der Skill und die zugehörige Dokumentation stehen unter der [MIT-Lizenz](LICENSE). Der vollständige englische Lizenztext enthält den Copyright-Hinweis `Copyright (c) 2026 Salestracks`.

Die identische [Lizenzdatei im Skillunterordner](project-memory/LICENSE) wird mitinstalliert, damit der Lizenzhinweis auch bei der Verteilung allein dieses Ordners erhalten bleibt. Bei Änderungen der Copyright-Angabe werden beide Dateien gemeinsam abgeglichen. Lizenzgrundlage ist der [MIT-Standardtext der Open Source Initiative](https://opensource.org/license/mit).

Eine öffentliche Repository-Adresse und veröffentlichte Releases sind noch nicht festgelegt. Der konkrete Installationsauftrag wird vor Veröffentlichung ergänzt und erprobt.
