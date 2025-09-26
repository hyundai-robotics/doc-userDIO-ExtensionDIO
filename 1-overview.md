# 1. Overview

In the Hi7 controller, the "User DIO Board (BD681)" and the "Extension DIO Board (BD682)" to process digital I/O signals and interface with conveyor signals.

{% hint style="info" %}
In this manual, DIO stands for Digital Input and Output.
{% endhint %}

The "Extension DIO Board (BD682)" cannot be used independently, and it must be used together with the "User DIO Board (BD681)."

<br>

< Table 1. Board Specification>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 200px; text-align: center;">
            Board Name<br>
            (Board Identifier)
        </th>
        <th style="width: 350px; text-align: center;">
            Board Features
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            User DIO Board<br>
            ( BD681 )
        </td>
        <td> 
             - Digital Input 16 ch <br>
             - Digital Ouput 16 ch
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            Extension DIO Board<br>
            ( BD682 )
        </td>
        <td> 
             - Digital Input 16 ch <br>
             - Digital Ouput 16 ch (Relay Output (8 ch) Included)<br> 
             - Conveyor Interface 2 ch <br> 
             - Not for standalone use (requires BD681)
        </td>
    </tr>
</tbody>
</table>

<br>
A maximum of 48 I/O channels can be controlled using two BD681 boards and one BD682 board.
<br><br>

For proper use of the User DIO and Extension DIO, the following items must be configured and verified.<br>

1. EtherCAT Configuration<br>
2. Board Switch Check<br>
3. FB block Configuration<br>
4. Embedded PLC Configuration<br>
5. Sensor Sync Configuration<br>

