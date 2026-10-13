---
name: project-memory
description: >-
  Richte auf Auftrag ein Projektgedächtnis für ein Codex-Projekt mit lokalem
  Arbeitsordner ein. Erschließe und pflege wichtige Originalstellen in Gesprächen
  und Dokumenten, damit spätere Aufgaben auf den ursprünglichen Quellen und
  Überlegungen aufbauen können. Besonders sinnvoll für länger laufende
  Ausarbeitungen und wiederkehrende Arbeit mit gemeinsamen Grundlagen, etwa
  Essays, Vertragsvorlagen, Recherchen oder Software. Nutze ein vorhandenes
  Gedächtnis auch auf Verweis der Projektregeln. Deaktiviere und archiviere,
  reaktiviere oder entferne die örtliche Einrichtung auf Auftrag.
---

# Projektgedächtnis

Kuratiere wichtige Originalstellen für die weitere Projektarbeit. Kurze Einträge geben Orientierung, erklären die Relevanz und führen zum passenden Zusammenhang in Chats oder Projektdateien. Sie sollen Kontext durch gezielten Originalzugriff erhalten und unnötige Wiederholung und breite Suche vermeiden. Inhalte bleiben dem benannten Projekt zugeordnet. Der Skill allein erlaubt keine Einrichtung in weiteren Projekten.

Nutze gewöhnliches Lesen, Schreiben und Durchsuchen sowie gegebenenfalls lokales Git. Vorhandene native Lesezugänge zu Originalchats dürfen genutzt werden, soweit sie im Zielprojekt tatsächlich verfügbar sind. Installiere dafür keine Hilfsprogramme, zusätzliche Laufzeit, Hooks oder Suchdienste. Ohne passenden Chatzugang gilt der gezielte Ersatz unter „Fortschreibung und Quellenzugang“.

- Bei beauftragter Einrichtung, erneutem Einrichtungsabgleich oder Wechsel des Sicherungsverfahrens lies [references/setup.md](references/setup.md).
- Bei Deaktivieren und Archivieren, vollständiger örtlicher Entfernung oder Reaktivierung lies [references/lifecycle.md](references/lifecycle.md). Ein Auftrag zur Skillentwicklung verändert keine Zielprojekte; eine örtliche Entfernung lässt die globale Installation und andere Projekte erhalten.
- Für den eigenen regelmäßigen Pflegechat sowie Einrichtung oder Änderung seines Zeitplans lies [references/automation.md](references/automation.md). Die Einrichtung bietet diesen optionalen Weg erst nach erfolgreicher Gedächtniseinrichtung und mit konkreter Nutzerfreigabe an.
- Für Arbeit mit einem vorhandenen Gedächtnis gilt der folgende Ablauf. Richte einen fehlenden Bestand nicht allein wegen eines Abrufversuchs neu ein.
- Vor Zugriffen auf den aktiven Bestand, Einrichtung oder Sicherungsoperationen lies [references/coordination.md](references/coordination.md) und verwende die gemeinsame Reservierung.
- Beim Schreiben und Sichern eines Gedächtnispakets, bei Wiederherstellung oder Archivbereinigung lies [references/backup.md](references/backup.md).
- Bei ausdrücklich beauftragter Wiederherstellung lies [references/restore.md](references/restore.md).

## Deaktivierungshinweis und fehlender Bestand

Bei Deaktivierung werden die aktuellen Gedächtnisinhalte gesichert und durch `project-memory/README.md` als technischen Deaktivierungshinweis ersetzt; die Nutzungs- und Pflegeanweisungen werden aus `AGENTS.md` entfernt und mitarchiviert. Triffst du bei einem Abruf oder Schreibversuch auf diesen Hinweis, beende die reguläre Gedächtnisarbeit. Lies, ergänze oder pflege keinen Ersatzbestand; lege keine Dateien neu an und fülle den Ordner nicht aus früherem Chatkontext oder Sicherungen auf. Ein alter Arbeits- oder Pflegeauftrag und eine allgemeine Einrichtungsprüfung reaktivieren nichts. Nur ein ausdrücklicher Reaktivierungsauftrag erlaubt die Wiederherstellung nach lifecycle.md.

