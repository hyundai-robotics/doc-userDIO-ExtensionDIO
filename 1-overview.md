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