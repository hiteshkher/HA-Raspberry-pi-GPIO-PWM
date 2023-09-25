1. Install pigpio add-on
There is an excellent collection of add-ons called “Poeschl Home Assistant Add-ons”, one of them is pigpio which will let you send PWM data on a GPIO pin.

To install, open the “Add-ons, Backups and Supervisor” from the Configuration and then click on ADD-ON STORE button. Now you need to add the repository by clicking the menu button (the tree-dots button in the top right corner) and add the following URL:

https://github.com/Poeschl/Hassio-Addons


2.Installation
HACS
The recommend way to install ha-rpi_gpio_pwm is through HACS.

Manual installation
Copy the ha-rpi_gpio_pwm folder and all of its contents into your Home Assistant's custom_components folder. This folder is usually inside your /config folder. If you are running Hass.io, use SAMBA to copy the folder over. You may need to create the custom_components folder and then copy the ha-rpi_gpio_pwm folder and all of its contents into it.

Configuration
To enable this platform, add the following lines to your configuration.yaml:

# Example configuration.yaml entry
light:
  - platform: rpi_gpio_pwm
    leds:
      - name: Lightstrip Cupboard
        pin: 17
