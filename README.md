# thesis-style-guide



## Definitionen

Der Gesamttext wird bezeichnet als *Dissertation* oder *Doktorarbeit* oder einfach nur *Text* oder *Arbeit*. 

Ebene 1: Der Text gliedert sich in einzelne …

\# Kapitel 

(z.B. „1. Einführung”, „7. Resümee”). 

Ebene 2: Ein Kapitel hat  

\## Abschnitte

, auch bezeichnet als Unterkapitel

(z.B. „1.4. Zentrale Fragestellungen”).  

Ebene 3: Ein Abschnitt setzt sich aus verschiedenen 

\### Unterabschnitten 

zusammen. (z.B. „z.B. 1.4.2. Forschungsfragen”).  

Ebene 4: Unterabschnitte bestehen aus 

\#### Textteilen

und haben keine eigene Nummerierung mehr.  

## Abbildungen

### Einfügen von Abbildungen

Zur Einbindung von Abbildungen wird auf den pandoc-Filter [pandoc-crossref](https://github.com/lierdakil/pandoc-crossref) zurückgegriffen. Er ermöglicht die automatische Nummerierung von Abbildungen und anderen Elementen der Arbeit. Damit sowohl Abbildungstitel als auch Abbildungsbeschreibung angezeigt werden können, wird ein kleiner Trick angewendet: Es werden zwei Bilddateien eingefügt, die obere ist jedoch nur ein Bild in der Größe von 1x1px in weiß. Ein Beispiel:  

    ![**Abbildungstitel**](/Users/ausse/Dropbox/__DISSERTATION/__HAUPTDOKUMENT/1.png){#fig:yolo}

    ![Bildbeschreibung](/Users/ausse/Dropbox/__DISSERTATION/_Abbildungen/5/10_yolo.png)

### Verweis im Text

Der Verweis im Text passiert mittels des Ausdrucks `@fig:bildkurzbezeichnung`. Die Bildkurzbezeichnung wird immer kleingeschrieben. Das Wort „Abbildung” wird automatisch bei der Umwandlung von Markdown hinzugefügt. Beispiel für Verweise im Text: 
	
    Zu sehen ist das in @fig:yolo:

Dieser Ausdruck wird nach der Umwandlung in Markdown zu: 

    Zu sehen ist das in Abbildung 1: 

Soll das Wort „Abbildung” weggelassen werden, fügt man es in eckiger Klammer ein. So wird der folgende Text in Markdown

    Schauen Sie sich Bild [-@fig:yolo] an. 

zu

    Schauen Sie sich Bild 1 an.
