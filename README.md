# fauxmax-config
ZMK Configuration for FauxMax macropad

## Background
This is a small project to get ZMK working for the [FauxMax](https://mechboards.co.uk/products/romac-macro-pad) macropad using a [nRFMicro](https://github.com/joric/nrfmicro/wiki/ALternatives) clone.  Goal is to get the underglow, the display, and bluetooth, and ZMK studio working.

The basic keymapping, layers, and the rotary encoder all work as expected.

## ToDo
  * [x] Underglow
  * [x] Display
  * [x] Bluetooth
  * [x] ZMK Studio


## Building 

Use the following command to build with ZMK Studio support 

```
uv run west build -p -b nice_nano_v2 -S studio-rpc-usb-uart -- -DSHIELD=fauxmax -DCONFIG_ZMK_STUDIO=y
```

Use the following to build _without_ ZMK Studio support

```
uv run west build -p -b nice_nano_v2 -- -DSHIELD=fauxmax 
```
