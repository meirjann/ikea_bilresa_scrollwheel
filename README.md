# IKEA Bilresa Scroll Wheel – One Layer (Matter/Universal)

Inspired by [fangathome/ikea_bilresa_scrollwheel](https://github.com/fangathome/ikea_bilresa_scrollwheel), I've created a simple blueprint to control the new **IKEA Bilresa Scroll Wheel** over Matter.

> [!CAUTION]
> Currently, the Home Assistant Core can't process multipresses from Matter live. It waits until the press or scroll is finished. This can be annoying when controlling lights. I'll update this blueprint once this PR is live:
> https://github.com/home-assistant/core/pull/159045
>
> Due to this issue the automation gets unreliable if you **scroll > 7** "clicks". I'll fix it until the PR is live.

<a href="https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2Fmeirjann%2Fikea_bilresa_scrollwheel%2Fblob%2Fmain%2Fikea_bilresa_scroll_wheel.yaml" target="_blank">![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)</a>

## Features

- Control lights, a media player or any number entities with the scroll wheel.
- Create custom actions for the centre button including single, double and triple presses and holds.
- Customise the step size from one scroll "click" to 20.
- Enable scroll lock for lights to prevent them from being turned off.
- Set a minimum brightness for your lights.

![Blueprint example image in home assistant](https://github.com/meirjann/ikea_bilresa_scrollwheel/blob/main/screenshots/blueprint.png)

## Installation / Usage

### 1. Multi-Layer Switch

The Bilresa Scroll Wheel has three "layers" indicated by small LEDs. However, this blueprint only controls one layer.

> [!IMPORTANT]
> To use all three layers, create this automation three times, selecting the appropriate event entities for each layer.

Home Assistant interprets the scroll wheel as nine buttons:

```bash
Button-1: Layer 1 - clockwise
Button-2: Layer 1 - counterclockwise
Button-3: Layer 1 - button
Button-4: Layer 2 - clockwise
Button-5: Layer 2 - counterclockwise
Button-6: Layer 2 - button
Button-7: Layer 3 - clockwise
Button-8: Layer 3 - counterclockwise
Button-9: Layer 3 - button
```
