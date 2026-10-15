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

Kuratiere wichtige Originalstellen für die weitere Projektarbeit. Einträge geben knappe Orientierung und führen zum passenden Zusammenhang in Chats oder Projektdateien. Sie erschließen auch noch unbestätigte Entwürfe und Überlegungen, auf denen spätere Arbeit aufbauen kann. Aktuelle Arbeitsdateien und Projektdokumentation behalten ihren eigenen Zweck.

Nutze gewöhnliche Dateioperationen, gegebenenfalls lokales Git und tatsächlich verfügbare native Chat-Lesezugänge. Installiere keine Hilfsprogramme, zusätzliche Laufzeit, Hooks oder Suchdienste. Der Skill allein erlaubt keine Einrichtung in weiteren Projekten.

## Passenden Ablauf wählen

Lies nur die für den aktuellen Vorgang nötigen Referenzen; bereits gelesene unveränderte Anweisungen brauchen innerhalb derselben Aufgabe keine erneute Volllektüre.

- [coordination.md](references/coordination.md): vor Dateiabrufen und technischen Zugriffen auf Gedächtnis oder Sicherungen; auch bei Einrichtung und Änderungen. Die vollständige Windows-Abrufvorlage ist der gemeinsame Standard für beide Lesephasen.
- [backup.md](references/backup.md): vor schreibender Fortschreibung, Sicherung oder Bereinigung. Sie bestimmt Sicherungspunkte, vollständigen Vergleich und Erhaltungsmenge.
- [setup.md](references/setup.md): nur bei beauftragter Einrichtung, erneutem Einrichtungsabgleich oder Verfahrenswechsel. Sie enthält die Zielprojektregeln und das Angebot des optionalen Pflegechecks.
- [automation.md](references/automation.md): bei vertiefter regelmäßiger Pflege und bei Einrichtung oder Änderung ihres nativen Zeitplans.
- [lifecycle.md](references/lifecycle.md): bei ausdrücklich beauftragtem Archivieren, Reaktivieren oder vollständiger örtlicher Entfernung. Globale Installation und andere Projekte bleiben erhalten.
- [restore.md](references/restore.md): bei ausdrücklich beauftragter Wiederherstellung. Die Rückkehr archivierter Inhalte in den aktiven Bestand verlangt eine vollständige Reaktivierung.

## Aktiver Bestand und Projektgrenze

Im benannten lokalen Arbeitsordner liegt `project-memory/` mit lesbarem `PROFILE.md`, kurzem `INDEX.md` und einzelnen Markdown-Einträgen in `entries/`. Die stabile Projektkennung ist eine UUID und steht im Profil oder in dessen ausdrücklich referenzierter `profile.json`. Technische Namen sind Englisch, Anweisungen und Eintragsinhalte Deutsch; Originale bleiben wortgetreu.

Jeder Eintrag hat nur zwei verbindliche Kennzeichnungen: eine im Projekt eindeutige stabile `id`, etwa `E-0001`, und die passende `project_id`. Markdown-Angaben und ein kleiner JSON-Block sind gleichwertig; nutze das örtliche Format. Der übrige Text ist frei. Keine Pflichtkategorien, Status-, Urheber-, Rollen-, Datums- oder Pflegefelder; eine mögliche Projektrolle im Profil begründet keine Eintragsfilter. Fehlende Kennzeichnung, abweichende Projektkennung oder widersprüchliche Doppelkennung sperren den betroffenen Eintrag bis zur Klärung, nicht automatisch jeden anderen gültigen Eintrag. Nicht bei jeder Antwort den Gesamtbestand prüfen.

