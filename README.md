# half-life_starbie

  A custom banyan tree shaped and themed tamagotchi based off of [starbie](https://github.com/SharKingStudios/Starbie/blob/main/Week%201%20Guide.md) in half-life. It's inspired by my friend group at school called the banyan. It is powered by a Seeed XIAO ESP32 c3, with motion and humidity sensors, an monochrome OLED display and MX switches and keycaps.

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

# Jouralling

[Click to view my journalling](JOURNAL.md)
<details>
  <summary>Click to view my timelapses</summary>

  [Click to view timelapse 1 (starting PCB)](https://lapse.hackclub.com/timelapse/Cmzgq96uHY-p)
  [Click to view timelapse 2 (adding silkscreen to PCB)](https://lapse.hackclub.com/timelapse/j08qLoLR9cuI)
  [Click to view timelapse 3 (Finishing PCB)](https://lapse.hackclub.com/timelapse/VBQeAIEWYwXP)
  [Click to view timelapse 4 (Made firmware and BOM)](https://lapse.hackclub.com/timelapse/K467jB09zgaI)
  
</details>

---

# Credits

- [Hack Club](https://hackclub.com/) for making and organizing half life and everything else :)
- [Logan Peterson (@SharKingStudios)](https://github.com/SharKingStudios/Starbie/) for making the very intuitive guide!
- Me for designing everything else
