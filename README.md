# Welche Vorteile bietet eine SAP-Lösung?

SAP deckt alle Prozesse eines global agierenden Konzerns ab. Keine andere Lösung deckt alle Anwendungsfälle so gut vernetzt ab.

## Modus

Ein Modus ist ein einzelnes SAP-Fenster im Desktop. Es können typischerweise 5 bis 6 Fenster parallel geöffnet sein.

# Logistik

Logistik bezeichnet die Bereitstellung der richtigen Menge von Ressourcen zur richtigen Zeit, in der richtigen Qualität am richtigen Ort.

## Arten von logistischen Gütern

- Material
- Personal
- monetäre Leistungen
- ...

# Organisationsebenen von SAP

1. **Mandant**: abgeschlossenes System mit eigenen Datenbanken
2. **Buchungskreis**: Abgeschlossene Buchhaltung (mind. 1 pro Land aufgrund der unterschiedlichen Steuerrechte)

# Transaktion

Programm in SAP, das für einen bestimmten Zweck ausgelegt ist

# Stammdaten

Stammdaten sind Daten, die im System **zentral** hinterlegt und durchsuchbar sind. Bei Auswahl eines Stammdatums werden alle benötigten Daten automatisch geladen und die Felder ausgefüllt.
Somit ist ein Stammdatum die Basis für ein effizientes Arbeiten.

## Arten

- Debitorenstammdaten
  - Einkauf
  - Verkauf
  - Finanzdaten
- Kreditorenstammdaten
  - Einkauf
  - Verkauf
  - Finanzdaten
- Materialstammdaten
- Nachrichten
- Infosätze
  - Konditionen
    - **Vorsteuer**
- Konditionssätze
  - Konditionen
    - **Umsatzsteuer**

## Versandarten von Nachrichten

- EDI (IDoc)
- Fax
- E-Mail
- Druck

# Sichten

Spezifische Anforderungen einer Abteilung werden zu ein und demselben Material pro Abteilung spezifisch zusammengefasst zur Verfügung gestellt. Die Abteilungen arbeiten im Regelfall mit den ihnen zugeordneten Sichten.
Ein Einkäufer benötigt andere Informationen als ein Konstrukteur.

## Gliederung von Sichten auf Materialien
- Branche (Healthcare, Automotive)
- Materialart

## Gelten Informationen in Sichten nur für diese Sichten?

Nein, es reicht eine einmalige Eingabe eines Datums. In den Sichten kann anschlißend das Datenfeld ein- und ausgeblendet werden.

## Warum werden beim Anlegen ein Großteil der Sichten angegeben? Wie nennt man diese Art der Datenerfassung? Welche Vorteile bringt dies?

**Zentrale Datenerfassung**: Eigenschaften werden gesammelt und zentrale **Stelle** gibt alle erfoderlichen Daten ein.
+ einfacher
+ übersichtlicher (Big-Picture)
+ Datenstruktur ist homogen (gleichmäßiger)
+ besser zu koordinieren
+ geringere Fehlerquelle (eingebender Mitarbeiter weiß Bescheid)
- evtl. werden sehr spezifische, aber trotzdem wichtige Daten nicht erfasst
- kann langsamer sein

### Was ist das Gegenteil?

**Dezentrale Erfassung**: Jede **Stelle** erfasst die für sie relevanten Daten selbst mit Hilfe der zur Verfügung stehenden Sichten
+ wirklich spezifischen Anforderungen sind exakt vorhanden
+ Informationsvorsprung: Bei der zentralen Erfassung müssen alle Daten zusammengesammelt werden
- Abteilungsegoismen und fehlerhafte oder unvollständige Daten --> Wildwuchs
- heterogenere Daten
- komplexer zu koordinieren

## Was ist eine Grundsicht?

Unbedingt erfoderliche und allgemein gültige Daten.
- Bezeichnung
- Basismengeneinheit

## Infosatz

Ein Infosatz ist ein Stammdatum.

### Einkaufsinfosatz

Ein Einkaufsinfosatz legt fest, welcher Lieferant, welche Materialien, an welche Organisationseinheiten zu welchen Konditionen liefert.
Er wird während des Angebotsvergleichs erstellt.

