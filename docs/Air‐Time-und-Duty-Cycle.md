### Maximale Air-Time / Duty Cycle

Der Arbeitszyklus von Funkgeräten wird häufig gesetzlich geregelt. Bitte prüfe die Vorschriften deiner lokalen Behörde, um sicherzugehen.

In Europa werden die Arbeitszyklen in Abschnitt 4.3.3 der Norm ETSI EN300.220-2 V3.2.1 (2018-06) geregelt. Dieser Standard definiert die folgenden Subbänder und deren Tastverhältnisse:

* K (863–865 MHz): 0,1 %
* L (865–868 MHz): 1 %
* M (868–868,6 MHz): 1 %
* N (868,7–869,2 MHz): 0,1 %
* P (869,4–869,65 MHz): 10 %
* Q (869,7–870 MHz): 1 %

Die Umrechnung von airtime zu duty cycle erfolgt mit folgender Formel:

`duty_cycle = 100/(airtime_factor + 1)`

Zusätzlich spezifiziert die LoRaWAN-Spezifikation Tastverhältnisse für die Verbindungsfrequenzen, die für Over-the-Air-Aktivierungen (OTAA) von jedem LoRaWAN-kompatiblen Endgerät verwendet werden. In den meisten Regionen beträgt das Tastverhältnis für diese Frequenzen 1 %.
Richtlinie zur fairen Nutzung

