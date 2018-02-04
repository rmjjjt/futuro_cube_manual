# 17.32 ReadRGBLed

Reads the actual RGB color that is currently displayed on the cube

Syntax: `ReadRGBLed(wi)` 

* `wi` walker or spot index

Returns: Color that is in currently displayed on the **real cube surface** at the **moment of calling the function**.

Example: `col=ReadRGBLed(2)`, reads the RGB led color from square index 2

See also: [ReadCanvas](/17-api-native-functions/1731-readcanvas.md)

