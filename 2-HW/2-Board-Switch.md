# 2.2. 电路板开关

BD681板开关位置如下图所示。<br>

![](../_assets/01.사용자DIO_보드_스위치_위치.png)<br>
<图1. 用户DIO板开关位置>
<br>

![](../_assets/03.사용자DIO_보드_스위치_ON_OFF.png)<br>
<图2. 用户DIO板开关ON/OFF>

<br>

<表1. 电路板开关设置信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            BD681开关 <br>
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">OFF</td>
        <td> - 扩展DIO（BD682）联动模式<br>
             - 基本构成时（BD681+BD682）使用<br>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">ON</td>
        <td> - 用户DIO（BD681）单独模式<br>
             - 扩展DIO（BD682）无法联动<br>
             - 在基本构成中添加BD681时使用<br> 
             - 需应用于添加的第2个BD681<br>
        </td>
    </tr>
</tbody>
</table>


{% hint style="warning" %}
为确认开关而从控制器中拆卸电路板时，务必先关闭控制器电源，并确认电路板电源关闭后再进行拆卸。
{% endhint %}

<表2. 用户DIO模式组合可否使用>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 150px; text-align: center;">
            用户DIO（BD681），<br> 
            扩展DIO（BD682）数量
        </th>
        <th style="width: 150px; text-align: center;">
            BD681开关<br>
            ON/OFF
        </th>
        <th style="width: 110px; text-align: center;">
            可否使用
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
        <td style="text-align: center;">O（可使用）</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681：1 EA
        </td>
        <td style="text-align: center;">
            OFF
        </td>
        <td style="text-align: center;">X（不可使用）</td>
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
        <td style="text-align: center;">O（可使用）</td>
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
        <td style="text-align: center;">X（不可使用）</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681开关OFF<br>
            #2 BD681开关ON
        </td>
        <td style="text-align: center;">O（可使用）</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关 OFF<br>
            #2 BD681 开关 OFF
        </td>
        <td style="text-align: center;">X（不可使用）</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681：2 EA<br>
            BD682：1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关 ON<br>
            #2 BD681开关OFF
        </td>
        <td style="text-align: center;">X（不可使用）</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681开关ON<br>
            #2 BD681开关ON
        </td>
        <td style="text-align: center;">X（不可使用）</td>
    </tr>
</tbody>
</table>
<br>

