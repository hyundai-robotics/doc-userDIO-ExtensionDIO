# 4.1. How to Use DIO

If the cables are properly connected to the connectors of BD681 and BD682, refer to the following instructions for controlling digital inputs and outputs.
<br>

<mark style="color:green;">**- Linkage with Controller Input/Output Signals**</mark>

For details on the linkage between the controller I/O signals and the board I/O, please refer to "[Robot Controller Operation Manual - (Input/Output Signal Setting)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/english-tp630/7-system/3-control-parameter/2-io-signal-setting/README)".

<br>

<mark style="color:green;">**- Board Input/Output Control Using TP**</mark>

For controlling board outputs and checking inputs from the TP, refer to "[Robot Controller Operation Manual - (Public Output)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/english-tp630/6-monitoring/2-io/4-user-output)" and "[Robot Controller Operation Manual - (Public Input)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/english-tp630/6-monitoring/2-io/3-user-input)".

<br>

<mark style="color:green;">**- Board Input/Output Control Using Job**</mark>

For linking board inputs and outputs in a Job, refer to "[Robot Controller Function Manual - Robot Language HRScript (FB Object: Digital I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/english/6-external-comm/1-fb-io/README)".

<br><br>
Additionally, the User DIO provides a function to configure the digital output state in case a momentary EtherCAT communication error occurs (e.g., transition to Pre-OP or Safe-OP state due to a communication error).

**- The location of the menu: [system] - [12: Option System] - [UserDIO Board Setting]**

![](../_assets/23.연결_오류시_디지털_출력_설정_en.png)<br>
< Figure 1. Digital Output Setting on Connection Error><br>

<br>

< Table 1. Digital Output Setting Information on Connection Error>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            Setting Value
        </th>
        <th style="width: 370px; text-align: center;">
            Note
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            Clear Value<br>
            (Default)
        </td>
        <td> 
             - Set all board outputs to OFF on connection error
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            Hold Value
        </td>
        <td> 
             - On connection error, hold board outputs at the last value
        </td>
    </tr>
</tbody>
</table>

<br>
If you want to change the configured value, select the desired setting and press the [v OK] button.<br><br>

![](../_assets/24.연결_오류시_디지털_출력_설정값_변경_en.png)<br>
< Figure 2. Change of Digital Output Setting on Connection Error><br>

