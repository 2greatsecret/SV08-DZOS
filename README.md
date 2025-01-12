**DZOS: DYNAMIC Z OFFSET AND SOAK**

**AUTHOR:** TRANSFORM

**CURRENT VERSION:** 0.1.35

**VERSION DATE:** 2025-01-11

**WORK IN PROGRESS**




# DISCLAIMER:
1. This is beta software, use your best judgement if it's right for you.
2. Stock SV08 support only. Refer to Stock folder. When mainline klipper is working, a mainline folder will be added.
3. Dynamic soaking coming in a future version.


# INSTALL:
1. Use winSCP or any method to access the sv08 filesystem. (user: sovol password: sovol)
2. Drag and drop the two folders (klipper and printer_data) provided into the /home/sovol folder.
3. Restart printer completely!
4. Add [include dzos.cfg] to the bottom of your printer.cfg above the commented out part.
5. The dzos.cfg overrides your PRINT_START and [homing_override]. [homing_override] changes are mandatory but if you'd like to adjust your own PRINT_START, 
just add the DZOS call and remove the replacement from the macro in the same place as I placed it.

# USAGE:
1. Enable DZOS by using the DZOS Enable macro. Once done hit 'SAVE CONFIG' in the web interface and restart.
2. Wait for your printer to be at room temperature. It's very important to be room temperature.
3. Run the following macro: DZOS_INIT_SETUP.
4. Follow the on screen instuctions carefully!
5. Once you printer reboots each print will calculate the z
6. DZOS Disable macro will stop the code from running. You should also move the [include dzod.cfg] from the bottom, to the top of your printer.cfg to avoid [homing_override] issues.
7. Happy testing!

