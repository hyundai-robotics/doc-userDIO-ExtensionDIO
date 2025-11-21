# 1. 概要

在Hi7控制器中，可通过“用户DIO板（BD681）”和“扩展DIO板（BD682）”进行数字输入/输出信号及输送带接口。

{% hint style="info" %}
在说明书中，DIO表示数字输入与输出（Digital Input and Output）。
{% endhint %}

“扩展DIO板（BD682）”不能单独使用，需与“用户DIO板（BD681）”配合使用。

<br>

<表1. 电路板规格>

<table>
<thead>
<tr>
<th style="width: 50px; text-align: center;">
No.
</th>
<th style="width: 110px; text-align: center;">
电路板名称<br>
（电路板标识符）
</th>
<th style="width: 300px; text-align: center;">
电路板功能信息
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;">
<strong>1</strong>
</td>
<td style="text-align: center;">
用户DIO板<br>
( BD681 )
</td>
<td>
- 数字输入16通道 <br>
- 数字输入16通道
</td>
</tr>
<tr>
<td style="text-align: center;">
<strong>2</strong>
</td>
<td style="text-align: center;">
扩展DIO板<br>
( BD682 )
</td>
<td>
- 数字输入16通道 <br>
- 数字输出16通道（含继电器输出8通道）<br>
- 输送带接口2通道 <br>
- 不可单独使用（需与BD681配合使用）
</td>
</tr>
</tbody>
</table>

<br>
可通过2个BD681和1个BD682来实现最多48通道的输入/输出控制。
<br><br>

要正常使用用户DIO及扩展DIO，就需要对以下项目进行设置及确认。<br>

1. 以太网通信连接<br>
2. 电路板开关确认<br>
3. FB块设置<br>
4. 内置PLC使用与否确认<br>
5. 传感器同步设置<br>

