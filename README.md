# IKEA Bilresa Scroll Wheel – Matter Rework

This Home Assistant blueprint provides advanced control for the **IKEA Bilresa Scroll Wheel** (Matter version). It is a refined rework of the original [Bilresa Scroll Wheel Extension](https://github.com/fangathome/ikea_bilresa_scrollwheel), optimized for Matter-based event entities and featuring enhanced logic for brightness control and multi-press actions.

## ✨ Features

* **Scroll Lock:** Option to prevent the light from turning on accidentally by rotating the wheel when the light is off.
* **Minimum Brightness:** Define a lower limit so the light never accidentally turns off or becomes too dim while scrolling down.
* **Advanced Center Button:** Supports Single Press, Double Press, Triple Press, and Long Press (Hold) for custom **actions**.
* **Matter Optimized:** Specifically designed to work with `event` entities provided by Matter-integrated IKEA devices.

## 🛠 Installation & Usage

<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmeirjann%2Fikea_bilresa_scrollwheel%2Fblob%2Fmain%2Fikea_bilresa_scroll_wheel.yaml" target="_blank" rel="noreferrer noopener"><img src="https://my.home-assistant.io/badges/blueprint_import.svg" alt="Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled." /></a>

### 1. Multi-Layer Note

The IKEA Bilresa remote supports up to 3 "layers" (indicated by the small LEDs). This blueprint controls **one layer at a time**.

> [!IMPORTANT]
> If you want to use all 3 layers of your remote, you need to **import and create this automation 3 times**, selecting the specific event entities for each respective layer.

### 2. Configuration

1. **Scroll Events:** Map the `Right` and `Left` event entities of your Bilresa.
2. **Center Button:** Map the `Center` event entity.
3. **Target Light:** Select the light or light group you want to control.
4. **Min Brightness:** Set your preferred minimum (e.g., 10%) to ensure the light stays visible during dimming.
5. **Actions:** Define what should happen when you press or hold the center button.

## 📂 Folder Structure (for Manual Installation)

To maintain multi-language support, ensure the files are placed in a folder structure like this:

```text
/config/blueprints/automation/your_folder/
├── ikea_bilresa_scroll_wheel.yaml
└── translations/
    ├── en.json
    └── de.json

```

---

## 🤝 Credits

This blueprint is a rework and improvement of the work by [fangathome](https://github.com/fangathome/ikea_bilresa_scrollwheel). Huge thanks for the original logic and inspiration!

---

(this documentation is AI-generated)
