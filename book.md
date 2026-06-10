
[__SOURCE](README.md)
# Hi7 Robot Controller Function Manual - User DIO, Extension DIO



[__SOURCE](0-about-this-manual/precautions.md)
# Precautions

{% include file="en/precautions.md" %}

[__SOURCE](1-overview.md)
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


[__SOURCE](2-HW/README.md)
# 2. Hardware

[__SOURCE](2-HW/1-HW-Inform/README.md)
# 2.1. Hardware Information

The User DIO (BD681) allows integration and configuration with various devices through digital I/O ports.<br>
The Extension DIO (BD682) also allows additional digital I/O ports and synchronization with conveyor signals.<br>
The basic hardware configuration of the board is as follows.<br>

{% hint style="warning" %}
When using two BD681 boards, ensure that the installation positions and switch ON/OFF settings are correct.
To prevent board damage, one BD681 board must be installed in the original BD671 slot.
{% endhint %}

![](../../_assets/25.사용자DIO_보드.png)<br>
< Figure 1. User DIO (BD681)>

<br>

![](../../_assets/26.사용자DIO_보드_커넥터.png)<br>
< Figure 2. User DIO (BD681) Connector>

<br>

![](../../_assets/29.확장DIO_보드.png)<br>
< Figure 3. Extension DIO (BD682)>

<br>

![](../../_assets/30.확장DIO_보드_커넥터.png)<br>
< Figure 4. Extension DIO (BD682) Connector>

[__SOURCE](2-HW/1-HW-Inform/1-Digital-Input.md)
# 2.1.1. Digital Input

The figure and table below illustrate the pin configuration of the terminal block for digital inputs.<br>
Each terminal block supports up to 16 input signals and can accept either NPN or PNP type inputs depending on the application.<br>
Installing an additional BD682 adds 16 digital input points.<br>

![](../../_assets/27.사용자DIO_보드_커넥터_DIN.png)<br>
< Figure 1. User DIO (BD681) Digital Input Connector>

{% hint style="info" %}
Pins 1 and 10, as well as Pins 11 and 20, are internally connected on the board.
{% endhint %}

< Table 1. User DIO (BD681) Digital Input Connector>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>        
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1 ~ 8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A1 </strong></font>
        </td>
        <td style="text-align: center;">Digital Input 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B1 </strong></font>
        </td>
        <td style="text-align: center;">Digital Input 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">Digital Input 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">Digital Input 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A3</td>
        <td style="text-align: center;">Digital Input 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B3</td>
        <td style="text-align: center;">Digital Input 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A4</td>
        <td style="text-align: center;">Digital Input 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B4</td>
        <td style="text-align: center;">Digital Input 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A5</td>
        <td style="text-align: center;">Digital Input 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B5</td>
        <td style="text-align: center;">Digital Input 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A6</td>
        <td style="text-align: center;">Digital Input 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B6</td>
        <td style="text-align: center;">Digital Input 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A7</td>
        <td style="text-align: center;">Digital Input 7</td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">B7</td>
        <td style="text-align: center;">Digital Input 15</td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">A8</td>
        <td style="text-align: center;">Digital Input 8</td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B8</td>
        <td style="text-align: center;">Digital Input 16</td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

When an additional Extension DIO (BD682) is installed, the pin map is as shown below.<br>

![](../../_assets/31.확장DIO_보드_커넥터_DIN.png)<br>
< Figure 2. Extension DIO (BD682) Digital Input Connector>

{% hint style="info" %}
Pins 1 and 10, as well as Pins 11 and 20, are internally connected on the board.
{% endhint %}