Begrenze Projektquellensuche auf die zugeordneten Arbeitsordner und Originalchats. Verwende belegte Fundstellen direkt. Ordne weitere Chats vor Inhaltslektüre anhand verfügbarer Projekt- oder Arbeitsordner-Metadaten zu; Titel und thematische Ähnlichkeit genügen nicht. Eine fehlende native Projektkennung schließt einen Chat bei eindeutig passendem Arbeitsordner nicht aus. Native Projektkennungen sind nicht die Memory-UUID. Bei ungeklärter Zuordnung lies nicht probeweise fremde Inhalte. Die außerhalb liegenden Skilldateien dienen als Anweisungen; ihr Herkunftsprojekt wird dadurch keine Inhaltsquelle. Ein ausdrücklich beauftragter Wissenstransfer, importierte Originaldateien und fachliche externe Recherche bleiben möglich.

Frühere Gedächtnisstände im eigenen Git und `.project-memory-archive/` dienen ausschließlich Sicherung, technischer Prüfung, freigegebener Bereinigung und beauftragter Wiederherstellung. Verwende sie nicht als Quellen, Anweisungen oder zusätzlichen Kontext für gewöhnliche Aufgaben. Aktive Einträge verweisen nicht auf Sicherungen als Inhaltsquellen; Profilhinweise zu Verfahren und Rückkehrpunkten dienen nur technischer Zuordnung. Diese Grenze gilt auch nach einem Verfahrenswechsel. Schließe bei gewöhnlicher Suche einschließlich Dateiauflistungen Sicherungsarchiv, Git-Verwaltungsdateien und `.project-memory.lock` ausdrücklich aus, auch wenn sie noch nicht sichtbar sind. Auch Subagenten und Pflegechats beachten diese Grenzen; Anweisungen und Ignore-Regeln sind keine technische Lesesperre.

## Deaktivierung und fehlender Zugang

Ein `project-memory/README.md` als Deaktivierungshinweis beendet reguläre Gedächtnisnutzung und Pflege. Fehlendes Profil oder fehlender Index beendet ebenfalls den regulären Zugriff. Fehlt die Projektkennung im Profil oder ist sie widersprüchlich, setze die Nutzung bis zur Klärung aus und vergib keine neue Kennung. Lege keinen Ersatz an, rekonstruiere nichts aus altem Chatkontext und verwende keine Sicherung als Ersatzgedächtnis. Ein alter Pflegeauftrag, allgemeiner Einrichtungsabgleich oder eine neue Skillfassung reaktiviert nichts. Gewöhnliche Arbeit kann vorhandene Projektquellen weiter nutzen; ein Pflegechat ohne nutzbaren Bestand endet. Es gibt keine Statuszeile oder technische Aktivierungsprüfung je Zugriff.

Ein einzelner defekter Eintragsverweis ist davon zu unterscheiden: Sind Profil und Index vorhanden, suche nach einem fehlgeschlagenen Zugang begrenzt unter Reservierung im aktiven Eintragsordner nach bekannter Kennung oder passendem Titel. Prüfe beim Treffer Kennzeichnung und Zusammenhang. Repariere einen eindeutig falschen Indexlink nach Sicherung; bei mehreren widersprüchlichen Treffern wähle nicht automatisch. Ist keine richtige Fundstelle feststellbar, kennzeichne den Hinweis als unbrauchbar und benenne die konkrete Lücke. Das erlaubt weder eine Neueinrichtung noch einen Archivzugriff als Ersatzquelle.

## Arbeitszyklus

