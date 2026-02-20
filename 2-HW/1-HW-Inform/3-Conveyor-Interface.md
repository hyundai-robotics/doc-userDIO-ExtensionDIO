# 2.1.3. 输送机同步配置

下图和表格说明了用于输送机同步的编码器输入和限位开关的端子块的引脚配置。<br>
该系统总共由两个输入通道组成，每个通道可以通过选择两种编码器类型之一（开集电极或线路驱动）进行连接。<br>

![](../../_assets/33.扩展DIO_板_连接器_Conveyor.png)<br>
< 图 1. 扩展 DIO (BD682) 输送机接口连接器>

< 表 1. 扩展 DIO (BD682) 输送机接口连接器>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 220px; text-align: center;">描述</th>        
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 220px; text-align: center;">描述</th>   
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">PA2_P</td>
        <td style="text-align: center;">
            通道 2<br>
            线路驱动型编码器<br>
            A 信号输入正极
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">PA1_P</td>
        <td style="text-align: center;">
            通道 1<br>
            线路驱动型编码器<br>
            A 信号输入正极
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">PA2_N</td>
        <td style="text-align: center;">
            通道 2<br>
            线路驱动型编码器<br>
            A 信号输入负极
        </td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">PA1_N</td>
        <td style="text-align: center;">
            通道 1<br>
            行驱动器类型编码器<br>
            A信号输入负向
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">PB2_P</td>
        <td style="text-align: center;">
            通道2<br>
            行驱动器类型编码器<br>
            B信号输入正向
        </td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">PB1_P</td>
        <td style="text-align: center;">
            通道1<br>
            行驱动器类型编码器<br>
            B信号输入正向
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">PB2_N</td>
        <td style="text-align: center;">
            通道2<br>
            行驱动器类型编码器<br>
            B信号输入负向
        </td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">PB1_N</td>
        <td style="text-align: center;">
            通道1<br>
            行驱动器类型编码器<br>
            B信号输入负向
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">LDLS2</td>
        <td style="text-align: center;">
            通道2<br>
            行驱动器类型编码器<br>
            限位开关
        </td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">LDLS1</td>
        <td style="text-align: center;">
            通道1<br>
            行驱动器类型编码器<br>
            限位开关
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">地面</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">地面</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">P2+</td>
        <td style="text-align: center;">
            通道 2<br>
            开放集电极类型编码器<br>
            电源
        </td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">P1+</td>
        <td style="text-align: center;">
            通道 1<br>
            开放集电极类型编码器<br>
            电源
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">
            通道 2<br>
            开放集电极类型编码器<br>
            A 信号输入
        </td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">A1</td>
        <td style="text-align: center;">
            通道 1<br>
            开放集电极类型编码器<br>
            A 信号输入
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">
            通道 2<br>
            开放集电极类型编码器<br>
            B 信号输入
        </td>
<td style="text-align: center;">19</td>
<td style="text-align: center;">B1</td>
<td style="text-align: center;">
    通道 1<br>
    开放集电极类型编码器<br>
    B 信号输入
</td>
</tr>
<tr>
    <td style="text-align: center;">10</td>
    <td style="text-align: center;">OCLS2</td>
    <td style="text-align: center;">
        通道 2<br>
        开放集电极类型编码器<br>
        限位开关
    </td>
    <td style="text-align: center;">20</td>
    <td style="text-align: center;">OCLS1</td>
    <td style="text-align: center;">
        通道 1<br>
        开放集电极类型编码器<br>
        限位开关
    </td>
</tr>
</tbody>
</table>
<br>
<br>

< Table 2. Extension DIO (BD682) 输送带接口输入信号电气规格>

<table>
<thead>
<tr>
    <th style="width: 20px; text-align: center;">编号</th>
    <th style="width: 100px; text-align: center;">
        信号
    </th>
    <th style="width: 100px; text-align: center;">
        电气规格
    </th>
    <th style="width: 200px; text-align: center;">
        注释
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
            100 kHz 或更低
        </td>
        <td style="text-align: center;">
            线驱动器类型编码器信号
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
            线驱动器类型编码器<br>
            限位开关信号
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
            开集电极类型编码器电源
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
            100 kHz 或更低
        </td>
        <td style="text-align: center;">
            开集电极类型编码器信号
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
            开放集电极类型编码器<br>
            限位开关信号
        </td>
    </tr>
</tbody>
</table>
<br>