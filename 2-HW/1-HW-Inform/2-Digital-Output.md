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