## Kontrakte

Ein Kontrakt speichert die gleichen Daten wie ein Infosatz, ist allerdings für größere Mengen und längere Zeiträume vereinbart. Ein Anwendungsbeispiel ist z.B. ein Projekt.

### Arten von Kontrakten

- Mengenkontrakt: Welche Materialien zu einer bestimmten Stückzahl und zu bestimmten Konditionen
- Wertkontrakt: Der monetäre Umfang, aber **nicht** die Materialien, in denen der Gesamtwert aus Lieferungen und Leistungen bezogen werden kann

### Lieferplan

Bei einem Lieferplan handelt es sich um einen Mengenkontrakt, bei dem die Menge, das Material, der Lieferort und das Lieferdatum genau vereinbart werden.
Dieser kann z.B. automatisch vom System erzeugt werden.

# Bewegungsdaten

Werden durch den Abschluss einer Transaktion erzeugt.
- Belegnummer
- Nachrichtenverlauf
- Bewegungsverlauf (In welchen Abteilungen befand sich das Material?)
- Reservierungen
- Ausgaben
- Inventure
- Dispositionslisten

# Materialwirtschaft

## Materialgruppe != Materialart

Materialart: grobgranularste Einteilung

- Rohstoffe
- Handelsware
- Fertigprodukt

Materialgruppe: etwas feingranularere Einteilung

- Elektroartikel
- Lebensmittel
- Möbel

## Warum gibt es unterschiedliche Materialarten?

Ein Rohstoff kann z.B. nicht weiter verkauft werden.

## Wozu benötigt man alternative Mengeneinheiten?

Andere Mengeneinheit im Einkauf (z.B. Kiste Schrauben) als in der Produktion (Stück Schraube)

## Klassifizierung

Bekanntgabe, dass das Material über gewisse Eigenschaften verfügt. (z.B. Drehzahl, Farbe, ...)

# Wozu benötigt man zusätzliche Sprachen?

**Automatischer** Lookup des System basierend auf der Sprache des Kunden --> Stammdaten werden automatisch geladen.
--> **Konditionstechnik**

# Qualitätsmanagement

1. Qualitätsmerkmale anlegen
2. Prüfplan erstellen
3. Buchung in Qualitätsprüfbestand
4. Durchführen der Prüfung
5. Prüfergebnis beurteilen
6. Verwendungsentscheid
  - Verwendung erst **nach** dem Verwendungsentscheid möglich

## Qualitätsmerkmale

Welche Eigenschaft soll überprüft werden und wie soll das gewünschte Ergebnis aussehen? (z.B. Sitz soll sauber und nicht zerkratzt sein) 
Können allgemein gültig sein, d.h. für alle Materialien verwendet werden. Sie können aber auch sehr spezifisch sein.
Einschränkungen über verschiedene Organisationseinheiten:
- Werke
- Lager
- Produktionsabschnitte

### Prüfarten

- Qualitativ: entspricht bestimmten nicht-messbaren Kriterien (Sitz ist zerkratzt, verschmutzt, etc.)
- Quantitativ: messbare Merkmale (bestimmte(s) Maß/Gewicht/Festigkeit wird eingehalten) (Reißprobe, Druckprobe, chemische Probe)

## Prüfplan

Ein Prüfplan verknüpft ein oder mehrere Qualitätsmerkmale mit einem Material.
Alle Orte und Zeitpunkte der Prüfungen werden die gesamte Organisationseinheit (z.B. Werk) sowie den gesamten Prozess umfassend festgelegt.
Z.B. Sitz muss nur während des Einbauens und vor der Auslieferung überprüft werden

## Typische Prüforte / Prüfabschnitte des Prozesses?

- **Materialeingang**
- Produktion
- Warenausgangskontrolle
- ...

## Auslöser Qualtitätsprüfung

- Wareneingang
  - Richtigkeit der Lieferung
  - Quantität der Lieferung
  - Qualität der Verpackung
- Warenausgang

## Optische Sichtkontrolle

Eine Kontrolle auf beschädigte Verpackung (optische Sichtkontrolle) ist ebenfalls eine Qualitätskontrolle --> Vormerk erstellen

## Bestandsart