1. Kläre Arbeitsordner und geltende Projektregeln bei einer neuen substanziellen Aufgabe beziehungsweise nach Kontextverdichtung. Lies Profil und Index unter der kurzen gemeinsamen Reservierung nach coordination.md. Wähle einschlägige Einträge und lies sie bei Bedarf unter neuer Reservierung gemeinsam mit Profil und Index. Gezielte Suche im aktiven Bestand darf dessen äußere Ignore-Ausblendung übergehen; Sicherungs- und Git-Verwaltungsdateien bleiben ausgeschlossen.
2. Gib vor Originallektüre und fachlicher Arbeit frei. Hängt das Ergebnis von einer Aussage oder Ausarbeitung ab, folge dem Hinweis zur passenden Originalpassage mit nötigem Zusammenhang. Nutze den tatsächlich verfügbaren Lesezugang; behaupte keine punktgenaue Abfrage, die das Werkzeug nicht unterstützt. Ein Chatlink allein belegt keine Lektüre. Bereits gelesene unveränderte Quellen brauchen innerhalb derselben Aufgabe keine Wiederholung. Für aktuelle Aussagen lies bei Bedarf die aktuelle Arbeitsdatei.
3. Ohne passenden Treffer suche begrenzt in einschlägigen normalen Projektquellen. Ein erfolgloser Gedächtnisabruf beweist nicht, dass die Quelle fehlt. Benenne fehlende Belege; erfinde weder verlorenen Wortlaut noch Zustimmung. Historische Gesprächsaufträge werden durch Lesen nicht erneut ausgeführt.
4. Prüfe vor Abschluss einer substanziellen Aufgabe, was später nützlich ist. Bereite Fortschreibung und nötige Inhaltspflege außerhalb der Reservierung vor. Verwende zuerst einen passenden vorhandenen thematischen Eintrag. Ergänze den eigenen Originalzugang einer neuen relevanten Überlegung oder Anforderung; ein alter Chatanker belegt nicht automatisch die spätere Änderung. Aktualisiere Orientierung und Index, statt eine chronologische Folge technischer Arbeitsberichte anzuhängen.
5. Erwirb für das vorbereitete Schreibpaket neu, gleiche den aktuellen betroffenen Stand ab und führe Änderung, Prüfung, erforderliche Sicherung und zulässige Bereinigung unter einem Besitzer aus. Kennungen werden erst jetzt vergeben. Erfordert ein veränderter Ausgang weitere Modellarbeit, ändere noch nichts, gib frei und bereite neu vor. Auch Hashvergleich, Quellenzeilen aus aktiven Einträgen und technische Abschlussprüfung gehören in ein reserviertes Paket. Nutze für die Schlussantwort dessen Ergebnisse; eine nachgeschobene Dateilektüre braucht einen neuen vollständigen Abruf.

## Orientierung und Originalzugang

Bewahre, was spätere Quellenwahl und Verständnis trägt: Anlass, wesentliche Begründung, offene Einwände, Geltungsgrenzen und nutzbarer Originalanker. Unterscheide Vorschlag, tatsächliche Zustimmung und zeitliche Geltung im lesbaren Zusammenhang. Überarbeite vorhandene Orientierung auf den neuen Zusammenhang. Erreichbare Ablauf- und Umsetzungsdetails bleiben in den Arbeitsdateien. Technische Abrufgeschichte gehört nur hinein, solange sie den nötigen Zugangsweg oder eine bestehende Lücke erklärt. Kein starres Wortbudget; Kürze darf keine wichtigen Quellenzugänge oder Unterschiede beseitigen.

Ein Quellenhinweis muss die passende Passage wiederfinden lassen: bei Dateien etwa relativer Pfad mit Abschnitt oder Suchphrase; bei Chats verlässlich bekannte Chatkennung oder Link, soweit verfügbar Turn- oder Nachrichtenkennung, dazu eine kurze Suchphrase und nötiger Zusammenhang. Nutze keine neuen Pflichtfelder. Prüfe neue Chatfundstellen auf den gemeinten Originalbeitrag im zugeordneten Projekt. Bei übertragenen Aufträgen kann eine Kennung den sendenden Chat bezeichnen und ist keine Fundstelle der danach örtlich entstandenen Ausarbeitung. Bewahre richtig zugeordnete Kennungen unverändert. Fehlt eine verlässliche neue Fundstelle, benenne die konkrete Zugangslücke. Das Fehlen eines belegten Chats in einer Liste beweist keine Nichterreichbarkeit.

