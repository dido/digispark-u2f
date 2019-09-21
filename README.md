digispark-u2f
=============

U2F implementation for Digispark + ATECC508a-SSHDA-T

This is based on Yohanes Nugroho's Teensy LC U2F implementation, but
uses an ATECC508A-SSHDA-T CryptoAuth chip over I²C to do all the
cryptographic heavy lifting.

Most of the stuff is still unimplemented as of now (2019-09-22) of
course.

=== Hardware

I've built the hardware, including a pushbutton switch wired
to P1 on the Digispark intended for use as the user presence
check. The circuit is fairly simple, with the ATECC508A pins wired as
follows:

Pin|Connection
---|----------
4|Ground
5|Digispark P0 (SDA) + 4.7kΩ pullup to 5v
6|Digispark P2 (SCL) + 4.7kΩ pullup to 5v
8|5v

The Digispark is wired as follows:

Pin|Connection
---|----------
P0|ATECC508A pin 5 (SDA) + 4.7kΩ pullup to 5v
P1|Momentary pushbutton with 10kΩ pullup to 5v
P2|ATECC508A pin 6 (SCL) + 4.7kΩ pullup to 5v

I'll draw a schematic when I have the time.

License
-------

See LICENSE.txt