Legt fest in welchem Lagerzustand sich das Material befindet befindet (z.B. in Transit, auf Lager, Qualitätsprüfbestand, ...).

### Qualitätsprüfbestand

Ware ist physisch im Werk/Lager vorhanden, aber **nicht verfügbar**.
Nicht frei umbuchbar, es muss eine Qualitätsprüfung und ein Verwendungsentscheid erfolgen.

## Verwendungsentscheid

Ist das Ergebnis der Qualitätsprüfung und gibt an, was mit dem geprüften Material passiert.

### Positiver Verwendungsentscheid

Material wird in den regulären Bestand übernommen.

### Negativer Verwendungsentscheid

Es muss eine manuelle Entscheidung über die Verwendung erfolgen.
Z.B. Übernahme in B-Ware, Rücksendung, ...

# MRP und MRP2

1. MRP - einstufig, nur das direkt benötigte Material wird disponiert
2. MRP2 - Produktionsstückliste wird aufgeflöst, benötigte Unterprodukte werden miteinbezogen, Kapazitäten der Produktionsanlagen werden terminiert, etc.

## Ergebnisse

1. Bestellanforderung --> wird zu Bestellung (Prozess kann vollständig automatisiert werden)
2. Planauftrag --> wird zu Fertigungsauftrag (hilfreich bei Unterkapazitäten normalerweise selbst hergestellter Produkte)

# Konditionen

Allgemeine Bedingungen --> **Konditionstechnik**

Können auch Zuschläge sein (Transportzuschlag, Legierungszuschlag bei Edelmetallen).

## Konditionstechnik

System ermittelt alle Konditionen und deren Wirkung anhand des folgenden Schemas:

1. Gibt es Konditionen?
2. Trifft die Kondition zu?
3. Ist die Konition gültig? (Zeitraum, Kunde, ...)
4. Welche Auswirkungen hat die Kondition?

Der Vorschlagswert kann überschrieben werden, es können z.B. Konditionen in der Höhe geändert werden oder ganz entfernt werden.

Die Konditionstechnik ist ein zentrales Element von SAP und gilt nicht nur für Rabatte, Zuschläge, Versandkosten, Steuern, etc. sondern analog auch für **Nachrichten** und **Stammdaten**.

## Kopfkonditionen

Eine Kopfkondition wird auf alle Positionen eines Beleges angewandt.

- Arbeitserleichterung
- Fehlerminimierung

## Positionskonditionen

Eine Positionskondition ist nur für eine Position eines Beleges gültig.

- flexibler

## Staffelrabbat

Mit steigender Menge nehmen die Kosten für ein einzelnes Stück des Materials ab. Schwellenwerte sind die Staffeln

Ab 1 Stück kostet mich das Einzelstück €305, ab 10 Stück kostet mich das Einzelstück €295, ab 30 Stück kostet mich das Einzelstück €285

Macht Preislisten mit Staffelrabbaten und manuellem Lookup obsolet

## Naturalrabatt

- Draufgabe: 100 Stück werden bestellt und 105 Stück geliefert
- Dreingabe: 100 Stück werden bestellt und nur 95 Stück müssen bezahlt werden
- Muss nicht das gleiche Produkt sein, z.B. Mountainbike und gratis Urlaubsgutschein

## Substitut

Produkt wird durch ein mindestens gleichwertiges Produkt **ersetzt**.
Z.B. Kiste Duff mit einem gratis Glas. Diese Aktion gilt nur während der Weihnachtszeit.

## Umsatzsteuer

Umsatzsteuer ist auch eine Kondition. Diese kann unter bestimmten Umständen entfallen
- Kunde in einem Drittland (EU-Ausland)
- Vorsteuerabzug

# Beschaffungszyklus

1. Bedarfsermittlung
  - Wer benötigt etwas? Für wie viele Stellen muss ich disponieren?
  - Was wird benötigt?
  - In welcher Quantität und Qualität wird es benötigt?
  - Wann wird es benötigt?
2. Bezugsquellenfindung
  - Sammeln von Informationen / Aussenden von Anfragen / Einholen von Angeboten
  - Wo bekomme ich die Materialien?
  - Zu welchen Konditionen? Welche Materialien?
  - Welche Erstzmaterialien?
