# Test-SmoothMQTT

A Unity spike for talking to an MQTT broker — the connectivity groundwork for
the Home Assistant XR projects.

## Why it exists

Before building a smart-home control panel in a headset, the boring question
had to be answered first: can Unity hold a reliable MQTT connection, subscribe
to a wildcard topic, publish typed payloads, and survive a broker that
authenticates? This project is where that was tested, against the same
`BedroomLights/state`-style topics the XR projects later use.

It is deliberately not an XR project — there is no headset in the loop, so a
failure here is an MQTT failure and nothing else.

## What's covered

The smoothMQTT example scenes exercise the cases that mattered:

| Scene | Case |
|---|---|
| `001_MQTTBroker` | Broker connection |
| `002_Receive_Value_Range_LigthGradient` | Subscribing to a value range |
| `003_Publish_Value_From_Slider_LightGradient` | Publishing from UI input |
| `004_Eventtrigger_for_static_payload` | Fixed payloads on an event |
| `005_Working_With_Datatypes` | Typed payloads and converters |
| `006_Triggers_and_Collisions` | Publishing from scene events |
| `007_May_I_See_Your_Credentials` | Authenticated brokers |
| `008_Conditional_Use_of_Sensor_Data` | Conditional subscribers |
| `101_MQTTBroker_using_SSL` | TLS |
| `SampleScene` | Scratch scene — wildcard subscribe against the live broker |

## Built with

Unity 2022.3.3f1 · smoothMQTT

## Related

The XR work this fed into:
[HomeAssistant_VR](https://github.com/mohitshukla02/HomeAssistant_VR) ·
[HA_Passthrough](https://github.com/mohitshukla02/HA_Passthrough) ·
[SmartHomeOS](https://github.com/mohitshukla02/SmartHomeOS)

## Third-party assets

Bundles the smoothMQTT package and its example scenes, which remain under
their own license.

## License

Copyright © 2026 Mohit Shukla. All rights reserved.

This repository is made publicly viewable for portfolio and demonstration
purposes only. No license is granted to use, copy, modify, merge, publish,
distribute, sublicense, or sell copies of Test-SmoothMQTT or any part of
it, in whole or in part, without prior written permission from the
copyright holder.
