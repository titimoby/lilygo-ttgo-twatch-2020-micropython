# :snake: MicroPython for LilyGO TTGO T-Watch-2020 :snake:
************************************************************************
## 📄 Description:
This is a fork of the official version of the micropython v1.12 with **bluetooth support**. \
This micropython fork is **SPECIALLY** sharpened and designed for LilyGO TTGO T-Watch-2020-V1 watches.  \
**Other TTGO watch models are not supported!**
************************************************************************
## 🎆 Integrated libraries:
1. **`bma423` - Low-g driver acceleration sensor.** \
   Written in C by [lewisxhe](https://github.com/lewisxhe). \
   Was taken from [here](https://github.com/lewisxhe/MicroPython_ESP32_psRAM_LoBo)

2. **`pcf8563` - Real-time clock/calendar driver.** \
   Written in Python by [lewisxhe](https://github.com/lewisxhe).  \
   Was taken from [here](https://github.com/lewisxhe/MicroPython_ESP32_psRAM_LoBo)

3. **`lvgl` - Popular embedded graphics library.** \
   Written in C.

4. **`ft6x36` - Touch screen driver.** \
   Written in C.  \
   Was taken from [here](https://github.com/lvgl/lv_port_esp32).

5. **`AXP202` - Advanced multi-channel power management chip driver.** \
   Written in Python.  \
   Updated to latest version by Anodev.  \
   Was taken from [here](https://github.com/lewisxhe/MicroPython_ESP32_psRAM_LoBo).

6. **`st7789_lvgl` - Display driver.** \
   Written in C. \
   Was taken from [here](https://github.com/lvgl/lv_port_esp32).
7. **`ttgo` - Port of the official [library](https://github.com/Xinyuan-LilyGO/TTGO_TWatch_Library) for LilyGo TTGO watches.** \
   Written in Python by Anodev.
8. **`ir` - Driver for ir sender.** \
   Written in C. \
   Was taken from [here](https://github.com/haxplore/ESP32_RMT_IRLib).
> Examples of using these libraries are located in the `examples/ttgo/` folder \
> For api look `ports/esp32/boards/LILYGO_T_WATCH_2020_V1` folder
************************************************************************
## :arrow_down: Download prebuild firmware:
**[Download](https://github.com/OPHoperHPO/lilygo-ttgo-twatch-2020-micropython/releases/download/1.2/firmware.bin)**
### Versions of the programs that were used to build the image:
1. **ESP-IDF** - 4.0
2. **Micropython** - 1.12
3. **lvgl** - 7.*
> See the `latest` branch for the latest micropython version.
************************************************************************
## 🔨 Build Instructions
### 🧷 WARNING:
Please set `ESPIDF` parameter for the esp-idf install dir. \
It needs to match Micropython expected esp-idf, otherwise a warning will be displayed (and build will probably fail) \
For more details refer to [Setting up the toolchain and ESP-IDF](https://github.com/littlevgl/lv_micropython/blob/master/ports/esp32/README.md#setting-up-the-toolchain-and-esp-idf) \
For more details please refer to [Micropython ESP32 README](https://github.com/micropython/micropython/blob/master/ports/esp32/README.md).
### 🏷 Commands:
1. Install all important libraries via `sudo apt-get install build-essential libreadline-dev libffi-dev git pkg-config libsdl2-2.0-0 libsdl2-dev python`
2. Clone this repo via `git clone https://github.com/OPHoperHPO/lilygo-ttgo-twatch-2020-micropython`
3. Clone all submodules via `git submodule update --init --recursive`
4. Configure esp-idf and toolchain
5. Edit paths to esp-idf and toolchain in `makefile` in `ports/esp32`
6. Build mpy-cross via `make -C mpy-cross`
7. Build micropython and flash it via `make -C ports/esp32 deploy`
************************************************************************
## 💵 Support me:
  You can thank me for developing any of my projects, provide financial support for developing new projects and buy me a small cup of coffee.☕ \
  Just support me on these platforms:
  * ![](https://github.com/OPHoperHPO/OPHoperHPO/raw/master/assets/imgs/boosty_logo.jpeg) [**Boosty**](https://boosty.to/anodev)
  * ![](https://github.com/OPHoperHPO/OPHoperHPO/raw/master/assets/imgs/donationalerts_logo.png) [**DonationAlerts**](https://www.donationalerts.com/r/anodev_development)
  * ![](https://github.com/OPHoperHPO/OPHoperHPO/raw/master/assets/imgs/paypal_logo.jpg) [**PayPal**](https://paypal.me/anodev)
************************************************************************
## 📄 More information:
* Micropython [README](https://github.com/micropython/micropython/blob/master/README.md)
* LVGL [docs](https://docs.lvgl.io/v7/en/html/get-started/micropython.html)
* LilyGo TTGO T-Watch-2020-V1 [pinmap](https://github.com/Xinyuan-LilyGO/TTGO_TWatch_Library/blob/master/docs/pinmap.md)
* Official LilyGo TTGO T-Watch-2020-V1 [arduino library](https://github.com/Xinyuan-LilyGO/TTGO_TWatch_Library)
* Official LilyGo [docs](https://t-watch-document-en.readthedocs.io/en/latest/introduction/product/2020.html)
