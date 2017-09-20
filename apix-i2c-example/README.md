Digi APIX I2C Sample Application
=================================

Sample application to access and manage I2C slaves using the Digi APIX library.

The application writes a page of an external EEPROM memory with random
data and then reads the data back to validate it (tested with 24FC1026).

The I2C connections for the sample depend on the running platform:
 - **CCIMX6 SBC**: I2C connector of the board.
    - VCC: Pin 3
    - GND: Pin 6
    - I2C-3 SDA: Pin 2
    - I2C-3 SCL: Pin 1
 - **CCIMX6UL SBC Express**: Expansion connector of the board.
    - VCC: Pin 1
    - GND: Pin 6
    - I2C-1 SDA: Pin 3
    - I2C-1 SCL: Pin 5
 - **CCIMX6UL SBC Pro**: I2C connector of the board.
    - VCC: Pin 3
    - GND: Pin 6
    - I2C-2 SDA: Pin 2
    - I2C-2 SCL: Pin 1

Running the application
-----------------------
Once the binary is in the target, launch the application:

```
#> apix-i2c-example
Example application using libdigiapix I2C support

Usage: %s <i2c-bus> <i2c-address> <address-size> <page-size> <page-index>

<i2c-bus>       I2C bus index to use
<i2c-address>   Address of the I2C EEPROM memory
<address-size>  Number of EEPROM memory address bytes
<page-size>     EEPROM memory page size in bytes
<page-index>    EEPROM memory page index to use

Aliases for SPI can be configured in the library config file
```

Compiling the application
-------------------------
This example can be compiled using a Digi Embedded Yocto based toolchain. Make
sure to source the corresponding toolchain of the platform you are using, e.g:

```
$> . <DEY-toolchain-path>/environment-setup-cortexa7hf-vfp-neon-dey-linux-gnueabi
$> make
```

More information about [Digi Embedded Yocto](https://github.com/digi-embedded/meta-digi).

License
-------
Copyright 2017, Digi International Inc.

Permission to use, copy, modify, and/or distribute this software for any purpose
with or without fee is hereby granted, provided that the above copyright notice
and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH
REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT,
INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS
OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER
TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF
THIS SOFTWARE.