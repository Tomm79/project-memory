# Kooperative Zugriffskoordination

Lies diese Referenz vor dem ersten Zugriff auf ein vorhandenes Gedächtnis und vor Einrichtung, Fortschreibung, Sicherung, Wiederherstellung oder Archivbereinigung. Alle Chats, Pflegechats und Subagenten am selben örtlichen Bestand verwenden dieses Verfahren. Es koordiniert regelkonforme Zugriffe; gewöhnliche Schreibrechte anderer Programme oder eines abweichenden Chats bleiben bestehen. Ein Änderungspaket wird dadurch nicht zu einer absturzsicheren Transaktion.

## Gemeinsame Reservierung

Bestimme aus dem beauftragten Arbeitsordner die tatsächliche örtliche Projektwurzel. Verwende genau die reguläre Datei `.project-memory.lock` unmittelbar darin, außerhalb von `project-memory/` und `.project-memory-archive/`. Verschiedene Pfadschreibweisen desselben Bestands dürfen keine getrennten Reservierungen ergeben. Symlinks, Junctions, Verzeichnisse oder Sonderdateien am Markerpfad sind ein Klärungsfall. Der Entwurf gilt für denselben Bestand auf einem gewöhnlichen lokalen Dateisystem; Synchronisationskopien und mehrere Rechner werden nicht dadurch koordiniert.

Erzeuge den Marker exklusiv in einer Dateisystemoperation, die bei vorhandener Datei fehlschlägt. Eine Existenzprüfung mit anschließendem gewöhnlichem Schreiben reicht nicht. Erst erfolgreiche Erstellung und Beschriftung erlauben den Zugriff. Verwende eine neue zufällige UUID als `owner_token` je Reservierung. Halte außerdem `created_at` als UTC-Zeit und `purpose` als kurzen lesbaren Anlass fest; eine tatsächlich bekannte Chatkennung kann ergänzen. Das sind technische Angaben im temporären Marker, keine neuen Eintrags- oder Profilfelder oder Projektanweisungen. Die Startzeit ist keine Ablaufzeit. Eigentum verlangt deinen eigenen nachweislich erfolgreichen Erwerb; das Lesen einer fremden Besitzerkennung erlaubt keine Übernahme.

Ein vorhandener leerer, unlesbarer oder unvollständig beschrifteter Marker gilt ebenfalls als belegt beziehungsweise ungeklärt. Fehler wegen Rechten, Pfaden oder fehlgeschlagener Beschriftung sind keine gewöhnliche Belegtmeldung. Installiere keine Laufzeit oder Helfer, wenn die nötige exklusive Operation fehlt; halte den Gedächtniszugriff an und benenne das Hindernis. Erfasse und erhalte eigene Besitzerkennung und absoluten Markerpfad für den Abschluss.

## Kurze Zugriffspakete

Prüfe vor jedem Paket die aktuelle äußere Aktivierung aus SKILL.md und unmittelbar nach erfolgreichem Erwerb nochmals, bevor Profil, Index oder Einträge gelesen oder verändert werden. Bei inzwischen `paused`, `archived` oder ungeklärtem Zustand führe einen vorbereiteten regulären Zugriff nicht aus und gib den selbst erworbenen Marker ohne Inhaltsänderung frei. Der übrige Auftrag darf normale Projektquellen nutzen; ein Pflegechat endet ohne Gedächtnisarbeit. Ausdrücklich beauftragte Einrichtung, Lebenszyklusübergänge oder technische Wiederherstellung verwenden ihren begrenzten Umfang; sie leiten daraus keine allgemeine Aktivierung ab. Die Reservierung allein erlaubt keinen Zugriff auf einen deaktivierten Bestand.

Bündele im Normalfall Erwerb, die vorbereiteten Dateioperationen und die konsistenzabhängige Freigabe in einem gewöhnlichen Datei-/Shellaufruf. Halte den Marker möglichst nicht über weitere Modellrunden oder Werkzeugfreigaben hinweg. Für die Eintragsauswahl kannst du zunächst Profil und Index gemeinsam lesen und freigeben; lies beim danach gezielt reservierten Abruf Profil, Index und gewählte Einträge nochmals zusammen. Das verbindet einen konsistenten Abruf mit kurzer Reservierung. Eine nur vorab angelegte Datei, deren Freigabe erst ein späterer Werkzeugaufruf ausführt, kann andere Chats während dessen Blockade unnötig aussperren.

