# Einleitung :smiley_cat:

Hallo, das hier ist dein eigenes Repository wo du Sachen ausprobieren kannst =).
Mit den hier genannten Übungen wirst du fit um bei uns direkt mit zu entwickeln.

Bitte habe stets im Hinterkopf dass wir einen hohen Anspruch an Qualität haben und auch
von dir diesen Anspruch verlangen. Codereviews also ein 4 - Augenprinzip ist essentiell.
Das wird nicht gemacht um jemanden zu schikanieren, sondern um die eigene Qualität

zu steigern und gemeinsam besser zu werden.
Wichtig: Scheue dich niemals zu fragen, lieber 100 x mal zu oft gefragt als einmal zu wenig =).

Aktuell programmieren wir hauptsächlich mit JavaScript. Du kennst diese Sprache evtl.
aus dem Webbereich. Allerdings hat sich sehr viel getan. Inzwischen konkurriert
JavaScript mit Sprachen wie Python.

Wir haben uns für eine NodeJS (ein JavaScript Framework, mehr dazu unter Hilfreiches)
Umgebung entschieden weil man mit NodeJS auch andere Sprachen einfach integrieren kann.
Sprich es ist egal ob man eine C++ Library einfügt oder eine Python lib benutzt.
Es gibt noch mehr Vorteile die du sicher beim Entwickeln feststellen wirst.

# Aufgaben :bulb:

Dieser Bereich ist untergliedert in "hilfreiches" und die tatsächlichen Aufgaben.

## Hilfreiches :envelope:

