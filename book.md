
[__SOURCE](1-overview.md)
# 1. 概述

在 Hi7 控制器中，“用户 DIO 板 (BD681)” 和 “扩展 DIO 板 (BD682)” 用于处理数字 I/O 信号并与传送带信号接口。

{% hint style="info" %}
在本手册中，DIO 代表数字输入和输出。
{% endhint %}

“扩展 DIO 板 (BD682)” 不能独立使用，必须与“用户 DIO 板 (BD681)” 一起使用。

<br>

< 表 1. 板规格>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            编号
        </th>
        <th style="width: 200px; text-align: center;">
            板名称<br>
            (板识别号)
        </th>
        <th style="width: 350px; text-align: center;">
            板特点
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            用户 DIO 板<br>
            ( BD681 )
        </td>
        <td> 
             - 数字输入 16 ch <br>
             - 数字输出 16 ch
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            扩展 DIO 板<br>
            ( BD682 )
        </td>
        <td> 
             - 数字输入 16 通道 <br>
             - 数字输出 16 通道 (包含继电器输出 (8 通道))<br> 
             - 输送带接口 2 通道 <br> 
             - 不可单独使用 (需要 BD681)
        </td>
    </tr>
</tbody>
</table>

<br>
最多可以使用两个 BD681 板和一个 BD682 板控制 48 个 I/O 通道。
<br><br>

为了正确使用用户 DIO 和扩展 DIO，必须配置和验证以下项目。<br>

1. EtherCAT 配置<br>
2. 板开关检查<br>
3. FB 块配置<br>
4. 嵌入式 PLC 配置<br>
5. 传感器同步配置<br>
[__SOURCE](2-HW/README.md)
# 2. 硬件
[__SOURCE](2-HW/1-HW-Inform/README.md)
# 2.1. 硬件信息

用户DIO (BD681) 通过数字I/O端口允许与各种设备的集成和配置。<br>
扩展DIO (BD682) 还允许额外的数字I/O端口和与传送带信号的同步。<br>
电路板的基本硬件配置如下。<br>

{% hint style="warning" %}
使用两个BD681电路板时，请确保安装位置和开关ON/OFF设置正确。
为了防止电路板损坏，必须将一个BD681电路板安装在原始BD671插槽中。
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
# 2.1.1. 数字输入

下面的图和表说明了数字输入端子块的引脚配置。<br>
每个端子块最多支持16个输入信号，并且可以根据应用接受NPN或PNP类型的输入。<br>
安装额外的BD682可添加16个数字输入点。<br>

![](../../_assets/27.사용자DIO_보드_커넥터_DIN.png)<br>
< 图 1. 用户 DIO (BD681) 数字输入连接器>

{% hint style="info" %}
第1和第10引脚以及第11和第20引脚在电路板上是内部连接的。
{% endhint %}

< 表 1. 用户 DIO (BD681) 数字输入连接器>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>        
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号（1 ~ 8）
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号（9~16）
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A1 </strong></font>
        </td>
        <td style="text-align: center;">数字输入1</td>
        <td style="text-align: center;">12</td>
