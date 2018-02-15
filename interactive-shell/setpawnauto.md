# 15.28 setpawnauto

Auto script start for multiple scripts - from FW 4.5

Syntax: `setpawnauto event source [index]`

* `event` : ”std” or ”charge” or ”menu”
* `source` : ”std” or ”flash” or ”mycube”
* `index` : index of script in FLASH, if blank, than it equals 0

Example:

* `setpawnauto std`, resets everything to default 

* `setpawnauto menu flash 2`, sets script of index 2 in FLASH to be automatically started prior to menu

* `setpawnauto menu flash`, sets script of index 0 in FLASH to be automatically started prior to menu

* `setpawnauto charge flash 3`, sets script of index 3 in FLASH to be automatically started instead of standard charging

* `setpawnauto charge std`, sets standard charging

* `setpawnauto charge mycube`, sets MYCUBE script to be automatically started instead of standard charging



