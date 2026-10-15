# Einrichtung und erneuter Abgleich

Nutze diesen Ablauf nur für eine beauftragte Einrichtung oder einen entsprechenden Abgleich. Die Verfügbarkeit des Skills richtet kein Gedächtnis ein.

## Ziel und vorhandener Stand

Bestimme den tatsächlich benannten Projektarbeitsordner. Lies geltende Projektregeln und prüfe vorhandene Dateien am Ziel einschließlich fremder Änderungen. Ein vorhandenes eigenes Gedächtnis wird mit bestehender Kennung, Inhalt und Historie weiterverwendet; eine Wiederholung ist keine Neuanlage. Unklare Zuordnung, fremder Bestand, bereits außen verfolgte Gedächtnisdateien oder Submodule sind ein Klärungs- beziehungsweise Migrationsfall. Überschreibe sie nicht mit Vorlagen und vergib nicht automatisch eine andere Kennung.

Ein Deaktivierungshinweis in `project-memory/README.md` beendet eine allgemeine Einrichtung oder einen gewöhnlichen Abgleich ohne Gedächtnis- oder Sicherungslektüre und ohne Neueinrichtung. Nur ein ausdrücklicher Reaktivierungsauftrag folgt [lifecycle.md](lifecycle.md). Fehlen bei einem bereits eingerichteten Bestand Profil oder Index, ersetze sie nicht mit Vorlagen und lies nicht ersatzweise das Archiv; kläre den Befund. Ein einzelner defekter Eintragsverweis bei vorhandenem Profil und Index folgt dagegen der begrenzten Suche und Reparatur aus SKILL.md; er macht nicht den ganzen Bestand unbenutzbar. Bestehende ältere Anweisungen zum bloßen Pausieren werden ebenfalls nicht durch einen allgemeinen Einrichtungsaufruf in eine Nutzungseinbindung umgewandelt; ihr Abgleich gehört zu einem ausdrücklich beauftragten Lebenszyklusübergang.

Lies für die Einrichtung und jeden erneuten Abgleich [coordination.md](coordination.md). Entdecke geltende Zielregeln zuerst ohne Änderungen. Bereits eingerichtete Gedächtnisabrufe folgen anschließend der dort geltenden Koordination. Verwende für die neue Regel den einen temporären regulären Marker `<project-root>/.project-memory.lock` in der tatsächlich aufgelösten örtlichen Projektwurzel, außerhalb von Gedächtnis und Sicherungsarchiv. Neueinrichtung, erneuter Abgleich und ein freigegebener Verfahrenswechsel sind selbst geschützte Änderungspakete: Reservierung erwerben, betroffenen aktuellen Stand erneut lesen, zugehörige Dateien und Regeln ändern, prüfen und den Gedächtnisstand sichern, dann freigeben. Innerhalb desselben Pakets wird keine zweite Reservierung erworben.

Die Koordination wirkt nur zwischen Beteiligten, die sie befolgen. Bei der Einführung in einen vorhandenen Bestand müssen noch laufende Gedächtnisänderungen älterer Chats ohne diese Regel zunächst abgeschlossen oder gezielt unterbrochen sein; eine neu erzeugte Reservierung hält diese Schreiber nicht an. Kläre diesen Übergang bei einem ungeklärten laufenden Zugriff, bevor du den Bestand umstellst. Ersetze ältere örtliche Anweisungen nur im beauftragten Abgleich. Ein vorhandener fremder Marker wird nicht übernommen oder nach Alter entfernt; das Lesen seiner Besitzerkennung begründet kein Eigentum. Bei belegtem Zugriff gelten die begrenzten Versuche und der Wiederanlauf aus der Koordinationsreferenz; benenne einen danach ausstehenden Einrichtungsteil.

Halte keine reguläre Reservierung während Recherche, Entwurf oder einer ausstehenden Nutzerentscheidung. Liegt etwa die Freigabe der Aufbewahrung noch nicht vor, schließe das konsistente Paket ab, gib die Reservierung vor der Frage frei und lies nach erneutem Erwerb den Stand nochmals. Ein nicht sicher freigebbarer Teilumbau folgt dem Fehlerabschluss unten. Bereits konkret erteilte Freigaben gelten in ihrem Umfang weiter.

## Sicherungsverfahren auswählen

Bei ausführbarem Git prüfe die tatsächliche Arbeitskopie mit `git -C <project-root> rev-parse --is-inside-work-tree` und `--show-toplevel`. Auch eine übergeordnete Arbeitskopie zählt. Eine `.git`-Datei kann eine gültige Git-Zuordnung enthalten. Ordne Fehler ein: Ein nicht ausführbarer Aufruf, fehlendes Zugriffsrecht oder anderer Prüfungsfehler beweist keine Gitfreiheit.