3. Lieferantenauswahl
  - Lieferbedingungen
  - Kriterien der Auswahl (z.B. Orderbuch)
4. Bestellabwicklung
  - formeller Akt der Bestellung
  - **Bestätigungsverfahren**
    - Auftragsbestätigung einholen (wichtig um Verständnis des Lieferanten von der Bestellung zu überprüfen --> Reaktionsmöglichkeiten)
    - sonstige Dokumente (Einfuhrbestimmungen) einholen
5. Bestellüberwachung
  - Kann der Lieferant die Bestellkriterien einhalten?
  - Kann der Lieferant gemäß den Kritieren der Logistik liefern?
  - Via Konditionstechnik kann das System automatisch mit dem Lieferanten kommunizieren und Warnungen versenden
  - Agieren auf Lieferschwierigkeiten des Lieferanten
  - **Avis**
    - Information über eintreffende Lieferung trifft vor der eigentlichen Lieferung ein
    - Datenfluss vor Materialfluss
    - Voreinspeisung der Informationen ins System
    - bessere Disponierungsmöglichkeiten
      - Lagerplatz
      - Personaleinteilung
      - Umgang mit gefährlichen Gütern
6. Wareneingang
  - Prüfen, ob man der tatsächliche Warenempfänger ist (z.B. Lieferung auf Baustelle)
  - Vollständigkeit der Daten?
  - Prüfung **Quantität und Qualität**, sofern möglich
    - mit Vorbehalt übernehmen
  - optische Prüfung (Sichtkontrolle)
  - Daten werden für **Lieferantenbeurteilung** verwendet
  - Materialien werden üblicherweise mit Vorbehalt übernommen --> weitgehend akzeptiert
  - großes Verbesserungspotential mit automatisierter Datenerfassung (Barcode, QR-Code, NFC-Tags)
  - Wareneingangbearbeitungszeit
    - Gibt es Materialien, die bestimmten Anforderungen unterliegen? z.B. Lebensmittel, Pharmazeutika, gefährliche Materialien --> **Lagervorschriften**
    - Qualitätsprüfung (aufgrund von verschiedenen Bewegungsarten (z.B. Buchung in den Qualitätsprüfbestand))
      - **Prüfung --> Prüfungsergebnis --> Verwendungsentscheid**
	- evtl. Buchung in den Zollbestand
7. Rechnungsprüfung
  - Bestellnummer/Lieferscheinnummer prüfen und nachverfolgen
    - bei Nichtvorhandensein bis zum letzten Tag warten und erst zum letzten Zeitpunkt Meldung an den Kunden --> Zeit wird gewonnen
  - Kann die Rechnung einer Bestellung zugeordnet werden?
  - Stimmt die Rechnung mit dem Lieferschein und den eingetroffenen Materialien überein? --> **Wareneingangsbezogene Rechnungsprüfung**
    - (System kontrolliert automatisch): Bei Diskrepanzen wird die Rechnung gesperrt
    - System erfordert Bestätigung --> Abklärung der Differenz
    - Alternative: Schwellenwert kann gesetzt werden
  - Rechnung erfassen
8. Zahlungsabwicklung
  - Skonto
  - Bei Ausnutzung durch den Kunden:
    A. Kunden mahnen
    B. Kunden sperren und evtl. Kosten einklagen; Vorsicht: System bucht die Bestellung selbst bei Inanspruchnahme der Toleranzgrenze als vollständig ein
  - bei Zahlungszielverfehlungen situativ entscheiden
    - Gespräch mit Kunden (anrufen und nachfragen)
  - Mahnung schicken
  - Miteinkalkulieren des ungerechtfertigten Rabbates

**Die Reihenfolge im Vertrieb ist analog**.
  
## Wodurch kann ein Bedarf entstehen?

- Auftragslage (Verbrauch)
- saisonale Einflüsse
- vorhersagbarer Verbrauch
- Werbung

## Rechnung erfassen

Bestellnummer und Betrag eingeben, um **wareneingangsbezogene Rechnungsprüfung** anzustoßen.
Bei Unstimmigkeiten wird die **Rückstandsbehandlung** angestoßen. Hierfür wird der Einkaufswerteschlüssel herangezogen.

