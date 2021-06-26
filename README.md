## Original_Project Code
Original Project Located [HERE](https://github.com/fredrike/esphome-nodes)

This project has been updated to work with OpenWeatherMap

# esphome-nodes
Different ESP-based WiFi nodes connected to [Home Assistant](https://home-assistant.io) via [ESPHome](https://esphome.io)

They expect a `secrets.yaml` file with the following:

```yaml
wifi_password: ""
api_password: ""
ota_password: ""
```

## Display node
<img
src="https://raw.githubusercontent.com/thjubeck/esphome-nodes/master/images/Display.jpg" width='450px'>

Built using a [4.2inch e-Paper Module](https://www.waveshare.com/wiki/4.2inch_e-Paper_Module) connected to an [E-Paper ESP32 Driver Board](https://www.waveshare.com/wiki/E-Paper_ESP32_Driver_Board).

Note the following connections used in ESPHome.

```yaml
spi:
  clk_pin: 13
  mosi_pin: 14

display:
  - platform: waveshare_epaper
    id: epaper
    cs_pin: 15
    busy_pin: 25
    reset_pin: 26
    dc_pin: 27
    model: 4.20in
```

The file [`package-display_node.yaml`](https://github.com/thjubeck/esphome-nodes/blob/master/homeassistant-config/package-display_node.yaml
) is a package that should be added to Home Assistant to provide the **display node** with data.


## Icons

Icon list can be found [Here](https://pictogrammers.github.io/@mdi/font/5.4.55/)

Icons can be addded by using /U000(5 character icon code goes here)
  Example /U000F02DC is the code for a house icon