Ohne ausführbares Git prüfe den Arbeitsordner und seine übergeordneten Ordner mit gewöhnlichen Dateioperationen auf Repositoryhinweise, insbesondere `.git` als Datei oder Verzeichnis. Sind die nötigen Ordner lesbar und ohne solche Hinweise, ist der Kopienzweig möglich. Bei Git-Hinweisen oder ungeklärter Zuordnung halte den betreffenden Einrichtungsteil an und erkläre den Befund. Verlange kein Git für einen festgestellten unversionierten Arbeitsordner.

Erhalte bei einem späteren Übergang die bisherige funktionierende Sicherung, bis das neue Verfahren vollständig geprüft ist. Gleiche anschließend Profil und Zielprojektregel auf das neue Verfahren ab. Ausschlüsse tatsächlich vorhandener Alt-Sicherungen bleiben erhalten. Vorhandene Kopien werden nicht automatisch zu Commits.

Für beide Verfahren gelten die Paketregeln aus [backup.md](backup.md): Den geprüften Stand nach einem zusammenhängenden Fortschreibungs- oder Pflegepaket sichern, einschließlich neuer Einträge und Ergänzungen. Vor einer Überarbeitung bestehender Inhalte ist nur dann eine zusätzliche Sicherung nötig, wenn der tatsächliche Ausgangsstand noch nicht gesichert ist. Es gibt keine Sicherung pro Datei und keine weitere Sicherung eines bereits gesicherten identischen Stands.

Erkläre im Kopienverfahren die begrenzte Aufbewahrung vor ihrer Aktivierung: Vorgeschlagen sind die 20 jüngsten geprüften Generationen und höchstens drei benannte Rückkehrpunkte; während einer laufenden Bearbeitung benötigte Sicherungen bleiben vorübergehend geschützt. Das erhält einen begrenzten Wiederherstellungsbestand, keine vollständige dauerhafte Historie. Lege die konkrete örtliche Regel vor und hole die Freigabe dafür ein; eine schon erteilte konkrete Freigabe gilt weiter. Ohne Freigabe kann die Sicherung weiterlaufen, ältere Kopien werden jedoch nicht entfernt. Bei einem Altbestand werden weder eine unbegrenzte Aufbewahrung noch das Sicherungsverfahren still umgestellt. Die Details der Prüfung und Bereinigung stehen in [backup.md](backup.md).

## Dateien und kurze Projektregel

Für eine Neuanlage erstelle `project-memory/PROFILE.md`, `INDEX.md` und `entries/`. Vergib eine neue UUID ausschließlich für ein tatsächlich neues Projektgedächtnis. Neue Einträge sind einzelne Markdown-Dateien mit `id` und `project_id`; ein anfangs kurzer Index genügt. Zusätzliche JSON-Dateien oder anfängliche Einträge sind nicht erforderlich.

Halte das Profil kurz. Es enthält die Projektkennung, den örtlichen Projektzusammenhang und Arbeitsordner, das ausgewählte Sicherungsverfahren sowie tatsächlich freigegebene örtliche Abweichungen. Im Kopienverfahren gehören die konkret freigegebene Zahl der Generationen und benannten Rückkehrpunkte beziehungsweise die ausstehende Freigabe dazu; bei eingerichtetem Check seine bestätigte native Kennung und Konfiguration. Allgemeine Abläufe werden über den tatsächlich lesbaren Skillpfad und dessen zuständige Referenzen erschlossen, nicht vollständig kopiert. Insbesondere werden Wartewerte nicht ein zweites Mal im Profil festgeschrieben. Dafür sind keine zusätzlichen Pflichtfelder, technischen Zähler oder JSON-Konfiguration nötig.

Eine kurze Einordnung genügt: Das Gedächtnis kuratiert Originalstellen in Chats und vorhandenen Projektdateien; Abruf, Sicherung nach Änderungspaketen, kooperative Koordination und die zwei Pflegestufen folgen der aktuellen Skillfassung. Es verlangt keine routinemäßige Belegkopie. Die örtlichen Sicherungs- und Zugriffswege müssen eindeutig bleiben. Der temporäre Marker gehört nicht zum gesicherten Bestand und wird nicht dauerhaft leer angelegt. Bei einem beauftragten Abgleich korrigiere widersprüchliche ältere Profilanweisungen, ohne Kennung, Quellen oder übrigen Bestand zu ersetzen.

