## HW Setup

1. Using RFCube Suite, upload the newest FW for the cube. You can always fint it at: RFCubeFW/MainCube
2. New Cube FW allows you to upload the newest communication FW into the Nordic BLE chip (this chip is next to man ST CPU and drives all RF communication). The FW is located in RFCube/NordicBleChip.There is a python updater, which you have to use in following manner:

**ble_update.py com_port file_name**
**com_port** - port on which the cube is enumerated
**file_name** - binary file with the Nordic FW

**Example WIN:**
ble_update.py COM1 RFC_HW_1_3_Nordic_rev2_S117_Bluetooth_Low_Energy_ver_1_1.bin

**Example MacOX** (ls /dev/tty* can help to find the device):
ble_update.py  /dev/tty.usbmodem1411 RFC_HW_1_3_Nordic_rev2_S117_Bluetooth_Low_Energy_ver_1_1.bin


3. Now we have to completely erase and update FW in the BL620 Laird dongle. This is done with a special program called **nrfjprog**. You can find download links in the [SW requirements section](ble/sw-reqs.md). FW for the BL620 DongleFW/Laird-BL620. Just a little note here. We are completely erasing the pre-programmed factory SW and we will use our own proprietary. The only reason we have used this USB dongle is that it is easily available and nicely packaged. Thus, it has several limitations - read below. To upload the FW, you have to execute following commands:

**nrfjprog --eraseall -f nrf51**
(this first command is needed to run this just once with a fresh dongle to remove write protection. Next time, you can use the second command only)
**nrfjprog --program fw_name.hex -f nrf51  --sectorerase**
**fw_name** - dongle latest FW
**nrfjprog --reset -f nrf51**
This restarts the dongle, or you can replug it...

Example (can be done all in one batch file):
**nrfjprog --eraseall -f nrf51**
**nrfjprog --program Laird_Dongle_BL620_1_RFC_Dongle_ver_1_1.hex -f nrf51  --sectorerase**
**nrfjprog --reset -f nrf51**
