# 3.2. 板开关检查


如果电路板已经安装在控制器中，可以在TP屏幕上检查内部开关状态，如下所示。<br>

**- 菜单位置：[system] - [12: Option System] - [UserDIO Board Setting]**

您可以在“UserDIO模式”条目下的“UserDIO列表”中检查。

{% hint style="info" %}
为了正确检查[User DIO Board Setting]，必须成功将BD681连接到EtherCAT。
{% endhint %}


![](../_assets/02.사용자DIO_보드_설정_TP_en.png)<br>
< Figure 1. UserDIO板设置TP UI><br>

<br>

< Table 1. 用户DIO模式项目>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">
            BD681开关 <br>
            开/关
        </th>
        <th style="width: 110px; text-align: center;">
            用户DIO模式
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">关</td>
        <td style="text-align: center;">
            使用Ext_DIO <br>
            (BD681 + BD682)
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">开</td>
        <td style="text-align: center;">
            仅用户DIO <br>
            (BD681)
        </td>
    </tr>
</tbody>
</table>
<br>


使用两个用户DIO板时，如果两个用户DIO板开关都设置为关，系统将输出错误<strong>"E55005 : 检测到用户DIO板模式设置错误."</strong> <br>
要解决此错误，请将独立用户DIO板的开关设置为开。

{% hint style="warning" %}
如果发生错误"E55005 : 检测到用户DIO板模式设置错误."，则用户DIO板和扩展DIO板无法正常使用。您必须在使用之前纠正板开关设置。
{% endhint %}

{% hint style="info" %}
如果BD681 SW版本为1.3.0或更高，则无需单独设置开关。
{% endhint %}

<br>

< Table 2. 支持的用户DIO模式组合>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 250px; text-align: center;">
            用户DIO (BD681) /<br> 扩展DIO (BD682) 数量
        </th>
        <th style="width: 150px; text-align: center;">
            BD681开关<br>
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
            BD681 : 1台
        </td>
        <td style="text-align: center;">
            开<br>
            (仅用户DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1台
        </td>
        <td style="text-align: center;">
            关<br>
            (使用Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            关<br>
            (使用Ext_DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681 : 1台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            开<br>
            (仅用户DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2台
        </td>
        <td style="text-align: center;">
            #1 BD681开关开<br>
            (仅用户DIO)<br><br>
            #2 BD681开关开<br>
            (仅用户DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2台
        </td>
        <td style="text-align: center;">
            #1 BD681开关关<br>
            (使用Ext_DIO)<br><br>
            #2 BD681开关开<br>
            (仅用户DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2台
        </td>
        <td style="text-align: center;">
            #1 BD681开关开<br>
            (仅用户DIO)<br><br>
            #2 BD681开关关<br>
            (使用Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2台
        </td>
        <td style="text-align: center;">
            #1 BD681开关关<br>
            (使用Ext_DIO)<br><br>
            #2 BD681开关关<br>
            (使用Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
        <td style="text-align: center;">
            BD681 : 2台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            #1 BD681开关关<br>
            (使用Ext_DIO)<br><br>
            #2 BD681开关开<br>
            (仅用户DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            #1 BD681开关关<br>
            (使用Ext_DIO)<br><br>
            #2 BD681开关关<br>
            (使用Ext_DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
        <td style="text-align: center;">
            BD681 : 2台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            #1 BD681开关开<br>
            (仅用户DIO)<br><br>
            #2 BD681开关关<br>
            (使用Ext_DIO)
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2台<br>
            BD682 : 1台
        </td>
        <td style="text-align: center;">
            #1 BD681开关开<br>
            (仅用户DIO)<br><br>
            #2 BD681开关开<br>
            (仅用户DIO)
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
</tbody>
</table>
<br>