Beobachtete Besonderheiten des nativen Chatzugangs gehören nur hinein, wenn sie künftige Abrufe tatsächlich erleichtern: etwa ein bekannter Originalchat, der trotz fehlendem Listentreffer direkt lesbar ist, oder die Fundstelle eines übernommenen Auftrags. Verallgemeinere diese Beobachtung nicht zur garantierten Schnittstelle und verlange keine vollständigen Chatabrufe.

Ergänze in der `.gitignore` des Arbeitsordners die drei örtlich verankerten Regeln und erhalte vorhandene Inhalte:

```gitignore
# project-memory:start
/project-memory/
/.project-memory-archive/
/.project-memory.lock
# project-memory:end
```

Bereite die Regeln auch ohne äußeres Git für eine spätere Einrichtung vor. Die Kommentargrenzen kennzeichnen ausschließlich neu angelegte eigene Regeln oder im beauftragten Abgleich eindeutig zugeordnete Altregeln; fremde gleichlautende Ausschlüsse werden erhalten und nicht als eigene übernommen. Bereits vorhandene passende Regeln werden nicht dupliziert. Sie sind Vorsorge und verlangen weder einen Archivordner noch beide Sicherungsverfahren oder einen dauerhaften Marker. Eine Ignore-Regel entfernt keine bereits verfolgten Dateien; prüfe die wirksame Abgrenzung, wenn ein äußeres Git vorhanden ist.

Ergänze die primären Zielprojektregeln in `<project-root>/AGENTS.md` mit einem kurzen verbindlichen Verweis; fehlt die Datei, lege sie an. Berücksichtige wirksame vorhandene Overrides und kläre einen widersprüchlichen Regelbestand, statt eine unwirksame Einrichtung zu melden. Setze den tatsächlich lesbaren absoluten Pfad zur verwendeten `SKILL.md` und die tatsächliche örtliche Projektwurzel für den Marker ein; kopiere keinen Platzhalter. Erhalte übrige Anweisungen. Trenne den eigenen Nutzungsabschnitt mit `<!-- project-memory:start -->` und `<!-- project-memory:end -->` vom eigenständigen Sicherungsausschluss mit `<!-- project-memory-backup:start -->` und `<!-- project-memory-backup:end -->`. Bei einem Altbestand erfolgt diese Zuordnung nur im beauftragten Abgleich und anhand belegbar eigener Anweisungen; übernimm keine fremden Regeln in die Abschnitte. Löse dabei einen früheren gemischten eigenen Block gezielt in diese zwei Abschnitte auf. Eine geeignete Formulierung für den erst nach erfolgreicher Prüfung eingebundenen Nutzungsabschnitt ist:

```markdown
<!-- project-memory:start -->
Bei neuen substanziellen Aufgaben und nach Kontextverdichtung lies erneut die aktuelle Dateifassung des Skills `project-memory` unter `<skill-path>` und nutze sie.

Wende Abruf, Fortschreibung vor Arbeitsabschluss und laufende Pflege auf das örtliche `project-memory/` an, auch ohne ausdrückliche Skill-Nennung. Erledige laufende Inhaltspflege innerhalb des bestehenden Verfahrens selbstständig; funktionaler oder struktureller Umbau folgt einem konkreten erklärten Vorschlag und der Nutzerfreigabe für diesen Umfang. Ein Automatisierungsstart erteilt diese Freigabe nicht. Ein Deaktivierungshinweis in `project-memory/README.md` beendet Gedächtnisnutzung und Pflege; lege keinen Ersatz an und reaktiviere den Bestand nicht ohne ausdrücklichen Reaktivierungsauftrag. Fehlt der Skill oder fehlen Profil beziehungsweise Index des eingerichteten Bestands, melde das und richte ihn nicht automatisch neu ein. Ein einzelner defekter Eintragsverweis folgt der begrenzten Reparatur aus dem Skill.

Alle Chats, Subagenten und Automatisierungen befolgen die kooperative Zugriffskoordination des Skills: zusammengehörige Gedächtnisabrufe und vollständige Änderungspakete über `<project-root>/.project-memory.lock` reservieren; fremde Reservierungen nicht umgehen oder nach Alter entfernen. Gewöhnliche Projektquellensuche schließt diesen technischen Marker ausdrücklich aus.

Begrenze Projektquellensuche auf die diesem Projekt zugeordneten Arbeitsordner und Originalchats; die referenzierte Skilldatei dient als Arbeitsanweisung und macht ihr Herkunftsprojekt nicht zur Inhaltsquelle. Wissenstransfers aus anderen Projekten benötigen einen ausdrücklichen Auftrag; fachliche externe Recherche bleibt zulässig.

<!-- project-memory:end -->

<!-- project-memory-backup:start -->
<backup-exclusion>
<!-- project-memory-backup:end -->
```

