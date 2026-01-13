---

# ESP-01 ADC Mod

Вот аккуратно отформатированный и логически цельный вариант, без «разрыва» предложения:

> ESP-01 is **the only ESP module with DIP pins**, one of the most compact ESP boards, with **4 accessible pins** (with some limitations). However, the **lack of ADC** strongly limits its use in autonomous or analog projects.
> 
> The **ESP8266 is significantly more powerful than Arduino Uno/Nano**, with built-in Wi-Fi and vastly more memory, and there is a **huge number of ready-made modules** designed specifically for it.

This repository documents a simple hardware modification for ESP-01 modules that enables ADC usage.

![Soldering process](img/cover.JPG)

---

## What Was Modified

- Original **RESET routing** was intentionally removed, as rarely needed

- A thin wire was soldered directly to the **ESP-01 RST pin**

- The wire was routed to the **ESP8266 chip ADC pin pad**

- When the wire end was fully aligned with the pad, it was pressed with the soldering iron

- Nearby capacitor was temporarily removed for easier access

**All soldering was done using a regular soldering iron, lenses, and three hands—no hot air, no microscope.**

![Soldering process](img/soldering.jpg)

---

## Result

- Fully working **ADC (ex-RST) pin**

- Optional ADC access for **battery voltage monitoring**

- ESP-01 becomes suitable for:
  
  - Battery-powered devices
  
  - Ready for reading **any analog sensors**
  
  - Autonomous IoT nodes

---

## Notes

- Secure wires after soldering (glue or coating recommended)

- Verify connections with a multimeter before powering up

This modification allows reusing ESP-01 modules in modern low-power and analog projects instead of replacing them with larger ESP-12 or ESP32 boards.

---