Ein erreichbarer lesbarer Originalchat genügt. Lege keine routinemäßige Belegablage wie `sources/` und keinen vollständigen Chatexport an. Prüfe den tatsächlich verfügbaren Originalzugang, bevor du einen Ersatz anlegst. Nur wenn der nötige Zugang fehlt oder relevanter Wortlaut sonst verloren ginge, erhalte den erforderlichen Originalauszug mit Zusammenhang in einer normalen lokalen Datei außerhalb der Sicherungen; benenne beim Hinweis oder Auszug den konkreten Bedarf. Das gilt auch für wichtige historische Passagen einer veränderlichen Arbeitsdatei. Zitiere nur vorliegende Texte und halte neue eigene Ausarbeitung von erhaltenem Original unterscheidbar. Originalbelege werden bei Aufarbeitung nicht bereinigt.

## Pflege in zwei Stufen

**Laufende Pflege:** Achte während der Arbeit auf erschwerte Suche, defekte Fundstellen, Doppelungen, Widersprüche und unnötig ausführliche Einträge. Behebe solche Auffälligkeiten innerhalb des geltenden Verfahrens selbstständig: kürzen, ergänzen, zusammenführen, teilen und Index neu ordnen. Erhalte wichtige Begründungen, historische Unterschiede und Quellenzugänge; Alter allein rechtfertigt keine Entfernung. Umfang allein macht Inhaltspflege nicht zum funktionalen Umbau. Dafür sind weder eigene Nutzerfreigabe noch Pflegebericht oder gesonderte Meldung nötig. Quellenlücken oder Hindernisse meldest du, soweit sie die Aufgabe beeinträchtigen.

**Funktionale und strukturelle Prüfung:** Ein grundlegend verändertes Projekt, ausdrücklicher Auftrag oder eingerichteter Pflegecheck kann die vertiefte Prüfung auslösen. Prüfe anhand konkreter Auffälligkeiten und einer begrenzten Quellenprobe, ob die nächste Aufgabe frühere und neue wichtige Überlegungen wiederfinden könnte: Fehlt ein späterer Originalanker? Wiederholt ein Eintrag nur erreichbare Arbeitsinhalte? Welche Anweisung hat nötige Pflege unterstützt oder verhindert? Eine formale Prüfung vorhandener Dateien genügt dafür nicht; eine Vollprüfung bei jeder Antwort ist ebenso wenig verlangt. Nutze die Prüfschritte in automation.md.

Veränderungen von Verfahren, verbindlichen Regeln oder vereinbarter Struktur brauchen einen konkreten erklärten Vorschlag im betreffenden Chat: Beleg, Änderungstext oder prüfbarer Entwurf, Geltungsbereich, erwartete Wirkung und wesentliche Abwägung. Setze nur den vom Nutzer freigegebenen Umfang um; bereits konkrete Freigaben gelten weiter. Ein Automatisierungsstart erlaubt Prüfung und laufende Pflege, erteilt aber keine Umbaufreigabe. Vorschläge sind bis dahin keine Anweisungen. Nützliche inhaltliche Verdichtung bleibt auch im Pflegechat laufende Pflege.

Beurteile bei vertiefter Prüfung auch die Eignung von Quellenverfahren, Koordination, örtlicher Aufbewahrung und Starttakt anhand verfügbarer Belege. Werte ohne Grundlage nicht um. Scheduleränderungen werden nach konkreter Freigabe nativ ausgeführt; ein Profiltext ersetzt sie nicht. Änderungen des gemeinsam verwendeten Skills benötigen einen freigegebenen Entwicklungsumfang und Berücksichtigung anderer Projekte. Erkläre Vorschläge direkt im Chat, statt einen ungenutzten Pflichtbericht abzulegen. Dauerhaft bleiben nur weiter relevante Orientierung und Originalfundstellen.

