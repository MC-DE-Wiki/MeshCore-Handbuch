## Firmware-Bin-Datei auf ESP32 flashen

Die Installation der Firmware-Bin-Dateien auf den verschiedenen ESP32-Boards ist mittlerweile ganz einfach. Am einfachsten geht das mit dem browserbasierten Online-Flasher von Adafruit:

https://adafruit.github.io/Adafruit_WebSerial_ESPTool/

Hier wird „**WebSerial**“ verwendet. Möglicherweise musst du dies in den Browsereinstellungen explizit zulassen und/oder „experimentelle“ Funktionen aktivieren. Eine Erklärung dazu findest du hier:

https://learn.adafruit.com/adafruit-magtag/web-serial-esptool

Wenn du dein ESP32-Board per USB anschließt und oben rechts auf „Verbinden“ klickst, kannst du festlegen, welche Partitionen überschrieben werden sollen. Die werkseitigen Standardpartitionen reichen in der Regel aus. In Extremfällen musst du möglicherweise den Bootloader und andere Systempartitionen wiederherstellen, bevor du die Hauptpartition „Anwendung“ hochlädst. 

Die Hauptpartition „Anwendung“ befindet sich am Offset 0x10000. Gebe diesen Wert im oberen Menü ein, klicke auf „Datei auswählen“ und wähle die .bin-Datei auf deinem lokalen Dateisystem aus. Klicke anschließend auf „Programm“, um den Upload zu starten. 

Warte, bis der Fortschrittsbalken angezeigt wird. Wenn alles abgeschlossen ist, trenne die Karte vom Computer und schließe sie wieder an, um sie zurückzusetzen (oder drücke die Reset-Taste).

![20250415-1305](https://github.com/user-attachments/assets/46c90449-825a-46b4-8d9b-a8585ce52aae)


[Quelle](https://buymeacoffee.com/ripplebiz/flashing-firmware-bin-esp32)