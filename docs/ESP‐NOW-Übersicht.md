Der ESP-NOW-Code befindet sich nun im [GitHub-Repo](https://github.com/ripplebiz/MeshCore), zusammen mit Build-Zielen für die vier wichtigsten Firmware-Typen: Repeater, USB-Seriell-Companion, Raumserver und Terminal-Chat. Dies ist im Wesentlichen noch nur für Entwickler gedacht. Es gibt lediglich diese vier Generic_ESPNOW_*-Ziele, die du für das gewünschte Board anpassen musst.

Damit kannst du ein Mesh erstellen, das genau wie mit LoRa-Geräten funktioniert, jedoch über die WLAN-/ESP-NOW-Endgeräte (zum Beispiel einem Heltec V3). Die Reichweite zwischen den Knoten beträgt maximal etwa 500 Meter, in typischen Anwendungsfällen eher 100 Meter. Im Grunde ist es jedoch identisch: Repeater, Advert, Nachrichten, Räume usw. Die Latenz ist jedoch gering, sodass du beispielsweise problemlos Dutzende von Repeatern nutzen kannst.

![024750_1743994068106_espnowonlymesh jpg](https://github.com/user-attachments/assets/39428a3b-14b1-4bae-9bd3-072895909625)

(Beispiel für ein ESP-NOW-Netz, Repeater, Raumserver und einige Client-Knoten)

### Bridge

Es gibt bereits eine [Bridge-Firmware](https://buymeacoffee.com/ripplebiz/e/405835), die eine einfache ESP-NOW <-> LoRa-Bridge darstellt. Dies eröffnet vielfältige Möglichkeiten. HINWEIS: Dieses Bridge-Gerät ist technisch gesehen kein Knoten, da es keine ID hat.

![025617_1743994575917_bridgedespnowloramesh jpg](https://github.com/user-attachments/assets/811c6a95-71bd-4618-b167-b5f464cb734b)

Bezüglich Hops und Pfaden trägt der Bridge-Knoten nichts zu den Pfaddaten bei. Daher gehen die beiden LoRa-Knoten (blau) konzeptionell einen Hop zum ESP-NOW-Repeater (rot) in der Mitte.


### Bridging zweier LoRa-Netze

Du kannst zwei Bridge-Geräte verwenden, um zwei LoRa-Netze zu verbinden, die beispielsweise zwei verschiedene Spreizfaktoren nutzen:

![030429_1743995068111_bridgedsfmesh jpg](https://github.com/user-attachments/assets/7762ba6c-2964-44d9-84d2-04aab588f8df)

Denke daran, dass die beiden in jeder SF-Region abgebildeten Repeater konzeptionell nur einen Hop voneinander entfernt sind, obwohl sie über die Brücken in der Mitte kommunizieren.

### Gateway-Knoten

Eine fortschrittlichere Knoten-Firmware namens Gateway-Knoten ist in Arbeit. Dieser Knoten ist tatsächlich ein Knoten (hat eine ID) und kann wie Repeater Pakete für beide Seiten des Gateways routen und auch Pakete in und aus dem „anderen“ Mesh routen.

![031629_1743995788377_gatewayespnowloramesh jpg](https://github.com/user-attachments/assets/ba7a232b-8269-474b-a3f3-e9094d34cd81)

Es besteht außerdem die Möglichkeit, Regeln für Aspekte wie Sichtbarkeit zu konfigurieren (z. B. welche ESP-NOW-Geräte nur untereinander und nicht an das breitere LoRa-Netz weiterleiten sollen).

Diese Art der Konfiguration ist besonders nützlich für Gebäude oder Sensorcluster, bei denen nur ein Teil des ESP-NOW-Datenverkehrs an das breitere Netz weitergeleitet werden muss.

### Privates Sub-Netz

Eine Funktion, die bald benötigt wird, insbesondere wenn beispielsweise zwei ESP-NOW-Netze physisch nahe beieinander liegen, sind die von Reticulum als IFAC (Interface Access Codes) bezeichneten Schnittstellenzugriffscodes. Wahrscheinlicher ist, dass ein ESP-NOW-Netz standardmäßig privat sein sollte. Wenn es nur für ein Grundstück oder Gebäude gilt, sollte es keine Daten für andere Grundstücke weiterleiten. Und wenn ein breiterer Zugriff benötigt wird, sind Bridges/Gateways die Lösung. Ein öffentliches ESP-NOW-Netz ist weder wahrscheinlich noch praktisch.

Auf Protokollebene wird es daher eine Möglichkeit geben, IFAC-Codes in einzelne Pakete zu kodieren. Repeater/Gateways können die Weiterleitung sofort verweigern, wenn der IFAC-Code falsch ist oder gar nicht vorhanden ist (z. B. ein öffentliches Paket). So könnten zwei private ESP-NOW-Netze nebeneinander existieren (oder sich sogar überlappen) und die Pakete des jeweils anderen ignorieren. Dasselbe gilt für ein privates LoRa-Netz. Nur autorisierte Knoten dürfen für IFAC-Codes konfigurierte Repeater verwenden.

### Neue Gadgets

Der 2,8-Zoll-Touchpager, wurde überarbeitet (und vereinfacht), sodass er nun mit dem nackten Entwicklungsboard (einem Waveshare 2,8-Zoll-ESP32-S3 mit Touch-Display) ins Mesh eingebunden werden kann. Außerdem wurde die „Ultra“-Firmware auf das [T-Display S3 Touch Pro](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/T%E2%80%90Display-S3-Pro) portiert, ein wirklich praktisches kleines Gerät in einem übersichtlichen Gehäuse:

![032932_1743996571104_Screen_Shot_20250407_at_1 25 47_pm](https://github.com/user-attachments/assets/bf59990e-c151-4011-a0d8-3ef44106a010)

Solange sich also ein Bridge-Knoten in der Nähe befindet, können diese beiden Geräte (links) problemlos mit dem Rest des Meshes interagieren. Die „ESP-NOW only“-Firmware für [T-Display Pro](https://github.com/MC-DE-Wiki/MeshCore-Handbuch/wiki/T%E2%80%90Display-S3-Pro) gibt es bereits, die für das Waveshare wird in Kürze veröffentlicht.

[Quelle](https://buymeacoffee.com/ripplebiz/esp-now-overview)
