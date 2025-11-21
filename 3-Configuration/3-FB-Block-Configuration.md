# 3.3. FB块设置

FB块设置可在以下菜单中进行。

*- 菜单位置：[系统]-[2:控制参数]-[2:输入输出信号设置]-[6:fb块分配]**

![](../_assets/12.FB블럭할당.png)<br>
<图1. FB块分配菜单><br><br>

选择所要分配的fb块后，进行"用户DIO"设置即可。

![](../_assets/13.fb1_사용자DIO할당.png)<br>
<图2. fb1分配用户DIO示例><br><br>

자세한 사항은 "[详细内容请参考“机器人控制器操作说明书-(FB块分配)”。](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)" 을 참고하시기 바랍니다.

对于是否为用户DIO分配了FB块，可在[6:fb块分配]及[用户DIO板设置]菜单中进行确认。

![](../_assets/14.사용자DIO_FB_미할당.png)<br>
<图3. 用户DIO FB块未分配><br><br>

![](../_assets/15.사용자DIO_FB3_할당.png)<br>
<图4. 用户DIO fb3分配><br>

{% hint style="warning" %}
即使将用户DIO分配给多个FB块，<strong>也只能在编号最低的FB块中使用，其余已分配的FB块将被忽略控制</strong>。
{% endhint %}

按下图所示分配FB块时，可在fb2中控制用户DIO，而fb5中输入的值将被忽略。

![](../_assets/16.사용자DIO_FB_다중할당.png)<br>
<图5. 用户DIO fb多重分配示例><br>
