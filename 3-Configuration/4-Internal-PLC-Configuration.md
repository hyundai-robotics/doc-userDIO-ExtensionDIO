# 3.4. Embedded PLC Configuration Check

To properly link the User DIO using FB blocks, it is necessary to check the Embedded PLC settings.

**- Embedded PLC off (Not Used)**<br>

The functions of the embedded PLC will be turned off. When this occurs, the logical outputs of the robot controller, FB0.DO0–FB9.DO959, will be automatically outputted as the physical outputs (means bypassing), FB0.Y0–FB9.Y959, and the physical inputs, FB0.X0–FB9.X959, will be automatically inputted as logical inputs, FB0.DI0–FB9.DI595.<br><br>

**- Embedded PLC Used**

Since the Ladder Logic loaded from the Embedded PLC affects the inputs and outputs of the FB blocks, caution is required.

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
< Figure 1. Example of Logical/Physical I/O Connections of FB1 in Ladder Logic><br>

For more details on the Embedded PLC, refer to "[Robot Controller Function Manual – Embedded PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/english/README)"
