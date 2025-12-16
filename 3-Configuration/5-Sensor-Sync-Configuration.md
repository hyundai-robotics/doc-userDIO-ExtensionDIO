# 3.5. 传感器同步设置

{% hint style="info" %}
当不使用输送带编码器接口时，则无需进行“传感器同步”设置。
{% endhint %}

当使用BD682的输送带编码器接口时，则需要进行“传感器同步”设置。

**- 菜单位置：[系统] - [4: 应用参数] - [4: 传感器同步]**

![](../_assets/18.센서동기_설정_UI.png)<br>
<图1. 传感器同步设置UI><br><br>

要正常使用输送带编码器接口，就必须将“参数设置”的“同步状态”项目设置为“输送带”，并正常设置“输入信号分配”、“输出信号分配”。


![](../_assets/19.동기_상태_컨베이어_설정.png)<br>
<图2. 将同步状态设置为输送带><br>

关于“参数设置”的详细信息，请参考“[机器人控制器功能说明书 - 传感器同步 (传感器同步参数)](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/3-user-interface/3-3-sensor-sync-parameter)”。

<br>
BD682的输送带编码器接口与系统输入输出联动，因此需要进行输入输出信号分配。

如下图所示，按下UI下方的 **[BD640T BD68X] 按钮**，即可输入指定的输入输出编号。最后按下 **[v确认] 按钮**即可应用设置。

![](../_assets/20.채널1_시스템_입출력_설정.png)<br>
<图3. 通道1系统输入输出设置><br><br>

![](../_assets/21.채널2_시스템_입출력_설정.png)<br>
<图4. 通道2系统输入输出设置><br><br>

此外，可选择脉冲计数器类型、脉冲通信方式（编码器种类）。请参考下表内容。
<br>

<表1. 脉冲计数器类型、脉冲通信方式（编码器种类）信息>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            输出信号分配
        </th>
        <th style="width: 30px; text-align: center;">
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">
            备注
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>1</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            脉冲计数器类型
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            Up/Down计数器方式
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Up计数器方式（默认值）
        </td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>2</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            脉冲通信方式<br>
            （编码器类型）
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            开路集电极型编码器
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            线路驱动型编码器（默认值）
        </td>
    </tr>
</tbody>
</table>

<br>

如下图所示，点击复选框即可输入为ON。<br>
要应用设置，就必须按下**[v确认]按钮**。

![](../_assets/22.출력신호할당_ON.png)<br>
<图5. 应用脉冲计数器类型ON><br>

详细内容请参考“[机器人控制器功能说明书-传感器同步](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/README)”中与输送带相关的部分。
