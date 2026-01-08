# 2.2. Board Switch

The switch positions of the BD681 board are shown in the figure below.<br>

![](../_assets/01.사용자DIO_보드_스위치_위치.png)<br>
< Figure 1. User DIO Board switch positions>
<br>

![](../_assets/03.사용자DIO_보드_스위치_ON_OFF.png)<br>
< Figure 2. User DIO Board switch ON/OFF>

<br>

< Table 1. Board Switch Settings>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            BD681 Switch <br>
            ON/OFF
        </th>
        <th style="width: 400px; text-align: center;">Note</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">OFF</td>
        <td> - Extension DIO (BD682) Interface Mode<br>
             - Use in Basic Option Configuration (BD681 + BD682)<br>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">ON</td>
        <td> - User DIO (BD681) Standalone Mode <br>
             - Extension DIO (BD682) Integration Not Supported<br>
             - Used When Adding BD681 to the Basic Option Configuration<br> 
             - Required for the Second Added BD681 <br>
        </td>
    </tr>
</tbody>
</table>


{% hint style="warning" %}
When removing the board from the controller to check the switches, always turn off the controller power and make sure the board power is off before removal.
{% endhint %}

< Table 2. Supported User DIO Mode Combinations>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 250px; text-align: center;">
            User DIO (BD681) /<br> Extension DIO (BD682) Quantity
        </th>
        <th style="width: 150px; text-align: center;">
            BD681 Switch<br>
            ON/OFF
        </th>
        <th style="width: 110px; text-align: center;">
            Availability
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            ON
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF
        </td>
        <td style="text-align: center;">X (Unavailable)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            ON
        </td>
        <td style="text-align: center;">X (Unavailable)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            #2 BD681 Switch ON
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            #2 BD681 Switch OFF
        </td>
        <td style="text-align: center;">X (Unavailable)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            #2 BD681 Switch OFF
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            #2 BD681 Switch ON
        </td>
        <td style="text-align: center;">X (Unavailable)</td>
    </tr>
</tbody>
</table>
<br>

