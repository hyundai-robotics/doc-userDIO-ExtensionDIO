# 3.3. FB block Configuration

FB block settings can be configured in the following menu.

**- The location of the menu: [system] - [2:Control parameter] - [2:Input/Output signal setting] - [6:fb block allocation]**

![](../_assets/12.FB블럭할당_en.png)<br>
< Figure 1. FB block allocation menu><br><br>

Select the FB block you want to assign and configure it as "User DIO".

![](../_assets/13.fb1_사용자DIO할당_en.png)<br>
< Figure 2. Example of User DIO Assigned to FB1><br><br>

For more details, refer to "[Robot Controller Operation Manual - (FB Block Allocation)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)".

Whether an FB block has been assigned to the User DIO can be checked in the [6: FB block allocation] and [UserDIO Board Setting] menus.

![](../_assets/14.사용자DIO_FB_미할당_en.png)<br>
< Figure 3. User DIO FB Block Not Assigned><br><br>

![](../_assets/15.사용자DIO_FB3_할당_en.png)<br>
< Figure 4. User DIO Assigned to FB3><br>

{% hint style="warning" %}
Even if the User DIO is assigned to multiple FB blocks, it is only available in the FB block with the lowest number, and the control signals from the other assigned FB blocks will be ignored.
{% endhint %}

As shown in the figure below, when the FB blocks are assigned, User DIO control is available from FB2, while the parameter values entered in FB5 are ignored.

![](../_assets/16.사용자DIO_FB_다중할당_en.png)<br>
< Figure 5. Example of Multiple FB Assignments for User DIO><br>
