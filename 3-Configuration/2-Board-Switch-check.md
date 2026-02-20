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