- [MDN](https://developer.mozilla.org/de/docs/Web/JavaScript) ist die erste Anlaufstelle wenn man wissen möchte wie eine bestimmte
Funktion von JavaScript funktioniert.

- [Stackoverflow](https://stackoverflow.com/) sollte kein Fremdwort sein, dort findest du viele Fragen zu allen Programmiersprachen
und die dazu gehörigen Antworten.

- [Github](https://github.com/explore) die Welt des offenen Quellcodes. Wenn du Zeit hast schau ruhig mal durch was es so gibt,
die Leute kommen auf die verrücktesten Ideen. Vieles wird auch in der Industrie genutzt.

- Achte bei allen Fragen und Antworten darauf dass diese aktuell sind, in der Welt
der IT ändert sich im Wochentakt etwas. Vorallem JavaScript kann sehr schnell ausrudern.

- Wenn du ein programmatisches Problem hast zerlege es auf das kleinese Problem und arbeite diese ab.
Dein Problem als ganzes wirst du nur sehr selten "gegoogled" bekommen.
Außer es ist eine Anfänger frage dann schon :D.

### Off Topic :coffee:

Wenn du sehen willst was ich so treibe dann kannst du meine Profile stalken auf Stackoverflow und Github:

- [Güney aka. Megajin Stackoverflow](https://meta.stackoverflow.com/users/4457744/megajin)
- [Güney aka. Megajin Github](https://github.com/Megajin)


## Aufgaben Schritt für Schritt :memo:

Ich werde mich bemühen alles so verständlich wie möglich zu formulieren. Sollte etwas unklar sein einfach fragen =).
Allerdings solltest du immer bedenken dass ich vieles so formuliere dass gewisse Fragen offen bleiben damit du lernst Zusammenhänge zu knüpfen.


### Umgebung einrichten :telescope:

1. Richte dir unter C:\ einen ordner ein, für deine Projekte.
Dort legst du bitte alle nötigen Dateien ab wie zB. den cmder ordner.
Als nächstes machst du einen unterordner (C:\Projekte\Git), den du Git nennst. Dort werden alle
Repositories rein geclont, von uns oder extern. Achtung nicht für die Git-Software verwenden!

1. [cmder](http://cmder.net/) einfach "Download full" benutzen.

1. [Git](https://git-scm.com/) Windows download. Wenn du installierst, dann nimm immer
die Optionen wo man die Windows eigenen Tools benutzt!

1. [Atom](https://atom.io/) Das ist unsere Entwicklungsumgebung. Eigentlich ein einfacher Texteditor, aber mit seinen
Erweiterungen wird Atom zur optimalen Enwicklungsumgebung. Damit wir den gleichen Stand haben,
solltest du unter File > Settings (Ctrl + , [Kommataste]) dann Install gehen und folgende Packages installieren
(Themes werden auch so installiert nur musst du den reiter rechts dann wechseln von package auf theme):

- atom-ide-ui
- atom-material-syntax (findet ihr unter Themes)
- atom-material-syntax-dark (findet ihr unter Themes)
- atom-material-syntax-light (findet ihr unter Themes)
- atom-material-ui (findet ihr unter Themes)
- docblockr
- emmet
- git-plus
- git-time-machine
- highlight-selected
- atom-typescript
- linter-eslint
- minimap
- minimap-highlight-selected
- multi-cursor-plus
- pigments
- prettier-atom
- react
- seti-icons
- split-diff


Als nächstes öffnest du die `keymap.cson` -> File > Keymap...
Dort trägst du ganz unten folgendes ein:
```CoffeeScript
'atom-text-editor':
    'ctrl-alt-k': 'prettier:format'
    'ctrl-q': 'emmet:expand-abbreviation'

'atom-text-editor[data-grammar~="jsx"]:not([mini])':
    'ctrl-q': 'emmet:expand-abbreviation'
  ```


  Mit <code>ctrl + alt + k</code> rückst du markierte Texte automatisch richtig ein.
  Mit <code>ctrl + q</code> kannst du emmet triggern in HTML - Dateien:  [Emmet Cheat Sheet](https://docs.emmet.io/cheat-sheet/)

  1. [NodeJS](https://nodejs.org/en/) unbedingt die "current" laden und installieren, <b><u>nicht</b></u> die LTS!

  1. Starte deinen Rechner neu und versuche dann in cmder (bitte immer als Admin starten)
  folgende Befehle `node -v` und `npm -v` jetzt sollten die Versionen erscheinen.
  erscheinen keine Versionen hast du was falsch gemacht :D.

  ### Aufgaben :chart_with_upwards_trend:

  Wie du die Aufgaben angehst ist komplett dir überlassen es gibt kein Schritt für Schritt.
  Warum? Ganz einfach wenn ich dir alles vorgebe und vorkaue kannst du dich niemals selbst entfalten.
  Du kannst immer deinen eigenen Stil verwenden ABER in einem Maß wie es in unsere
  Konform passt zB. ESDOC Dokumentationen. Falls du weißt was `short circuits` sind
  auch bekannt unter `lambda` - Ausdruck (was übrigens falsch ist) sollte dir klar sein
  dass nicht jeder das lesen kann, auch dass man diese nur da benutzen sollte wo es Sinn macht.
  Falls du davon noch nichts gehört hast, es macht einiges einfacher. Warum ist es dann so kompiliziert? Hier ein sehr einfaches Beispiel:

  ```JavaScript
  // Das hier ist das normale Beispiel.
  let myVariable = 50;
  if (myVariable === 50) {
    // do stuff if is true.
  } else {
    // do stuff if is false.
  }
  ```



  ```JavaScript
  // Das hier ist ein short circuit.
  let myVariable = 50;
  myVariable === 50 ? /** do stuff if is true */ : /** do stuff if is false*/;
  ```

  Wie du siehst ist das noch überschaubar aber in komplexen Funktioinen kann das zu Verwirrung führen.

  Wie auch immer kommen wir zu deinen Aufgaben. Bitte arbeite diese von oben bis unten durch weil die Aufgaben auch untereinander Abhängig sein können.

  - Verstehe was JavaScript ist und was Backend JavaScript und Frontend JavaScript (Web) unterscheidet.
  Finde heraus was "Single Thread" im Beispiel von JavaScript bedeutet und ob JavaScript
  auch "Multi Thread" kann. Unterscheide zwischen Web und NodeJS.

  - WICHTIG: Verstehe warum JavaScript eine asynchrone Sprache ist und nicht wie zB.
  Python oder C# synchron. Außerdem warum JavaScript keine typisierte Sprache ist
  und was das bedeutet bzw. für folgen hat.

  - Finde heraus was JavaScript ES6/7 ist und versuche es zu verstehen.

  - Clone dieses Repo falls noch nicht gemacht in den Git Ordner (C:\Projekte\Git).
  Navigiere in cmder in den ordner mit `cd C:\Projekte\Git`
  Du musst keinen neuen Ordner erstellen das passiert automatisch.
  Im Ordner Git musst du nur den Befehl `git clone {LINK VON DEINEM REPOSITORY}` absetzen.
  Initialisiere dein Projekt mit `npm init` drücke einfach immer Enter bis die Dialoge fertig sind. Jetzt sollte eine `package.json` existieren in deinem Projekt.
  Erstelle eine Datei `index.js`. Dort schreibst du folgendes rein `console.log('Hello World!');`
  In deiner `package.json` fügst du unter "scripts" folgendes ein:

  ```JavaScript
  "start": "node index.js"
  ```


  Es sollte jetzt so aussehen:

  ```JavaScript
  "scripts": {
    "start": "node index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  }
  ```

  Du kannst jetzt dein Projekt testweise starten indem du diesen Befehl in cmder eintippst `npm start`.
  Jetzt sollte Hello World erscheinen in der Konsole.

  - Commit & Push: Drücke `ctrl + shift + h` um in Atom Git-Plus zu öffnen.
  Jetzt navigierst du auf `Add all, Commit And Push`. Schreibe einen kurzen Text in das Fenster welches aufgeht und dann `ctrl + s`.
  Merke dir das gut, das solltest du nach jedem Abgeschlossenen Schritt tun um deine Änderungen Historisch auf zu bewahren.
  Du kannst in Bitbucket unter "commits" sehen was sich geändert hat oder hier in Atom mit `alt + t`.

  - Versuche erstmal einige JavaScript Funktionen von MDN aus und mache dich mit den Typen vertraut, jetzt kannst du ja einfach testen ob alles tut.

  - Lerne was JavaScript primitive Typen sind und wie man Objekte erstellt und diese auch benutzt.
