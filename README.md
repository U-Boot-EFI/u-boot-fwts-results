Firmware Test Suite results for U-Boot
======================================

December 27th, 2020

The Firmware Test Suite (https://wiki.ubuntu.com/FirmwareTestSuite) comprises
multiple tests that can be run from Linux to test if the UEFI firmware is
correctly implemented.

| Test           | Subtest                                         | Service           | Result |
|----------------|-------------------------------------------------|-------------------|--------|
| uefirtvariable | Test UEFI RT variable services supported status | GetVariable       | PASS   |
| uefirtvariable | Test UEFI RT variable services supported status | GetNextVarName    | PASS   |
| uefirtvariable | Test UEFI RT variable services supported status | SetVariable       | SKIP   |
| uefirtvariable | Test UEFI RT variable services supported status | QueryVariableInfo | SKIP   |

The test was done with Linux 5.10.2 and FWTS patched [1] to read the supported
runtime services using an IOCTL introduced in Linux 5.11 [2].

* [1] https://lists.ubuntu.com/archives/fwts-devel/2020-December/012484.html
* [2] https://lore.kernel.org/r/20201127192051.1430-1-xypron.glpk@gmx.de
