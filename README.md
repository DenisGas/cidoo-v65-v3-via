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

# How to Add the Keyboard to VIA (Chrome Only)

> ⚠️ Use **Google Chrome**. Other browsers may not properly detect the keyboard.

---

## 1️⃣ Download the JSON File

Download the VIA JSON file:

* Use the fixed version from this repository
* Or download the original file from the official Epomaker website

Make sure you download the correct version for your connection mode:

* **Wired (USB)**
* **2.4G Wireless**

---

## 2️⃣ Open VIA

Go to:
👉 [https://www.usevia.app/](https://www.usevia.app/)

---

## 3️⃣ Open Settings

Click the **Settings** icon.

<img width="1913" height="899" alt="image" src="https://github.com/user-attachments/assets/8c1e24e4-8b2f-4e4a-b4be-b5af1fed69b0" />

---

## 4️⃣ Enable the Design Tab

Turn on the toggle to show the **Design** tab.

<img width="1919" height="613" alt="image" src="https://github.com/user-attachments/assets/32adf9c1-25a3-4fca-ae48-a789e923be64" />

---

## 5️⃣ Open the Design Tab

Go to the **Design** tab (brush icon).

<img width="1916" height="588" alt="image" src="https://github.com/user-attachments/assets/5835d394-b762-4819-8cfe-c6eaec38e6ff" />

---

## 6️⃣ Enable V2 Definitions

Turn ON:

**“Use V2 definitions (deprecated)”**

<img width="1611" height="704" alt="image" src="https://github.com/user-attachments/assets/187ba398-b675-4c5b-a259-225ca828e6dc" />

---

## 7️⃣ Click Load

Press the **Load** button.

<img width="1826" height="654" alt="image" src="https://github.com/user-attachments/assets/23cdd6b4-f53d-4abc-86ab-a9c8e8811952" />

---

## 8️⃣ Select the Correct JSON File

Choose the VIA JSON file that matches your current connection mode:

* Wired (USB)
* 2.4G Wireless

<img width="698" height="288" alt="image" src="https://github.com/user-attachments/assets/2459abc1-db08-4edc-80dc-741fc15de368" />

---

## 9️⃣ Select Your Keyboard

After loading the file, select your keyboard from the list.

<img width="1791" height="760" alt="image" src="https://github.com/user-attachments/assets/33b41cb8-ec87-4c0b-bf09-52eacfd0c46c" />

---

## 🔟 Go to the Configure Tab

Switch to the **Configure** tab (keyboard icon).

<img width="1759" height="856" alt="image" src="https://github.com/user-attachments/assets/add7d524-7761-40af-8ecc-3e49dbd33f56" />

---

## ✅ Done

Your keyboard should now be correctly detected in VIA and ready for customization.

<img width="1916" height="903" alt="image" src="https://github.com/user-attachments/assets/6eb65eb3-1959-408d-bfcb-bab876836829" />

---

If the keyboard is not detected:

* Make sure you are using **Google Chrome**
* Check your connection mode (USB / 2.4G)
* Reload the page and reconnect the keyboard

---









