# badge-2025

Repository containing the schematics for the flex PCB badge distributed at ESC{21}.

The schematics are licensed under the CERN OHL S v2 license.

The badge has been designed by [Jacopo Franco](https://www.jacopofranco.com/), that we thank for the effort in making this literal show of force a reality ;)

Special thanks to [Kezi](https://github.com/Kezii), [Kowalski](https://github.com/kowalski7cc), [K3lite](https://github.com/k3lite) & [Baobots](https://github.com/baobots) for the efforts spent into debugging & flashing all of them during the camp.

<video src="https://github.com/user-attachments/assets/acb0492f-e134-4207-b74a-9145ce9de10b"
       autoplay
       loop
       muted
       playsinline
       width="600">
  Your browser does not support the video tag.
</video>

---

# Badge Instructions

## Assembly

* The badge must be folded into position.
* To keep it fixed, we recommend using **UV glue**, **superglue**, or **thin double-sided tape**.
* **Do not solder directly** onto the PET substrate — this is very challenging, even with bismuth low-temperature solder.

## Flashing
**USB communication is not supported** — the port is for charging only.
To flash the badge the first time, make use of the UART and the power pins as below.
<img width="1218" height="875" alt="image" src="https://github.com/user-attachments/assets/7f707868-9cc5-4d37-8273-82cef5252e65" />

![IMG_20250902_101329](https://github.com/user-attachments/assets/165c65da-b0e7-44ce-9ee8-5df67cab85ef)

### USB-C Connector

* The USB-C must also be folded.
* Align the tab with the solid line located after the resistors.
* With the **copper contacts facing outward**, insert the connector into a male USB Type-C cable.
![photo_2025-09-19_21-49-55](https://github.com/user-attachments/assets/9454eea4-f0d2-480c-87d8-d513d1e05e67)

---

## Charging
* There are no LEDs to indicate charging progress. The charger is however guaranteed to fully charge the battery in 2.5h. The battery is fully protected and the charger has multiple overcurrent, overvoltage and temperature protections. It can trickle-charge.
* An **interrupt pin** connected to the charger will change state during charging. You will have to implement it yourself.

---

## Firmware

* The badge ships with the **WLED firmware** by default.
* * Firmware updates can be done via **WLED OTA** or the **Serial pads**.
* To connect:

  1. Connect to the Wi-Fi network:

     ```text
     SSID: wled-ap  
     Password: wled1234
     ```
  2. Open the address in your browser:

     ```text
     4.3.2.1
     ```

---


## Pinout

```text
Charger status:       GPIO 10
Battery voltage:      Analog GPIO 3 (divider only enabled when LED MOSFET is ON)
LEDs MOSFET:          GPIO 4
LED data:             GPIO 8
I²C SDA:              GPIO 7
I²C SCL:              GPIO 6
Touch button 1:       GPIO 0
Touch button 2:       GPIO 1
```

---
