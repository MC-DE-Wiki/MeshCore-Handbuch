### ESP32 OTA-Updates

Die Repeater- und Room-Server-Versionen ab v1.4.1 bieten die Möglichkeit, die Firmware OTA  (over the air) zu aktualisieren. [Melde dich einfach bei deinem Repeater oder Room-Server an](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/MeshCore%E2%80%90FAQ#repeater) und gebe in der Befehlszeilenschnittstelle „_start ota_“ ein. Daraufhin erhältst du eine URL, mit der du deinen Webbrowser verbinden kannst:

![428592531-2a8b474c-2d5e-4848-ac1c-0e0cd51d7155](https://github.com/user-attachments/assets/faa9ae39-9d95-4cbb-8b02-718250b5add6)

Der ESP32 erstellt die WLAN-SSID „**MeshCore-OTA“**, mit der du deinen Laptop oder dein Smartphone verbindest. Navigiere anschließend zur vorher angegebenen URL. Die Webseite sollte dann angezeigt werden. Beachte, dass unten der Knotenname und der Boardtyp angezeigt werden, z. B. „_SNR1 (Heltec) (Heltec V3)_“. Überprüfe die Richtigkeit und wähle anschließend über „_Datei auswählen_“ die neue Firmware-.bin-Datei aus. 

![428600770-3b2b95f1-686a-4eea-a734-486cd24614d6](https://github.com/user-attachments/assets/42c43f20-698b-458f-aae8-22b39db4e4ab)

**Hinweis**: Dies muss die „reguläre“-bin-Datei sein, nicht die -merged.bin!

![428597224-1b61bddd-38f7-446b-be43-c793078a16ba](https://github.com/user-attachments/assets/34d82f01-8932-4c81-9114-8d184ed96603)

Wenn alles gut geht, startet der Knoten neu, und du solltest eine entsprechende Anzeige sehen. Um das OTA-Update abzubrechen, gebe einfach „**reboot**“ in der Befehlszeilenschnittstelle ein.

![428592610-1a2d2377-6459-4a40-9bd9-60a872226e70](https://github.com/user-attachments/assets/729cf654-d0b0-40c8-a533-3426d852982a)

[Quelle](https://buymeacoffee.com/ripplebiz/meshcore-update-5)

