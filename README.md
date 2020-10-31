Firmware Test Suite results for U-Boot
======================================

October 31st, 2020

The Firmware Test Suite (https://wiki.ubuntu.com/FirmwareTestSuite) comprises
multiple tests that can be run from Linux to test if the UEFI firmware is
correctly implemented.

| Test           | Subtest                                         | Service           | Result |
|----------------|-------------------------------------------------|-------------------|--------|
| uefirtvariable | Test UEFI RT variable services supported status | GetVariable       | PASS   |
| uefirtvariable | Test UEFI RT variable services supported status | GetNextVarName    | PASS   |
| uefirtvariable | Test UEFI RT variable services supported status | SetVariable       | FAIL   |
| uefirtvariable | Test UEFI RT variable services supported status | QueryVariableInfo | FAIL   |

As of 2020-10-31 the FWTS has does not support the EFI\_RT\_PROPERTIES\_TABLE
introduced in UEFI 2.8 errata A. So it does not skip the supported status test
for the SetVariable() and QueryVariableInfo() services.