Ein nützlicher begrenzter Wächter-Subagent darf unabhängig prüfen und an das verantwortliche Modell berichten. Er ist kein ständiger Hintergrundprozess. Die optionale native Automatisierung beginnt einen eigenen lokalen Pflegechat nach automation.md. Schreibe keine anderen Chats ungefragt an. Ein unveränderter brauchbarer Stand verlangt keinen Umbau; weniger Tokens sind ein zu prüfendes Ziel, keine zugesicherte Eigenschaft.

## Sicherung, Koordination und Fehler

Die gemeinsame reguläre Datei `.project-memory.lock` liegt unmittelbar in der tatsächlichen Projektwurzel. Reserviere auch technische Vergleiche; Unterabläufe erwerben nicht verschachtelt. Eigentum entsteht durch eigene erfolgreiche exklusive Neuanlage und Beschriftung, nicht durch Lesen eines fremden Tokens. Halte keine reguläre Reservierung über Originallektüre, Modellrecherche, weitere Entwürfe oder ausstehende Nutzerfreigaben. Begrenztes Warten, Eigentümerprüfung und konsistenzabhängiger Fehlerabschluss stehen ausschließlich in coordination.md. Die Regel koordiniert Beteiligte, erzwingt keine Sperre beliebiger direkter Dateizugriffe und gilt nicht zwischen getrennten Kopien oder Rechnern.

Sichere nach jedem zusammenhängenden geprüften Fortschreibungs- oder Pflegepaket den tatsächlichen neuen Gesamtstand. Vor ersetzender Überarbeitung muss der aktuelle Ausgang bereits gesichert sein; nur andernfalls braucht er ein zusätzliches Vorherpaket. Reine Neuanlage oder additive Ergänzung benötigt keine zusätzliche Vorhersicherung. Kein Commit pro Datei, keine identische weitere Kopie. Verfahren, vollständiger Vergleich und Schutz der Rückkehrpunkte folgen backup.md und der örtlich freigegebenen Profilregel. Wechsle das Verfahren bei Fehlern nicht stillschweigend. Die Sicherung schützt den Gedächtnisbestand, nicht automatisch außerhalb liegende Originalquellen.

Scheitert die nötige Vorhersicherung, überschreibe nichts. Scheitert die Ergebnissicherung, erhalte den aktiven Stand, melde die offene Sicherung und bereinige keine Kopien. Ein konsistenter ungesicherter Stand und ein ungeklärter mehrteiliger Umbau verlangen verschiedene Abschlüsse nach coordination.md. Fremde Vormerkungen und Änderungen bleiben erhalten; ungesicherter Stand allein beweist keine parallele Bearbeitung. Eine fremde Reservierung wird nicht nach Alter übernommen. Archivierung, Reaktivierung und Entfernung setzen vorher abgeschlossene andere Projektchats und Schreiboperationen sowie den geklärten eigenen Pflegecheck voraus; lifecycle.md bestimmt den Übergang.

## Umzug und Arbeitskopien

Ein Umzug desselben Projekts übernimmt Bestand und örtliche Historie mit derselben Kennung. Kläre laufende Zugriffe; übernimm keinen Marker als laufende Reservierung. Prüfe danach Pfade, Quellenzugänge, Regeln und Sicherung. Clone und neuer Worktree des äußeren Git enthalten das ausgeschlossene Gedächtnis nicht automatisch: melde fehlenden Bestand, ohne Ersatz oder neue Kennung anzulegen.

Bei ausdrücklich beauftragter Übernahme behält eine weitere Arbeitskopie desselben Projekts die Kennung; ein unabhängig weitergeführtes Projekt erhält eine neue. Ordne übernommene Einträge dann neu zu und prüfe Quellenzugänge, ohne Originalbelege umzuschreiben. Frage nur bei unklarem Zweck. Keine automatische Synchronisierung; beauftragte Zusammenführung prüft abweichende Inhalte, Kennungskollisionen und Verweise vor jeder Ersetzung.