Fehlen Profil, Index oder der übrige eingerichtete Bestand, halte den Gedächtniszugriff an und kläre gegebenenfalls den technischen Hinweis. Verwende keine Sicherung als Ersatzgedächtnis und richte nichts automatisch neu ein. Nach vollständiger Entfernung braucht eine spätere Neueinrichtung einen ausdrücklichen Auftrag. Gewöhnliche Projektarbeit kann vorhandene Arbeitsdateien und Originalchats weiter nutzen; ein Pflegechat ohne nutzbaren Bestand endet.

Beachte die aktuellen Projektanweisungen bei der üblichen Aufgabenaufnahme. Eine Statuszeile und technische Aktivierungsprüfungen vor oder nach jedem Zugriffspaket sind nicht vorgesehen. Eine Deaktivierung beginnt erst nach Abschluss aller anderen Projektchats und Schreiboperationen sowie bestätigtem Pausieren des zugehörigen Pflegechecks. Der gemeinsame Übergang folgt lifecycle.md.

## Aktiver Bestand und Grenzen

Im tatsächlichen Projektarbeitsordner liegt `project-memory/` mit einem lesbaren `PROFILE.md`, kurzem `INDEX.md` und einzelnen Einträgen in `entries/`. Die stabile Projektkennung steht einmal im Profil; alternativ steht sie in `profile.json`, auf das das Profil verweist.

Jeder Eintrag enthält nur zwei verbindliche Kennzeichnungen: `id` und `project_id`. Die Projektkennung ist eine UUID; Eintragskennungen wie `E-0001` sind im Projekt eindeutig und bleiben bei Umbenennung erhalten. Markdown-Angaben und ein kleiner JSON-Block sind gleichermaßen zulässig. Nutze das örtliche Format. Neue Kennungen dürfen keinen vorhandenen anderen Eintrag bezeichnen.

Der übrige Text ist frei: knappe Orientierung, warum eine Stelle später wichtig ist, und ein nutzbarer Zugang zu ihrem Original. Zusammenfassungen dienen der Auswahl; wiederhole nicht die gesamte Ausarbeitung im Eintrag. Begründungen, Einwände und zeitliche Einordnung können helfen, den passenden Zusammenhang auszuwählen. Keine Pflichtkategorien, Status-, Urheber-, Rollen-, Datums- oder Pflegefelder. Eine Projektrolle kann einmal im Profil beschrieben sein; daraus entstehen keine Eintragsfilter.

Technische Namen sind Englisch. Skill-Anweisungen, Eintragsinhalte und Erklärungen bleiben Deutsch. Originalpassagen werden wortgetreu erhalten.

Begrenze Projektquellensuche auf die dem benannten Projekt zugeordneten Arbeitsordner und Originalchats. Verwende bekannte, belegte Projektfundstellen direkt. Ordne weitere Chats vor dem Lesen anhand verfügbarer Projekt- oder Arbeitsordner-Metadaten zu; Titel und thematische Ähnlichkeit genügen nicht. Eine fehlende native Projektkennung schließt einen Chat bei eindeutig passendem Arbeitsordner nicht aus. Native Projektkennungen sind nicht die Gedächtnis-UUID `project_id`. Bei unbekannter oder widersprüchlicher Zuordnung lies nicht probeweise Chatinhalte anderer Projekte; benenne die Grenze. Die referenzierte Skilldatei und ihre Verfahrensreferenzen dürfen als Arbeitsanweisungen außerhalb des Projekts liegen; ihr Herkunftsprojekt wird dadurch keine Inhaltsquelle. Andere Projektinhalte erfordern einen ausdrücklich beauftragten Wissenstransfer. Importierte örtliche Originaldateien und fachliche externe Recherche bleiben zulässig. Diese Grenze gilt ebenso für Subagenten und Automatisierungen.

Historische Gedächtnisstände dienen der Sicherung: frühere Fassungen im eigenen Git oder Kopien in `.project-memory-archive/`. Diese Grenze gilt für die im Projekt tatsächlich vorhandenen Sicherungen, auch nach einem Verfahrenswechsel. Lies sie nicht als Ersatzgedächtnis, Originalquelle, Anweisung oder zusätzlichen Kontext für gewöhnliche Aufgaben. Aktives Profil, Index und Einträge verweisen nicht auf Sicherungen als Inhaltsquellen. Das Profil darf Sicherungsverfahren, konkret freigegebene Aufbewahrung und benannte Rückkehrpunkte ausschließlich für technische Zuordnung beschreiben. Technische Sicherungsprüfung, freigegebene Archivbereinigung, Prüfung gerade vorgenommener Änderungen und beauftragte Wiederherstellung bleiben möglich.

