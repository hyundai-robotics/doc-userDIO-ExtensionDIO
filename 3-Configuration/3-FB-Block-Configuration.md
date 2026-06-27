# 3.3. FB块配置

FB块设置可以在以下菜单中配置。

**- 菜单位置: [system] - [2:Control parameter] - [2:Input/Output signal setting] - [6:fb block allocation]**

![](../_assets/12.FB블럭할당_en.png)<br>
< Figure 1. FB块分配菜单><br><br>

选择要分配的FB块，并将其配置为“用户DIO”。

![](../_assets/13.fb1_사용자DIO할당_en.png)<br>
< Figure 2. 分配给FB1的用户DIO示例><br><br>

有关更多详细信息，请参阅"[Robot Controller Operation Manual - (FB Block Allocation)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/zh-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign?cont_model=Hi7)"。

用户DIO是否已被分配FB块，可以在[6: FB块分配]和[用户DIO板设置]菜单中检查。

![](../_assets/14.사용자DIO_FB_미할당_en.png)<br>
< Figure 3. 用户DIO FB块未分配><br><br>

![](../_assets/15.사용자DIO_FB3_할당_en.png)<br>
< Figure 4. 用户DIO分配给FB3><br>

{% hint style="warning" %}
即使用户DIO被分配给多个FB块，它仅在编号最低的FB块中可用，并且来自其他分配FB块的控制信号将被忽略。
{% endhint %}

如下图所示，当FB块被分配时，用户DIO控制可以从FB2获取，而在FB5中输入的参数值将被忽略。

![](../_assets/16.사용자DIO_FB_다중할당_en.png)<br>
< Figure 5. 用户DIO的多个FB分配示例><br>