Bereite ein Schreibpaket außerhalb des Markers anhand der gelesenen Inhalte vor. Weicht der unter neuer Reservierung gelesene betroffene Stand inzwischen ab und verlangt der Abgleich weitere Modellarbeit, ändere noch nichts, gib frei und bereite die Ergänzung auf diesem aktuellen Stand neu vor. Gib nach einem bereits teilweise ausgeführten Paket nur nach der Konsistenzregel unten frei. Ein unerwartet blockierter weiterer Werkzeugaufruf wird zuerst beendet beziehungsweise geklärt; eine noch laufende Operation erlaubt keine vorzeitige Freigabe.

1. **Abruf:** Erwirb die Reservierung, lies Profil, Index und gezielt benötigte Einträge beziehungsweise suche im aktiven Bestand. Gib danach frei, bevor du Originalquellen aufrufst, fachlich recherchierst oder Ausarbeitungen erstellst. Kein vollständiger Bestandsabruf allein wegen der Reservierung. Bereits übernommene Orientierung bleibt nutzbar; ein späterer neuer Dateizugriff braucht eine neue Reservierung. Eine Markerprüfung vor und nach freier Mehrdateilektüre garantiert keinen konsistenten Stand.
2. **Schreiben:** Bereite Inhalt und benötigte Originalbelege vorher vor. Erwirb dann neu, lies den betroffenen aktuellen Bestand erneut und übernimm zwischenzeitliche Änderungen. Vergib freie Kennungen erst jetzt. Halte Einträge, Index, Profil, erforderliche Vorhersicherung, Ergebnissicherung und zugehörige technische Bereinigung im selben Paket unter einem Besitzer. Die Sicherung folgt backup.md. Keine Modellrecherche oder ausstehende Nutzerfreigabe innerhalb des Pakets halten.
3. **Einrichtung, Wiederherstellung und Lebenszyklus:** Der entsprechende beauftragte Ablauf ist ebenfalls ein Paket unter dieser Reservierung. Technische Sicherungsprüfung und Bereinigung nutzen denselben Schutz. Bei Pausieren, Archivieren oder Entfernen müssen nach lifecycle.md vorher alle anderen Projektchats und ihre Schreibvorgänge abgeschlossen sein; ein freier Marker allein reicht nicht. Schedulerverwaltung erfolgt außerhalb der Reservierung. Nach Freigabe eingehende weitere Änderungen beginnen ein neues Paket und beachten die dann gültige Aktivierung.

Prüfe vor schreibenden Schritten und vor Freigabe, dass der Marker noch regulär ist und deine Besitzerkennung enthält. Bei fehlendem oder fremdem Marker halte weitere Änderungen an; übernimm keine neue Reservierung mitten in einem teilweise ausgeführten Paket, ohne den Zustand abzugleichen. Erhalte den aktiven Bestand und kläre den Verlust der Reservierung.

Ein Eigentümer koordiniert sein Paket. Sicherung und weitere Unterabläufe erwerben keine verschachtelte Reservierung. Ein Subagent darf nicht auf denselben Marker warten müssen, während sein Auftraggeber ihn hält und auf den Subagenten wartet. Delegierte Quellenarbeit geschieht außerhalb des Pakets; der Eigentümer führt die abschließenden Gedächtnisänderungen aus.

## Belegt, warten und erneut versuchen

Bei eindeutig belegtem regulärem Marker wiederhole den exklusiven Erwerb mit fünf Sekunden Abstand, höchstens 30 Sekunden in einer Wartephase. Bündele die kurzen Versuche möglichst in einem gewöhnlichen Datei-/Shellaufruf. Kein dauerhaft laufender Prozess, keine Warteschlange und keine neue Automatisierung sind dafür erforderlich. Der erste erfolgreiche Erwerb beendet das Warten und reserviert unmittelbar; eine gesonderte Frei-Meldung gibt es nicht. Mehrere Wartende erhalten keine garantierte Reihenfolge.

Bleibt der Zugriff belegt, erledige vorhandene unabhängige Arbeit. Danach ist für denselben nötigen Zugriff höchstens eine zweite Wartephase mit derselben Grenze erlaubt; ohne unabhängige Arbeit schließe mit dem konkreten Hindernis ab. Überschreite die Grenzen nicht durch neue Schleifen oder Umbenennung des Vorgangs. Benenne ausstehenden Abruf beziehungsweise Fortschreibung und die bekannte Belegung. Keine stille Auslassung, kein fremdes Ersatzgedächtnis und kein selbstständiger Hintergrundversuch nach Ende der Modellrunde. Bei später tatsächlich fortgesetzter Arbeit ist ein neuer Versuch möglich.

