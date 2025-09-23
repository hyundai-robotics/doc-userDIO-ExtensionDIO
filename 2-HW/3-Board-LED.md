# 2.3. Board Status LED


BD681 is equipped with an LED that indicates the board status.<br>
By checking the LED operation status, you can verify whether the board is functioning normally.

![](../_assets/34.보드_LED.png)<br>
< Figure 1. Board Status LED>

<br>

![](../_assets/35.보드_LED_상세.png)<br>
< Figure 2. Board Status LED Details>

<br>

< Table 1. Board Status LED Details>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 80px; text-align: center;">LED Color</th>
        <th style="width: 110px; text-align: center;">LED Name</th>
        <th style="width: 180px; text-align: center;">Note</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">IO_LED</td>
        <td style="text-align: center;">MCU (CPU 1) Status</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">MOD_LED</td>
        <td style="text-align: center;">MCU (CM) Status</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">EtherCAT Operating Status</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">Red</td>
        <td style="text-align: center;">EC_LED_ERR</td>
        <td style="text-align: center;">EtherCAT Error Status</td>
    </tr>
</tbody>
</table>
<br>

<br>

< Table 2. LED Indication by EtherCAT Status>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED Name</th>
        <th style="width: 160px; text-align: center;">LED Status</th>
        <th style="width: 160px; text-align: center;">EtherCAT Status</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">OFF</td>
        <td style="text-align: center;">INIT</td>
    </tr>
    <tr>
        <td style="text-align: center;">Flashing</td>
        <td style="text-align: center;">Pre-OP</td>
    </tr>
    <tr>
        <td style="text-align: center;">Single Flashing</td>
        <td style="text-align: center;">Safe-OP</td>
    </tr>
    <tr>
        <td style="text-align: center;">ON</td>
        <td style="text-align: center;">OP</td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">EC_LED_ERR</td>
        <td style="text-align: center;">OFF</td>
        <td style="text-align: center;">No Error</td>
    </tr>
    <tr>
        <td style="text-align: center;">Flashing</td>
        <td style="text-align: center;">Error</td>
    </tr>
</tbody>
</table>
<br>

<br>

< Table 3. LED Indication by MCU Operating Status>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED Name</th>
        <th style="width: 160px; text-align: center;">LED Status</th>
        <th style="width: 160px; text-align: center;">MCU Operating Status</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">
            IO_LED,<br>
            MOD_LED
        </td>
        <td style="text-align: center;">
            Flashing at<br>
            2-second intervals
        </td>
        <td style="text-align: center;">
            waiting for <br>
            EtherCAT connection
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            Flashing at<br>
            0.25-second intervals            
        </td>
        <td style="text-align: center;">
            EtherCAT connection Ok,<br>
            Waiting for Initial Settings            
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            Flashing at<br>
            0.75-second intervals
        </td>
        <td style="text-align: center;">
            EtherCAT connection Ok,<br>
            Initial Settings Ok
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            Flashing at<br>
            0.1-second intervals
        </td>
        <td style="text-align: center;">
            EtherCAT Status error,<br>
            Initial Settings Ok
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
If the IO_LED and MOD_LED do not flash (whether they are off or remain steadily on), it indicates that the MCU is not operating normally.
{% endhint %}
