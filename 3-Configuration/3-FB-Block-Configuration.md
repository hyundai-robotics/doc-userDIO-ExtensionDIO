# 3.3. FB块配置

FB块设置可以在以下菜单中配置。

**- 菜单的位置: [系统] - [2:控制参数] - [2:输入/输出信号设置] - [6:FB块分配]**

![](../_assets/12.FB블럭할당_en.png)<br>
< 图 1. FB块分配菜单><br><br>

选择您想要分配的FB块，并将其配置为“用户DIO”。

![](../_assets/13.fb1_사용자DIO할당_en.png)<br>
< 图 2. 分配给FB1的用户DIO示例><br><br>

有关更多详细信息，请参见“[机器人控制器操作手册 - (FB块分配)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)”。

可以在[6: FB块分配]和[用户DIO板设置]菜单中检查FB块是否已分配给用户DIO。

![](../_assets/14.사용자DIO_FB_미할당_en.png)<br>
< 图 3. 用户DIO FB块未分配><br><br>

![](../_assets/15.사용자DIO_FB3_할당_en.png)<br>
< 图 4. 用户DIO分配给FB3><br>

{% hint style="warning" %}
即使用户DIO已分配给多个FB块，它仅在编号最低的FB块中可用，来自其他已分配FB块的控制信号将被忽略。
{% endhint %}

如下面的图所示，当FB块被分配时，用户DIO控制可以从FB2使用，而在FB5中输入的参数值将被忽略。

![](../_assets/16.사용자DIO_FB_다중할당_en.png)<br>
< 图 5. 用户DIO的多个FB分配示例><br>