<td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B1 </strong></font>
        </td>
        <td style="text-align: center;">数字输入 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">数字输入 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">数字输入 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A3</td>
        <td style="text-align: center;">数字输入 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B3</td>
        <td style="text-align: center;">数字输入 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A4</td>
        <td style="text-align: center;">数字输入 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B4</td>
        <td style="text-align: center;">数字输入 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A5</td>
        <td style="text-align: center;">数字输入 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B5</td>
        <td style="text-align: center;">数字输入 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A6</td>
        <td style="text-align: center;">数字输入 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B6</td>
        <td style="text-align: center;">数字输入 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A7</td>
        <td style="text-align: center;">数字输入 7</td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">B7</td>
        <td style="text-align: center;">数字输入 15</td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">A8</td>
        <td style="text-align: center;">数字输入 8</td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B8</td>
        <td style="text-align: center;">数字输入 16</td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM 信号 (1~8)
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM 信号 (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

当安装附加扩展 DIO (BD682) 后，引脚图如下所示。<br>

![](../../_assets/31.扩展DIO_板_连接器_DIN.png)<br>
< Figure 2. 扩展 DIO (BD682) 数字输入连接器>

{% hint style="info" %}
引脚 1 和 10，以及引脚 11 和 20，在板上是内部连接的。
{% endhint %}

< Table 2. 扩展 DIO (BD682) 数字输入连接器>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>        
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
<th style="width: 120px; text-align: center;">描述</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM 信号 (1~8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM 信号 (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A9 </strong></font>
        </td>
        <td style="text-align: center;">数字输入 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B9 </strong></font>
        </td>
        <td style="text-align: center;">数字输入 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A10</td>
        <td style="text-align: center;">数字输入 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B10</td>
        <td style="text-align: center;">数字输入 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A11</td>
        <td style="text-align: center;">数字输入 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B11</td>
        <td style="text-align: center;">数字输入 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
```html
<td style="text-align: center;">A12</td>
<td style="text-align: center;">数字输入 4</td>
<td style="text-align: center;">15</td>
<td style="text-align: center;">B12</td>
<td style="text-align: center;">数字输入 12</td>
</tr>
<tr>
<td style="text-align: center;">6</td>
<td style="text-align: center;">A13</td>
<td style="text-align: center;">数字输入 5</td>
<td style="text-align: center;">16</td>
<td style="text-align: center;">B13</td>
<td style="text-align: center;">数字输入 13</td>
</tr>
<tr>
<td style="text-align: center;">7</td>
<td style="text-align: center;">A14</td>
<td style="text-align: center;">数字输入 6</td>
<td style="text-align: center;">17</td>
<td style="text-align: center;">B14</td>
<td style="text-align: center;">数字输入 14</td>
</tr>
<tr>
<td style="text-align: center;">8</td>
<td style="text-align: center;">A15</td>
<td style="text-align: center;">数字输入 7</td>
<td style="text-align: center;">18</td>
<td style="text-align: center;">B15</td>
<td style="text-align: center;">数字输入 15</td>
</tr>
<tr>
<td style="text-align: center;">9</td>
<td style="text-align: center;">A16</td>
<td style="text-align: center;">数字输入 8</td>
<td style="text-align: center;">19</td>
<td style="text-align: center;">B16</td>
<td style="text-align: center;">数字输入 16</td>
</tr>
<tr>
<td style="text-align: center;">10</td>
<td style="text-align: center;">
    <font style="color:rgb(0, 230, 0);"><strong> COM_IN_A </strong></font>
</td>
<td style="text-align: center;">
    COM 信号 (1~8)
</td>
<td style="text-align: center;">20</td>
<td style="text-align: center;">
    <font style="color:rgb(112, 48, 160);"><strong> COM_IN_B </strong></font>
</td>
```
<td style="text-align: center;">
            COM 信号 (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
数字输入的 NPN 和 PNP 类型由连接到 COM 针脚的电压决定，如下表所示。
{% endhint %}

< Table 3. 数字输入 NPN, PNP 连接信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">COM 针脚电压</th>
        <th style="width: 250px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">24 V</td>
        <td> 
            NPN 输入的电压<br>
            (信号有效低)
        </td>
    </tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">0 V</td>
        <td> 
            PNP 输入的电压<br>
            (信号有效高)
        </td>
    </tr>
</tbody>
</table>
[__SOURCE](2-HW/1-HW-Inform/2-Digital-Output.md)
# 2.1.2. 数字输出

下面的图和表展示了数字输出端子块的引脚配置。<br>
每个端子块支持最多16个输出信号，并可以根据应用接受NPN或PNP类型的输出。<br>
安装额外的BD682可以增加16个数字输出点。<br>

![](../../_assets/28.用户DIO_板_连接器_DOUT.png)<br>
< Figure 1. 用户 DIO (BD681) 数字输出连接器>

{% hint style="info" %}
引脚1和10，以及引脚11和20，在板上是内部连接的。
{% endhint %}

< Table 1. 用户 DIO (BD681) 数字输出连接器>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>        
        <th style="width: 50px; text-align: center;">引脚号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号 (1 ~ 8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号 (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A1 </strong></font>
        </td>
        <td style="text-align: center;">数字输出 1</td><
<table>
    <tr>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B1 </strong></font>
        </td>
        <td style="text-align: center;">数字输出 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">数字输出 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">数字输出 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A3</td>
        <td style="text-align: center;">数字输出 3</td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">B3</td>
        <td style="text-align: center;">数字输出 11</td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">A4</td>
        <td style="text-align: center;">数字输出 4</td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">B4</td>
        <td style="text-align: center;">数字输出 12</td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">A5</td>
        <td style="text-align: center;">数字输出 5</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">B5</td>
        <td style="text-align: center;">数字输出 13</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">A6</td>
        <td style="text-align: center;">数字输出 6</td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">B6</td>
        <td style="text-align: center;">数字输出 14</td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A7</td>
        <td style="text-align: center;">数字输出 7</td>
    </tr>
</table>
```html
<td style="text-align: center;">18</td>
<td style="text-align: center;">B7</td>
<td style="text-align: center;">数字输出 15</td>
</tr>
<tr>
<td style="text-align: center;">9</td>
<td style="text-align: center;">A8</td>
<td style="text-align: center;">数字输出 8</td>
<td style="text-align: center;">19</td>
<td style="text-align: center;">B8</td>
<td style="text-align: center;">数字输出 16</td>
</tr>
<tr>
<td style="text-align: center;">10</td>
<td style="text-align: center;">
<font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
</td>
<td style="text-align: center;">
COM 信号 (1~8)
</td>
<td style="text-align: center;">20</td>
<td style="text-align: center;">
<font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
</td>
<td style="text-align: center;">
COM 信号 (9~16)
</td>
</tr>
</tbody>
</table>
<br>

安装额外的扩展 DIO (BD682) 时，针脚映射如下所示。<br>

![](../../_assets/32.扩展DIO_板_连接器_DOUT.png)<br>
< Figure 2. 扩展 DIO (BD682) 数字输出连接器>

{% hint style="info" %}
引脚 1 和 10，以及引脚 11 和 20，在电路板上是内部连接的。
{% endhint %}

{% hint style="info" %}
在 BD682 上，引脚 12 到 19（数字输出 9-16）是继电器输出。
{% endhint %}

< Table 2. 扩展 DIO (BD682) 数字输出连接器>
```
<<<SOURCE_MARKDOWN_START>>>        <th style="width: 50px; text-align: center;">引脚编号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>        
        <th style="width: 50px; text-align: center;">引脚编号</th>
        <th style="width: 50px; text-align: center;">信号</th>
        <th style="width: 120px; text-align: center;">描述</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号 (1~8)
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM信号 (9~16)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">
            <font style="color:rgb(0, 112, 192);"><strong> A9 </strong></font>
        </td>
        <td style="text-align: center;">数字输出 1</td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">
            <font style="color:rgb(255, 0, 0);"><strong> B9 </strong></font>
        </td>
        <td style="text-align: center;">数字输出 9</td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">A10</td>
        <td style="text-align: center;">数字输出 2</td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">B10</td>
        <td style="text-align: center;">数字输出 10</td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">A11</td>
        <td style="text-align: center;">数字输出 3</td>
        <td style="text-align: center;">14</td><<<SOURCE_MARKDOWN_END>>>
```
<td style="text-align: center;">B11</td>
<td style="text-align: center;">数字输出 11</td>
</tr>
<tr>
<td style="text-align: center;">5</td>
<td style="text-align: center;">A12</td>
<td style="text-align: center;">数字输出 4</td>
<td style="text-align: center;">15</td>
<td style="text-align: center;">B12</td>
<td style="text-align: center;">数字输出 12</td>
</tr>
<tr>
<td style="text-align: center;">6</td>
<td style="text-align: center;">A13</td>
<td style="text-align: center;">数字输出 5</td>
<td style="text-align: center;">16</td>
<td style="text-align: center;">B13</td>
<td style="text-align: center;">数字输出 13</td>
</tr>
<tr>
<td style="text-align: center;">7</td>
<td style="text-align: center;">A14</td>
<td style="text-align: center;">数字输出 6</td>
<td style="text-align: center;">17</td>
<td style="text-align: center;">B14</td>
<td style="text-align: center;">数字输出 14</td>
</tr>
<tr>
<td style="text-align: center;">8</td>
<td style="text-align: center;">A15</td>
<td style="text-align: center;">数字输出 7</td>
<td style="text-align: center;">18</td>
<td style="text-align: center;">B15</td>
<td style="text-align: center;">数字输出 15</td>
</tr>
<tr>
<td style="text-align: center;">9</td>
<td style="text-align: center;">A16</td>
<td style="text-align: center;">数字输出 8</td>
<td style="text-align: center;">19</td>
<td style="text-align: center;">B16</td>
<td style="text-align: center;">数字输出 16</td>
</tr>
<tr>
<td style="text-align: center;">10</td>
<td style="text-align: center;">
<font style="color:rgb(0, 230, 0);"><strong> COM_OUT_A </strong></font>
</td>
<td style="text-align: center;">
COM 信号 (1~8)
```
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">
            <font style="color:rgb(112, 48, 160);"><strong> COM_OUT_B </strong></font>
        </td>
        <td style="text-align: center;">
            COM 信号 (9~16)
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
数字输出的 NPN 和 PNP 类型由连接到 COM 引脚的电压决定，如下表所示。
{% endhint %}

< Table 3. 数字输出 NPN, PNP 连接信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">COM 引脚电压</th>
        <th style="width: 250px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">24 V</td>
        <td> 
            PNP 输出电压<br>
            (信号高电平有效)
        </td>
    </tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">0 V</td>
        <td>
            NPN 输出电压<br>
            (信号低电平有效)
        </td>
    </tr>
</tbody>
</table>
[__SOURCE](2-HW/1-HW-Inform/3-Conveyor-Interface.md)
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
[__SOURCE](2-HW/2-Board-Switch.md)
# 2.2. 板开关

BD681 板的开关位置如下图所示。<br>

![](../_assets/01.用户DIO_板_开关_位置.png)<br>
< Figure 1. 用户 DIO 板开关位置>
<br>

![](../_assets/03.用户DIO_板_开关_ON_OFF.png)<br>
< Figure 2. 用户 DIO 板开关 ON/OFF>

<br>

< Table 1. 板开关设置>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">
            BD681 开关 <br>
            开/关
        </th>
        <th style="width: 400px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">关</td>
        <td> - 扩展 DIO (BD682) 接口模式<br>
             - 用于基本选项配置 (BD681 + BD682)<br>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">开</td>
        <td> - 用户 DIO (BD681) 独立模式 <br>
             - 不支持扩展 DIO (BD682) 集成<br>
             - 在将 BD681 添加到基本选项配置时使用<br> 
             - 需要第二个添加的 BD681 <br>
        </td>
    </tr>
</tbody>
</table>


{% hint style="warning" %}
在从控制器上拆下电路板以检查开关时，请始终关闭控制器电源，并确保在拆卸之前电路板电源已关闭。
{% endhint %}
< Table 2. 支持的用户 DIO 模式组合>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 250px; text-align: center;">
            用户 DIO (BD681) /<br> 扩展 DIO (BD682) 数量
        </th>
        <th style="width: 150px; text-align: center;">
            BD681 开关<br>
            开/关
        </th>
        <th style="width: 110px; text-align: center;">
            可用性
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
            开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            关
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            关
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关打开<br>
            #2 BD681 开关打开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关关闭<br>
            #2 BD681 开关打开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关打开<br>
            #2 BD681 开关关闭
        </td>        
<font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 关闭
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 打开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 关闭
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 打开<br>
            #2 BD681 关闭
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2 个<br>
            BD682 : 1 个
        </td>
        <td style="text-align: center;">
            #1 BD681 打开<br>
            #2 BD681 打开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
</tbody>
</table>
<br>
[__SOURCE](2-HW/3-Board-LED.md)
# 2.3. 板状态 LED

BD681 配备了一个指示板状态的 LED。<br>
通过检查 LED 的操作状态，您可以验证板是否正常工作。

![](../_assets/34.보드_LED.png)<br>
< Figure 1. 板状态 LED>

<br>

![](../_assets/35.보드_LED_상세.png)<br>
< Figure 2. 板状态 LED 详情>

<br>

< Table 1. 板状态 LED 详情>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 80px; text-align: center;">LED 颜色</th>
        <th style="width: 110px; text-align: center;">LED 名称</th>
        <th style="width: 180px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">绿色</td>
        <td style="text-align: center;">IO_LED</td>
        <td style="text-align: center;">MCU (CPU 1) 状态</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">绿色</td>
        <td style="text-align: center;">MOD_LED</td>
        <td style="text-align: center;">MCU (CM) 状态</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">绿色</td>
        <td style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">EtherCAT 操作状态</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">红色</td>
        <td style="text-align: center;">EC_LED_ERR</td>
<td style="text-align: center;">EtherCAT 错误状态</td>
    </tr>
</tbody>
</table>
<br>

<br>

< Table 2. 由 EtherCAT 状态指示的 LED>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED 名称</th>
        <th style="width: 160px; text-align: center;">LED 状态</th>
        <th style="width: 160px; text-align: center;">EtherCAT 状态</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">关闭</td>
        <td style="text-align: center;">初始化</td>
    </tr>
    <tr>
        <td style="text-align: center;">闪烁</td>
        <td style="text-align: center;">预操作</td>
    </tr>
    <tr>
        <td style="text-align: center;">单闪烁</td>
        <td style="text-align: center;">安全操作</td>
    </tr>
    <tr>
        <td style="text-align: center;">开启</td>
        <td style="text-align: center;">操作</td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">EC_LED_ERR</td>
        <td style="text-align: center;">关闭</td>
        <td style="text-align: center;">无错误</td>
    </tr>
    <tr>
        <td style="text-align: center;">闪烁</td>
        <td style="text-align: center;">错误</td>
    </tr>
</tbody>
</table>
<br>

<br>
< Table 3. LED 指示灯根据 MCU 操作状态>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED 名称</th>
        <th style="width: 160px; text-align: center;">LED 状态</th>
        <th style="width: 160px; text-align: center;">MCU 操作状态</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">
            IO_LED,<br>
            MOD_LED
        </td>
        <td style="text-align: center;">
            每 2 秒<br>
            闪烁一次
        </td>
        <td style="text-align: center;">
            等待 <br>
            EtherCAT 连接
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.25 秒<br>
            闪烁一次            
        </td>
        <td style="text-align: center;">
            EtherCAT 连接正常,<br>
            等待初始设置            
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.75 秒<br>
            闪烁一次
        </td>
        <td style="text-align: center;">
            EtherCAT 连接正常,<br>
            初始设置正常
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.1 秒<br>
            闪烁一次
        </td>
        <td style="text-align: center;">
            EtherCAT 状态错误,<br>
            初始化设置正常
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
如果 IO_LED 和 MOD_LED 不闪烁（无论是关闭还是持续保持开启），则表示 MCU 正常运行。
{% endhint %}
[__SOURCE](3-Configuration/README.md)
# 3. 如何配置用户 DIO 和扩展 DIO
[__SOURCE](3-Configuration/1-EtherCAT-Configuration.md)
# 3.1. EtherCAT 配置

EtherCAT 配置步骤如下。

确保在控制器关闭时正确连接 LAN 电缆。

<mark style="color:green;">**- 单个 BD681 配置 ( BD681 + BD682 )**</mark>

![](../_assets/05.BD681_1개_케이블_연결.png)<br>
< Figure 1. 单个 BD681 电缆连接>

如上图所示，将 BD642 的下部 LAN 连接器连接到 BD681 的上部 LAN 连接器，然后打开控制器电源。如果 EtherCAT 正常连接，可以在 TP 上的 "UserDIO List" 中验证，如下所示。

**- 菜单位置: [system] - [12: Option System] - [UserDIO Board Setting]**

![](../_assets/07.BD681_1개_사용자DIO_보드_설정_en.png)<br>
< Figure 2. 单个 BD681 配置><br>

![](../_assets/08.BD681_상태표시_LED_en.png)<br>
< Figure 3. BD681 状态 LED><br>

当连接成功完成时，BD681 板上的状态指示 LED 的操作如下。

- BD681 状态 LED 操作
1. 每2秒闪烁一次（等待 EtherCAT 连接）
2. 每0.25秒闪烁一次（EtherCAT 连接正常，等待初始设置）
3. 每0.75秒闪烁一次（EtherCAT 连接正常，初始设置正常）
<br><br>

<mark style="color:green;">**- 使用 2 个 BD681 单元的配置 ( #1_BD681 + BD682 + #2_BD681 )**</mark>

![](../_assets/09.BD681_2개_케이블_연결.png)<br>
< Figure 4. 使用 2 个 BD681 单元的电缆连接>

如上图所示，将 BD681 #2 插入 BD681 #1 旁边的插槽。

{% hint style="info" %}
对于 #2 BD681，主板开关必须设置为 ON。
{% endhint %}

有关主板开关的详细信息，请参阅手册中的 "[2.2 主板开关](../2-HW/2-Board-Switch.md)" 和 "[3.2 主板开关检查](./2-Board-Switch-check.md)"。

将 BD642 的下部 LAN 连接器连接到 #1 BD681 的上部 LAN 连接器，然后将 #1 BD681 的下部 LAN 连接器连接到 #2 BD681 的上部 LAN 连接器。之后，打开控制器电源。如果 EtherCAT 成功连接，可以在 TP 上进行检查，如下所示。

![](../_assets/11.BD681_2개_사용자DIO_보드_설정_en.png)<br>
< Figure 5. BD681 (2 单元) 配置><br>

当连接成功建立时，BD681 板的状态 LED 操作与 "单个 BD681 配置" 中 "BD681 状态 LED 操作" 描述的方式相同。

<mark style="color:green;">**- 使用 2 个 BD681 单元的配置 ( #1_BD681 + #2_BD681 + BD682 )**</mark>
![](../_assets/09_2.BD681_2个_电缆_连接.png)<br>
< Figure 6. 2个BD681单元的电缆连接>

如上图所示，将BD681 #1插入BD681 #2旁边的插槽中。

{% hint style="info" %}
对于#1 BD681，电路板开关必须设置为开启。
{% endhint %}

![](../_assets/11_2.BD681_2个_用户DIO_板_设置_en.png)<br>
< Figure 7. BD681 (2个单元) 配置><br>

<mark style="color:green;">**- 2个BD681单元的配置 ( #1_BD681 + #2_BD681 )**</mark>

{% hint style="info" %}
要在没有BD682的情况下使用两个BD681板，#1 BD681和#2 BD681的电路板开关必须都设置为开启。
{% endhint %}

![](../_assets/37.BD681_2个_连接(BD682_X)_en.png)<br>
< Figure 8. 没有BD682的BD681 (2个单元) 配置><br>
[__SOURCE](3-Configuration/2-Board-Switch-check.md)
# 3.2. 板开关检查


如果板已经在控制器中组装，则可以在TP屏幕上检查内部开关状态，如下所示。<br>

**- 菜单位置: [system] - [12: Option System] - [UserDIO Board Setting]**

您可以在“UserDIO List”下的“UserDIO Mode”条目中进行检查。

{% hint style="info" %}
为了在[User DIO Board Setting]中正确检查，BD681必须成功连接到EtherCAT。
{% endhint %}


![](../_assets/02.사용자DIO_보드_설정_TP_en.png)<br>
< Figure 1. UserDIO Board Setting TP UI><br>

<br>

< Table 1. User DIO Mode Item>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">
            BD681 开关 <br>
            开/关
        </th>
        <th style="width: 110px; text-align: center;">
            UserDIO 模式
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">关</td>
        <td style="text-align: center;">
            使用 Ext_DIO <br>
            (BD681 + BD682)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">开</td>
        <td style="text-align: center;">
            仅 UserDIO <br>
            (BD681)
        </td>
    </tr>
</tbody>
</table>
<br>

当使用两个用户 DIO 板时，如果两个用户 DIO 板的开关都设置为 OFF，系统将输出错误 <strong>"E55005 : 检测到用户 DIO 板开关设置错误."</strong> <br>
要解决此错误，请将独立用户 DIO 板的开关设置为 ON。

{% hint style="warning" %}
如果出现错误 "E55005 : 检测到用户 DIO 板开关设置错误."，则用户 DIO 板和扩展 DIO 板无法正常使用。在使用它们之前，必须纠正板开关设置。
{% endhint %}

<br>

< Table 2. 支持的用户 DIO 模式组合>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 250px; text-align: center;">
            用户 DIO (BD681) /<br> 扩展 DIO (BD682) 数量
        </th>
        <th style="width: 150px; text-align: center;">
            BD681 开关<br>
            开/关
        </th>
        <th style="width: 110px; text-align: center;">
            可用性
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
            开<br>
            (仅用户 DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
<td style="text-align: center;">
            关闭<br>
            (使用 Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 台<br>
            BD682 : 1 台
        </td>
        <td style="text-align: center;">
            关闭<br>
            (使用 Ext_DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681 : 1 台<br>
            BD682 : 1 台
        </td>
        <td style="text-align: center;">
            打开<br>
            (仅限 UserDIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 台
        </td>
        <td style="text-align: center;">
            #1 BD681 开关打开<br>
            (仅限 UserDIO)<br><br>
            #2 BD681 开关打开<br>
            (仅限 UserDIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 台
        </td>
        <td style="text-align: center;">
            #1 BD681 关<br>
            (使用 Ext_DIO)<br><br>
            #2 BD681 开<br>
            (仅用户 DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 台
        </td>
        <td style="text-align: center;">
            #1 BD681 开<br>
            (仅用户 DIO)<br><br>
            #2 BD681 关<br>
            (使用 Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 台
        </td>
        <td style="text-align: center;">
            #1 BD681 关<br>
            (使用 Ext_DIO)<br><br>
            #2 BD681 关<br>
            (使用 Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
        <td style="text-align: center;">
            BD681 : 2 台<br>
            BD682 : 1 台
        </td>
        <td style="text-align: center;">
            #1 BD681 关<br>
(使用 Ext_DIO)<br><br>
            #2 BD681 开关开启<br>
            (仅限 UserDIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2 个<br>
            BD682 : 1 个
        </td>
        <td style="text-align: center;">
            #1 BD681 开关关闭<br>
            (使用 Ext_DIO)<br><br>
            #2 BD681 开关关闭<br>
            (使用 Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
        <td style="text-align: center;">
            BD681 : 2 个<br>
            BD682 : 1 个
        </td>
        <td style="text-align: center;">
            #1 BD681 开关开启<br>
            (仅限 UserDIO)<br><br>
            #2 BD681 开关关闭<br>
            (使用 Ext_DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2 个<br>
            BD682 : 1 个
        </td>
        <td style="text-align: center;">
            #1 BD681 开关开启<br>
            (仅限 UserDIO)<br><br>
            #2 BD681 开关开启<br>
            (仅限 UserDIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
</tbody>
</table>
<br>
[__SOURCE](3-Configuration/3-FB-Block-Configuration.md)
# 3.3. FB块配置

FB块设置可以在以下菜单中配置。

**- 菜单的位置: [系统] - [2:控制参数] - [2:输入/输出信号设置] - [6:FB块分配]**

![](../_assets/12.FB블럭할당_en.png)<br>
< 图 1. FB块分配菜单><br><br>

选择您想要分配的FB块，并将其配置为“用户DIO”。

![](../_assets/13.fb1_사용자DIO할당_en.png)<br>
< 图 2. 分配给FB1的用户DIO示例><br><br>

有关更多详细信息，请参见“[机器人控制器操作手册 - (FB块分配)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)”。

可以在[6: FB块分配]和[用户DIO板设置]菜单中检查FB块是否已分配给用户DIO。

![](../_assets/14.사용자DIO_FB_미할당_en.png)<br>
< 图 3. 用户DIO FB块未分配><br><br>

![](../_assets/15.사용자DIO_FB3_할당_en.png)<br>
< 图 4. 用户DIO分配给FB3><br>

{% hint style="warning" %}
即使用户DIO已分配给多个FB块，它仅在编号最低的FB块中可用，来自其他已分配FB块的控制信号将被忽略。
{% endhint %}

如下面的图所示，当FB块被分配时，用户DIO控制可以从FB2使用，而在FB5中输入的参数值将被忽略。

![](../_assets/16.사용자DIO_FB_다중할당_en.png)<br>
< 图 5. 用户DIO的多个FB分配示例><br>
[__SOURCE](3-Configuration/4-Internal-PLC-Configuration.md)
# 3.4. 嵌入式 PLC 配置检查

要正确连接使用 FB 块的用户 DIO，有必要检查嵌入式 PLC 设置。

**- 嵌入式 PLC 关闭（未使用）**<br>

嵌入式 PLC 的功能将被关闭。当发生这种情况时，机器人控制器的逻辑输出 FB0.DO0-FB9.DO959 将自动输出为物理输出（即绕过），FB0.Y0-FB9.Y959，物理输入 FB0.X0-FB9.X959 将自动输入为逻辑输入 FB0.DI0-FB9.DI595。<br><br>

**- 嵌入式 PLC 使用中**

由于从嵌入式 PLC 加载的梯形逻辑会影响 FB 块的输入和输出，因此需要谨慎操作。

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
< Figure 1. 梯形逻辑中 FB1 的逻辑/物理 I/O 连接示例><br>

有关嵌入式 PLC 的更多详细信息，请参阅 "[机器人控制器功能手册 - 嵌入式 PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/en/README?cont_model=Hi7)"
[__SOURCE](3-Configuration/5-Sensor-Sync-Configuration.md)
# 3.5. 传感器同步配置

{% hint style="info" %}
如果不使用输送机编码器接口，则无需配置“传感器同步”设置。
{% endhint %}

当使用BD682的输送机编码器接口时，必须进行“传感器同步”设置。

**- 菜单位置: [system] - [4: 应用参数] - [4: 传感器同步]**

![](../_assets/18.센서동기_설정_UI_en.png)<br>
< 图 1. 传感器同步配置 UI><br><br>

要使用输送机编码器接口，请在“参数设置”中将“同步”项设置为“输送机”，并适当配置“输入信号分配”和“输出信号分配”。

![](../_assets/19.동기_상태_컨베이어_설정_en.png)<br>
< 图 2. 设置为输送机><br>

有关“参数设置”的更多详细信息，请参见“[机器人控制器功能手册 - 传感器同步（参数设置）](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/3-user-interface/3-3-sensor-sync-parameter?cont_model=Hi7)”。

<br>
由于BD682的输送机接口与系统I/O相连，因此需要进行输入和输出信号分配。

如下图所示，按下位于UI下方的**[BD640T BD68X]按钮**以输入指定的I/O编号。最后，按下**[v OK]按钮**以应用设置。

![](../_assets/20.채널1_시스템_입출력_설정_en.png)<br>
< 图 3. 通道 1 系统 I/O 配置><br><br>

![](../_assets/21.채널2_시스템_입출력_설정_en.png)<br>
< 图 4. 通道 2 系统 I/O 配置><br><br>

此外，您还可以选择“脉冲计数类型”和“脉冲通信类型”（编码器类型）。有关详细信息，请参阅下表。
<br>

< 表 1. 脉冲计数类型和脉冲通信类型（编码器类型）信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">
            No.
        </th>
        <th style="width: 200px; text-align: center;">
            输出信号分配
        </th>
        <th style="width: 30px; text-align: center;">
            开/关
        </th>
        <th style="width: 250px; text-align: center;">
            注意
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>1</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            脉冲计数类型
        </td>
        <td style="text-align: center;">
            开<br>(1)
        </td>
        <td> 
            上/下计数方法
        </td>
    </tr>        
        <td style="text-align: center;">
            关<br>(0)
        </td>
        <td> 
            上计数方法（默认）
        </td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>2</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            脉冲通信类型<br>
            （编码器类型）
        </td>
        <td style="text-align: center;">
            开<br>(1)
        </td>
        <td> 
            开集电极型编码器
        </td>
    </tr>        
        <td style="text-align: center;">
            关<br>(0)
        </td>
        <td> 
            线路驱动型编码器（默认）
        </td>
    </tr>
</tbody>
</table>
如下面的图所示，您可以通过点击复选框将其设置为开启。<br>
要应用该设置，请务必按下 **[v OK] button**。

![](../_assets/22.출력신호할당_ON_en.png)<br>
< Figure 5. Pulse Count Type ON Applied><br>

{% hint style="info" %}
使用开漏类型编码器时，“脉冲线错误”功能不可用。<br>
因此，您必须将“脉冲线错误”在“输入信号分配”中设置为“-1（未使用）”。
{% endhint %}

{% hint style="warning" %}
使用开漏类型编码器时，如果未将“脉冲线错误”设置为“-1（未使用）”，则在控制器重启时可能会出现错误 E27001（输送带脉冲线异常）。
{% endhint %}

![](../_assets/36.오픈콜렉터_엔코더_펄스라인에러_설정_en.png)<br>
< Figure 6. Open Collector Type Encoder Pulse line error setting><br>

有关详细信息，请参阅"[机器人控制器功能手册 - 传感器同步](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/README?cont_model=Hi7)"中的输送带相关部分。
[__SOURCE](4-Usage/README.md)
# 4. 如何使用用户 DIO 和扩展 DIO
[__SOURCE](4-Usage/1-DIO-Usage.md)
# 4.1. 如何使用 DIO

如果电缆正确连接到 BD681 和 BD682 的连接器，请参考以下指令以控制数字输入和输出。
<br>

<mark style="color:green;">**- 与控制器输入/输出信号的联动**</mark>

有关控制器 I/O 信号与板 I/O 之间联动的详细信息，请参考 "[机器人控制器操作手册 - (输入/输出信号设置)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/README)"。

<br>

<mark style="color:green;">**- 使用 TP 进行板输入/输出控制**</mark>

有关控制板输出和检查来自 TP 的输入的信息，请参考 "[机器人控制器操作手册 - (公共输出)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/4-user-output)" 和 "[机器人控制器操作手册 - (公共输入)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/3-user-input)"。

<br>

{% hint style="info" %}
请注意，受控 I/O 范围取决于 BD681 和 BD682 的组合。
{% endhint %}

![](../_assets/38.DIO_ctrl.png)<br>
< Figure 1. 根据板组合的 I/O 控制范围示例><br>

<br>

<mark style="color:green;">**- 使用作业进行板输入/输出控制**</mark>

有关在作业中链接板输入和输出的信息，请参考 "[机器人控制器功能手册 - 机器人语言 HRScript (FB 对象: 数字 I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/en/6-external-comm/1-fb-io/README?cont_model=Hi7)"。

<br><br>
此外，用户 DIO 提供了一种功能，可以在发生瞬时 EtherCAT 通信错误时配置数字输出状态（例如，由于通信错误而过渡到 Pre-OP 或 Safe-OP 状态）。

**- 菜单位置: [系统] - [12: 选项系统] - [用户 DIO 板设置]**

![](../_assets/23.연결_오류시_디지털_출력_설정_en.png)<br>
< Figure 2. 连接错误时的数字输出设置><br>

<br>

< Table 1. 连接错误时的数字输出设置信息>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            设置值
        </th>
        <th style="width: 370px; text-align: center;">
            注释
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            清除值<br>
            （默认）
        </td>
        <td> 
             - 连接错误时将所有板输出设置为 OFF
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            保持值
        </td>
        <td> 
             - 在连接错误时，将板输出保持在最后一个值
        </td>
    </tr>
</tbody>
</table>

<br>
如果您想更改配置的值，请选择所需的设置并按[v OK]按钮。<br><br>

![](../_assets/24.连接_错误时_数字输出_设置值_更改_en.png)<br>
< Figure 3. 连接错误时数字输出设置的更改><br>
[__SOURCE](4-Usage/2-Conveyor-Usage.md)
# 4.2. 如何使用输送机接口

如果电缆正确连接到 BD682 的连接器，请参考以下说明以控制输送机接口。
<br>

<mark style="color:green;">**- 控制器与输送机接口的集成**</mark>

有关使用电路板集成控制器和输送机接口的详细信息，请参阅 “[机器人控制器功能手册 - 传感器同步](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/en/README?cont_model=Hi7)” 的与输送机相关部分。