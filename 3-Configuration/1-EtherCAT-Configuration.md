# 3.1. EtherCAT设置

EtherCAT设置按如下方式进行。

请务必在控制器断电（OFF）的状态下正确连接LAN电缆。

<mark style="color:green;">**<mark style="color:green;">- BD681单板构成（BD681+BD682）</mark>**</mark>

![](../_assets/05.BD681_1개_케이블_연결.png)<br>
<图1. BD681单板的电缆连接>

如上图所示，连接BD642下方的LAN连接器与BD681上方的LAN连接器后，打开控制器电源。正常连接EtherCAT后,可在TP的“用户DIO列表”中查看，如下所示。

*- 菜单位置：[系统]-[选配装置]-[用户DIO板设置]**

![](../_assets/07.BD681_1개_사용자DIO_보드_설정.png)<br>
<图2. BD681单板用户DIO板设置><br>

![](../_assets/08.BD681_상태표시_LED.png)<br>
<图3. BD681状态指示LED><br>

BD681板的状态指示LED在正常连接完成时，将按如下方式工作。

- BD681板状态指示LED工作
1. 以2秒间隔闪烁（EtherCAT连接等待中）
2. 以0.25秒间隔闪烁（EtherCAT连接OK，默认设定值等待中）
3. 以0.75秒间隔闪烁（EtherCAT连接OK，初始设置OK）
<br><br>

<mark style="color:green;">**<mark style="color:green;">- BD681双板构成(#1_BD681+BD682+#2_BD681)</mark>**</mark>

![](../_assets/09.BD681_2개_케이블_연결.png)<br>
<图4. BD681双板电缆连接>

如上图所示，在#1 BD681位置旁插入#2 BD681。

{% hint style="info" %}
# #2 BD681的电路板开关必须为ON。
{% endhint %}

보드 스위치에 대한 세부 내용은 "[关于电路板开关的详细内容，请参考“2.2 电路板开关”及“3.2 电路板开关确认”说明书。](../2-HW/2-Board-Switch.md)" 및 "[关于电路板开关的详细内容，请参考“2.2 电路板开关”及“3.2 电路板开关确认”说明书。](./2-Board-Switch-check.md)" 매뉴얼을 참고하시기 바랍니다.

连接BD642下方的LAN连接器与#1 BD681上方的LAN连接器后，将#1 BD681下方的LAN连接器与#2 BD681上方的LAN连接器相连。然后，打开控制器电源。正常连接EtherCAT后，可在TP中查看，如下所示。

![](../_assets/11.BD681_2개_사용자DIO_보드_설정.png)<br>
<图5. BD681双板用户DIO板设置><br>

BD681板的状态指示LED在正常连接时，其工作方式与“BD681单板构成”的“BD681板状态指示LED工作”相同。


