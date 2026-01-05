# IKEA Bilresa Scroll Wheel – One Layer (Matter/Universal)

This Home Assistant blueprint is a precision-engineered rework for the **IKEA Bilresa Scroll Wheel** (Matter version). It solves common issues like inconsistent dimming steps and provides a "smart" interface for controlling various entity types automatically.

[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/meirjann/ikea_bilresa_scrollwheel/blob/main/ikea_bilresa_scroll_wheel.yaml)

## ✨ Features

* **Smart Entity Detection:** Automatically detects if you are controlling a `light`, `number`, or `input_number` helper and adjusts services and safety logic accordingly.
* **Precision Step Fix (Exact 5% steps):** Thanks to an optimized rounding logic (`| round(0)`), uneven jumps (like 4% or 6%) are eliminated. Scrolling follows exact increments based on your chosen step size.
* **Scroll Lock (Lights only):** Prevents accidentally turning the light on by rotating the wheel when it is currently off.
* **Minimum Brightness (Lights only):** Defines a lower limit to ensure the light never accidentally turns off or becomes too dim while scrolling down.
* **Advanced Center Button:** Supports Single Press, Double Press, Triple Press, and Long Press (Hold) for custom actions.
* **Matter Optimized:** Specifically designed for `event` entities provided by Matter-integrated IKEA devices.

## 🛠 Installation & Usage

### 1. Multi-Layer Note
The IKEA Bilresa remote supports up to 3 "layers" (indicated by the small LEDs). This blueprint controls **one layer at a time**.
> [!IMPORTANT]
> To use all 3 layers of your remote, you need to **create this automation 3 times**, selecting the specific event entities for each respective layer.

### 2. Configuration
1. **Scroll Events:** Map the `Right` and `Left` event entities of your Bilresa.
2. **Center Button:** Map the `Center` event entity.
3. **Target Entity:** Select any Light, Number, or Input Number.
4. **Settings:** Define your Step Size and (for lights) the Minimum Brightness and Power-on Lock.

## 📂 Folder Structure (for Multi-Language Support)
To enable translations (e.g., German UI), ensure your files are placed in a folder structure like this:
```text
/config/blueprints/automation/your_folder/
├── ikea_bilresa_one_layer.yaml
└── translations/
    ├── en.json
    └── de.json
```

🤝 Credits

This blueprint is a rework and improvement of the work by fangathome. Huge thanks for the original logic and inspiration!

---

this documentation is AI-generated