Die Wartegrenze erlaubt weder Löschung noch Übernahme eines fremden Markers. Ändere Intervalle oder Grenzen nur als begründete, konkret freigegebene Verfahrensänderung. Die funktionale und strukturelle Pflege prüft Warteaufwand, zu lange gehaltene Reservierungen, vergessene Freigaben und offene Fortschreibungen; fehlende Beobachtungen rechtfertigen keine erfundenen Verbesserungsbelege.

## Abschluss, Fehler und Abbruch

Gib nach dem geprüften Paket ausschließlich deine eigene Reservierung frei: Alle zugehörigen Schreib-, Git- und Kopieraufrufe müssen tatsächlich beendet sein. Prüfe den absoluten festen Markerpfad, regulären Dateityp und exakte selbst erworbene Besitzerkennung unmittelbar davor und entferne nur diese einzelne Datei. Kein rekursives Löschen. Normale erfolgreiche Koordination braucht keine Meldung an den Nutzer.

Bei kontrolliertem Fehlerabschluss erhalte den zu erhaltenden Bestand, geprüfte Sicherungen und fremde Änderungen und prüfe die zum Ablauf passende Strukturkonsistenz: bei aktiver Nutzung Profil, Index und betroffene Einträge; bei Archivierung den Hinweis und vollständig wiederherstellbaren Rückkehrstand; bei Entfernung die tatsächlich verbliebenen Inhalte und Ausschlussregel. Ein konsistenter, aber noch ungesicherter Stand kann nach konkreter Meldung und Eigentümerprüfung freigegeben werden. Ist ein mehrteiliger Umbau unvollständig und die Konsistenz nicht geklärt, erhalte den Marker als ungeklärten Abbruch, benenne die betroffenen Teiländerungen und lasse vor normalem Abruf zuerst den Wiederanlauf prüfen. Kein stiller Rückbau fremder Arbeit. Bei gescheiterter Vorhersicherung keine ersetzende Bearbeitung beginnen; bei gescheiterter Ergebnissicherung keine Archivbereinigung anschließen. Eine bekannte ungesicherte Fassung ist beim nächsten Schreibpaket erneut abzugleichen. Falls die eigene Markerbeschriftung vor jedem Inhaltszugriff scheitert, darf nur der im selben Aufruf nachweislich selbst erzeugte Marker kontrolliert entfernt werden; bei unklarer Eigentümerschaft bleibt er erhalten.

Ein harter Abbruch kann einen Marker und ein teilweise ausgeführtes Paket zurücklassen. Alter, Wartefrist oder fehlender kurzlebiger Shellprozess beweisen kein Ende des verantwortlichen Chats. Entferne einen fremden oder ungeklärten Marker nur nach belegtem Ende des Vorgangs oder ausdrücklicher Klärung für genau diesen Umfang. Halte die bekannte Besitzerkennung fest, prüfe unmittelbar vor Entfernung denselben Marker erneut und verhindere gleichzeitig laufende Wiederanläufe. Nach Entfernung neu regulär erwerben und aktiven Bestand, Kennungen, Indexbeziehungen und Sicherungsstand prüfen, bevor weiter geschrieben wird. Ohne verlässliche Klärung bleibt der betreffende Zugriff blockiert. Ein ruhendes Projekt wird nicht automatisch weiterbearbeitet.

## Gewöhnliche Operationen unter Windows und macOS

Die folgenden Bausteine zeigen die exklusive Operation und die Eigentümerfreigabe. Verbinde sie im Normalfall mit dem vorbereiteten Zugriff in einem Aufruf nach dem vorstehenden Paketablauf; die alleinige `acquired`-Ausgabe ist kein abgeschlossener Gedächtniszugriff. Setze die Variablen aus der bereits geprüften tatsächlichen Projektwurzel und erhalte die eigene Besitzerkennung für den Abschluss. Typ- und Pfadprüfung, begrenzte Wiederholung und Fehlerabschluss aus den Abschnitten oben gelten weiterhin. Speichere dafür kein dauerhaftes Hilfsprogramm im Zielprojekt.

Lies und schreibe Marker und Gedächtnis-Markdown als UTF-8. Bei Windows PowerShell 5.1 muss die Kodierung ausdrücklich gesetzt werden, etwa durch `Get-Content -Encoding UTF8` oder `IO.File.ReadAllText` mit UTF-8; sonst können Umlaute bei aufeinanderfolgenden Änderungen beschädigt werden.

