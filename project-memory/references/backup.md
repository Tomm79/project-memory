# Sicherung und begrenzte Aufbewahrung

Lies diese Referenz beim Schreiben eines Gedächtnispakets, bei Aufarbeitung, beauftragter Wiederherstellung und technischer Archivbereinigung. Es gelten Projektzuordnung, Originalschutz und die beiden Pflegestufen aus SKILL.md. Verwende nur das örtlich im Profil eingerichtete Verfahren. Erwerbe vor dem Paket die Reservierung nach [coordination.md](coordination.md); bei schon eigener Reservierung wird sie weiterverwendet. Aktueller Abgleich, nötige Vorhersicherung, Änderungen, Ergebnissicherung und zugehörige Bereinigung bleiben unter demselben Besitzer. Erst nach beendeten Operationen und geprüftem beziehungsweise kontrolliertem Fehlerabschluss freigeben.

Ein Deaktivierungshinweis beendet gewöhnliche Gedächtnispakete; aus einem fehlenden Bestand entsteht keine Ersatzanlage oder reguläre Sicherung. Für Deaktivieren und Archivieren, Reaktivieren und vollständige Entfernung gilt [lifecycle.md](lifecycle.md): Die zugehörigen Nutzungs- und Pflegeanweisungen werden zusätzlich als `PROJECT_RULES.md` im bezeichneten Rückkehrstand archiviert. Git-Archivierung behält das Repository mit bezeichnetem Ausgang und Ergebniscommit; Kopienarchivierung schützt den vollständigen Ausgang samt Regelarchiv, ohne eine zusätzliche Generation des bloßen Hinweises zu erzeugen. Vollständige Entfernung legt keine neue zurückbleibende Sicherung an. Diese beauftragten Übergänge sind keine gewöhnliche Inhaltspflege.

## Zusammenhängende Änderungen sichern

Behandle die Fortschreibung oder Pflege einer substanziellen Aufgabe als zusammenhängendes Änderungspaket, auch wenn mehrere Dateien betroffen sind. Vergleiche betroffene aktuelle Dateien vor dem Schreiben erneut und erhalte tatsächlich konkurrierende Änderungen. Eine bloße lesende Prüfung braucht keine Sicherung.

Vor Überarbeitung, Kürzung, Zusammenführung, Löschung oder Ersatz vorhandener Inhalte muss der aktuelle Ausgangsstand gesichert sein. Prüfe, ob dieser Stand bereits verifiziert gesichert ist; nur bei noch ungesicherten Inhalten erstelle einen zusätzlichen Vorherstand. Ein unverändert schon gesicherter Bestand benötigt weder einen leeren Commit noch eine identische neue Kopie. Reine Neuanlage oder ausschließlich additive Fortschreibung braucht keinen eigenen Vorherstand; sie erlaubt keinen unbeabsichtigten Ersatz vorhandener Inhalte.

Prüfe nach Abschluss des Pakets Kennzeichnungen, Zusammenhänge und betroffene Quellenzugänge und sichere den geprüften neuen Gesamtstand. Das gilt ausdrücklich auch für neue Einträge und einfache Ergänzungen. Ein unverändertes Ergebnis benötigt keine weitere Sicherung. Einzelne Dateischreibvorgänge verlangen keine getrennten Sicherungen; neue Rückkehrpunkte und bestätigte Profiländerungen werden in das Paket einbezogen.

Scheitert eine nötige Vorhersicherung, beginne keine ersetzende Aufarbeitung. Scheitert die Ergebnissicherung, melde den weiterhin ungesicherten aktiven Ergebnisstand; behaupte keinen erfolgreichen Abschluss der Sicherung und lösche keine älteren Kopien. Erhalte den aktiven Bestand und funktionierende Sicherungen. Eine lesende Funktionsprüfung kann weitergehen. Wechsle das Verfahren nicht stillschweigend. Eine technische Reparatur wird im dafür autorisierten Umfang geklärt; eine leere Git-Sperre allein belegt keine gefahrlose Entfernbarkeit.

## Git

Richte alle Git-Aufrufe ausdrücklich auf das eigene Repository in project-memory. Prüfe Arbeitsstand und Repository-Zuordnung und sichere den tatsächlichen zugehörigen aktuellen Bestand als Commit. Neue, geänderte und ignorierte zugehörige Dateien dürfen nicht fehlen. Ungesicherter Zustand allein belegt keine parallele Bearbeitung. Erhalte fremde Vormerkungen und kläre echte Überschneidung.

