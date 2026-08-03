⚠️ Note on this Fork: This fork adds support for Raspberry Pi 5 (OS Bookworm) by implementing libgpiod control for PN7160 pins, following the [official NXP guide](https://community.nxp.com/t5/NFC-Knowledge-Base/Porting-PN7160-NCI2-stack-to-Raspberry-Pi-5-OS-Bookworm/ta-p/1977521). The original repository uses deprecated sysfs which fails on modern Linux kernels (6.6+).

linux_libnfc-nci
================

branch NCI2.0_PN7160: Linux NFC stack for PN7160 NCI2.0 based NXP NFC Controller.
For previous NXP NFC Controllers support (PN7150, PN7120) refer to branch master.

Information about NXP NFC Controller can be found on [NXP website](https://www.nxp.com/products/identification-and-security/nfc/nfc-reader-ics:NFC-READER).

Further details about the stack [here](https://www.nxp.com/doc/AN13287).

Release version
---------------
- NCI2.0-R1.1 fix limitation about multiple T5T, fix issue with MIFARE Classic read after write, cleanup of alternate transport definition, cleanup of logs 
- NCI2.0-R1.0 is the first official release of Linux libnfc-nci stack for PN7160

Possible problems, known errors and restrictions of R1.1:
---------------------------------------------------------
- LLCP1.3 support requires OpenSSL Cryptography and SSL/TLS Toolkit (version 1.0.1j or later)
- To install on 64bit OS, apply patch
