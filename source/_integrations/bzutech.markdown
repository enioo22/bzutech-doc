---
title: Bzu Tech
description: Instructions on how to setup BzuTech devices within Home Assistant.
ha_category:
  - Sensors
ha_release: 2024.1
ha_iot_class: Cloud Polling
ha_config_flow: true
ha_codeowners:
  - '@enioo22'
ha_domain: bzutech
ha_quality_scale: bronze
ha_platforms:
  - sensor
ha_integration_type: integration
---

The **Bzu Tech** {% term integration %} allows you to integrate your [BzuCloud](https://cloud.bzutech.com.br) sensors and devices in Home Assistant. It provides a sensor {% term entity %} that can be used in automations, dashboards and more.

## Prerequisites

To use this integration, you need:

- A [BzuCloud account](https://cloud.bzutech.com.br/register) (Available Worldwide)
- One or more supported Bzu Tech devices registered to your account
  - Every Bzu Tech device is compatible!

## Configuration

- Login with your Bzu Cloud account

![Login step](/images/integrations/bzutech/bzutech-login-step.png)

- Select the device you want added to your Home Assistant

![Device Selection](/images/integrations/bzutech/bzutech-device_selection.png)

- Select which port/sensor from that device you want

![Sensor/port Selection](/images/integrations/bzutech/bzutech-port-step.png)

- Configuration done! Now your Bzu Tech sensors are available to use

![Sensors available](/images/integrations/bzutech/bzutech-sensors.png)

## Sensors

Available devices and sensors:

- EP101:
  - Temperature (ºC), Humidity (%), Luminosity (lx).
- EP111:
  - Temperature (ºC), Humidity (%), Luminosity (lx), PIR (motion detected).
- EP121:
  - Temperature (ºC), Humidity (%), Luminosity (lx), PIR (motion detected), Door opening status.
- EP200:
  - Temperature (ºC), Humidity (%), VOC, Particulate Matter PM(0.5, 1.0, 2.5, 4.0, 10), Door opening status.
- EP300:
  - Sound (dB).
- EP400:
  - Voltage (V), Current (A), Active Power (W), Apparent Power (VA).
- EP500:
  - Relative Pressure (Pa).
- EP510:
  - Pressure (atm).
- EP610:
  - Water Depth (m).
- EP700:
  - Water Flow  (L/s), Water Volume (L).
- EP800:
  - Water PH, Water ORP (mV), Conductivity (µmhos/cm), Temperature (ºC) and Humidity (%).

## Troubleshooting

Here are some common issues you might encounter:

### Authentication failed

- Verify your BzuCloud credentials

### Sensor shows unavailable

- Check if the device is online in BzuCloud
- Reload the integration

For other issues, try reloading the integration or check the Home Assistant logs for more details.

{% include integrations/config_flow.md %}