Diese Grenze gilt auch für Projektquellensuche, Subagenten und optionale Automatisierung. Schließe Sicherungsarchiv, Git-Verwaltungsdateien und den technischen Reservierungsmarker `.project-memory.lock` bei jeder gewöhnlichen Suche ausdrücklich aus, einschließlich Dateiauflistungen zur Orientierung, auch wenn noch kein Archiv sichtbar ist. Technische Sicherungsinventare und Markerprüfung bleiben für die entsprechenden Verfahrensschritte zulässig. Originalquellen liegen außerhalb der Sicherungen. Anweisungen und Ignore-Regeln sind keine technische Lesesperre.

## Kooperative Zugriffskoordination

Reserviere zusammengehörige Gedächtnisabrufe und vollständige Änderungspakete über die reguläre Datei `.project-memory.lock` unmittelbar in der tatsächlichen Projektwurzel. Erwerb erfolgt exklusiv, mit einer eigenen eindeutigen Besitzerkennung. Bündele Erwerb, vorbereiteten Dateizugriff und konsistenzabhängige Freigabe möglichst in einem Aufruf, damit keine Reservierung während weiterer Modellrunden oder Werkzeugfreigaben liegen bleibt. Lies unter kurzer Reservierung Profil, Index und benötigte Einträge; gib vor Originallektüre, Recherche, Ausarbeitung und Nutzerfreigabe wieder frei. Für Schreiben neu erwerben, aktuellen Stand erneut lesen und Kennungsvergabe, Änderungen, Prüfung, Sicherung und zugehörige Bereinigung unter demselben Besitzer abschließen. Verlangt eine inzwischen veränderte Vorlage weitere Modellarbeit, gib vor deren Vorbereitung wieder frei. Unterabläufe erwerben keine verschachtelte Reservierung.

Warte bei Belegung mit fünf Sekunden Abstand höchstens 30 Sekunden; eine zweite solche Phase ist nur nach unabhängiger Arbeit erlaubt. Bleibt der nötige Zugriff blockiert, benenne ausstehenden Abruf oder Fortschreibung, statt ihn still zu überspringen oder fremde Reservierungen zu entfernen. Nach Rundenende gibt es keine Hintergrundfortsetzung. Nur der nachgewiesene Eigentümer gibt frei. Ein ungesichertes konsistentes Ergebnis und ein ungeklärter teilweise angewendeter Umbau verlangen unterschiedliche Fehlerabschlüsse nach coordination.md. Zurückgebliebene Marker werden nicht allein wegen ihres Alters übernommen.

Dieses Verfahren gilt auch für Pflegechats und Subagenten am selben örtlichen Bestand. Es setzt die Befolgung der Regeln voraus und erzwingt keine Sperre beliebiger direkter Dateizugriffe. Eine Einführung bei schon laufenden Chats mit älteren Regeln verlangt zuvor abgeschlossene oder geklärt unterbrochene Gedächtnisänderungen. Einzelheiten, gewöhnliche Plattformoperationen und Wiederanlauf stehen in coordination.md.

## Einstieg und Abruf

