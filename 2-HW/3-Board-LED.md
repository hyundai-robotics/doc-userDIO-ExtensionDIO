# 2.3. 板状态 LED

BD681 配备了一个 LED，指示板状态。<br>
通过检查 LED 的操作状态，您可以验证板是否正常工作。

![](../_assets/34.보드_LED.png)<br>
< Figure 1. 板状态 LED>

<br>

![](../_assets/35.보드_LED_상세.png)<br>
< Figure 2. 板状态 LED 详细信息>

<br>

< Table 1. 板状态 LED 详细信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
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

< Table 2. LED 根据 EtherCAT 状态的指示>

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

< Table 3. LED 根据 MCU 操作状态的指示>

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
            每 2 秒闪烁一次
        </td>
        <td style="text-align: center;">
            正在等待 <br>
            EtherCAT 连接
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.25 秒闪烁一次            
        </td>
        <td style="text-align: center;">
            EtherCAT 连接正常,<br>
            正在等待初始设置            
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.75 秒闪烁一次
        </td>
        <td style="text-align: center;">
            EtherCAT 连接正常,<br>
            初始设置正常
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            每 0.1 秒闪烁一次
        </td>
        <td style="text-align: center;">
            EtherCAT 状态错误,<br>
            初始设置正常
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
如果 IO_LED 和 MOD_LED 不闪烁（无论是关闭还是持续开启），则表示 MCU 运作不正常。
{% endhint %}