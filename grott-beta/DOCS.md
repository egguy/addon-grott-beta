# Grott - Home Assistant native MQTT integration

This intergration allows you to connect your Growatt inverter to Home Assistant using the Grott

## Configuration

To allow the addon to work, you need to configuration the data logger to send the data to the addon. This is done by configuring the data logger to send the data to the IP address of the Home Assistant instance.

### Configuration of the data logger

You can refer to the excellent tutorial by [Muppet3000](https://github.com/muppet3000/): https://github.com/muppet3000/homeassistant-grott/blob/main/docs/setup/datalogger.md

### Configuration of the addon

#### Use of the integrated grott HA plugin

This plugin is integrated in the addon and is automatically installed when the addon is started. You don't need to do anything.

#### Grott Grott Home Assistant Custom Component

To do this, you can disable the option `Home Assistant plugin` and enable the option `Enable grott MQTT`.

Then you need to follow the instructions on the [Grott Home Assistant Custom Component](https://github.com/muppet3000/homeassistant-grott/) page.

## Configuration of grott

1. Click on **Configuration**

   - If you use the mosquitto addon, **don't change this option**. If you are **not** using the Mosquitto broker addon fill in your MQTT details (leave empty when using the Mosquitto broker addon). Format is e.g.: <br>

     ```yaml
     host: <IP>
     port: 1883
     user: my_user
     password: my_password
     ```

   - Click **Save**
   - **Tip:** it is possible to refer to variables in the Home Assistant `secrets.yaml` file by using e.g. `password: '!secret mqtt_pass'`

1. If multiple inverters, please refer on how to configure them on this documentation: <https://github.com/johanmeijer/grott/wiki/Multi-Inverter-support>
1. Start the addon by going to **Info** and click **Start**
1. Configure your data logger using the information contained here: [Rerouting Growatt Wifi TCPIP data via your Grott Server](https://github.com/johanmeijer/grott/wiki/Rerouting-Growatt-Wifi-TCPIP-data-via-your-Grott-Server)
   - Use the local IP of your home assistant
   - Don't use ths DNS, the datalogger can't resolve `homeassistant.local`
