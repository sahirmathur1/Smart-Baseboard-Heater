# Article for Baseboard Heater

Done: No
High Priority: No
Not Required: No

# Smart-Baseboard-Heater

DIY Baseboard Thermostat for 220VAC Electrical Heater.

This project turns your 240 VAC electric baseboard heater to a smart baseboard heater that allows you to:

- Set up a temperature sensor far away from the heater allowing for a more representative temperature measurement for the room.
- Control the baseboard heater’s temperature from Google Home, Alexa, via Home Assistant.
- Monitor power consumption.

# Things you need

|  | Description | Specification | Link |
| --- | --- | --- | --- |
| 1 | Relay | Current Rating: 16 A  Voltage Rating: 240 VAC | https://www.shelly.cloud/en-us/products/product-overview/shelly-plus-1-pm-ul |
| 2 | Cable | Gauge: 12/2 | https://www.homedepot.com/p/Southwire-25-ft-12-2-Solid-Romex-SIMpull-CU-NM-B-W-G-Wire-28828221/202316378 |
| 3 | Wago Connectors | Voltage Rating: 300 V Current: 20 A | https://www.homedepot.com/p/Southwire-25-ft-12-2-Solid-Romex-SIMpull-CU-NM-B-W-G-Wire-28828221/202316378 |

# Tools

|  | Description |
| --- | --- |
| 1 | Wire Stripper |
| 2 | Non Contact Voltage Tester |
| 3 | Screwdriver |

<aside>
💡 Warning: Working with high voltage is very dangerous. Please hire an electrician to complete the high voltage scope.

</aside>

# Instructions

1. Turn off the breaker for the 240 VAC supply going to the baseboard heater.
2. Turn the heat on by turning the thermostat on the baseboard heater to max, you may still hear a click, wait for a few minutes and make sure there is no heat coming out of the baseboard heater.
3. Turn the thermostat off.
4. Open the baseboard heater’s panel that has the thermostat with a screwdriver.
5. Ensure there are no sources of electrical energy using the Non Contact Voltage tester.
6. Identify the following cables and label them:
    1. Phase 1
    2. Phase 2
    3. Phase to Thermostat
    4. Thermostat to Thermal Cutoff
    5. Phase to Heater 
7. Wire the relay [details to follow]
8. Turn the power on
9. Program the relay’s name [details to follow]
10. Set the WiFi settings on the relay [details to follow]
11. Add to Home Assistant [details to follow]
12. Go to File Editor on Home Assistant [details to follow]
13. Paste the Generic thermostat YAML entry [details to follow]
14. Set the temperature sensor entity and the heater entity [details to follow]
15. Reboot Home Assistant
16. Add the thermostat card to your dashboard [details to follow]

# FAQ

## How do I determine how much power my baseboard heater draws?

Source: [https://www.gcea.coop/energy-efficiency/energy-evaluations/baseboard-heater-information/#:~:text=Baseboard heaters typically use 250,watts (250 times 6)](https://www.gcea.coop/energy-efficiency/energy-evaluations/baseboard-heater-information/#:~:text=Baseboard%20heaters%20typically%20use%20250,watts%20(250%20times%206)).

You can try multiplying the feet the baseboard heaters length by 250 to get a rough idea. I would add 25% to be very sure. You could also use a clamp power meter to find out how much power the baseboard heater circuit is drawing and multiply the voltage to get Watts.
