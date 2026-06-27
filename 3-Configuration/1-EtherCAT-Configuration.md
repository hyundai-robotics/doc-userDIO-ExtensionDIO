# 3.1. EtherCAT 配置

EtherCAT 配置如下进行。

确保在控制器关闭的情况下正确连接 LAN 电缆。

<mark style="color:green;">**- 单个 BD681 配置 ( BD681 + BD682 )**</mark>

![](../_assets/05.BD681_1개_케이블_연결.png)<br>
< Figure 1. 单个 BD681 电缆连接>

如上图所示，将 BD642 的下 LAN 连接器连接到 BD681 的上 LAN 连接器，然后打开控制器电源。如果 EtherCAT 正常连接，可以在 TP 的 "UserDIO List" 中进行验证，如下所示。

**- 菜单位置：[system] - [12: Option System] - [UserDIO Board Setting]**

![](../_assets/07.BD681_1개_사용자DIO_보드_설정_en.png)<br>
< Figure 2. 单个 BD681 配置><br>

![](../_assets/08.BD681_상태표시_LED_en.png)<br>
< Figure 3. BD681 状态 LED><br>

当连接成功完成时，BD681 板上的状态指示 LED 的操作如下。

- BD681 状态 LED 操作
1. 以 2 秒间隔闪烁（等待 EtherCAT 连接）
2. 以 0.25 秒间隔闪烁（EtherCAT 连接正常，等待初始设置）
3. 以 0.75 秒间隔闪烁（EtherCAT 连接正常，初始设置正常）
<br><br>

<mark style="color:green;">**- 使用 2 个 BD681 单元的配置 ( #1_BD681 + BD682 + #2_BD681 )**</mark>

![](../_assets/09.BD681_2개_케이블_연결.png)<br>
< Figure 4. 使用 2 个 BD681 单元的电缆连接>

如上图所示，将 BD681 #2 插入 BD681 #1 旁边的插槽。

{% hint style="info" %}
对于 #2 BD681，电路板开关必须设置为 ON。
{% endhint %}

有关电路板开关的详细信息，请参阅手册中的 "[2.2 Board Switch](../2-HW/2-Board-Switch.md)" 和 "[3.2 Board Switch Check](./2-Board-Switch-check.md)"。

将 BD642 的下 LAN 连接器连接到 #1 BD681 的上 LAN 连接器，然后将 #1 BD681 的下 LAN 连接器连接到 #2 BD681 的上 LAN 连接器。之后，打开控制器电源。如果 EtherCAT 成功连接，可以在 TP 上检查，如下所示。

![](../_assets/11.BD681_2개_사용자DIO_보드_설정_en.png)<br>
< Figure 5. BD681 (2 个单元) 配置><br>

当连接成功建立时，BD681 板的状态 LED 操作与 "单个 BD681 配置" 中 "BD681 状态 LED 操作" 描述的相同。

<mark style="color:green;">**- 使用 2 个 BD681 单元的配置 ( #1_BD681 + #2_BD681 + BD682 )**</mark>

![](../_assets/09_2.BD681_2개_케이블_연결.png)<br>
< Figure 6. 使用 2 个 BD681 单元的电缆连接>

如上图所示，将 BD681 #1 插入 BD681 #2 旁边的插槽。

{% hint style="info" %}
对于 #1 BD681，电路板开关必须设置为 ON。
{% endhint %}

![](../_assets/11_2.BD681_2개_사용자DIO_보드_설정_en.png)<br>
< Figure 7. BD681 (2 个单元) 配置><br>

<mark style="color:green;">**- 使用 2 个 BD681 单元的配置 ( #1_BD681 + #2_BD681 )**</mark>

{% hint style="info" %}
要在没有 BD682 的情况下使用两个 BD681 板，#1 BD681 和 #2 BD681 板的开关必须都设置为 ON。
{% endhint %}

![](../_assets/37.BD681_2개_연결(BD682_X)_en.png)<br>
< Figure 8. 没有 BD682 的 BD681 (2 个单元) 配置><br>