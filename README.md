# How to flash: 

already added this to udev rules:

```
# Atmel ATMega32U4
SUBSYSTEMS=="usb", ATTRS{idVendor}=="03eb", ATTRS{idProduct}=="2ff4", TAG+="uaccess", RUN{builtin}+="uaccess"
# Atmel USBKEY AT90USB1287
SUBSYSTEMS=="usb", ATTRS{idVendor}=="03eb", ATTRS{idProduct}=="2ffb", TAG+="uaccess", RUN{builtin}+="uaccess"
# Atmel ATMega32U2
SUBSYSTEMS=="usb", ATTRS{idVendor}=="03eb", ATTRS{idProduct}=="2ff0", TAG+="uaccess", RUN{builtin}+="uaccess"
```

and reloaded

- Then, edit the keymap json (online preferably)
- download json
- Plug in board, press reset button
- run `qmk flash /full/path/to/json` (yes that sucks)