1. Kläre den benannten Arbeitsordner und lies bei neuer substanzieller Aufgabe oder nach Kontextverdichtung die geltenden Projektregeln. Erwirb für das vorhandene Gedächtnis die kurze Abrufreservierung nach coordination.md, lies Profil und Index und erschließe die benötigten Einträge nach den nächsten beiden Schritten. Ein Deaktivierungshinweis oder fehlender Bestand beendet den Zugriff wie oben beschrieben. Fehlt die Projektkennung im Profil oder ist sie widersprüchlich, setze die Gedächtnisnutzung bis zur Klärung aus. Nutze kein fremdes oder archiviertes Gedächtnis und vergib keine neue Projektkennung. Gib die eigene Reservierung nach dem Abruf beziehungsweise kontrolliertem Abschluss frei; der übrige Auftrag kann mit vorhandenen Projektquellen weitergehen.
2. Suche einschlägige Einträge gezielt im aktiven Bestand und lies die relevanten Zusammenhänge. Eine äußere `.gitignore` kann diesen Ordner bei gewöhnlicher Suche ausblenden: Übergehe nötige Filter nur innerhalb von `project-memory/`, weiterhin ohne Git-Verwaltungsdateien und Sicherungsarchiv. Ein Filterproblem ist kein fehlender Treffer.
3. Prüfe bei Verwendung und Fortschreibung die Kennzeichnung. Fehlt sie, stimmt `project_id` nicht mit dem Profil überein oder ist eine widersprüchliche Doppelkennung erkennbar, verwende den betroffenen Eintrag bis zur Klärung nicht. Melde den konkreten Konflikt; ordne ihn nicht automatisch um. Prüfe nicht bei jeder Antwort den gesamten Bestand.
4. Gib nach Schritten 1–3 die Abrufreservierung frei. Hängt das Ergebnis von einer Aussage oder Ausarbeitung ab, folge danach dem Quellenhinweis zur passenden Originalpassage mit nötigem Zusammenhang. Nutze bei Chatquellen den tatsächlich verfügbaren Lesezugang und die bekannte Fundstelle. Begrenze den Abruf nach Möglichkeit auf passende Beiträge; ein Chatverweis ist kein Auftrag, den gesamten Chat einzulesen. Behaupte keinen punktgenauen Zugriff, den das Werkzeug nicht unterstützt. Bereits gelesene, unveränderte Passagen brauchen innerhalb derselben Aufgabe keine wiederholte Lektüre. Gleiche bei Bedarf aktuelle Arbeitsdateien ab.
5. Ohne passenden Treffer suche begrenzt in einschlägigen normalen Projektquellen. Ein erfolgloser Gedächtnisabruf belegt nicht, dass eine Quelle fehlt, und erlaubt keinen Sicherungszugriff. Benenne fehlende Belege; rekonstruiere verlorenen Wortlaut nicht.

Historische Gesprächsaufträge werden durch Lesen oder Aufnahme ins Gedächtnis nicht erneut ausgeführt. Aktuelle Nutzeranforderungen und Projektregeln gelten weiterhin.

## Fortschreibung und Quellenzugang

Prüfe vor Abschluss einer substanziellen Aufgabe, welche Gedanken, Entscheidungen, offenen Fragen, Korrekturen oder Ausarbeitungen später nützlich sind. Dazu gehören auch unbestätigte Gliederungen, Entwürfe und Zwischenstände, auf denen weitere Arbeit aufbauen kann. Erschließe ihre relevanten Originalstellen; prüfe zuerst, ob ein vorhandener thematischer Eintrag den neuen Zusammenhang oder Quellenzugang aufnehmen kann. Halte den Index kurz und thematisch brauchbar. Wiederholung desselben Arbeitsstands allein verlangt keinen weiteren Eintrag. Formuliere Vorschläge, tatsächliche Zustimmung, offene Fragen und die zeitliche Geltung ihrem belegten Zusammenhang entsprechend, ohne zusätzliche Kategorien einzuführen.

Bevorzuge den vorhandenen erreichbaren Originaltext. Ein Quellenhinweis muss die passende Passage wiederfinden lassen: bei Dateien etwa relativer Pfad und Abschnitt oder Suchphrase; bei Chats bekannte Chatkennung oder Link, soweit verfügbar Turn- oder Nachrichtenkennung, dazu Abschnitt oder kurze Suchphrase und der relevante Zusammenhang. Halte nur tatsächlich bekannte Angaben fest; erfinde keine Kennungen oder Anker. Diese Hinweise bleiben freier Text, keine zusätzlichen Schemafelder. Wähle gezielt Originalbeiträge; umfangreiche Werkzeugausgaben sind nur bei tatsächlichem Quellenbedarf einzulesen.

Prüfe bei einer neuen Chatfundstelle, dass die Kennung den gemeinten Originalbeitrag im zugeordneten Projekt bezeichnet. Bei einem übertragenen Auftrag kann eine Kennung den sendenden Chat bezeichnen; sie ist damit keine Fundstelle der danach im aktuellen Chat entstandenen Ausarbeitung. Übernimm verlässlich zugeordnete Kennungen auch in Links unverändert. Fehlt eine solche Fundstelle, benenne die Zugangslücke statt einen scheinbar vollständigen Quellenhinweis einzutragen. Nutze bereits belegte Fundstellen direkt; ihre Abwesenheit aus einer Chatliste belegt weder fehlende Erreichbarkeit noch falsche Projektzuordnung.

