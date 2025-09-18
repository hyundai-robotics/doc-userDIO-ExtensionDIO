# 2.1. Board Switch Configuration

The board switch positions are as shown in the figure below.<br>

![](../_assets/01.사용자DIO_보드_스위치_위치.png)<br>
< Figure 1. User DIO Board switch positions>
<br>

{% hint style="warning" %}
Always turn off the controller power and verify that the board power is off before removing the board.
{% endhint %}

<br>
You can also check the board switch status on the TP screen as shown below.<br><br>

**- TP Menu : [System] - [옵션장치] - [사용자DIO 보드 설정]**

'사용자DIO 목록' 에서 '사용자DIO 모드' 항목으로 확인할 수 있습니다.

{% hint style="info" %}
[사용자DIO 보드 설정]에서 정상적으로 확인하려면, BD681의 EtherCAT 연결이 정상적으로 되어야 합니다.
{% endhint %}

EtherCAT 연결에 대한 세부 내용은 "[2.2. EtherCAT 설정](./2-EtherCAT-Configuration.md)" 매뉴얼을 참고하시기 바랍니다.

![](../_assets/02.사용자DIO_보드_설정_TP.png)<br>
<그림 2. 사용자DIO 보드 설정 TP UI><br>

<br>

<표 1. 사용자DIO 모드 항목>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 110px; text-align: center;">
            사용자DIO 모드
        </th>
        <th style="width: 30px; text-align: center;">
            스위치 <br>
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">비고</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">
            Use Ext_DIO <br>
            (BD681 + BD682)
        </td>
        <td style="text-align: center;">OFF</td>
        <td> - 확장DIO (BD682) 연동 모드<br>
             - 기본 구성시 (BD681 + BD682) 사용<br>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            Only UserDIO <br>
        </td>
        <td style="text-align: center;">ON</td>
        <td> - 사용자DIO (BD681) 단독 모드 <br>
             - 확장DIO (BD682) 연동 불가<br>
             - 기본 구성에 BD681 추가시 사용<br> 
             - 추가된 2번째 BD681에 적용 필요 <br></td>
    </tr>
</tbody>
</table>
<br><br>

![](../_assets/03.사용자DIO_보드_스위치_ON_OFF.png)<br>
<그림 3. 사용자DIO 보드 스위치 ON/OFF>

사용자 DIO 보드를 2개 사용할 때, 2번째 사용자 DIO 보드 스위치가 OFF 되어있으면 <strong>"E55005 2번째 사용자 DIO 보드 스위치 설정 오류 감지"</strong> 에러를 출력합니다.
해당 에러를 해결하기 위해서는 2번째 사용자 DIO 보드 스위치를 ON으로 변경하여야 합니다.

{% hint style="warning" %}
"E55005 2번째 사용자 DIO 보드 스위치 설정 오류 감지" 에러가 발생하였을 경우, 사용자 DIO 보드와 확장 DIO 보드를 정상적으로 사용할 수 없습니다. 보드의 스위치 설정을 올바르게 변경한 후에 사용해야 합니다.
{% endhint %}

