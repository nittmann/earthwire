# Featurelist

## Frame
- Es gibt zwei Klassen von Objekten: *Flugzeug* und *Projektil*.
- Aus *Flugzeug* erben sowohl das Spieler-Flugzeug und die KI ihre Objekte.
- Betreffende Attribute (Koordinaten, Lebenspunkte, Stats, ...) sollten provisorisch hinzugefügt werden.
- Ein Loop überprüft bei *Flugzeug* ob die Lebenspunkte auf 0 gefallen sind.

## Navigation
- Der Spieler kann sich mit dem Steuerkreuz in den Himmelsrichtungen und auch diagonal bewegen bewegen.
- Der Spieler sieht immer in Richtung Osten.
- Kollision mit Bildschirm, verhindert dass der Spieler aus dem Spielbereich gerät. 
- Die Größe des Spielers ist variable (für Grafiken).
- Die Bewegung ist statisch und hängt nicht nach, sobald man das Steuerkreuz loslässt.

## Schießen 
- Der Spieler kann mit dem *A-Knopf* ein *Projektil* abfeuern, der Richtung Osten fliegt.
- Die Vertikale Bewegung hat keinen Einfluss auf die vertikale Bewegung des *Projektils*.
- Das *Projektil* wird beim Verlassen des Bildschirm zerstört.
- Die Größe des *Projektils* ist variable (für Grafiken).
- Beim Abschuss des *Projektils* wird ein Sound abgespielt (Platzhaltersounds reichen vorerst).

## Gegner (Kollision)
- Der Spieler kann mit statischen Gegnern kollidieren.
- Bei Kollision werden beide Flugzeuge zerstört, in dem ihre Lebenspunkte auf 0 fallen.
- Die Animation soll austauschbar sein.

## Gegner (Schießen)
- Die Gegner sind in der Lage in einem zufälligen Zeitraum *Projektile* abzufeuern, welche Richtung Westen fliegen.
- Diese haben alle Verhaltensweisen wie die *Projektile* des Spielers.
- Wenn ein *Projektil* ein Objekt *Flugzeug* trifft, reduziert es die Lebenspunkte um einen provisorischen Wert.
- Bei Kollision mit einem Objekt *Flugzeug* wird das Projektil zerstört.

## Projektile & Zerstörung
- Bei Abschuss eines *Projektils* speichert das Projektil, ob es der Spieler oder der Computer abgefeuert hat.
- Bei Zerstörung (Lebenspunkte auf 0) eines Gegners durch den Spieler wird ein gelb-roter Lichteffekt abgespielt.
- Bei der Zerstörung eines Flugzeugs soll eine provisorische Animation abgespielt werden.
- Sobald der Spieler zerstört wird, startet das Spiel von neuem.
- Beim Zerstören eines Flugzeugs (egal ob Spieler oder Computer) wird ein Sound abgespielt.

## Gegner (Bewegung)
- Die Gegner bewegen sich automatisch in Richtung Osten.
- Sie sollen sich nicht vertikal bewegen, da sonst die Gefahr besteht, dass sie sich gegenseitig treffen.
- Wenn die Gegner den Bildschirm verlassen, werden sie zerstört.

## Statistiken
- Beim Zerstören eines Gegners durch ein *Projektil* des Spielers wird eine Variable *Punkte* erhöht.
- Die Punkte werden als Zahl angezeigt.
- Die *Rüstung* des Spielers wird in Form eines Schild-Icons und mit einem Balken angezeigt.
- Eine neue Variable *Munition* wird in Form eines Patronen-Icons und mit einem Balken angezeigt.

## Munitions-Mechanik
- Mit jedem Schuss sinkt die Munition.
- Ist die Munition auf 0 kann nicht mehr geschossen werden.
- Will der Spieler bei 0 Munition schießen, 
- Mit dem *B-Knopf* lädt sich über eine provisorische Zeit der Balken der Munition wieder auf.
- Nach dem Aufladen ist das Schießen wieder möglich.

## Gegner (Spawn)
- Zufällig werden Gegner am rechten Bildschirmrand erscheinen.
- Über den Verlauf der Zeit erscheinen mehr Gegner, die öfter schießen.

## Persönliches Scoreboard
- Sobald der Spieler stirbt, werden die Punkte in ein Array abgespeichert.
- Das Array wird dann nach Größe sortiert.

## GameLoop abschließen
- Sobald der Spieler stirbt wird das aktuelle Scoreboard angezeigt.
- Mit dem Druck auf den *A-Knopf* wird ein neues Spiel gestartet.

## Pause
- Beim betätigen des *META-Knopfs* pausiert das Spiel.
- Ein Titel "Pausiert" erscheint.
- Der Spieler bewegt sich nicht mehr und kann auch nicht mehr schießen.
- Die Gegner bewegen sich nicht mehr und schießen nicht.
- Beim betätigen des *A-Knopfs* wird das Spiel fortgesetzt.

## Grafik
- Die Platzhaltergrafiken werden ausgetauscht.
- Die Kollision funktioniert weiterhin.

## Hintergrundgrafik (optional)
- Eine Hintergrundgrafik wird eingefügt.
- Die Hintergrundgrafik scrollt *gekachelt* mit dem Spieler langsam mit (Parallax Effekt).

## Musik (optional)
- Eine Hintergrundmusik wird beim Spielen abgespielt.
- Eine andere Hintergrundmusik für das Scoreboard.