Ersetze `<backup-exclusion>` durch den Sicherungsausschluss passend zum ausgewählten und im Profil beschriebenen Verfahren. Nutze in einer Neuanlage nur die passende Formulierung. Bei einer bestehenden Einrichtung ersetze ausschließlich den zugehörigen Sicherungsabsatz; erhalte übrige Projektanweisungen. Tatsächlich vorhandene Sicherungen eines früheren Verfahrens bleiben zusätzlich ausgeschlossen. Dieser eigenständige Sicherungsabschnitt bleibt bei Deaktivierung und Archivierung bestehen; nur der Nutzungsabschnitt wird nach [lifecycle.md](lifecycle.md) entfernt und in `PROJECT_RULES.md` des Rückkehrstands archiviert.

**Eigenes Gedächtnis-Git:**

> Frühere Gedächtnisstände im eigenen Git dienen ausschließlich der Sicherung, technischen Prüfung und ausdrücklich beauftragten Wiederherstellung. Sie werden für laufende Aufgaben nicht als Quellen, Anweisungen oder zusätzlicher Kontext verwendet. Aktive Einträge verweisen nicht auf Sicherungsstände. Gewöhnliche Suchen einschließlich Dateiauflistungen und rekursive Lektüre schließen Git-Verwaltungsdateien aus; das gilt auch für Subagenten und Automatisierungen. Die Prüfung aktueller Änderungen bleibt zulässig.

**Kopiensicherung:**

> `.project-memory-archive/` dient ausschließlich Sicherung, technischer Prüfung, Bereinigung nach der konkret freigegebenen örtlichen Aufbewahrungsregel und ausdrücklich beauftragter Wiederherstellung. Archivtexte werden für laufende Aufgaben nicht als Quellen, Anweisungen oder zusätzlicher Kontext verwendet. Aktive Einträge verweisen nicht auf Sicherungsstände. Gewöhnliche Suchen einschließlich Dateiauflistungen und rekursive Lektüre schließen das Archiv ausdrücklich aus; das gilt auch für Subagenten und Automatisierungen. Die Prüfung aktueller Änderungen bleibt zulässig.

Der Sicherungsausschluss gilt bereits beim Anlegen der Sicherung; bereite ihn im Kopienverfahren vor dem Anlegen des Archivs vor. Binde den Nutzungsabschnitt erst nach erfolgreicher Abschlussprüfung in `AGENTS.md` ein. Bereite seinen Text zuvor außerhalb der wirksamen Projektanweisungen vor. Eine Statuszeile und eine technische Aktivierungsprüfung bei Gedächtniszugriffen werden nicht eingerichtet.

## Arbeitsordner gehört zu Git

1. Prüfe äußeren Arbeitsstand und vorhandene Ziele. Erhalte fremde vorgemerkte und ungespeicherte Arbeit.
2. Prüfe die wirksamen örtlichen Ignore-Regeln. Der aktive Bestand darf nicht im äußeren Index liegen oder dort als eingebettetes Repository neu aufgenommen werden. Keine Submodul-Einrichtung.
3. Richte ein gewöhnliches eigenes Git in `project-memory/` ein. Bei Wiederholung verwende das schon vorhandene eigene Repository. Richte jeden Gedächtnis-Git-Aufruf ausdrücklich darauf.
4. Sichere den zugehörigen aktuellen Gedächtnisstand tatsächlich mit einem ersten Commit beziehungsweise prüfe den vorhandenen aktuellen Commit. Verändert sich das Profil während der Einrichtung, muss auch diese Endfassung gesichert sein. Prüfe, dass zugehörige Dateien nicht durch innere Ignore-Regeln fehlen.

Git muss hier verfügbar und zum Committen nutzbar sein. Fehlen notwendige Git-Einstellungen oder Rechte, erkläre den konkreten Fehler statt fremde Identität oder globale Konfiguration zu ändern. Ein gescheiterter Git-Zweig wird nicht still auf Kopien umgestellt. Die Einrichtungsdateien im äußeren Projekt werden nach dessen eigenem Git-Verfahren behandelt; Gedächtnisdateien bleiben abgegrenzt. Es gibt keinen automatischen Push.

## Arbeitsordner ohne Git