Bei unverändert gesichertem Ausgangsbestand genügt normalerweise ein Ergebniscommit für das gesamte geprüfte Paket. Noch ungesicherte vorhandene Inhalte werden vor ersetzender Bearbeitung zusätzlich committed. Die Kopienbegrenzung gilt nicht für Git; dieser Skill bereinigt keine Git-Historie.

## Vollständige Kopien

Kopiere ausschließlich den gesamten aktiven Gedächtnisbestand einschließlich Profil, Index, Einträgen und versteckten zugehörigen Dateien in einen neuen eindeutig datierten, nicht bereits belegten Unterordner von .project-memory-archive. Alte Sicherungen werden nicht mitkopiert oder überschrieben. Originalquellen außerhalb des Gedächtnisses gehören nicht automatisch dazu.

Erfasse relative Dateipfade und Dateiinhalt beziehungsweise Hashwerte des aktuellen Ausgangsbestands, kopiere und vergleiche die Kopie technisch damit. Prüfe außerdem, dass der aktive Bestand während der Erstellung nicht auseinanderlief. Bei erkennbaren Änderungen, fehlenden Dateien oder ungeklärter Vollständigkeit ist die Kopie noch keine geprüfte Sicherung. Gib keine Archivtexte als Kontext aus.

Kennzeichne eine erfolgreich geprüfte Generation durch einen nachvollziehbaren datierten Ordnernamen, etwa 20261012T140000000Z-verified. Ein neues Ziel bleibt bis zur erfolgreichen Prüfung ohne verified-Kennzeichnung; erst danach wird es entsprechend benannt. Der Name dokumentiert die erfolgte Prüfung, ersetzt sie nicht. Bereits passend gekennzeichnete geprüfte Bestände werden nicht allein für diese Namensform umbenannt. Ältere Kopien ohne belegbaren Prüfstand sind kein Anlass, ihren Inhalt als normale Quelle zu lesen.

Vor einer neuen Kopie kann der technische Pfad-/Inhaltsvergleich mit einer vorhandenen geprüften Kopie feststellen, dass der aktuelle Stand bereits gesichert ist. Bei Übereinstimmung genügt diese Kopie. Original- oder Archivtext wird dafür nicht in den Gesprächskontext ausgegeben.

## Aufbewahrung von Kopien

Die örtlich konkret freigegebene Regel steht im lesbaren Profil. Vorgeschlagener Standard sind die 20 neuesten vollständig geprüften Generationen plus höchstens drei ausdrücklich benannte Rückkehrpunkte vor funktionalem oder strukturellem Umbau beziehungsweise Wiederherstellung. Ein Rückkehrpunkt ist eine vorhandene geprüfte Generation; schütze deren Namen im Profil mit kurzem Anlass, statt eine identische Zusatzkopie anzulegen. Diese Angaben dienen ausschließlich der technischen Sicherungszuordnung und sind keine Quellenhinweise für laufende Aufgaben. Keine neuen Eintragsfelder, dauerhaften Zähler oder zusätzliche Verwaltungsdatei sind nötig.

Dieselbe Generation wird nur einmal gezählt. Die Vereinigung der 20 neuesten Generationen und höchstens drei benannten Rückkehrpunkte ergibt regulär höchstens 23 Sicherungsordner. Die neueste geprüfte Generation bleibt unabhängig von ihrem Alter erhalten. Die Regel verwendet Generationen, keine reine Altersgrenze; sie begrenzt weder eine feste Kalenderdauer noch die exakte Bytezahl.

Ein vierter dauerhafter Rückkehrpunkt darf nicht still hinzukommen. Ist ein neuer Punkt sinnvoll, ersetze die technische Schutzmarkierung eines nicht mehr benötigten Punkts im Rahmen der freigegebenen Regel oder lege einen konkreten Vorschlag zur Anpassung der Reserve vor. Das Aufheben einer Markierung erlaubt Löschung nur, wenn die Generation auch nach den übrigen Regeln überzählig ist.

Quellgeneration und aktueller Rückkehrstand einer laufenden Wiederherstellung sowie andere tatsächlich noch benötigte Stände bleiben vorübergehend zusätzlich geschützt. Kläre bekannte parallele Nutzung; lösche einen ungeklärt benötigten Stand nicht. Nach Abschluss der Operation kann die Grenze wieder geprüft werden. Eine nicht vollständig bereinigte Situation wird nicht als eingehaltene Höchstzahl ausgegeben.