< Table 2. Extension DIO (BD682) Digital Input Connector>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>        
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A9 </strong></font>
        </td>
        <td style="text-align: center;">Digital Input 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B9 </strong></font>
        </td>
        <td style="text-align: center;">Digital Input 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A10</td>
        <td style="text-align: center;">Digital Input 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B10</td>
        <td style="text-align: center;">Digital Input 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A11</td>
        <td style="text-align: center;">Digital Input 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B11</td>
        <td style="text-align: center;">Digital Input 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A12</td>
        <td style="text-align: center;">Digital Input 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B12</td>
        <td style="text-align: center;">Digital Input 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A13</td>
        <td style="text-align: center;">Digital Input 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B13</td>
        <td style="text-align: center;">Digital Input 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A14</td>
        <td style="text-align: center;">Digital Input 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B14</td>
        <td style="text-align: center;">Digital Input 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A15</td>
        <td style="text-align: center;">Digital Input 7</td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">B15</td>
        <td style="text-align: center;">Digital Input 15</td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">A16</td>
        <td style="text-align: center;">Digital Input 8</td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B16</td>
        <td style="text-align: center;">Digital Input 16</td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
The NPN and PNP types of the digital input are determined by the voltage connected to the COM pin, as shown in the following table.
{% endhint %}

< Table 3. Digital Input NPN, PNP Connection Information>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">COM Pin Voltage</th>
        <th style="width: 250px; text-align: center;">Note</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">24 V</td>
        <td> 
            Voltage for NPN Input<br>
            (Signal Active Low)
        </td>
    </tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">0 V</td>
        <td> 
            Voltage for PNP Input<br>
            (Signal Active High)
        </td>
    </tr>
</tbody>
</table>



[__SOURCE](2-HW/1-HW-Inform/2-Digital-Output.md)
# 2.1.2. Digital Output

The figure and table below illustrate the pin configuration of the terminal block for digital outputs.<br>
Each terminal block supports up to 16 output signals and can accept either NPN or PNP type outputs depending on the application.<br>
Installing an additional BD682 adds 16 digital output points.<br>


![](../../_assets/28.사용자DIO_보드_커넥터_DOUT.png)<br>
< Figure 1. User DIO (BD681) Digital Output Connector>

{% hint style="info" %}
Pins 1 and 10, as well as Pins 11 and 20, are internally connected on the board.
{% endhint %}

< Table 1. User DIO (BD681) Digital Output Connector>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>        
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1 ~ 8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A1 </strong></font>
        </td>
        <td style="text-align: center;">Digital Output 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B1 </strong></font>
        </td>
        <td style="text-align: center;">Digital Output 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">Digital Output 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">Digital Output 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A3</td>
        <td style="text-align: center;">Digital Output 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B3</td>
        <td style="text-align: center;">Digital Output 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A4</td>
        <td style="text-align: center;">Digital Output 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B4</td>
        <td style="text-align: center;">Digital Output 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A5</td>
        <td style="text-align: center;">Digital Output 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B5</td>
        <td style="text-align: center;">Digital Output 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A6</td>
        <td style="text-align: center;">Digital Output 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B6</td>
        <td style="text-align: center;">Digital Output 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A7</td>
        <td style="text-align: center;">Digital Output 7</td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">B7</td>
        <td style="text-align: center;">Digital Output 15</td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">A8</td>
        <td style="text-align: center;">Digital Output 8</td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B8</td>
        <td style="text-align: center;">Digital Output 16</td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

When an additional Extension DIO (BD682) is installed, the pin map is as shown below.<br>

![](../../_assets/32.확장DIO_보드_커넥터_DOUT.png)<br>
< Figure 2. Extension DIO (BD682) Digital Output Connector>

{% hint style="info" %}
Pins 1 and 10, as well as Pins 11 and 20, are internally connected on the board.
{% endhint %}

{% hint style="info" %}
On the BD682, pins 12 through 19 (digital outputs 9-16) are relay outputs.
{% endhint %}