### Windows mit vorhandener PowerShell

Einzelner Erwerb, nachdem der feste Pfad und ein gegebenenfalls vorhandener Marker geprüft wurden:

```powershell
$ErrorActionPreference = 'Stop'
$memoryLockPath = Join-Path $memoryProjectRoot '.project-memory.lock'
$memoryOwnerToken = [guid]::NewGuid().ToString('D')
$memoryStream = [IO.File]::Open($memoryLockPath, [IO.FileMode]::CreateNew,
    [IO.FileAccess]::Write, [IO.FileShare]::None)
try {
    $memoryPayload = "owner_token: $memoryOwnerToken`ncreated_at: $([DateTime]::UtcNow.ToString('o'))`npurpose: $memoryPurpose`n"
    $memoryBytes = [Text.Encoding]::UTF8.GetBytes($memoryPayload)
    $memoryStream.Write($memoryBytes, 0, $memoryBytes.Length)
    $memoryStream.Flush()
} finally {
    $memoryStream.Dispose()
}
[pscustomobject]@{ status = 'acquired'; owner_token = $memoryOwnerToken }
```

Nur eine tatsächlich erkannte Dateiexistenz-Kollision wird als belegt behandelt. Unter Windows kennzeichnen bei dieser Operation die unteren 16 Bits von `IOException.HResult` mit 80 oder 183 die entsprechenden Existenzfehler. Andere Fehler anhalten und konkret einordnen. Eine bereits durchgeführte Erstellung mit anschließendem Schreibfehler ist kein erfolgloser Erwerb wegen Belegung.

Freigabe nach erneuter fester Pfad- und Typprüfung:

```powershell
$ErrorActionPreference = 'Stop'
$memoryRecordedOwner = Get-Content -LiteralPath $memoryLockPath -Encoding UTF8 -TotalCount 1
if ($memoryRecordedOwner -cne "owner_token: $memoryOwnerToken") {
    throw 'Die Reservierung gehört nicht mehr zu diesem Vorgang.'
}
Remove-Item -LiteralPath $memoryLockPath
```

### macOS mit vorhandener `/bin/sh`

Verwende die native Shell mit `set -C` für reguläre Marker. Prüfe vorher Symlinks und vorhandene Verzeichnisse beziehungsweise Sonderdateien und halte bei solchen Befunden an. Sämtliche beteiligten Schreiber erzeugen ausschließlich reguläre Marker und entfernen keine benutzte fremde Reservierung. Dann bietet die geschützte Umleitung die exklusive Neuanlage ohne zusätzliche Laufzeit. Die Beschriftung gehört zur Erfolgsprüfung:

```sh
memory_lock_path="$memory_project_root/.project-memory.lock"
memory_owner_token="$(uuidgen)" || exit 1
memory_created_at="$(date -u '+%Y-%m-%dT%H:%M:%SZ')" || exit 1
(
    umask 077
    set -C
    printf 'owner_token: %s\ncreated_at: %s\npurpose: %s\n' \
        "$memory_owner_token" "$memory_created_at" "$memory_purpose" \
        > "$memory_lock_path"
) || exit 1
printf 'acquired %s\n' "$memory_owner_token"
```

Ein Umleitungs- oder Schreibfehler verlangt Einordnung; nicht jeder Fehler bedeutet eine belegte Reservierung. Eigentümerfreigabe nach erneuter Pfad- und regulärer Typprüfung:

```sh
IFS= read -r memory_recorded_owner < "$memory_lock_path" || exit 1
[ "$memory_recorded_owner" = "owner_token: $memory_owner_token" ] || exit 1
rm "$memory_lock_path"
```

`set -C` muss vor der geschützten Umleitung in derselben Shell gelten. Ein außerhalb der Klammern platzierter Umleitungsoperator würde den dort gesetzten Schutz nicht nutzen. Die konkrete macOS-Ausführung bleibt im Zielsystem zu prüfen; ein Windows-Versuch belegt sie nicht.

Primärbelege: [Microsoft: FileMode.CreateNew](https://learn.microsoft.com/en-us/dotnet/api/system.io.filemode), [Microsoft: Systemfehler 80 und 183](https://learn.microsoft.com/en-us/windows/win32/debug/system-error-codes--0-499-), [Apple: Shell-Umleitung](https://github.com/apple-oss-distributions/shell_cmds/blob/main/sh/redir.c), [POSIX: Shell-Ausgabeumleitung](https://pubs.opengroup.org/onlinepubs/9799919799/utilities/V3_chap02.html#tag_19_07_02).
