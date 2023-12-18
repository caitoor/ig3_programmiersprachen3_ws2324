# IG3 – Programmiersprachen 3 (WS 23/24)

## Abgabe

Alle Studierenden geben ein Svelte-Projekt mit folgenden Kriterien ab:

### Must-Have (~ bestehens-relevant)

- Lauffähiges Svelte-Projekt
- Dynamisch geladene Inhalte (z. B. aus JSON)
- mind. 2 sinnvolle Svelte-Komponenten
- Einbindung einer API (REST)
- Grundlegende Möglichkeit der Benutzerinteraktion (Buttons, Filter, etc.)


### Should Have (~ relevant für Note vor dem Komma)

- Responsive Design (Mobile + Desktop)
- Vernünftiges Erscheinungsbild, das der Projektidee zuträglich ist
- Verschiedene Unterseiten (Routes), die dieselben Daten auf andere Art und Weise sichtbar machen
- Sinnvolle Ordner- und Dateistruktur

### Could Have (~ relevant für die Note nach dem Komma)

- OpenAI-API-Anbindung
- Verwendung eines Stores
- Komplizierte statistische Berechnungen
- Auslagerung von Code-Teilen in Module zur besseren Übersichtlichkeit
- Anbindung einer Datenbank (z. B. SQLite oder mongoDB Atlas)
- Drag & Drop
- Physics Engine
- Toggle für Dark Mode
- Screenreader-Unterstützung
- Mehrsprachigkeit
- Datenvisualisierungen / Charts / etc.
- Animationen
- ...

### Abgabemodalitäten

- Abgabe als git-Repo auf GitHub (public oder private mit Einladung)
- Ordentliche Dokumentation in der Readme.md
- Alle nötigen Credentials etc. auf separaten Kanälen
- Screencast, der alle Features zeigt

### Bewertungskriterien

- Anforderungen erfüllt?
- lauffähig?
- eigener Code über Unterrichtsprojekt hinaus?

**Von der 4,0 zur 1,0 dann relevant:**

- Komplexität des Projekts
- Herangehensweise, Umgang mit Schwierigkeiten im Verlauf
- the more, the better (Anzahl sinnvoller Features)
- the better, the better (Codequalität, Struktur von Code und Repo)
- the smarter, the better (Konzept, Komplexität)

**Hinweis:** Anwesenheit, Mitarbeit und Beiträge im Kurs (Quantität und Qualität) sind mit 30% der Gesamtnote gewichtet.

**Tipp:** Macht irgendwo eine übersichtliche Dokumentationsseite, in der ihr eure Must / Should / Could Haves auflistet, damit ich nichts übersehe.

### Projektideen

Das Thema "Dinosaurier" ist zwar verdammt cool, aber nicht verpflichtend. Wenn ihr euch für ein anderes Thema bzw. einen anderen Datensatz entscheidet, achtet aber darauf, dass ihr dadurch nicht die Komplexität verringert oder die Anforderungen nicht mehr passen. Hier ein paar Ideen, was man mit dem Dino-Thema anstellen könnte:

- Spielkartenübersicht mit Zusatzinformationen und Filterfunktionen (solider Standard)
- Spielbares Dino-Quartett
    - 2 Spieler am selben Rechner
    - 2 Spieler an unterschiedlichen Rechnern über Websockets
    - 1 Spieler gegen Computer-KI (Bonus: Schwierigkeitsgrad einstellbar)
- Dino-Karten-Generator 
  - Bonus: Speicherung in externer Datenbank
  - Bonus: On-the-fly Generierung mit AI-APIs
- Dino Hardcore-Memory (in jedem Zug werden ein Stat und ein > oder < Symbol zufällig aufgedeckt und man muss ein Pärchen in der richtigen Reihenfolge aufdecken)
- Katzen-Quartett mit per API geladenen Katzenbildern
- Dino-Quiz-App
- ...