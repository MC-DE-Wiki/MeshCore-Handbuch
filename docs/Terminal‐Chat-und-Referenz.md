Wenn Du Heltecs oder andere Boards in der Schublade liegen hast und kein T-Deck besitzt, ist es kostenlos, ein eigenes kleines Mesh einzurichten. Flashe einfach zwei „Terminal Chat“-Knoten, und schon kannst du über eine Kommandozeile chatten. Flashe einen Repeater-Knoten, stecke ihn in eine Tupperware-Dose und werfe ihn in einen Baum – und voilà: enorme Reichweite! 

Der Terminal Chat wurde bereits mit diesem Setup getestet:

![20250525-0900](https://github.com/user-attachments/assets/bc1697b2-0b62-49d2-bf3d-91142de49680)


#### Terminal‐Chat Referenz

Nachfolgend sind die Befehle aufgeführt, die du in den Terminal-Chat-Clients eingeben kannst:


```
set freq {frequency}
```
Stellt die LoRa-Frequenz ein. Beispiel: set freq 869.525

```
set tx {tx-power-dbm}
```
Legt die LoRa-Sendeleistung in dBm fest.

```
set name {name}
```
Legt deinen Anzeigennamen fest.

```
set lat {latitude}
```
Legt den Breitengrad im Advert fest. (Dezimalgrad)

```
set lon {longitude}
```
Legt den Längengrad im Advert fest. (Dezimalgrad)

```
set af {air-time-factor}
```
Legt den Air-Time Faktor fest


```
time {epoch-secs}
```
Stellt die Geräteuhr in UNIX-Epochesekunden ein. Beispiel:  time 1738242833


```
advert
```
Sendet ein Advertisement Paket

```
clock
```
Zeigt die aktuelle Uhrzeit gemäß der Geräteuhr an.


```
ver
```
Shows the device version and firmware build date.

```
card
```
Zeigt *deine* „Visitenkarte“ an, damit andere sie manuell _importieren_ können

```
import {card}
```
Importiert die angegebene Karte in deine Kontakte.

```
list {n}
```
Listet alle Kontakte in der Reihenfolge der aktuellsten auf. (optional {n}, ist das letzte n nach Anzeigendatum)

```
to
```
Zeigt den Namen des aktuellen Empfängerkontakts an. (für nachfolgende 'send' Befehle)

```
to {name-prefix}
```
Legt den Empfänger anhand des Namenspräfixes auf den _ersten_ passenden Kontakt (in der „Liste“) fest. (Du musst also nicht den ganzen Namen eingeben.)

```
send {text}
```
Sendet die Textnachricht (als DM) an den aktuellen Empfänger.

```
reset path
```
Setzt den Pfad zum aktuellen Empfänger zurück, um einen neuen Pfad zu ermitteln.

```
public {text}
```
Sendet die Textnachricht an den integrierten „öffentlichen“ Gruppenkanal















