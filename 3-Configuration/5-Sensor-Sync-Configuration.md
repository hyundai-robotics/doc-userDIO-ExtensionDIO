# 3.5. Sensor Synchronization Configuration

{% hint style="info" %}
If the conveyor encoder interface is not used, the "Sensor Synchronization" setting does not need to be configured.
{% endhint %}

When using the conveyor encoder interface of BD682, the "Sensor Synchronization" setting is required.

**- The location of the menu: [system] - [4: Application parameter] - [4: Sensor synchronization]**

![](../_assets/18.센서동기_설정_UI_en.png)<br>
< Figure 1. Sensor Synchronization Configuration UI><br><br>

To use the conveyor encoder interface, set the "Synchronization" item in "Parameter Setting" to "Conveyor" and configure both "Input Signal Assign" and "Output Signal Assign" properly.

![](../_assets/19.동기_상태_컨베이어_설정_en.png)<br>
< Figure 2. Set to Conveyor><br>

For more details on the "parameter setting", refer to "[Robot Controller Function Manual - Sensor Synchronization (parameter setting)](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/3-user-interface/3-3-sensor-sync-parameter)".

<br>
Since the conveyor interface of BD682 is linked to the system I/O, input and output signal assignment is required.

As shown in the figure below, press the **[BD640T BD68X] button** located under the UI to enter the specified I/O number. Finally, press the **[v OK] button** to apply the settings.

![](../_assets/20.채널1_시스템_입출력_설정_en.png)<br>
< Figure 3. Channel 1 System I/O Configuration><br><br>

![](../_assets/21.채널2_시스템_입출력_설정_en.png)<br>
< Figure 4. Channel 2 System I/O Configuration><br><br>

Additionally, you can select the "Pulse count type" and the "Pulse communication type" (encoder type). Please refer to the table below for details.
<br>

< Table 1. Pulse Count Type and Pulse Communication Type (Encoder Type) Information>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">
            No.
        </th>
        <th style="width: 200px; text-align: center;">
            Output Signal Assignment
        </th>
        <th style="width: 30px; text-align: center;">
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">
            Note
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>1</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            Pulse Count Type
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            Up / Down Count method
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Up Count method (Default)
        </td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>2</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            Pulse Communication Type<br>
            (Encoder Type)
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            Open Collector Type Encoder
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Line Driver Type Encoder (Default)
        </td>
    </tr>
</tbody>
</table>

<br>

As shown in the figure below, you can set it to ON by clicking the checkbox.<br>
To apply the setting, be sure to press the **[v OK] button**.

![](../_assets/22.출력신호할당_ON_en.png)<br>
< Figure 5. Pulse Count Type ON Applied><br>

For detailed information, refer to the conveyor-related section of "[Robot Controller Function Manual - Sensor Synchronization](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/README)".
