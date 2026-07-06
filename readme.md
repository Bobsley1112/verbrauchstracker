# 📈 LocalMeterLog

Eine kleine, werbefreie **Web-App zur Erfassung von Zählerständen** (Strom, Gas, Wasser, Öl, Pellets, Fernwärme, Solar/PV u. v. m.) – läuft komplett offline im Browser, ohne Server, ohne Konto, ohne Tracking.

Alle Daten bleiben **ausschließlich lokal auf dem eigenen Gerät** gespeichert (`localStorage`). Es findet keinerlei Datenübertragung statt.

👉 Einfach `index.html` öffnen – fertig. Kein Build, keine Installation, keine Abhängigkeiten.

---

## ✨ Funktionen

### Zähler verwalten
- Beliebig viele Zähler anlegen, umbenennen und die Einheit anpassen (kWh, m³, l, kg, …)
- Vordefinierte Zähler für Strom, Gas, Wasser, Heizöl, Pellets und Fernwärme
- Eigene Zähler für alles Weitere anlegen (z. B. Wärmepumpe, Poolpumpe, Ladesäule)
- Zähler bei Bedarf löschen oder vorübergehend deaktivieren – **mindestens ein Zähler bleibt immer erhalten**
- Zweirichtungszähler (z. B. PV-Anlage: Bezug **und** Einspeisung) werden getrennt erfasst und ausgewertet
- Optionale Zähler-Nummer je Zähler hinterlegbar

### Tarife & Kosten
- Arbeitspreis (€ je Einheit) je Zähler hinterlegbar
- **Grundpreis (€/Monat)** je Zähler hinterlegbar – wird anteilig für den jeweils gefilterten Zeitraum berechnet
- Automatische Kostenberechnung: Arbeitspreis, Grundpreis (zeitanteilig) sowie Gesamtkosten inkl. Grundpreis
- Bei Zweirichtungszählern zusätzlich: Vergütung für Einspeisung sowie Netto-Kosten

### Auswertung
- Übersichtliche Kennzahlen: Durchschnittsverbrauch pro Tag, letzter Zeitraum, Gesamtverbrauch, Kosten
- Verlaufsdiagramm (SVG) je Verbrauchsart
- Zeitraum-Filter: Gesamtzeitraum, letzte 365 Tage, letztes Kalenderjahr, oder freie Von/Bis-Auswahl
- Chronologische Liste aller erfassten Ablesungen inkl. Verbrauch seit letzter Ablesung
- Erkennung von Zählerwechseln (z. B. bei rückläufigem Zählerstand)

### Daten-Export & Sicherung
- Export als **Excel (.xlsx)** oder **CSV (.csv)** – inkl. Zählerstände und berechnetem Verbrauch je Zeitraum
- Vollständige **JSON-Sicherung** aller Daten und Einstellungen (Zähler, Tarife, Grundpreise, Zähler-Nummern, …)
- Sicherung jederzeit wieder importierbar – auch auf einem anderen Gerät
- Import erkennt Duplikate (gleiches Datum) und fragt vor dem Überschreiben nach

### Bedienung
- Helles/dunkles Design (folgt automatisch den Systemeinstellungen, manuell umschaltbar)
- Für Smartphone-Startbildschirm nutzbar (PWA-Metadaten enthalten, „Zum Home-Bildschirm hinzufügen“)
- Responsives Layout für Smartphone, Tablet und Desktop

---

## 🚀 Nutzung

1. Datei `index.html` herunterladen
2. Mit einem beliebigen Browser öffnen (Doppelklick genügt)
3. Optional: Datei auf dem Smartphone öffnen und über den Browser „Zum Startbildschirm hinzufügen“, um sie wie eine App zu nutzen

Es ist **kein Internetzugang** erforderlich – lediglich der optionale Excel-Export lädt beim ersten Mal einmalig eine kleine Bibliothek von einem CDN nach. Ohne Internetverbindung steht alternativ der CSV-Export zur Verfügung.

## 💾 Daten & Datenschutz

- Alle Eingaben werden ausschließlich im `localStorage` des jeweiligen Browsers gespeichert
- Es gibt keinen Server, kein Backend, keine Analyse- oder Tracking-Skripte
- Da die Daten browser- und geräteabhängig sind, empfiehlt sich eine regelmäßige **JSON-Sicherung** (Button „Sicherung speichern“), um Daten zwischen Geräten/Browsern zu übertragen oder vor Datenverlust (z. B. beim Leeren des Browser-Caches) zu schützen

## 🛠️ Technologie

- Eine einzelne, abhängigkeitsfreie `index.html`-Datei (HTML, CSS, Vanilla JavaScript)
- Kein Framework, kein Build-Prozess
- Diagramm-Rendering per reinem SVG
- Excel-Export optional über [SheetJS](https://sheetjs.com/) (wird nur bei Bedarf nachgeladen)

## 📄 Lizenz

Frei nutzbar und anpassbar für den privaten Gebrauch.
