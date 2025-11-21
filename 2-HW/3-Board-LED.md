# 2.3. 电路板状态LED

BD681具有可显示电路板状态的LED。<br>
根据LED的工作状态，可确认电路板是否正常工作。

![](../_assets/34.보드_LED.png)<br>
<图1. 电路板状态LED>

<br>

![](../_assets/35.보드_LED_상세.png)<br>
<图2. 电路板状态LED详细>

<br>

<表1. 电路板状态LED详细>

<table>
<thead>
<tr>
<th style="width: 20px; text-align: center;">No.</th>
<th style="width: 80px; text-align: center;">LED颜色</th>
<th style="width: 110px; text-align: center;">LED名称</th>
<th style="width: 160px; text-align: center;">备注</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>1</strong></td>
<td style="text-align: center;">Green</td>
<td style="text-align: center;">IO_LED</td>
<td style="text-align: center;">MCU(CPU 1)状态</td>
</tr>
<tr>
<td style="text-align: center;"><strong>2</strong></td>
<td style="text-align: center;">Green</td>
<td style="text-align: center;">MOD_LED</td>
<td style="text-align: center;">MCU(CM)状态</td>
</tr>
<tr>
<td style="text-align: center;"><strong>3</strong></td>
<td style="text-align: center;">Green</td>
<td style="text-align: center;">EC_LED_RUN</td>
<td style="text-align: center;">EtherCAT工作状态</td>
</tr>
<tr>
<td style="text-align: center;"><strong>4</strong></td>
<td style="text-align: center;">Red</td>
<td style="text-align: center;">EC_LED_ERR</td>
<td style="text-align: center;">EtherCAT错误状态</td>
</tr>
</tbody>
</table>
<br>

<br>

<表2. 根据EtherCAT状态的LED>

<table>
<thead>
<tr>
<th style="width: 110px; text-align: center;">LED名称</th>
<th style="width: 160px; text-align: center;">LED状态</th>
<th style="width: 160px; text-align: center;">EtherCAT状态</th>
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

<表3. 根据MCU工作状态的LED>

<table>
<thead>
<tr>
<th style="width: 110px; text-align: center;">LED名称</th>
<th style="width: 160px; text-align: center;">LED状态</th>
<th style="width: 160px; text-align: center;">MCU工作状态</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="4" style="text-align: center;">
IO_LED,<br>
MOD_LED
</td>
<td style="text-align: center;">以2秒间隔闪烁</td>
<td style="text-align: center;">EtherCAT连接等待中</td>
</tr>
<tr>
<td style="text-align: center;">以0.25秒间隔闪烁</td>
<td style="text-align: center;">
EtherCAT连接OK,<br>
默认设定值等待中
</td>
</tr>
<tr>
<td style="text-align: center;">以0.75秒间隔闪烁</td>
<td style="text-align: center;">
EtherCAT连接OK,<br>
初始设置OK
</td>
</tr>
<tr>
<td style="text-align: center;">以0.1秒间隔闪烁</td>
<td style="text-align: center;">
EtherCAT连接状态异常，<br>
初始设置OK
</td>
</tr>
</tbody>
</table>
<br>

{% hint style="info" %}
如IO_LED、MOD_LED不闪烁而停止（处于关闭或常亮状态），则表示MCU工作不正常。
{% endhint %}
