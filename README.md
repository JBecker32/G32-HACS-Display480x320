# G32-Display 480x320 (JC3248W535C)
ESPHome Projekt für ein JC3248W535 Display zur Verwendung mit einem Otto Wilde G32 Gasgrill.
Diese Variante der Firmware zeigt die Daten grafisch mit Hilfe von 'Arcs' und 'Bars' (also Bögen und Balken) in verschiedenen Farben an. Alternativ gibt es noch eine Variante in Grautönen und nur mit Zahlen anstatt Grafikelementen (owg-g32-ha-jc3248w535-numbers). 

<img width="1729" height="1106" alt="image" src="https://github.com/user-attachments/assets/a9158e56-d6d5-44fd-928d-42a75e272495" />

Das Projekt setzt auf einer benutzerdefinierten HACS Integration des Otto Wilde G32 Grills in Home Assistant auf (owg-g32-ha-integration von zaubii).
Das Gerät baut eine Wifi Verbindung zum Home Assistant auf. Es liest dann einige der von der Integration bereitgestellen Daten aus HA aus und stellt sie grafisch auf dem Display dar.

Die Hardware des JC3248W535 stellt einen Anschluß für einen externen Lithium Akku mit integrierter Ladeschaltung zur Verfügung. Die Spannung des Akkus wird gemessen und ausgewertet. Bei Unterschreiten eines bestimmten SOC (aus der Entladespannung abgeleitet) wird im Display ein Icon einer leeren Batterie eingeblendet.

Zusätzlich kann im JC3248W535 ein Piezo-Summer (nur Typen ohne eingebaute Elektronik!) angeschlossen werden. Ich benutze hier nicht den mit Speaker bezweichneten 2-poligen Anschluß (dieser wird über einen eingebauten I²C Chip angesteuert und ist aufwändiger in der Benutzung) sondern die GPIOs 9 und 14 auf dem 8-poligen Steckverbinder. Der Summer wird an diversen Stellen genutzt, so z.B. bei Aufbau und Verlust der Wifi Verbindung oder auch bei Temperaturwarnungen (more to follow ...).

# Hardware
Das Display ist ein JC3248W535C von der Firma Guition mit einer Diagonale von 3,5" und 480x320 Pixeln.

