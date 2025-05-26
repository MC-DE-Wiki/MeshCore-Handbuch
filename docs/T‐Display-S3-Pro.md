## T-Display S3 Pro MeshCore Anleitung

![P1090398-01](https://github.com/user-attachments/assets/3b21c0d5-44ee-483f-8d8a-4c67ec0b7f6b)

Mit der **ESP-NOW-Edition** der Firmware für das [T-Display S3 Pro](https://www.lilygo.cc/products/t-display-s3-pro?bg_ref=cq3pUU7cD3) lässt sich ein Standardgerät in einen **MeshCore-Pager** verwandeln, der nur das **WLAN-Funkmodul** nutzt, um ein Mesh zu bilden. 

HINWEIS: Du kannst die Firmware auch mit einem zusätzlichen MeshCore [ESP-NOW Bridge-Knoten](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/ESP%E2%80%90NOW-%C3%9Cbersicht#bridge) verwenden, um die Reichweite auf ein größeres LoRa-Mesh zu erweitern.

### Firmware flashen

Als Erstes musst du die Firmware flashen. Lade die Firmware [hier](https://buymeacoffee.com/ripplebiz/e/397095) herunter und folge anschließend [dieser Anleitung](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/Firmware%E2%80%90Bin%E2%80%90Datei-auf-ESP32-flashen) zum Flashen auf das Gerät. (Du kannst jede beliebige ESP32-Flashing-Methode verwenden, dies ist jedoch eine der einfacheren Möglichkeiten.) Es gibt zwei Firmware-Bin-Dateien:

- Flashe bei neuen Geräten die `-merged.bin` auf den Offset 0. -ODER-
- Um von der vorherigen Version zu aktualisieren, flashe die einfache `.bin` auf den Offset (hex) 10000.

### Ersteinrichtung

Du solltest den Ripple-Startbildschirm und anschließend einige Hilfebildschirme sehen, die die 4-Wege-Tipp-Navigation für die Benutzeroberfläche erläutern. (Tippe in die vier verschiedenen Quadranten des Bildschirms, um vorwärts, rückwärts, aufwärts und abwärts zu navigieren.) Tippe auf den orangefarbenen Kreis auf dem Display, um die Eingabetaste zu drücken:

![20250426-1325](https://github.com/user-attachments/assets/f5f57534-6461-4d34-9bd9-97b7383c46aa)

Du wirst zunächst aufgefordert, das erste Netzwerkprofil zu erstellen, wie bei der T-Deck-Firmware. Diese spezielle ESP-NOW-Version unterstützt nur MeshCore über ESP-NOW. Du musst also nur einen Namen für das Profil eingeben (standardmäßig „ESPNOW“).

Navigiere vom Startbildschirm aus in das Netzwerkprofilmenü (wähle das oberste Element aus und navigiere dann nach rechts). Du solltest folgende Menüpunkte sehen:

![20250425_141016-01](https://github.com/user-attachments/assets/6e7d7146-d1ee-4a2f-8ee2-77add477586b)

Als Erstes lege deinen Anzeigenamen fest. Navigiere in das Menü „_Identity_“, gebe einen Namen ein und drücke die Eingabetaste. Ein neuer öffentlicher Schlüssel wird automatisch für dieses Profil generiert.

Es empfiehlt sich, das Gerät an dieser Stelle neu zu starten und die Uhr korrekt einzustellen. Schalte es entweder mit dem Schalter aus oder drücke die Reset-Taste (auf der Unterseite). Nach dem Neustart sollte der Bildschirm „_Clock Sync_“ angezeigt werden:

![20250425_140531-01](https://github.com/user-attachments/assets/0b08190c-8e36-4d13-b6b2-14866af2f8fb)

**HINWEIS**: Das T-Display verfügt leider über kein integriertes RTC-Uhrmodul, daher wird die Uhr beim Neustart zurückgesetzt. Du musst die Unixzeit ([Epoch Time Converter](https://www.epochconverter.com/)) entweder manuell eingeben oder ein GPS-Modul anschließen.

### GPS anschließen

Der serielle Port ist mit einem Quiic-Stecker (in der Nähe des Netzschalters) gut sichtbar:

![20250502_123503-01](https://github.com/user-attachments/assets/d617acf7-19b2-4fe9-b6f9-11906a9ccf53)

(Die Pin-Belegung auf der T-Display-Seite sollte lauten: TX, RX, 3,3 V, GND)

### Kontakte entdecken

Die restliche Benutzeroberfläche ist identisch mit der des T-Decks. Normalerweise öffnest du den Bildschirm „_Discover_“, um andere Geräte zu entdecken, und wählst dann im Knotendetailbildschirm das Menü „_Add to Home_“ aus. Sobald Kontakte auf deinem Startbildschirm angezeigt werden, kannst du einfach zu den verschiedenen Konversationsbildschirmen navigieren.

### Zusammenfassung

Bedauerlicherweise scheint das T-Display keine Möglichkeit zu bieten, über eingehende Nachrichten zu informieren (es gibt weder einen Ton noch blinkende LEDs). Der Bildschirm sollte jedoch eine Nachrichtenvorschau anzeigen.

Es handelt sich also nicht um ein perfektes Gerät, aber es könnte im Haus oder auf dem Grundstück sehr nützlich sein, insbesondere in Kombination mit einem [ESP-NOW <-> LoRa Bridge-Knoten](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/ESP%E2%80%90NOW-%C3%9Cbersicht).

[Quelle](https://buymeacoffee.com/ripplebiz/t-display-s3-pro-meshcore-guide)