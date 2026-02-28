# CIDOO V65 V3 VIA Config Fix

This repository contains an **updated VIA JSON configuration** for the CIDOO V65 V3 keyboard.

## 🛠 Background

On this keyboard, standard commands for brightness control and battery display did **not work as expected**. After investigation, it turned out that the **keycodes were in the wrong order in the firmware**, which caused VIA to display incorrect labels and functions.

This fix **only reorders and renames the keycodes in VIA** so that the labels now correctly match their real functions. Firmware logic remains untouched.

---

## ⚡ Key Changes (with proper order)

| Original (OEM)                                                                           | Fixed for VIA                                                                | Function                            |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ----------------------------------- |
| `DESKTOP LIGHT LOW` <br>title: "desktop lihgt low" <br>shortName: "DESKTOP LIGHT LOW"    | `MAYBE KEY SCAN DELAY` <br>title: "KEY SCAN DELAY" <br>shortName: "KSDELAY"  | OEM function (technical scan delay) |
| `DESKTOP LIGHT HIGH` <br>title: "desktop lihgt high" <br>shortName: "DESKTOP LIGHT HIGH" | `DESKTOP LIGHT LOW` <br>title: "Brightness decrease" <br>shortName: "BRI −"  | Decrease brightness                 |
| `BATTERY STATUS` <br>title: "BATT_SHOW" <br>shortName: "BATT ST"                         | `DESKTOP LIGHT HIGH` <br>title: "Brightness increase" <br>shortName: "BRI +" | Increase brightness                 |
| `KEY SCAN DELAY` <br>title: "KEY SCAN DELAY" <br>shortName: "KSDELAY"                    | `BATTERY STATUS` <br>title: "Show battery level" <br>shortName: "BATT"       | Display battery level               |

> ⚠️ Note: The actual behavior of the buttons is determined by the firmware. This update only corrects **VIA labels and order** so they match real functions.

---

## 🎨 Visual Guide for VIA

* **BRI − (DESKTOP LIGHT LOW)** – decreases underglow/desktop brightness
* **BRI + (DESKTOP LIGHT HIGH)** – increases underglow/desktop brightness
* **BATT (BATTERY STATUS)** – shows current battery level
* **KSDELAY (MAYBE KEY SCAN DELAY)** – technical scan delay / OEM function
  
---

## 💾 Download

* [VIA 2.4G mode JSON](#)
* [VIA Wired (USB) mode JSON](#)

Use these files directly in VIA to correct the labels and order for your CIDOO V65 V3 keyboard.

---

## 📌 References

Original Epomaker files: 
* [VIA 2.4G mode JSON](https://epomaker.com/blogs/via-json/cidoo-v65-v3-2-4g-json-file)
* [VIA Wired (USB) mode JSON](https://epomaker.com/blogs/via-json/cidoo-v65-v3-usb)
* [Manual](https://epomaker.com/blogs/manuals/cidoo-v65-v3-manual)

---
