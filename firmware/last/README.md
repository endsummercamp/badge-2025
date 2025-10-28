# 🔧 Flashing and Configuring WLED Firmware for BadgESC{21}

## 1. Flashing Firmware

First, flash the `.bin` file:

<img width="1874" height="1191" alt="Flashing firmware example" src="https://github.com/user-attachments/assets/f4dc8a18-981e-4be3-9cb9-f124fd5c5853" />

---

### 1.1 Connect to Access Point (AP)

Since the firmware does not yet have your Wi-Fi credentials, the badge will create its own access point (AP).
Connect to it using the following information:

* **SSID:** `WLED-AP`
* **Password:** `wled1234`

---

## 2. Upload Configuration

Once connected to the device, find its IP address and navigate there.


1. At the top of the page, click **Config** → **Security & Updates**.
2. Scroll down until you reach **Backup & Restore** and **Restore presets**.
3. Upload the preset file:

   * `wled_presets_BadgESC{21}.json`
     *(Be sure to press **Upload** after selecting the file.)*
4. Next, in the **Restore configuration** section, select and upload the file:

   * `wled_cfg_BadgESC{21}.json`
5. Wait approximately **10 seconds**, then **toggle the power switch** to perform a full reboot.

---

### 2.1 Reconnect and Final Setup

After rebooting:

1. Reconnect to the Access Point `WLED-AP`.
2. 🔗 **[http://badgesc.local](http://badgesc.local)**
3. Navigate again to **Config → Wi-Fi Setup**.
4. Enter your local Wi-Fi network credentials to connect the badge to your home network.