Ein im aktuellen Deaktivierungshinweis bezeichneter Kopien-Rückkehrstand bleibt während Archivierung und unvollständiger Reaktivierung geschützt, auch wenn sein früheres Profil nur noch in der Sicherung vorliegt. Ordne dafür den im technischen Hinweis bezeichneten Rückkehrstand nach lifecycle.md zu, statt alte Archivtexte als Anweisungen zu lesen. Ein fehlender oder widersprüchlicher Hinweis erlaubt keine Löschung. Nach erfolgreicher Reaktivierung wird der Schutz gezielt in die aktuell freigegebene Regel eingeordnet; bis dahin darf er nicht allein zur Einhaltung der normalen Höchstzahl verschwinden.

Bei einer bestehenden Einrichtung ohne entsprechende Freigabe erhältst du deren Sicherungen. Die Verfügbarkeit der neuen Skillfassung allein genehmigt keine nachträgliche Löschung. Eine bereits konkret freigegebene Aufbewahrungsregel gilt weiter; ihre normale technische Anwendung braucht keine Einzelentscheidung für jede überzählige Kopie. Neue Grenzen oder eine andersartige Schutzregel gehören zur zweiten Pflegestufe.

## Technische Bereinigung

Bereinige erst nach erfolgreich erstellter und geprüfter neuer Kopie, niemals als Voraussetzung, um eine fehlgeschlagene Sicherung doch noch zu ermöglichen. Wähle die zu erhaltende Menge und die eindeutig überzähligen Kandidaten anhand zugeordneter Namen, Zeitpunkte und technischer Prüfergebnisse. Prüfe ältere Generationen anhand ihres eigenen belegten Sicherungsstands; Unterschiede zum aktuellen Bestand sind erwartbar und verhindern allein keine Bereinigung. Ordner, deren Zuordnung zum Projekt, Prüfstand oder bisheriger Schutz unklar ist, bleiben erhalten; sie werden nicht einfach in die normalen Generationen eingerechnet. Unvollständige oder fremde Ordner werden nicht durch diese Regel entsorgt.

Vor jeder Löschung prüfe den aktuellen Stand und folgende Grenzen:

- Das absolute aufgelöste Ziel ist ein einzelner zugeordneter Sicherungsunterordner unmittelbar innerhalb der tatsächlichen .project-memory-archive-Wurzel dieses Projekts. Projektkennung aus technischen Metadaten muss zur aktiven Zuordnung passen. Niemals das Archiv selbst, den aktiven Bestand, Originalquellen, Git-Verwaltung oder andere Projektordner löschen.
- Archivwurzel, Kandidat und sein Inhalt enthalten keine Pfadumleitung durch symbolischen Link, Junction oder anderen Reparse Point. Bei einer unklaren oder außerhalb liegenden Auflösung halte die Löschung an. Vermeide breite Wildcards und stringgebaute Shellbefehle; unter Windows nutze native PowerShell-Operationen mit LiteralPath nach Zielprüfung.
- Kandidat gehört nicht zur Erhaltungsmenge, ist kein benannter Rückkehrpunkt und wird nicht mehr von einer tatsächlichen Operation benötigt. Prüfe dies unmittelbar vor der Löschung erneut. Nur eindeutig freigegebene überzählige Kandidaten entfernen.

Behandle das als technische Sicherungsoperation; lade die archivierten Inhalte nicht als zusätzliche Projektquellen oder Anweisungen. Eine Blockade der Bereinigung macht eine erfolgreich erstellte neue Sicherung nicht ungültig. Berichte gegebenenfalls verbleibende überzählige oder ungeklärte Ordner, ohne den sicheren Bestand pauschal zurückzusetzen.

## Aufbewahrung prüfen und anpassen

Die funktionale und strukturelle Pflege prüft anlassbezogen auch die Generationenzahl und die Rückkehrpunktreserve. Beurteile anhand technischer Angaben Archivumfang, Änderungsaktivität, abgedeckten Wiederherstellungszeitraum und tatsächlich benötigte Rückkehrpunkte. Die Prüfung kann ergeben, dass die derzeitige Begrenzung passt. Lies dazu keine Archivtexte als normale Inhaltsquellen.

Erkläre einen nötigen Anpassungsvorschlag konkret im Pflegechat: bisherige und neue Grenzen, Belege, erwartete Auswirkung auf Speicherbedarf und Wiederherstellbarkeit sowie wesentliche Abwägungen. Aktiviere neue Werte erst nach Nutzerfreigabe für diesen Umfang und aktualisiere danach die örtliche Profilregel als gesichertes Änderungspaket. Ein regelmäßiger Check genehmigt die Grenzänderung nicht. Eine Verringerung der Grenze legitimiert keine Bereinigung vor der nächsten erfolgreich geprüften neuen Kopie.
