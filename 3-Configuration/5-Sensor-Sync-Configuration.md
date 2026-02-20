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