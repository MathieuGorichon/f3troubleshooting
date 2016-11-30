# f3troubleshooting

                 DFU                 VCP
			 ubuntu    windows   ubuntu    windows
Lux            ok        ok        ko         ok
diatone f3     ko        ko        ok          ?


CP210X : USB to UART Bridge

Silabs documentation and development kit : http://www.silabs.com/products/interface/usb-bridges/Pages/usb-bridges.aspx

## Vocabulaire

MCU : Microcontroller unit, the f3 processor

VCP : Virtual Com Port

COM : COM (Communication port[1]) is the original, yet still common, name of the serial port interface on IBM PC-compatible computers. It might refer not only to physical ports, but also to virtual ports, such as ports created by Bluetooth or USB-to-serial adapters. (https://en.wikipedia.org/wiki/COM_(hardware_interface))

UART : Universal Asynchronous Receiver Transmitter

USB : Universal Serial Bus

## Boards

Lux

Diatone f3
  - target : spracingf3

Dans Gestionnaire de périphérique  
  Avant utilisation zadig
  - Ports (COM et LPT)
    - Ports CP2102 USB to UART Bridge Controller (COM6)
  
Après utilisation de zadit et remplacement du driver usbser par WinUSB (v6.1.7600.16385)
  - Périphériques Universal Serial Bus
    - CP2102 USB to UART Bridge Controller
	
Désinstallation de Virtual Com Port Driver (depuis désintaller ou modifier un programme)
	
## Apprentissage

* Driver USB Serial (CDC) pour avoir un port COM
* Driver WinUSB pour avoir un périphérique USB
* Attention à bien avoir une led clignotante

## Copy pastes

SPRACINGF3 manual : http://seriouslypro.com/files/SPRacingF3-Manual-latest.pdf
  Getting started
Verify flight controller operation via the configuration software.
* Disconnect the flight controller from your computer.
* Disconnect ALL connectors and headers from the flight controller.
* Install latest Silicon Labs CP2102 USB to UART Bridge VCP Drivers
http://www.silabs.com/products/mcu/pages/usbtouartbridgevcpdrivers.aspx
* Install and launch the Cleanflight Configurator tool
https://chrome.google.com/webstore/detail/cleanflight-configurator/enacoimjcgeinfnnnpajinjgmkahmfgb
* Connect flight controller to computer via USB cable.
* Select the correct COM port if it is not automatically detected.
* Click connect, verify that communication is established. (Fig 3)