Ein auffindbarer und tatsächlich lesbarer Originalchat genügt als Quelle; lege dafür keine zusätzliche Belegdatei an. Ein Link allein belegt weder Erreichbarkeit noch erfolgte Lektüre. Prüfe vor einer Ersatzkopie den tatsächlich verfügbaren Originalzugang. Fehlt der nötige Zugang oder würde der relevante Wortlaut sonst verloren gehen, erhalte nur den erforderlichen Originalauszug mit Zusammenhang in einer normalen lokalen Datei außerhalb des Archivs. Benenne das konkrete Zugangs- oder Erhaltungsproblem kurz beim Quellenhinweis oder Auszug. Das gilt auch für entscheidende historische Passagen einer veränderlichen Arbeitsdatei ohne nutzbaren Originalzugang. Für Aussagen über deren aktuellen Stand lies die aktuelle Datei. Zitiere nur tatsächlich vorliegende Passagen; neue eigene Texte bleiben von erhaltenen Originalen unterscheidbar. Lege für das Gedächtnis keine routinemäßige zusätzliche Belegablage wie `sources/` an. Ein vollständiger Chatexport oder zusätzliches Quellenformular ist nicht erforderlich.

Originalbelege werden bei Aufarbeitung nicht bereinigt. Fehlende Wortlaute bleiben ausdrücklich benannte Lücken. Schließe zusammengehörige Fortschreibung und Pflege mit Prüfung und Sicherung des neuen Gedächtnisstands ab, auch bei neuen Einträgen oder einfachen Ergänzungen. Vor ersetzender Überarbeitung vorhandener Inhalte muss deren aktueller Ausgangsstand bereits gesichert sein; ein zusätzliches Vorherpaket ist nur bei noch ungesichertem Bestand nötig. Einzelne Dateischreibvorgänge erfordern keine eigenen Sicherungen.

## Pflege in zwei Stufen

### Laufende Pflege

Achte während der Projektarbeit selbstständig auf erschwerte Suche, wiederholte Fehlgriffe, Doppelungen, Widersprüche, verlorene Fundstellen und unnötig ausführliche Einträge. Behebe Auffälligkeiten und reorganisiere Inhalte innerhalb des geltenden Gedächtnisverfahrens: Einträge kürzen, ergänzen, zusammenführen oder teilen, Themen neu ordnen und den Index anpassen. Diese Pflege benötigt weder eine gesonderte Nutzerfreigabe noch einen Bericht oder eine eigene Meldung im Chat. Der Umfang allein macht eine inhaltliche Reorganisation nicht zum funktionalen Umbau. Eine Vollprüfung bei jeder Antwort ist nicht verlangt.

Behebe erkannte defekte Indexverweise und unzutreffende Quellenhinweise nach Sicherung. Kannst du die richtige Fundstelle noch nicht feststellen, kennzeichne den bisherigen Hinweis als unbrauchbar und benenne die konkrete Lücke. Erhalte historisch gültige Vorgaben und heutige Anforderungen in ihrem lesbaren Zusammenhang. Originalbelege und bestätigte Regeln werden durch laufende Pflege nicht umgeschrieben; die Fortschreibung des Projektkontexts folgt bereits belegten Änderungen. Melde Hindernisse oder Quellenlücken, soweit sie die laufende Arbeit beeinträchtigen.

Prüfe anlassbezogen, ob die Pflegeanweisungen zu brauchbarer Orientierung führen oder wiederholt nötige Pflege verhindern beziehungsweise unnötige Arbeit auslösen. Ein erkannter Bedarf zur Änderung des Verfahrens oder seiner Regeln gehört in die zweite Stufe.

### Funktionaler und struktureller Umbau

Grundlegende Änderungen im Projekt, ein ausdrücklicher Auftrag oder eine dafür eingerichtete Automatisierung können eine vertiefte Prüfung des Gedächtnisses und seiner Anweisungen auslösen. Prüfe Zweck, Aufbau, Quellenzugänge und Verfahren samt örtlichen Regeln und dem gemeinsam verwendeten Skill. Ein Umbau verändert die Funktionsweise oder vereinbarte Struktur, etwa Sicherungsverfahren, Quellenerschließung oder verbindliche Anweisungen; normale inhaltliche Neuordnung bleibt laufende Pflege.

