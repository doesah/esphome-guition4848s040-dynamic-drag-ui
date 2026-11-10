# DOESAH ESPHome Firmware for GUITION ESP32-S4-4848S040

**Flash the firmware online: https://doesah.com/firmware**



DOESAH Smart builds dynamic UI and customization solutions for embedded devices. It pairs high-performance device firmware with a cloud-based visual design platform, so your smart hardware interface no longer needs code edits and rebuilds — design by dragging in the browser, sync to the device in seconds, and connect to Home Assistant with minimal effort.

**No C++ / LVGL required. No ESPHome build environment to set up.** Just **drag and drop** to design your interface in the browser, or apply one of many **ready-made templates**, and the device downloads the UI from the cloud in real time. Combined with our Home Assistant blueprints, wiring a UI widget to an HA entity takes only a few seconds.

## Key Features

### Cloud Visual Drag & Drop UI Editor

- **What you see is what you get**: a full-featured web editor where you can freely drag switches, sliders, text, icons, charts, and other UI widgets.

- **One-click cloud deployment**: no local firmware build after designing. The device syncs the UI layout and resources generated in the cloud online with one click.

- **Dynamic updates**: adjust the layout anytime in the browser and the panel updates live right away. Reskinning your UI has zero barrier to entry.



### A Growing Template Library (Rich Template Hub)

- **Ready to use out of the box**: 4-inch screen templates in multiple styles — minimal, tech, luxury, and more.

- **Covers real use cases**: purpose-built layouts for whole-home lighting, HVAC (air conditioning / floor heating), media control, and environmental dashboards.

- **One-click apply**: start from a template instead of designing from scratch, and push it to the device directly.

### Dead-Simple HA Blueprint Integration

- **Zero-code binding**: comes with Home Assistant automation blueprints that integrate out of the box.

- **Effortless state mapping**: blueprints handle switching and mode control for complex entities like `switch`, `light`, `climate`, and `fan` for you.

- **Two-way, millisecond-level sync**: control your HA devices from the touch panel in real time, and device states on the HA side (including offline / `unavailable`) are pushed back to the panel within milliseconds and rendered correctly.



## Multi-language & High-Definition Large Font Engine

> 💡 **Solving a classic embedded UI memory problem**: rendering a large, high-definition font with thousands of Chinese glyphs inside the limited SRAM of the ESP32-S3 is a quick path to out-of-memory (OOM). The Doesah firmware reworks font management at the low level and solves both large fonts and multi-language rendering cleanly.
> 
> 

- **Full multi-language support**: native support for **Simplified Chinese, Traditional Chinese, and English** — easy to build internationalized products and multi-language interfaces. More languages are on the way.

- **Rich fonts and large font sets**: load custom fonts of your choice and render large, high-definition text smoothly.

- **Extreme PSRAM optimization**: our own font engine supports Simplified / Traditional Chinese and English plus very large font sets. Glyphs are read on demand straight from flash (On-Demand Flash Stream), instead of forcing the whole font set into PSRAM the traditional way, so the device stays smooth.



## Architecture & Local-First

> **Dynamic rendering & purely local control**: Doesah FSPane-G1 follows a **Local-First** design. We do provide a convenient cloud visual design platform, but day to day the device **needs no internet at all**.
> 
> 

### How Dynamic UI Rendering Works

- **UI structure is generated in the cloud**: when you design by dragging on the web platform, the cloud produces nothing but a lightweight UI structure description (DSL). There is no C++/LVGL compilation involved.

- **Download the structure once**: once the panel connects to the cloud, it downloads that UI structure file and stores it persistently in local flash (LittleFS).

- **Parse and draw locally**: the Doesah firmware ships with a high-performance dynamic UI rendering engine that parses the structure and draws the interface locally at boot.

- **Runs on the LAN, cloud-free**: after the structure file is downloaded, all interaction, button handling, and communication with Home Assistant **happens entirely on your local network (LAN)**. The panel keeps working even with no internet access.

### How Home Assistant Integration Works

- **It is just a native ESPHome device**: the panel connects to Home Assistant over the LAN through the standard ESPHome native API.

- **Widget interaction -> entity state dispatch**: touching the panel (tapping a switch, dragging a slider, changing a mode) **dispatches state updates for the matching virtual ESPHome entities to HA in real time**.

- **Blueprint listens automatically, zero-code takeover**: we wrote **HA automation blueprints** specifically for the panel. The blueprint watches panel entity changes in the background and controls your real devices (lights, AC, curtains, and so on) accordingly; changes on the real devices sync back to the panel display in milliseconds.

- **No more hand-written code**: skip the complex `automations.yaml`. Import the blueprint in the HA UI, pick your devices, and two-way integration is done.

### When the Device Talks to the Cloud

During normal device control and state sync, the device **never sends any device state data to the cloud**. It only communicates with the cloud when downloading interface configurations or applying OTA firmware updates:

## Quick Start in 3 Steps

### Flash the Firmware

Use the official flasher at https://doesah.com/firmware to flash your 4-inch ESP32-S3 panel in one click.

### Design Online and Download the UI

1. Go to https://doesah.com, create an account, and add your device with its serial number.

2. Pick a **preset template** or design your interface with the **drag & drop editor**.

3. Download the UI from the cloud to the panel with one click.

### Import the HA Blueprint and Bind

1. On the UI editor page, select the target widget and import the matching automation blueprint into Home Assistant with one click:

2. Choose your **FSPane panel** and the **HA entities** you want to control (lights, switches, climate, etc.). Save, and it takes effect immediately.

## Free Tier

- **Firmware and blueprints**: installing the firmware and configuring the blueprints is **completely free**.

- **Design and template access**: every user can log in to the cloud platform for free, use the drag & drop editor, and browse the template library.

- **Cloud UI download quota**: the free plan includes an **initial number of free downloads / syncs**, enough for evaluation and basic setups. Upgrade anytime for unlimited cloud syncs or the premium business templates.

## Support & Feedback

If you run into any issue while flashing or using the platform, or if you want to **unlock unlimited cloud syncs / buy premium business templates**:

- Open a ticket on the DOESAH Smart website: https://doesah.com/user/feedback

- **File a bug / suggestion on GitHub**: https://github.com/doesah/esphome-guition4848s040-dynamic-drag-ui/issues/


