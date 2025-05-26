Du kannst sowohl Repeater- als auch Room-Server-Geräte entweder seriell (und über die Terminal-App/Putty/Serial Monitor) oder über den T-Deck-CLI-Bildschirm konfigurieren.

## Nur serielle Befehle:

```
set freq {frequency}
```
Beispiel:  set freq 869.525


```
time {epoch-secs}
```
Beispiel:  time 1743400059

```
erase
```
Löscht das lokale Dateisystem des Gerätes vollständig.

```
log
```
Vollständigen Paketprotokollinhalt anzeigen.


## Befehle über die serielle Schnittstelle oder die T-Deck-Benutzeroberfläche

```
advert
```
Sendet ein Node-Info Paket (Bekanntmachung)

```
reboot
```
Startet das Gerät neu. (Beachte, dass du wahrscheinlich eine „Zeitüberschreitung“ Meldung bekommst, was normal ist.)

```
clock
```
Zeigt die aktuelle Uhrzeit gemäß der Geräteuhr an.

```
password {new-password}
```
Legt ein neues Administratorkennwort für das Gerät fest.

```
set af {air-time-factor}
```
Legt den Air-Time-Faktor fest.

```
set tx {tx-power-dbm}
```
Legt die LoRa-Sendeleistung in dBm fest. (Neustart zum Anwenden)

```
set repeat {on|off}
```
Aktiviert oder deaktiviert die Repeater-Rolle für diesen Knoten.

```
set allow.read.only {on|off}
```
Raumserver (room server) Wenn „on“, dann ist die Anmeldung mit leerem Passwort erlaubt, aber es können keine Posts im Raum erstellt werden. (nur lesbar)

```
set flood.max {max-hops}
```
Legt die maximale Anzahl von Hops für eingehende Flood-Pakete fest (wenn >= max, wird das Paket nicht weitergeleitet)

```
set advert.interval {minutes}
```
Legt das Timerintervall in Minuten fest, um ein lokales (Zero-Hop-)Advertisement-Paket zu senden. Zum Deaktivieren auf 0 setzen.

```
set flood.advert.interval {hours}
```
Legt das Timerintervall in Stunden für das Senden eines Flood-Advertisement-Pakets fest. Zum Deaktivieren auf 0 setzen.

```
set guest.password {guess-password}
```
Legt das Gastkennwort fest/aktualisiert es. (Bei Repeatern können Gastanmeldungen die Anfrage „Statistiken abrufen“ senden.)

```
set name {name}
```
Legt den Anzeigennamen fest.

```
set lat {latitude}
```
Legt den Breitengrad auf der Karte fest. (Dezimalgrad)

```
set lon {longitude}
```
Legt den Längengrad der Karte fest. (Dezimalgrad)

```
set radio {freq},{bw},{sf},{cr}
```
Legt komplett neue Radioparameter fest und speichert sie in den Einstellungen. Zur Anwendung ist ein Neustart erforderlich.

Beispiel: 869.525,250,11,5
```
log start
```
Startet die Paketprotokollierung im Dateisystem.

```
log stop
```
Stoppt die Paketprotokollierung im Dateisystem.

```
log erase
```
Löscht die Paketprotokolle aus dem Dateisystem.

```
ver
```
Zeigt die Geräteversion und das Firmware-Erstellungsdatum an.


## Befehle ausschließlich über das T-Deck
```
clock sync
```
Synchronisiert die Uhr des Geräts mit der Uhr des T-Decks.

[Quelle](https://github.com/ripplebiz/MeshCore/wiki/Repeater-&-Room-Server-CLI-Reference)