Bereite nötige Änderungen konkret zur Prüfung vor und erkläre sie direkt im betreffenden Projektchat: beobachtetes Problem, Änderungstext beziehungsweise Entwurf, Geltungsbereich, erwartete Wirkung und wesentliche Abwägungen. Setze funktionale oder strukturelle Umbauten und Regeländerungen erst nach Nutzerfreigabe um. Eine schon erteilte Freigabe für den konkreten Umfang gilt weiter. Der Start einer Automatisierung erlaubt die beauftragte Prüfung und laufende Pflege, erteilt allein aber keine Freigabe für einen Umbau. Vorschläge gelten bis zur Freigabe nicht als Anweisungen.

Steht eine Nutzerentscheidung aus, schließe den Lauf mit dem konkreten Vorschlag und der Freigabefrage ab. Prüfe bei späterer Freigabe den inzwischen aktuellen Bestand und setze den benannten Umfang um. Eine reine Funktionsprüfung braucht keine vorsorgliche Sicherung des gesamten Bestands; die Sicherungspflicht gilt vor aufarbeitenden Schreibänderungen.

Freigegebene örtliche Regeländerungen gehören ins Profil oder die Zielprojektregeln. Änderungen am gemeinsam verwendeten Skill benötigen einen dafür freigegebenen Entwicklungsumfang und die Prüfung ihrer Auswirkungen auf andere Projekte. Schreibe keine anderen Chats ungefragt an.

Ein begrenzter Wächter-Subagent kann bei verfügbarer Funktion und erkennbarem Nutzen prüfen und an das verantwortliche Modell berichten. Er läuft nicht ständig. Eine ausdrücklich eingerichtete native Automatisierung kann die vertiefte Prüfung in einem eigenen Projektchat starten. Beide beachten dieselben Projektgrenzen, Sicherungsschritte und Freigaben.

Der regelmäßige Check prüft vorrangig Verbesserungspotenziale von Funktion, Struktur und Regeln, auch die Angemessenheit seines Starttakts, der freigegebenen Generationenzahl und Rückkehrpunktreserve sowie der Zugriffskoordination: Warteaufwand, unnötig lange Reservierung, vergessene Freigabe und ausstehende Fortschreibung. Änderungen dieser Verfahrensgrenzen gehören als konkrete begründete Vorschläge zur zweiten Pflegestufe und werden erst nach Freigabe angewendet. Eine Änderung von Takt, Modell oder Aktivierung wird ebenfalls konkret vorgeschlagen und erst im freigegebenen Umfang nativ eingerichtet; ein Profiltext allein verändert keine Automatisierung.

## Sicherung bei Pflege und Umbau

Sichere nach jedem zusammenhängenden geprüften Fortschreibungs- oder Pflegepaket den neuen Gedächtnisstand. Vor ersetzender Aufarbeitung und Wiederherstellung muss der aktuelle Ausgangsstand gesichert sein; prüfe zuerst, ob dies bereits zutrifft. Reine Neuanlage und additive Fortschreibung brauchen keine zusätzliche Vorhersicherung. Unveränderte schon gesicherte Stände benötigen weder einen leeren Commit noch eine identische neue Kopie. Details einschließlich technischer Prüfung und Bereinigung stehen in [references/backup.md](references/backup.md). Das im Profil beschriebene Verfahren gilt; wechsle es bei Fehlern nicht stillschweigend.

- **Eigenes Gedächtnis-Git:** Richte Git ausdrücklich auf das eigene `project-memory/`-Repository. Sichere den tatsächlichen zugehörigen Bestand als Commit, einschließlich neuer, geänderter und ignorierter Dateien. Erhalte fremde Vormerkungen. Bei gesichertem Ausgangsbestand genügt normalerweise ein Ergebniscommit pro Paket; noch ungesicherte vorhandene Inhalte kommen vor ersetzender Bearbeitung als zusätzlicher Commit hinzu. Keine Historienbereinigung durch die Kopienregel.
- **Vollständige Kopien:** Kopiere den ganzen aktiven Bestand einschließlich versteckter zugehöriger Dateien in einen neuen datierten Archivunterordner und prüfe Pfade und Inhalte technisch. Nach neuer geprüfter Kopie wende nur die örtlich konkret freigegebene Aufbewahrung an: Standard 20 neueste geprüfte Generationen plus höchstens drei benannte Rückkehrpunkte, Überschneidungen einmal gezählt. Neueste geprüfte und laufend benötigte Stände bleiben geschützt. Lösche nur eindeutig überzählige zugeordnete Generationen nach den Zielprüfungen in backup.md; ohne entsprechende Freigabe und bei unklaren Altbeständen bleiben Kopien erhalten.

