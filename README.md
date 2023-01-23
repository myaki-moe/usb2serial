# usb2serial

A low cost open source USB to 3 port serial (2*UART + 1*DBUS) adapter.

Based on STM32F103 (blue pill) and bluepill-serial-monster firmware, usb2serial supports USB CDC protocol for plug and play (PnP).

低成本开源USB到三路串口 (2*UART + 1*DBUS) 转换器. 

基于STM32F103 (blue pill) bluepill-serial-monster固件, usb2serial支持基于USB CDC协议的即插即用.

## Quick Start | 快速开始

1. PCB proofing using GERBER file `usb2serial_pcb/gerber/`
2. SMD or hand soldering using [ibom](usb2serial_pcb/bom/ibom.html)
3. Build bluepill-serial-monster firmware
4. Pull-up BOOT0 and reset MCU to enter bootloader.
5. Flash the firmware using [stm32flash](https://sourceforge.net/p/stm32flash) from UART1
6. Testing

```bash
# connect TX and RX first
# list all serial device
ls /dev/ttyACM*
# do a loopback test
minicom -D /dev/ttyACM{YOUR_DEVICE_NUMBER}
```

1. 使用GERBER文件 `usb2serial_pcb/gerber/` 打样PCB
2. SMT或使用 [ibom](usb2serial_pcb/bom/ibom.html)手工焊接
3. 编译bluepill-serial-monster固件
4. 拉高BOOT0进入烧录模式
5. 使用 [stm32flash](https://sourceforge.net/p/stm32flash) 从UART1烧录固件
6. 测试

```bash
# connect TX and RX first
# list all serial device
ls /dev/ttyACM*
# do a loopback test
minicom -D /dev/ttyACM{YOUR_DEVICE_NUMBER}
```

## Toolchains | 工具链

* PCB Design: KiCad 6.0.9
* Complier: arm-none-eabi-gcc 12.2.0
* Firmware Programmer: [stm32flash](https://sourceforge.net/p/stm32flash) 0.7

* PCB设计: KiCad 6.0.9
* 编译器: arm-none-eabi-gcc 12.2.0
* 固件烧录: [stm32flash](https://sourceforge.net/p/stm32flash) 0.7

## License | 许可证

* The USB2CAN project is released under GPLv3 license.

* The bluepill-serial-monster project is released under MIT license.

* USB2CAN项目基于GPLv3协议发布

* bluepill-serial-monster项目基于MIT协议分发

## Related Projects | 相关项目

[bluepill-serial-monster](https://github.com/r2axz/bluepill-serial-monster)