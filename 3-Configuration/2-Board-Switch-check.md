# 3.2. 电路板开关确认


如电路板已组装至控制器，可在如下TP画面中确认内部开关状态。<br>

*- 菜单位置：[系统]-[选配装置]-[用户DIO板设置]**

可在“用户DIO列表”的“用户DIO模式”项目中进行确认。

{% hint style="info" %}
要在[用户DIO板设置]中正常确认，BD681的EtherCAT连接必须正常。
{% endhint %}


![](../_assets/02.사용자DIO_보드_설정_TP.png)<br>
<图1. 用户DIO板设置TP UI><br>

<br>

<表1. 用户DIO模式项目>

<table>
<thead>
<tr>
<th style="width: 20px; text-align: center;">No.</th>
<th style="width: 100px; text-align: center;">
BD681开关 <br>
ON/OFF
</th>
<th style="width: 110px; text-align: center;">
用户DIO模式
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


使用2个用户DIO板时，若第2个用户DIO板开关为OFF，则输出<strong>“E55005 检测到第2个用户DIO板开关设置错误”</strong>错误。
要解决该错误，就必须将第2个用户DIO板开关更改为ON。

{% hint style="warning" %}
当发生“E55005 检测到第2个用户DIO板开关设置错误”的错误时，则无法正常使用用户DIO板及扩展DIO板。必须正确更改电路板的开关设置后方可使用。
{% endhint %}

<br>

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
ON<br>
(Only UserDIO)
</td>
<td style="text-align: center;">O（可使用）</td>
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
<td style="text-align: center;">X（不可使用）</td>
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
<td style="text-align: center;">O（可使用）</td>
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
(Use Ext_DIO)<br><br>
#2 BD681开关ON<br>
(Only UserDIO)
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
#1 BD681开关OFF<br>
(Use Ext_DIO)<br><br>
#2 BD681开关OFF<br>
(Use Ext_DIO)
</td>
<td style="text-align: center;">X（不可使用）</td>
</tr>
<tr>
<td style="text-align: center;"><strong>7</strong></td>
<td style="text-align: center;">
BD681 : 2 EA<br>
BD682 : 1 EA
</td>
<td style="text-align: center;">
#1 BD681开关ON<br>
(Only UserDIO)<br><br>
#2 BD681开关OFF<br>
(Use Ext_DIO)
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
(Only UserDIO)<br><br>
#2 BD681开关ON<br>
(Only UserDIO)
</td>
<td style="text-align: center;">X（不可使用）</td>
</tr>
</tbody>
</table>
<br>