Neue, geänderte und ignorierte zugehörige Gedächtnisdateien gehören zum aktuell zu sichernden Bestand. Ihr ungesicherter Zustand allein belegt keine gleichzeitige Bearbeitung. Sichere nicht nur einen älteren bereits bekannten Stand. Vergleiche vor dem Schreiben innerhalb der eigenen Reservierung den betroffenen Dateistand erneut; bei tatsächlich erkennbarer Überschneidung erhalte die Änderungen und kläre den Konflikt. Die kooperative Reservierung ersetzt diesen Abgleich nicht und verhindert keinen regelwidrigen direkten Zugriff.

Scheitert die nötige Vorhersicherung, beginne keine ersetzende Aufarbeitung. Scheitert die Ergebnissicherung, erhalte den aktiven Stand und melde, dass dieser noch ungesichert ist; bereinige keine alten Kopien. Eine lesende Funktionsprüfung kann weitergehen. Eine leere Git-Sperre allein belegt keine gefahrlose Entfernbarkeit; technische Reparatur folgt nur dem autorisierten Umfang.

Erhalte bei Aufarbeitung wesentliche Zusammenhänge, Begründungen, offene Einwände und Quellenzugänge. Alter allein rechtfertigt keine Entfernung. Prüfe betroffene Verweise und Kennzeichnungen und passe den Index an. Beide Sicherungswege schützen den Gedächtnisbestand, nicht automatisch außerhalb liegende Originalquellen.

## Eignung der Regeln und Ergebnisse der vertieften Prüfung

Prüfe insbesondere: Führen knappe Hinweise zur passenden Originalstelle? Bleibt die Quellensuche im zugeordneten Projekt? Werden Quellen unnötig kopiert, zusammengefasst oder vollständig eingelesen? Wurde nötige Pflege übersehen, unnötig ausgelöst oder zu umfangreich ausgeführt? Weniger Tokens sind ein zu prüfendes Ziel, keine zugesicherte Eigenschaft jedes Abrufs. Eine Prüfung kann ergeben, dass kein Umbau nötig ist.

Erkläre Befunde, Entwürfe und vollständige Regelvorschläge der zweiten Stufe im betreffenden Chat. Erhalte im Gedächtnis nur weiter relevante Orientierung und deren Originalfundstellen. Eine zusätzliche Berichtsdatei braucht einen konkreten zusätzlichen Projektzweck oder Auftrag. Daraus entsteht keine Berichtspflicht für die laufende Pflege.

## Umzug und Arbeitskopien

Ein Umzug desselben Projekts übernimmt Bestand und örtliche Historie und behält `project_id`; kläre vorher laufende Zugriffe und übernimm den temporären Marker nicht als laufende Reservierung. Prüfe danach Pfade, Quellenzugänge, Regeln und Sicherungsverfahren. Clone oder neuer Worktree des äußeren Git übernehmen das ausgeschlossene Gedächtnis nicht automatisch. Melde fehlenden Bestand, ohne Ersatz, leeres Gedächtnis oder neue Kennung automatisch anzulegen.

Bei ausdrücklich beauftragter Übernahme behält eine weitere Arbeitskopie desselben Projekts die Kennung; ein unabhängig weitergeführtes Projekt erhält eine neue. Ordne übernommene Einträge im zweiten Fall dem neuen Projekt zu und prüfe Quellenzugänge, ohne Originalbelege umzuschreiben. Frage nur, wenn der konkrete Zweck unklar ist. Es gibt keine automatische Synchronisierung. Bei beauftragter Zusammenführung prüfe auseinanderentwickelte Inhalte, Kennungskollisionen und Verweise, bevor Bestände ersetzt werden.
