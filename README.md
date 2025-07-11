# G32-Display 480x320
ESPHome Projekt für ein JC3248W535 Display zur Verwendung mit einem Otto Wilde G32 Gasgrill.

![PXL_20250531_101818315 MP~2](https://github.com/user-attachments/assets/67b9ae62-9454-436c-98f0-ceb2c0f3f85f)

Dieses Projekt setzt auf einer benutzerdefinierten HACS Integration des Otto Wilde G32 Grills in Home Assistant auf (owg-g32-ha-integration von zaubii).
Das Gerät baut eine Wifi Verbindung zum Home Assistant auf. Es liest dann diverse Entitäten mit Daten eines G32 Grills aus HA aus und stellt sie grafisch auf dem Display dar.

Die Hardware des JC3248W535 stellt einen Anschluß für einen externen Lithium Akku mit integrierter Ladeschaltung zur Verfügung. Die Spannung des Akkus wird gemessen und ausgewertet. Bei Unterschreiten eines bestimmten SOC (aus der Entladespannung abgeleitet) wird im Display ein Icon einer leeren Batterie eingeblendet.

Zusätzlich kann im JC3248W535 ein Piezo-Summer (nur Typen ohne eingebaute Elektronik!) angeschlossen werden. Ich benutze hier nicht den mit Speaker bezweichneten 2-poligen Anschluß (dieser wird über einen eingebauten I²C Chip angesteuert und ist aufwändiger in der Benutzung) sondern die GPIOs 9 und 14 auf dem 8-poligen Steckverbinder. Der Summer wird an diversen Stellen genutzt, so z.B. bei Aufbau und Verlust der Verbindung zu Wifi und BT oder auch bei Temperaturwarnungen (more to follow ...).

