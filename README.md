# Scope and Data Document of the project

Silly project to test Github project interface and do some electronic/firmware/mechanical tasks.

# Scope 

## Purpose 

I wish to create a device where I can control a PWM signal or two. Its frequencies, time activated and duty cicles. 

## Outputs

To know which are going to be my inputs, first I need to know my outputs. I can have the same variation for both outputs.

|   | Value |
| ------------- | ------------- |
| Frequency  | 10 to 50 Hz |
| Voltage  | 10 ~ 15 V  |
| Current  | 700 ~ 1000 uA  |
| Resistance | 10.6 k to 13.4 k |
| Time active | 30 to 50 minutes |

Bipolar voltage. Resting duration of 20 ms.

I wish to use, as interface: 

* A display, to show information (also information that I can control). Configured as 4-bits to decrease the I/O usage.
* Mosfet os similar to control the "power part". Isolation is desired but not mandatory.
* Connector to connect test lids (like for workbench - banana cable with crocodile clips). 1 output (project can be modified later on a new version to conteamplate two outputs).

![image](https://github.com/Rafaelatff/Square-Function-Generator/assets/58916022/565230f9-8d15-4f00-bda6-f4bbbecec3e8)

## Inputs

Project will use a external power supply. It can come from a bench top power supply, to control the voltage input or other. The project will use a standard jack input. Most of the power supplies are 12V and can also be use. Once output can work in a range of 10 ~ 15V, the project design must consider those values plus a value (for drop voltage over the circuit).  The value for input will be 12 ~ 18 VDC.

![image](https://github.com/Rafaelatff/Square-Function-Generator/assets/58916022/211b91cc-0fc7-4ab3-9877-21e3882b3ee1)

I will use a development board (STM8S with stm8s003k3t6, same used on my graduation TCC) to control the outputs and show in the display the current configuration. The display uses 5 V to operate and the microcontroller 2.95 V to 5.5 V as operating voltage. If the project uses 5 V also to power the microcontroller, a voltage translater is needless. 

* External power supply connected by jack.
* 5 V regulator to supply the command part of the board.
* Potentiometer to configure the frequency range.
* Potentiometer to configure the Duty Cicle.
* Potentiometer to configure the activated time.
* One button + LED to other configurations.

## Tests

NOTE: Check time accuracy with 10 (up to 18) measurements. I will try to evolve the project by dedicating time from 1 to 3 times per week.