Lege weder für das Projekt noch für das Gedächtnis ein Git an. `project-memory/` bleibt der aktive Ordner. Sichere seine geprüfte Endfassung zur Abschlussprüfung nach [backup.md](backup.md) vollständig in einem neuen eindeutig bezeichneten Unterordner von `.project-memory-archive/`. Der Ausschluss muss vor Archivzugriff bekannt sein. Weitere Sicherungen und eine freigegebene Generationenbereinigung folgen derselben Referenz. Bestehende Kopien werden nicht überschrieben; ohne erteilte Aufbewahrungsfreigabe bleiben sie erhalten.

## Abschluss und Wiederanlauf

Prüfe unter der eigenen Reservierung örtliche Zuordnung, lesbares Profil und Index, passende eindeutige Kennzeichnungen vorhandener Einträge, Sicherungsverfahren, wirksame Markerabgrenzung und Projektregeln. Erst dann weise das Verfahren als eingerichtet aus und aktiviere den regulären Verweis. Gib die eigene Reservierung nach abgeschlossener Prüfung und Sicherung frei; berichte Arbeitsordner, ausgewähltes Verfahren und wesentliche Änderungen verständlich. Die Prüfung der örtlichen Einrichtung ist kein Nachweis, dass sämtliche bereits laufenden Chats die neue Regel beachten.

Bei einem Teilfehler gilt der Fehlerabschluss aus [coordination.md](coordination.md): Die selbst erworbene Reservierung erst nach Ende aller zugehörigen Schreib-, Git- und Kopierprozesse und bei konsistentem aktivem Bestand freigeben. Ein konsistenter, aber noch ungesicherter Stand darf mit ausdrücklicher Meldung freigegeben werden. Bei einem ungeklärten teilweise angewendeten Umbau bleibt der Marker als blockierter Abbruch bis zum geregelten Wiederanlauf bestehen; schließe mit dem konkreten Hindernis ab, statt eine Nutzerfreigabe unter einer gehaltenen Reservierung abzuwarten. Nenne verbliebene Änderungen, einen gegebenenfalls ungesicherten Stand, erfolgreich geprüften Umfang und fehlende Schritte. Nimm weder fremde Änderungen noch eine schon funktionierende Einrichtung pauschal zurück. Ein erneuter Aufruf setzt nach dem geregelten Zugriffserwerb am festgestellten Stand an.

## Regelmäßigen Check nach erfolgreicher Einrichtung anbieten

Direkt nach erfolgreicher Gedächtniseinrichtung und Freigabe der Reservierung lies [automation.md](automation.md) und informiere den Nutzer umfassend über Zweck, Funktion und Grenzen des regelmäßigen Checks: eigenständiger neuer lokaler Projektchat, Schwerpunkt auf funktionalen und strukturellen Verbesserungen sowie Eignung der Regeln, erlaubte laufende Inhaltspflege und getrennte Freigabe für Umbauten. Erkläre Ausführungsvoraussetzungen, Modellaufwand und die Möglichkeit, Frequenz zu ändern, den Check zu pausieren oder auf ihn zu verzichten. Das Angebot und die Freigabe warten außerhalb einer Reservierung. Ein deaktivierter und archivierter Bestand löst kein Einrichtungsangebot und keine Aktivierung des Checks aus; seine Reaktivierung folgt [lifecycle.md](lifecycle.md).

Lege den kurzen konkreten Prüfauftrag aus der Referenz, das zugeordnete Projekt, Starttakt mit Uhrzeit und Zeitzone sowie Modell und Denkaufwand vor und frage nach Freigabe. Veränderliche Skillregeln werden im Dauerauftrag nicht dupliziert. Nach Freigabe richte die passende native Automatisierung tatsächlich ein und prüfe die Rückmeldung; native Scheduleraufrufe erfolgen außerhalb der Reservierung. Erwirb danach für die kurze Dokumentation der bestätigten Konfiguration im Profil erneut den Zugriff, lies den aktuellen Stand und sichere das geprüfte Paket. Bei Wiederholung gleiche einen vorhandenen Check ab, statt einen zweiten anzulegen. Eine bereits dokumentierte Ablehnung oder unveränderte konkrete Freigabe muss nicht erneut allgemein abgefragt werden.

Die Gedächtniseinrichtung selbst bleibt bei ausstehender Freigabe, Ablehnung oder nicht verfügbarem Automatisierungszugang erfolgreich. Nenne getrennt die bestätigte Einrichtung des Jobs, einen tatsächlich beobachteten automatischen Lauf und die gegebenenfalls ungeprüfte oder blockierte Verwaltung aus einem unbeaufsichtigten Lauf. Ein interaktiver Erfolg beweist Letztere nicht. Es ist keine zusätzliche automatische Vollprobe vorgeschrieben. Erfinde keine eingerichtete Automatisierung und installiere keinen Ersatzscheduler.