< Table 2. Extension DIO (BD682) Digital Output Connector>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>        
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 120px; text-align: center;">Description</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A9 </strong></font>
        </td>
        <td style="text-align: center;">Digital Output 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B9 </strong></font>
        </td>
        <td style="text-align: center;">Digital Output 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A10</td>
        <td style="text-align: center;">Digital Output 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B10</td>
        <td style="text-align: center;">Digital Output 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A11</td>
        <td style="text-align: center;">Digital Output 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B11</td>
        <td style="text-align: center;">Digital Output 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A12</td>
        <td style="text-align: center;">Digital Output 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B12</td>
        <td style="text-align: center;">Digital Output 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A13</td>
        <td style="text-align: center;">Digital Output 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B13</td>
        <td style="text-align: center;">Digital Output 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A14</td>
        <td style="text-align: center;">Digital Output 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B14</td>
        <td style="text-align: center;">Digital Output 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A15</td>
        <td style="text-align: center;">Digital Output 7</td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">B15</td>
        <td style="text-align: center;">Digital Output 15</td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">A16</td>
        <td style="text-align: center;">Digital Output 8</td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B16</td>
        <td style="text-align: center;">Digital Output 16</td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (1~8)
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM Signal (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
The NPN and PNP types of the digital output are determined by the voltage connected to the COM pin, as shown in the following table.
{% endhint %}

< Table 3. Digital Output NPN, PNP Connection Information>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">COM Pin Voltage</th>
        <th style="width: 250px; text-align: center;">Note</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">24 V</td>
        <td> 
            Voltage for PNP Output<br>
            (Signal Active High)
        </td>
    </tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">0 V</td>
        <td>
            Voltage for NPN Output<br>
            (Signal Active Low)
        </td>
    </tr>
</tbody>
</table>



[__SOURCE](2-HW/1-HW-Inform/3-Conveyor-Interface.md)
# 2.1.3. Conveyor Synchronization Configuration

The figure and table below illustrate the pin configuration of the terminal block for the encoder input and limit switch used in conveyor synchronization.<br>
The system consists of two input channels in total, and each channel can be connected by selecting one of two encoder types (open collector or line driver).<br>

![](../../_assets/33.확장DIO_보드_커넥터_Conveyor.png)<br>
< Figure 1. Extension DIO (BD682) Conveyor Interface Connector>

< Table 1. Extension DIO (BD682) Conveyor Interface Connector>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 220px; text-align: center;">Description</th>        
        <th style="width: 50px; text-align: center;">Pin No.</th>
        <th style="width: 50px; text-align: center;">Signal</th>
        <th style="width: 220px; text-align: center;">Description</th>   
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">PA2_P</td>
        <td style="text-align: center;">
            Channel 2<br>
            Line Driver Type Encoder<br>
            A Signal Input Positive
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">PA1_P</td>
        <td style="text-align: center;">
            Channel 1<br>
            Line Driver Type Encoder<br>
            A Signal Input Positive
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">PA2_N</td>
        <td style="text-align: center;">
            Channel 2<br>
            Line Driver Type Encoder<br>
            A Signal Input Negative
        </td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">PA1_N</td>
        <td style="text-align: center;">
            Channel 1<br>
            Line Driver Type Encoder<br>
            A Signal Input Negative
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">PB2_P</td>
        <td style="text-align: center;">
            Channel 2<br>
            Line Driver Type Encoder<br>
            B Signal Input Positive
        </td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">PB1_P</td>
        <td style="text-align: center;">
            Channel 1<br>
            Line Driver Type Encoder<br>
            B Signal Input Positive
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">PB2_N</td>
        <td style="text-align: center;">
            Channel 2<br>
            Line Driver Type Encoder<br>
            B Signal Input Negative
        </td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">PB1_N</td>
        <td style="text-align: center;">
            Channel 1<br>
            Line Driver Type Encoder<br>
            B Signal Input Negative
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">LDLS2</td>
        <td style="text-align: center;">
            Channel 2<br>
            Line Driver Type Encoder<br>
            Limit Switch
        </td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">LDLS1</td>
        <td style="text-align: center;">
            Channel 1<br>
            Line Driver Type Encoder<br>
            Limit Switch
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">Ground</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">Ground</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">P2+</td>
        <td style="text-align: center;">
            Channel 2<br>
            Open Collector Type Encoder<br>
            Power
        </td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">P1+</td>
        <td style="text-align: center;">
            Channel 1<br>
            Open Collector Type Encoder<br>
            Power
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">
            Channel 2<br>
            Open Collector Type Encoder<br>
            A Signal Input
        </td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">A1</td>
        <td style="text-align: center;">
            Channel 1<br>
            Open Collector Type Encoder<br>
            A Signal Input
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">
            Channel 2<br>
            Open Collector Type Encoder<br>
            B Signal Input
        </td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B1</td>
        <td style="text-align: center;">
            Channel 1<br>
            Open Collector Type Encoder<br>
            B Signal Input
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">OCLS2</td>
        <td style="text-align: center;">
            Channel 2<br>
            Open Collector Type Encoder<br>
            Limit Switch
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">OCLS1</td>
        <td style="text-align: center;">
            Channel 1<br>
            Open Collector Type Encoder<br>
            Limit Switch
        </td>
    </tr>
</tbody>
</table>
<br>
<br>

< Table 2. Extension DIO (BD682) Conveyor Interface Input Signal Electrical Specifications>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            Signal
        </th>
        <th style="width: 100px; text-align: center;">
            Electrical Specifications
        </th>
        <th style="width: 200px; text-align: center;">
            Note
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">
            PA1_P, PA1_N<br>
            PB1_P, PB1_N<br>
            PA2_P, PA2_N<br>
            PB2_P, PB2_N<br>
        </td>
        <td style="text-align: center;">
            0 V ~ 5 V<br>
            100 kHz or less
        </td>
        <td style="text-align: center;">
            Line Driver Type Encoder Signal
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            LDLS1, LDLS2
        </td>
        <td style="text-align: center;">
            0 V / 5 V
        </td>
        <td style="text-align: center;">
            Line Driver Type Encoder<br>
            Limit Switch Signal
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            P1+, P2+
        </td>
        <td style="text-align: center;">
            24 V
        </td>
        <td style="text-align: center;">
            Open Collector Type Encoder Power
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            A1, B1<br>
            A2, B2
        </td>
        <td style="text-align: center;">
            0 V ~ 24 V<br>
            100 kHz or less
        </td>
        <td style="text-align: center;">
            Open Collector Type Encoder Signal
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            OCLS1, OCLS2
        </td>
        <td style="text-align: center;">
            0 V / 24 V
        </td>
        <td style="text-align: center;">
            Open Collector Type Encoder<br>
            Limit Switch Signal
        </td>
    </tr>
</tbody>
</table>
<br>

[__SOURCE](2-HW/1-HW-Inform/4-Board-Install-Slot.md)
# 2.1.4. Board Installation Slots

The BD681 and BD682 boards must be installed in the correct slots in the robot controller. <br>
The following figure shows the slot positions in the controller. <br>

When using two BD681 boards, one BD681 board must be installed next to the BD680 board.

![](../../_assets/39.Board_install_slot.png)<br>
< Figure 1. Board Installation Slots>


[__SOURCE](2-HW/2-Board-Switch.md)
# 2.2. Board Switch

{% hint style="info" %}
If the BD681 SW version is 1.2.0 or earlier, the switch settings must be configured appropriately. 
If the SW version is 1.3.0 or later, no separate switch setting is required.
{% endhint %}

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
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
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
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            #2 BD681 Switch ON
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            #2 BD681 Switch ON
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            #2 BD681 Switch OFF
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            #2 BD681 Switch OFF
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
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
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            #2 BD681 Switch OFF
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
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
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            #2 BD681 Switch ON
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
</tbody>
</table>
<br>


[__SOURCE](2-HW/3-Board-LED.md)
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

[__SOURCE](3-Configuration/README.md)
# 3. How to Configure User DIO and Extension DIO

[__SOURCE](3-Configuration/1-EtherCAT-Configuration.md)
# 3.1. EtherCAT Configuration

EtherCAT configuration is performed as follows.

Make sure to connect the LAN cable correctly while the controller is turned off.

<mark style="color:green;">**- Single BD681 Configuration ( BD681 + BD682 )**</mark>

![](../_assets/05.BD681_1개_케이블_연결.png)<br>
< Figure 1. Single BD681 Cable Connection>

As shown in the figure above, connect the lower LAN connector of BD642 to the upper LAN connector of BD681, and then turn on the controller power. If EtherCAT is connected normally, it can be verified on the TP under "UserDIO List," as shown below.

**- The location of the menu: [system] - [12: Option System] - [UserDIO Board Setting]**

![](../_assets/07.BD681_1개_사용자DIO_보드_설정_en.png)<br>
< Figure 2. Single BD681 Configuration><br>

![](../_assets/08.BD681_상태표시_LED_en.png)<br>
< Figure 3. BD681 status LED><br>

When the connection is successfully completed, the status indicator LED on the BD681 board operates as follows.

- BD681 status LED operation
1. Flashing at 2-second intervals (waiting for EtherCAT connection)
2. Flashing at 0.25-second intervals (EtherCAT connection Ok, Waiting for Initial Settings)
3. Flashing at 0.75-second intervals (EtherCAT connection Ok, Initial Settings Ok)
<br><br>

<mark style="color:green;">**- Configuration with 2 BD681 Units ( #1_BD681 + BD682 + #2_BD681 )**</mark>

![](../_assets/09.BD681_2개_케이블_연결.png)<br>
< Figure 4. Cable Connection with 2 BD681 Units>

As shown in the figure above, insert BD681 #2 into the slot next to BD681 #1.

{% hint style="info" %}
For #2 BD681, the board switch must be set to ON.
{% endhint %}

For detailed information on the board switch, refer to "[2.2 Board Switch](../2-HW/2-Board-Switch.md)" and "[3.2 Board Switch Check](./2-Board-Switch-check.md)" in the manual.

Connect the lower LAN connector of BD642 to the upper LAN connector of #1 BD681, and then connect the lower LAN connector of #1 BD681 to the upper LAN connector of #2 BD681. After that, turn on the controller power. If EtherCAT is connected successfully, it can be checked on the TP as shown below.

![](../_assets/11.BD681_2개_사용자DIO_보드_설정_en.png)<br>
< Figure 5. BD681 (2 Units) Configuration><br>

When the connection is established successfully, the status LED of the BD681 board operates in the same way as described in "Single BD681 Configuration" under "BD681 status LED operation"

<mark style="color:green;">**- Configuration with 2 BD681 Units ( #1_BD681 + #2_BD681 + BD682 )**</mark>

![](../_assets/09_2.BD681_2개_케이블_연결.png)<br>
< Figure 6. Cable Connection with 2 BD681 Units>

As shown in the figure above, insert BD681 #1 into the slot next to BD681 #2.

{% hint style="info" %}
For #1 BD681, the board switch must be set to ON.
{% endhint %}

![](../_assets/11_2.BD681_2개_사용자DIO_보드_설정_en.png)<br>
< Figure 7. BD681 (2 Units) Configuration><br>

<mark style="color:green;">**- Configuration with 2 BD681 Units ( #1_BD681 + #2_BD681 )**</mark>

{% hint style="info" %}
To use two BD681 boards without a BD682, both the #1 BD681 and #2 BD681 board switches must be set to ON.
{% endhint %}

![](../_assets/37.BD681_2개_연결(BD682_X)_en.png)<br>
< Figure 8. BD681 (2 Units) Configuration without a BD682><br>



[__SOURCE](3-Configuration/2-Board-Switch-check.md)
# 3.2. Board Switch Check


If the board has already been assembled in the controller, the internal switch status can be checked on the TP screen as shown below.<br>

**- The location of the menu: [system] - [12: Option System] - [UserDIO Board Setting]**

You can check it in the "UserDIO List," under the "UserDIO Mode" entry.

{% hint style="info" %}
In order to check correctly in [User DIO Board Setting], BD681 must be connected to EtherCAT successfully.
{% endhint %}


![](../_assets/02.사용자DIO_보드_설정_TP_en.png)<br>
< Figure 1. UserDIO Board Setting TP UI><br>

<br>

< Table 1. User DIO Mode Item>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            BD681 Switch <br>
            ON/OFF
        </th>
        <th style="width: 110px; text-align: center;">
            UserDIO Mode
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">OFF</td>
        <td style="text-align: center;">
            Use Ext_DIO <br>
            (BD681 + BD682)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">ON</td>
        <td style="text-align: center;">
            Only UserDIO <br>
            (BD681)
        </td>
    </tr>
</tbody>
</table>
<br>


When using two User DIO boards, if both User DIO board switches are set to OFF, the system will output the error <strong>"E55005 : User DIO Board mode setting error detected."</strong> <br>
To resolve this error, set the switch of the standalone User DIO board to ON.

{% hint style="warning" %}
If error "E55005 : User DIO Board mode setting error detected." occurs, the User DIO board and Extension DIO board cannot be used properly. You must correct the board switch settings before using them.
{% endhint %}

{% hint style="info" %}
If the BD681 SW version is 1.3.0 or later, no separate switch setting is required.
{% endhint %}

<br>

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
            ON<br>
            (Only UserDIO)
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF<br>
            (Use Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF<br>
            (Use Ext_DIO)
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
            ON<br>
            (Only UserDIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            (Only UserDIO)<br><br>
            #2 BD681 Switch ON<br>
            (Only UserDIO)
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            (Use Ext_DIO)<br><br>
            #2 BD681 Switch ON<br>
            (Only UserDIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            (Only UserDIO)<br><br>
            #2 BD681 Switch OFF<br>
            (Use Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            (Use Ext_DIO)<br><br>
            #2 BD681 Switch OFF<br>
            (Use Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            (Use Ext_DIO)<br><br>
            #2 BD681 Switch ON<br>
            (Only UserDIO)
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch OFF<br>
            (Use Ext_DIO)<br><br>
            #2 BD681 Switch OFF<br>
            (Use Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            (Only UserDIO)<br><br>
            #2 BD681 Switch OFF<br>
            (Use Ext_DIO)
        </td>
        <td style="text-align: center;">O (Available)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 Switch ON<br>
            (Only UserDIO)<br><br>
            #2 BD681 Switch ON<br>
            (Only UserDIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (Unavailable)</font>
        </td>
    </tr>
</tbody>
</table>
<br>

[__SOURCE](3-Configuration/3-FB-Block-Configuration.md)
# 3.3. FB block Configuration

FB block settings can be configured in the following menu.

**- The location of the menu: [system] - [2:Control parameter] - [2:Input/Output signal setting] - [6:fb block allocation]**

![](../_assets/12.FB블럭할당_en.png)<br>
< Figure 1. FB block allocation menu><br><br>

Select the FB block you want to assign and configure it as "User DIO".

![](../_assets/13.fb1_사용자DIO할당_en.png)<br>
< Figure 2. Example of User DIO Assigned to FB1><br><br>

For more details, refer to "[Robot Controller Operation Manual - (FB Block Allocation)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign?cont_model=Hi7)".

Whether an FB block has been assigned to the User DIO can be checked in the [6: FB block allocation] and [UserDIO Board Setting] menus.

![](../_assets/14.사용자DIO_FB_미할당_en.png)<br>
< Figure 3. User DIO FB Block Not Assigned><br><br>

![](../_assets/15.사용자DIO_FB3_할당_en.png)<br>
< Figure 4. User DIO Assigned to FB3><br>

{% hint style="warning" %}
Even if the User DIO is assigned to multiple FB blocks, it is only available in the FB block with the lowest number, and the control signals from the other assigned FB blocks will be ignored.
{% endhint %}

As shown in the figure below, when the FB blocks are assigned, User DIO control is available from FB2, while the parameter values entered in FB5 are ignored.

![](../_assets/16.사용자DIO_FB_다중할당_en.png)<br>
< Figure 5. Example of Multiple FB Assignments for User DIO><br>

[__SOURCE](3-Configuration/4-Internal-PLC-Configuration.md)
# 3.4. Embedded PLC Configuration Check

To properly link the User DIO using FB blocks, it is necessary to check the Embedded PLC settings.

**- Embedded PLC off (Not Used)**<br>

The functions of the embedded PLC will be turned off. When this occurs, the logical outputs of the robot controller, FB0.DO0-FB9.DO959, will be automatically outputted as the physical outputs (means bypassing), FB0.Y0-FB9.Y959, and the physical inputs, FB0.X0-FB9.X959, will be automatically inputted as logical inputs, FB0.DI0-FB9.DI595.<br><br>

**- Embedded PLC Used**

Since the Ladder Logic loaded from the Embedded PLC affects the inputs and outputs of the FB blocks, caution is required.

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
< Figure 1. Example of Logical/Physical I/O Connections of FB1 in Ladder Logic><br>

For more details on the Embedded PLC, refer to "[Robot Controller Function Manual - Embedded PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/en/README?cont_model=Hi7)"

[__SOURCE](3-Configuration/5-Sensor-Sync-Configuration.md)
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

For more details on the "parameter setting", refer to "[Robot Controller Function Manual - Sensor Synchronization (parameter setting)](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/3-user-interface/3-3-sensor-sync-parameter?cont_model=Hi7)".

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

{% hint style="info" %}
When using an open-collector type encoder, the 'Pulse line error' function is not available.<br>
Therefore, you must set 'Pulse line error' in the 'Input signal assign' to '-1 (Not Used)'.
{% endhint %}

{% hint style="warning" %}
When using an open-collector type encoder, if you do not set 'Pulse line error' to '-1 (Not Used)', error E27001 (Conveyor pulse line abnormal) may occur upon controller reboot.
{% endhint %}

![](../_assets/36.오픈콜렉터_엔코더_펄스라인에러_설정_en.png)<br>
< Figure 6. Open Collector Type Encoder Pulse line error setting><br>

For detailed information, refer to the conveyor-related section of "[Robot Controller Function Manual - Sensor Synchronization](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/README?cont_model=Hi7)".

[__SOURCE](4-Usage/README.md)
# 4. How to Use User DIO and Extension DIO
[__SOURCE](4-Usage/1-DIO-Usage.md)
# 4.1. How to Use DIO

If the cables are properly connected to the connectors of BD681 and BD682, refer to the following instructions for controlling digital inputs and outputs.
<br>

<mark style="color:green;">**- Linkage with Controller Input/Output Signals**</mark>

For details on the linkage between the controller I/O signals and the board I/O, please refer to "[Robot Controller Operation Manual - (Input/Output Signal Setting)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/README?cont_model=Hi7)".

<br>

<mark style="color:green;">**- Board Input/Output Control Using TP**</mark>

For controlling board outputs and checking inputs from the TP, refer to "[Robot Controller Operation Manual - (Public Output)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/4-user-output?cont_model=Hi7)" and "[Robot Controller Operation Manual - (Public Input)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/3-user-input?cont_model=Hi7)".

<br>

{% hint style="info" %}
Note that the controlled I/O range differs depending on the BD681 and BD682 combinations.
{% endhint %}

![](../_assets/38.DIO_ctrl.png)<br>
< Figure 1. Example of I/O control ranges according to board combinations><br>

<br>

<mark style="color:green;">**- Board Input/Output Control Using Job**</mark>

For linking board inputs and outputs in a Job, refer to "[Robot Controller Function Manual - Robot Language HRScript (FB Object: Digital I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/en/6-external-comm/1-fb-io/README?cont_model=Hi7)".

<br><br>
Additionally, the User DIO provides a function to configure the digital output state in case a momentary EtherCAT communication error occurs (e.g., transition to Pre-OP or Safe-OP state due to a communication error).

**- The location of the menu: [system] - [12: Option System] - [UserDIO Board Setting]**

![](../_assets/23.연결_오류시_디지털_출력_설정_en.png)<br>
< Figure 2. Digital Output Setting on Connection Error><br>

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
< Figure 3. Change of Digital Output Setting on Connection Error><br>


[__SOURCE](4-Usage/2-Conveyor-Usage.md)
# 4.2. How to Use Conveyor Interface

If the cables are properly connected to the connectors of BD682, refer to the following instructions for controlling conveyor interface.
<br>

<mark style="color:green;">**- Integration of Controller and Conveyor Interface**</mark>

For detailed information on the integration of the controller and conveyor interface using the board, refer to the conveyor-related section of the "[Robot Controller Function Manual - Sensor Synchronization](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/README?cont_model=Hi7)".

