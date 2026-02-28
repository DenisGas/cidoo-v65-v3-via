# CIDOO V65 V3 VIA Config Fix

This repository provides an **updated VIA JSON configuration** for the CIDOO V65 V3 keyboard.

It fixes incorrect key ordering in the OEM JSON that caused brightness and battery commands to behave incorrectly in VIA.

---

# 💾 Download

* [VIA 2.4G mode JSON](https://github.com/DenisGas/cidoo-v65-v3-via/releases/download/v1.0.0/CIDOO_V65_V3_2.4G.JSON)
* [VIA Wired (USB) mode JSON](https://github.com/DenisGas/cidoo-v65-v3-via/releases/download/v1.0.0/CIDOO_V65_V3_USB.JSON)

Use the file that matches your current connection mode.

---


# 🛠 Background

On the OEM version of the CIDOO V65 V3, several standard commands:

* Brightness increase
* Brightness decrease
* Battery status

did not work as expected inside VIA.

After investigation, it turned out that **the keycodes were placed in the wrong order** in the original JSON definition. Because VIA depends on the order of custom keycodes, the labels did not match the real firmware behavior.

This fix:

* Reorders the keycodes
* Corrects their labels
* Keeps firmware logic untouched

No flashing or firmware modification is required.

---

# ⚡ Key Changes (Corrected Order)

| Original (OEM)                                                                           | Fixed for VIA                                                                | Function               |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------- |
| `DESKTOP LIGHT LOW` <br>title: "desktop lihgt low" <br>shortName: "DESKTOP LIGHT LOW"    | `MAYBE KEY SCAN DELAY` <br>title: "KEY SCAN DELAY" <br>shortName: "KSDELAY"  | OEM technical function |
| `DESKTOP LIGHT HIGH` <br>title: "desktop lihgt high" <br>shortName: "DESKTOP LIGHT HIGH" | `DESKTOP LIGHT LOW` <br>title: "Brightness decrease" <br>shortName: "BRI −"  | Decrease brightness    |
| `BATTERY STATUS` <br>title: "BATT_SHOW" <br>shortName: "BATT ST"                         | `DESKTOP LIGHT HIGH` <br>title: "Brightness increase" <br>shortName: "BRI +" | Increase brightness    |
| `KEY SCAN DELAY` <br>title: "KEY SCAN DELAY" <br>shortName: "KSDELAY"                    | `BATTERY STATUS` <br>title: "Show battery level" <br>shortName: "BATT"       | Display battery level  |

> ⚠️ Important:
> The real behavior of the buttons is defined by the firmware.
> This update only fixes VIA labels and their order.

---

# 📊 Layout Comparison

## ❌ Incorrect VIA Layout (OEM JSON)

With the original OEM JSON file, VIA displays incorrect labels and mismatched key behavior.

<img width="1910" height="725" alt="image" src="https://github.com/user-attachments/assets/07429377-0ea3-423c-a2a2-c23eb0923939" />

### Issues:

* Brightness controls reversed
* Battery function mapped incorrectly
* Key order does not reflect firmware behavior

---

## ✅ Correct VIA Layout (Fixed JSON)

After applying the updated JSON from this repository, VIA displays the correct layout and behavior.

<img width="1919" height="783" alt="image" src="https://github.com/user-attachments/assets/d3974a61-4a49-46eb-bf63-fa68ebaaae3f" />

### Fixes:

* Keycodes reordered properly
* Brightness increase/decrease labeled correctly
* Battery status correctly assigned
* Layout now matches real hardware behavior

---

# 🎨 Visual Function Guide

* **BRI − (DESKTOP LIGHT LOW)** → Decrease brightness
* **BRI + (DESKTOP LIGHT HIGH)** → Increase brightness
* **BATT (BATTERY STATUS)** → Show battery level
* **KSDELAY (MAYBE KEY SCAN DELAY)** → OEM scan delay function

---

# 📌 Official References

Original files from Epomaker:

* VIA 2.4G JSON
  [https://epomaker.com/blogs/via-json/cidoo-v65-v3-2-4g-json-file](https://epomaker.com/blogs/via-json/cidoo-v65-v3-2-4g-json-file)

* VIA Wired (USB) JSON
  [https://epomaker.com/blogs/via-json/cidoo-v65-v3-usb](https://epomaker.com/blogs/via-json/cidoo-v65-v3-usb)

* Manual
  [https://epomaker.com/blogs/manuals/cidoo-v65-v3-manual](https://epomaker.com/blogs/manuals/cidoo-v65-v3-manual)

---

# 🔧 How to Add the Keyboard to VIA (Chrome Only)

> ⚠️ Use Google Chrome. Other browsers may not detect the keyboard properly.

---

## 1️⃣ Download the JSON

Download the JSON file:

* From this repository (fixed version)
* Or from the official Epomaker website

Make sure you choose the correct version:

* Wired (USB)
* 2.4G Wireless

---

## 2️⃣ Open VIA

Go to:
[https://www.usevia.app/](https://www.usevia.app/)

---

## 3️⃣ Open Settings

Click the **Settings** icon.

<img width="1913" height="899" alt="image" src="https://github.com/user-attachments/assets/8c1e24e4-8b2f-4e4a-b4be-b5af1fed69b0" />

---

## 4️⃣ Enable Design Tab

Enable the toggle to show the **Design** tab.

<img width="1919" height="613" alt="image" src="https://github.com/user-attachments/assets/32adf9c1-25a3-4fca-ae48-a789e923be64" />

---

## 5️⃣ Open Design Tab

Click the **Design** tab (brush icon).

<img width="1916" height="588" alt="image" src="https://github.com/user-attachments/assets/5835d394-b762-4819-8cfe-c6eaec38e6ff" />

---

## 6️⃣ Enable V2 Definitions

Turn ON:

**Use V2 definitions (deprecated)**

<img width="1611" height="704" alt="image" src="https://github.com/user-attachments/assets/187ba398-b675-4c5b-a259-225ca828e6dc" />

---

## 7️⃣ Click Load

Press the **Load** button.

<img width="1826" height="654" alt="image" src="https://github.com/user-attachments/assets/23cdd6b4-f53d-4abc-86ab-a9c8e8811952" />

---

## 8️⃣ Select the Correct JSON File

Choose the JSON file that matches your current connection mode.

<img width="698" height="288" alt="image" src="https://github.com/user-attachments/assets/2459abc1-db08-4edc-80dc-741fc15de368" />

---

## 9️⃣ Select Your Keyboard

After loading the file, select your keyboard from the list.

<img width="1791" height="760" alt="image" src="https://github.com/user-attachments/assets/33b41cb8-ec87-4c0b-bf09-52eacfd0c46c" />

---

## 🔟 Go to Configure Tab

Switch to the **Configure** tab (keyboard icon).

<img width="1759" height="856" alt="image" src="https://github.com/user-attachments/assets/add7d524-7761-40af-8ecc-3e49dbd33f56" />

---

## ✅ Done

Your keyboard should now be properly detected and ready for customization.

<img width="1916" height="903" alt="image" src="https://github.com/user-attachments/assets/6eb65eb3-1959-408d-bfcb-bab876836829" />

---

# 🚨 Troubleshooting

If VIA does not detect the keyboard:

* Make sure you are using **Google Chrome**
* Verify your connection mode (USB or 2.4G)
* Reload the page
* Reconnect the keyboard

---
