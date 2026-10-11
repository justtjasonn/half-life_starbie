# half-life_starbie

  A custom banyan tree shaped and themed tamagotchi based off of [starbie](https://github.com/SharKingStudios/Starbie/blob/main/Week%201%20Guide.md) in half-life. It is powered by a Seeed XIAO ESP32 c3, with motion and humidity sensors, an monochrome OLED display and MX switches and keycaps.

---

# Design images
These are my Kicad PCB schematic, PCB layout and 3d models of my PCB. Along with my drawings for the sprite for the firmware.
<details>
  <summary>Click to see schematic</summary>
  <img width="1919" height="1079" alt="dev1 1" src="https://github.com/user-attachments/assets/7ec87ce4-b8b9-482b-9109-fa57c217cfce" />
</details>
<details>
  <summary>Click to see PCB layout and design</summary>
  <img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/0657c213-a97c-4445-9419-748cd324a1f3" />
</details>
<details>
  <summary>CLick to see 3D renderings of my PCB</summary>
  <img width="3547" height="2009" alt="dev1 3" src="https://github.com/user-attachments/assets/7f513f57-79e7-4016-bc97-afb3a4ac154f" />
  <img width="3547" height="2009" alt="dev1 4" src="https://github.com/user-attachments/assets/4e8da723-b914-4654-bd3e-995662e0961c" />
</details>
<details>
  <summary>Click to see the tree sprite I made</summary>
    Colored version (not used):
  <br>
  <img width="361" height="465" alt="dev2 3" src="https://github.com/user-attachments/assets/2cb1b935-c53e-4bff-84b7-39e9c655e28c" />
  <br>
  Monochrome version(used):
  <br>
    <img width="360" height="465" alt="dev2 2" src="https://github.com/user-attachments/assets/5b88d918-9ce6-4130-a1d1-525e8b6dc268" />

</details>

---

# BOM

| Part | What it's for | Qty | Unit | Total | Vendor |
| --- | --- | --- | --- | --- | --- |
| [XIAO ESP32 C3](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) | For processing and running the firmware | 1 | $4.90 | $4.90 | [seed studio](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) |
| [0.96" SSD1306 OLED](https://e.tb.cn/h.jZynj421MeC2FqI?tk=I93tTr84Ais) | For displaying the sprite and its animations | 1 | $1.88 | $1.88 | [taobao/tmall (zave)](https://e.tb.cn/h.jZynj421MeC2FqI?tk=I93tTr84Ais) |
| [MPU6050 Sensor](https://e.tb.cn/h.jZyX4GKkPIZ3ast?tk=ZfUtTrRsbtL) | For controlling the tamagotchi by tilting | 1 | $1.40 | $1.40 | [Taobao](https://e.tb.cn/h.jZyX4GKkPIZ3ast?tk=ZfUtTrRsbtL) |
| [DHT11 humidity sensor module](https://e.tb.cn/h.jbPq5VsVxEpS1Ze?tk=xvSfTr8m0LC) | For detecting humidity in the air and sending it to the esp32 | 1 | $0.35 | $0.35 | [Taobao / Tmall](https://e.tb.cn/h.jbPq5VsVxEpS1Ze?tk=xvSfTr8m0LC) |
| [Green MX switches](https://e.tb.cn/h.jaogColeXqJfMwt?tk=q7kgTr8Syrr) | for the user to click and control the tamagotchi | 10 | $0.13 | $1.30 | [Taobao / Tmall](https://e.tb.cn/h.jaogColeXqJfMwt?tk=q7kgTr8Syrr) |
| [Green Keycaps](https://e.tb.cn/h.8AnWv1I2SZyVgNS?tk=wXyITrRM7ev) | For attaching on the mx switches | 5 | $0.15 | $0.75 | [Taobao (JSJT)](https://e.tb.cn/h.8AnWv1I2SZyVgNS?tk=wXyITrRM7ev) |
| [10KΩ resistors](https://e.tb.cn/h.jZyh801vTzVTZPe?tk=vzyZTrRAbD2) | To limit the power from the  esp32 to the OLED display | 10 | $0.04 | $0.40 | [Taobao / Tmall](https://e.tb.cn/h.jZyh801vTzVTZPe?tk=vzyZTrRAbD2) |
| [Custom PCB](https://jlcpcb.com/) | To connect all the componenets together and for extra design purposes | 5 | $0.80 | $4.00 | [JLCPCB](https://jlcpcb.com/) |
| **Parts subtotal** | — | — | — | **$14.98** | — |
| **Tax & shipping** | — | — | — | **$13.00** | — |
| **Total** | — | — | — | **$27.98** | — |


---

# Full wiring table(s)

Markdown
# PCB Wiring Table (`starbie_pcb`)

## Component Pinout Table

| Component Ref | Component Type | Pin Number | Pin Name / Function | Connected Net / Connection | Notes / Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **U1**[cite: 2] | XIAO ESP32-C3[cite: 2] | 1 | D0 | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 2 | D1 | **DHT11 DATA**[cite: 2] | Signal line to DHT11 sensor[cite: 2] |
| | | 3 | D2 | **GPIO2**[cite: 2] | Input from Push Button SW1[cite: 2] |
| | | 4 | D3 | **GPIO3**[cite: 2] | Input from Push Button SW2[cite: 2] |
| | | 5 | D4 | **SCL**[cite: 2] | I2C Clock (Display J1 & Header J2)[cite: 2] |
| | | 6 | D5 | **SDA**[cite: 2] | I2C Data (Display J1 & Header J2)[cite: 2] |
| | | 7 | D6 | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 8 | D7 | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 9 | D8 | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 10 | D9/BOOT | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 11 | D10 | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 12 | 3V3_OUT | **+3.3V**[cite: 2] | 3.3V Power Rail[cite: 2] |
| | | 13 | GND | **GND**[cite: 2] | Ground[cite: 2] |
| | | 14 | VBUS | **+5V**[cite: 2] | 5V Power Rail (USB VBUS)[cite: 2] |
| | | 15 | D3/MTDI | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 16 | D5/MTDO | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 17 | EN | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 18 | GND | **GND**[cite: 2] | Ground[cite: 2] |
| | | 19 | D2/MTMS | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 20 | D4/MTCK | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 21 | VBAT | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| | | 22 | GND | *Not Connected (NC)*[cite: 2] | Unused[cite: 2] |
| **U2**[cite: 2] | DHT11 Sensor[cite: 2] | 1 | VDD | **+3.3V**[cite: 2] | Power supply[cite: 2] |
| | | 2 | DATA | **DHT11 DATA**[cite: 2] | Data output to U1 Pin 2 & R1 Pin 2[cite: 2] |
| | | 3 | NC | *Not Connected (NC)*[cite: 2] | Internal no connect[cite: 2] |
| | | 4 | GND | **GND**[cite: 2] | Ground[cite: 2] |
| **J1**[cite: 2] | OLED Display Conn (1x04)[cite: 2] | 1 | Pin_1 | **SDA**[cite: 2] | I2C Data[cite: 2] |
| | | 2 | Pin_2 | **SCL**[cite: 2] | I2C Clock[cite: 2] |
| | | 3 | Pin_3 | **+3.3V**[cite: 2] | Display VCC[cite: 2] |
| | | 4 | Pin_4 | **GND**[cite: 2] | Display Ground[cite: 2] |
| **J2**[cite: 2] | Header Connector (1x08)[cite: 2] | 1 | Pin_1 | **+3.3V**[cite: 2] | Power output[cite: 2] |
| | | 2 | Pin_2 | **GND**[cite: 2] | Ground[cite: 2] |
| | | 3 | Pin_3 | **SCL**[cite: 2] | I2C Clock output[cite: 2] |
| | | 4 | Pin_4 | **SDA**[cite: 2] | I2C Data output[cite: 2] |
| | | 5–8 | Pin_5 to Pin_8 | *Not Connected (NC)*[cite: 2] | Unused pins[cite: 2] |
| **SW1**[cite: 2] | Push Button 1[cite: 2] | 1 | Pin 1 | **GPIO2**[cite: 2] | Connected to U1 Pin 3[cite: 2] |
| | | 2 | Pin 2 | **GND**[cite: 2] | Ground[cite: 2] |
| **SW2**[cite: 2] | Push Button 2[cite: 2] | 1 | Pin 1 | **GPIO3**[cite: 2] | Connected to U1 Pin 4[cite: 2] |
| | | 2 | Pin 2 | **GND**[cite: 2] | Ground[cite: 2] |
| **R1**[cite: 2] | 10k Resistor[cite: 2] | 1 | Pin 1 | **+3.3V**[cite: 2] | Pull-up power connection[cite: 2] |
| | | 2 | Pin 2 | **DHT11 DATA**[cite: 2] | Pull-up resistor for DHT11 data line[cite: 2] |

## Net Summary Table

| Net Name | Description | Connected Pins |
| :--- | :--- | :--- |
| **+3.3V**[cite: 2] | Main 3.3V Power Rail | U1 pin 12, U2 pin 1, J1 pin 3, J2 pin 1, R1 pin 1[cite: 2] |
| **+5V**[cite: 2] | USB 5V Power Rail | U1 pin 14[cite: 2] |
| **GND**[cite: 2] | Common Ground | U1 pin 13, U1 pin 18, U2 pin 4, J1 pin 4, J2 pin 2, SW1 pin 2, SW2 pin 2[cite: 2] |
| **SDA**[cite: 2] | I2C Serial Data | U1 pin 6 (D5), J1 pin 1, J2 pin 4[cite: 2] |
| **SCL**[cite: 2] | I2C Serial Clock | U1 pin 5 (D4), J1 pin 2, J2 pin 3[cite: 2] |
| **GPIO2**[cite: 2] | Button 1 Input Line | U1 pin 3 (D2), SW1 pin 1[cite: 2] |
| **GPIO3**[cite: 2] | Button 2 Input Line | U1 pin 4 (D3), SW2 pin 1[cite: 2] |
| **DHT11 DATA**[cite: 2] | Sensor Data Line with Pull-up | U1 pin 2 (D1), U2 pin 2, R1
