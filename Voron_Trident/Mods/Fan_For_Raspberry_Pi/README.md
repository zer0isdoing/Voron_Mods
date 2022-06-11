# Fan For Raspberry Pi
 
It is fan mount for DIN rail to cool down the raspberry pi. 
 
![alt text](Images/rp_fan.HEIC)

You need to add this fan in your config file. I am using fan as a 'temperature fan'. Which means, klipper will always try to keep raspberry pi at target temperature. As feedback, I am using temperature of raspberry pi. For this you need to flash your raspberry pi as a second mcu. For that, you can follow [this](https://www.klipper3d.org/RPi_microcontroller.html). 

```
## Raspberry Pi Fan
[temperature_fan rpi_fan]
pin: <PIN_NUMBER>
max_power: 1.0
shutdown_speed: 0.0
kick_start_time: 5.0
cycle_time:0.01
off_below:0.1
sensor_type: temperature_host
min_temp: 0
max_temp: 80
target_temp: 50.0
control: watermark
```

**BOM:**
| Material               															| Quantity |
| ------------------------------------  											| -------- |
| M3x12 Button Head Screw          												   	|        4 |
| [40x10 Fan](https://s.click.aliexpress.com/e/_A9V7Yd)             				|        1 |