### Wareneingangsbezogene Rechnungsprüfung

Die eingegebene Summe muss dem Wert der Einzelposten der Bestellungen (Menge * Preis pro Stück) entsprechen.
Differenzen könnten aufgrund von ungeplanten Bezugsnebenkosten oder Fehler des Lieferanten entstehen.

#### Behandlung von Unstimmigkeiten

Bei Abweichungen wird die Rechnung gesperrt. Anschließend ist eine **Klärung** erforderlich.

### Einkaufswerteschlüssel

Dieser legt fest, dass bei Abweichungen um einen gewissen Toleranz- oder Schwellenwert die Bestellung trotzdem als abgeschlossen gilt.

## Optimierung Warenübernahme/Wareneingangsprozess

### Zeitliche Optimierungen

**Datenfluss dem Materialfluss vorziehen**
  - Aviso: Welche Ware kommt zu welcher Bestellung in welcher Menge geliefert
    - Vorbereitung
  - Daten systemtechnisch erfassen, aber noch nicht als okay kennzeichenen
  - z.B. Barcode oder RFID


## Lieferantenbeurteilung

Die Informationen aus dem Wareneingang werden vom Qualitätsmanagement in objektive Kenzahlen miteinbezogen.
Darüber hinaus werden noch die Ergebnisse der Qualtitätsprüfungen miteinbezogen.
Der Einkauf kann mittels des **Orderbuches** auf die Kennzahlen zugreifen.

### Orderbuch

Pro Material kann eingetragen, wer liefern darf und wer bestimmt **nicht** liefern (Sperre) darf.
Das Orderbuch verhindert somit unter anderem Bestellungen von unerwünschten Lieferanten.
Ein laufendes Insolvenzverfahren ist ebenfalls ein möglicher Sperrgrund.
Beim Orderbuch handelt es sich um eine Blacklist.

#### Quotierung

Bei mehreren Lieferanten im Orderbuch festgelegt werden, welche Lieferanten welchen Anteil (z.B. in Prozent) pro Auftrag liefern.

## Belegnavigation

Innerhalb einer Prozesskette kann ohne Verlassen der Transaktion auf alle vorgehenden und nachfolgenden Dokumente zugegriffen werden.
Z.B. Einstieg über Rechnung --> Bestellung --> Anfrage --> Lieferschein --> ...
Ermöglicht eine sehr schnelle Navigation

# Bezahlung

System kümmert sich anhand der hinterlegten Zahlungsbedingungen um die Bezahlung.

# Änderungen

Stammdaten können flexibel nach Werk, Buchungskreis, etc. geändert werden.
Diese Änderungen können **sofort** oder **geplant** erfolgen.

# Inventur

Bestandsaufnahme. Als **Folge** wird verglichen, ob der Soll- und der Ist-Bestand übereinstimmen.
Abweichungen werden als Differenz bezeichnet.
Ziel der Inventur ist es, dass der Staat nachvollziehen kann, dass die Steuerberechnung korrekt durchgeführt wurde.

## Arten der Inventur

### Stichtagsinventur

Zu einem gewissen Stichtag (typischerweise gegen Ende des Geschätsjahres) wird eine Inventur durchgeführt.
Die Informationen werden normalerweise in die Bilanz übernommen.

### Permanente Inventur

Die Inventur wird laufend über das Jahr verteilt durchgeführt und es wird der gesamte Bestand eines oder mehrerer, aber nicht aller Materialien erfasst.

#### Cycle Counting

Eine Abwandlung der permanenten Inventur, bei der in bestimmten, sehr kurzen Intervallen, z.B. täglich,  wöchentlich oder monatlich gezählt wird.
+ Differenzen sind wesentlich rascher erkennbar --> geringere Reaktionszeit

### Stichprobeninventur

Bestimmte Unternehmen müssen unter passenden Wirtschaftsprüfern nur Stichproben von Materialien entnehmen.

# Fixierte Prüfungsfrage

Wo ist der Unterschied zwischen dezentraler und zentraler Datenerfassung bei Materialstammdaten? Wo sehen Sie Vorteile und Nachteile?
