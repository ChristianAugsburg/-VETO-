# 🚫 VETO (Realtime Tabu-Style Classroom Game)

Ein elegantes, webbasiertes Wort-Umschreibungs-Spiel im klassischen "Tabu"-Stil, optimiert für den direkten Einsatz im Unterricht über **Moodle**-Textseiten. Das System bietet ein integriertes Dozenten-Dashboard, einen lokalen persistenten Cache und eine dynamische, automatische **Präsentationsansicht (Beamer-Fenster)** für das Smartboard inklusive nativer Toneffekte über die Web Audio API.

---

## 🛠️ Technische Kontaktdaten (Support & Feedback)

Für Fragen, Fehlerberichte (Issues) oder Funktionserweiterungen wende dich bitte an:

* **Entwickler:** Christian
* **Mastodon (Fediverse):** [@Christian_Augsburg@mastodon.social](https://mastodon.social/@Christian_Augsburg)
* **Lizenz:** Veröffentlicht und geschützt unter den Bedingungen der **GNU General Public License v3.0 (GPL-3.0)**.

---

## 💻 Funktionsweise & Features

* **Schnittstellenfreier Betrieb:** Das Spiel läuft komplett im Browser-Frontend des Dozenten (Client-Side). Es erfordert keine Datenbank-Konfiguration für Schülergeräte.
* **Persistent Cache:** Einmal importierte Kartensets werden via `localStorage` im Browser-Cache gespeichert (`bycs_tabu_cards`). Ein versehentliches Neuladen der Moodle-Seite führt nicht zu Datenverlust.
* **Zwei-Fenster-Synchronisation:** Per Klick öffnet sich ein synchronisiertes Beamer-Fenster. Während der *Wächter* auf dem Master-Bildschirm die Tabu-Wörter kontrolliert, sieht die Klasse auf dem Smartboard nur den Raten-Begriff im Großformat.
* **KI-Prompt-Schnittstelle:** Ein integrierter Prompt-Generator liefert maßgeschneiderte Befehle für LLMs (ChatGPT, Gemini, Claude), um sekundenschnell themenbasierte Wortschätze zu generieren.

---

## 📥 Import-Format für Kartensets

Das System nutzt ein einfaches, tabulator- bzw. zeilenbasiertes Pipe-Format. Neue Karten können direkt per Copy-Paste in das KI-Importfeld eingefügt werden.

**Format pro Zeile:**
```text
Begriff | Tabu-Wort 1, Tabu-Wort 2, Tabu-Wort 3, Tabu-Wort 4, Tabu-Wort 5
Beispiele:
Plaintext

Apfel | rot, Obst, Baum, Kern, Saft
Browser | Internet, Webseite, Chrome, Firefox, Link
Zelle | Biologie, Mikroskop, Kern, Pflanze, Leben

```
## 🎮 Kurzanleitung für den Unterricht

  Teams anlegen: Trage im Setup-Screen die Namen deiner Gruppen ein (z.B. Reihe 1, Reihe 2).

  Karten brennen: Kopiere dir fertige Wortlisten aus deiner VETO-Schatzkiste, füge sie ins Importfeld ein und klicke auf 🚀 Karten brennen.

  Beamer-Modus aktivieren: Klicke auf 🖥️ Beamer öffnen (Popups im Browser erlauben!) und schiebe das neue Fenster auf das Smartboard.

  Das VETO-Prinzip im Klassenzimmer:

  Die aktive Gruppe schickt mindestens zwei Schüler nach vorne.

  Der Erklärer: Steht mit dem Rücken zum Smartboard, schaut auf das Dozenten-Display und umschreibt den Begriff.

  Der Wächter: Steht am Dozenten-Display und kontrolliert, dass der Erklärer keines der 5 verbotenen Wörter nutzt. Bei einem Regelverstoß ruft er VETO! und die Lehrkraft klicke auf 💀 Fehler.

  Wird der Begriff erraten, klickt die Lehrkraft auf ✨ Richtig und die Karte fliegt visuell auf den Ablagestapel.

## 📝 Lizenzbestimmungen (GPL-3.0)

Dieses Programm ist freie Software: Sie können es unter den Bedingungen der GNU General Public License, wie von der Free Software Foundation veröffentlicht, weitergeben und/oder modifizieren (entweder gemäß Version 3 der Lizenz oder jeder späteren Version).

Die Verteilung erfolgt in der Hoffnung, dass das Programm nützlich sein wird, aber OHNE JEDE GEWÄHRLEISTUNG. Weitere Details entnehmen Sie bitte der im Repository hinterlegten LICENSE Datei oder dem offiziellen GNU-Portal unter https://www.gnu.org/licenses/.
