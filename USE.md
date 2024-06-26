# Use cases
Recommandations for pratical uses of the logger
## Messages sent
Messages emitted by F9P/F9R depending on the configuration (may not reflect the current state of the code)

| Configuration | UART1(log) | UART2(BT) |
| --- | --- | --- |
| F9P (base) | <ins>NMEA</ins><br>GNGGA<br><ins>UBX</ins><br>RXM-RAWX<br>RXM-SFRBX<br>(NAV-SVIN if Survey-In used)| <ins>RTCM</ins><br>1005<br>1077<br>1087<br>1097<br>1127<br>1230 |
| F9P (rover) | <ins>NMEA</ins><br>GNGGA<br>GNGSA<br>GNGST<br>G*GSV<br>GNRMC<br>GNVTG<br><ins>UBX</ins><br>RXM-RAWX<br>RXM-SFRBX<br>NAV_POSLLH<br>NAV-PVT<br>NAV-SAT<br>TIM-TIM2 (timestamp of waypoints) | <ins>NMEA</ins><br>GNGGA<br>GNGLL<br>GNGSA<br>GNGST<br>G*GSV<br>GNRMC<br>GNVTG |
| F9R (no HPS) | <ins>NMEA</ins><br>same as previous<br><ins>UBX</ins><br>same as previous<br>+<br>ESF-RAW | <ins>NMEA</ins><br>same as previous |
| F9R (with HPS) | <ins>NMEA</ins><br>same as previous<br>+<br>GNTHS<br><ins>UBX</ins><br>same as previous<br>+<br>ESF-STATUS<br>ESF-ALG<br>NAV-ATT | <ins>NMEA</ins><br>same as previous<br>+<br>GNTHS |
| F9R (with HPS & automotive) | <ins>NMEA</ins><br>same as previous<br><ins>UBX</ins><br>same as previous<br>+<br>NAV-RELPOSNED | <ins>NMEA</ins><br>same as previous |
