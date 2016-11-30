# f3troubleshooting

                 DFU                 VCP
			 ubuntu    windows   ubuntu    windows
Lux            ok        ok        ko         ok
diatone f3     ko        ko        ok          ?


CP210X : USB to UART Bridge

Silabs documentation and development kit : http://www.silabs.com/products/interface/usb-bridges/Pages/usb-bridges.aspx

## Vocabulaire

MCU : Microcontroller unit, the f3 processor

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

Driver USB Serial (CDC) pour avoir un port COM
Driver WinUSB pour avoir un périphérique USB
Attention à bien avoir une led clignotante
  
