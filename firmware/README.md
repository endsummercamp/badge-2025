![photo_2025-09-17_22-10-04](https://github.com/user-attachments/assets/5ef2ba0d-c5d9-491a-9bbe-13408f437ca4)

![photo_2025-09-02_09-13-37](https://github.com/user-attachments/assets/165c990e-35e8-48a7-97b6-f48975532ef7)

The badge USB is physically unstable because of very tight tolerances in the port.
Please notice the points used to flash the badge in the picture above. You will need some thin-tip probes.

The .bin file is all you need. It's a 1:1 dump of the internal memory, containing WLED and all its settings. Feel free to flash it and then recompile a fresh new version.


## How to flash the first time

```
esptool.py --port=/dev/ttyUSB0 write-flash 0x0 backup.bin
```

---

# Recompiling the Firmware for BadgESC{21}

If you wish to recompile the WLED firmware yourself to customize features or update configurations, follow the instructions below.

## Steps to Recompile

1. Open the official WLED Web Compiler:
   [https://wled-compile.github.io/](https://wled-compile.github.io/)

2. Click **Load configuration from a file**.

3. From your computer, select the configuration file:
   `WLED_compile_dd_mm_yyyy_BadgESC{21}.json`

4. Click **Regenerate** to rebuild the firmware using the provided configuration.

5. After regeneration, you may customize and compile your firmware as required.

After compilation, download the resulting `.bin` file and flash it to your device following the standard WLED installation procedure.
