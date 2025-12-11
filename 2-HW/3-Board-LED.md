# 2.3. 보드 상태 LED

BD681 에는 보드 상태를 알 수 있는 LED가 있습니다.<br>
LED의 동작 상태에 따라서 보드의 정상 동작 유무를 확인할 수 있습니다.

![](../_assets/34.보드_LED.png)<br>
<그림 1. 보드 상태 LED>

<br>

![](../_assets/35.보드_LED_상세.png)<br>
<그림 2. 보드 상태 LED 상세>

<br>

<표 1. 보드 상태 LED 상세>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 80px; text-align: center;">LED 색상</th>
        <th style="width: 110px; text-align: center;">LED 이름</th>
        <th style="width: 160px; text-align: center;">비고</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">IO_LED</td>
        <td style="text-align: center;">MCU (CPU 1) 상태</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">MOD_LED</td>
        <td style="text-align: center;">MCU (CM) 상태</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">Green</td>
        <td style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">EtherCAT 동작 상태</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">Red</td>
        <td style="text-align: center;">EC_LED_ERR</td>
        <td style="text-align: center;">EtherCAT 에러 상태</td>
    </tr>
</tbody>
</table>
<br>

<br>

<표 2. EtherCAT 상태에 따른 LED>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED 이름</th>
        <th style="width: 160px; text-align: center;">LED 상태</th>
        <th style="width: 160px; text-align: center;">EtherCAT 상태</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">EC_LED_RUN</td>
        <td style="text-align: center;">OFF</td>
        <td style="text-align: center;">INIT</td>
    </tr>
    <tr>
        <td style="text-align: center;">Flashing</td>
        <td style="text-align: center;">Pre-OP</td>
    </tr>
    <tr>
        <td style="text-align: center;">Single Flashing</td>
        <td style="text-align: center;">Safe-OP</td>
    </tr>
    <tr>
        <td style="text-align: center;">ON</td>
        <td style="text-align: center;">OP</td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">EC_LED_ERR</td>
        <td style="text-align: center;">OFF</td>
        <td style="text-align: center;">No Error</td>
    </tr>
    <tr>
        <td style="text-align: center;">Flashing</td>
        <td style="text-align: center;">Error</td>
    </tr>
</tbody>
</table>
<br>

<br>

<표 3. MCU 동작 상태에 따른 LED>

<table>
<thead>
    <tr>
        <th style="width: 110px; text-align: center;">LED 이름</th>
        <th style="width: 160px; text-align: center;">LED 상태</th>
        <th style="width: 160px; text-align: center;">MCU 동작 상태</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="4" style="text-align: center;">
            IO_LED,<br>
            MOD_LED
        </td>
        <td style="text-align: center;">2초 간격으로 점멸</td>
        <td style="text-align: center;">EtherCAT 연결 대기중</td>
    </tr>
    <tr>
        <td style="text-align: center;">0.25초 간격으로 점멸</td>
        <td style="text-align: center;">
            EtherCAT 연결 OK,<br>
            초기 설정값 대기중
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">0.75초 간격으로 점멸</td>
        <td style="text-align: center;">
            EtherCAT 연결 OK,<br>
            초기 설정 OK
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">0.1초 간격으로 점멸</td>
        <td style="text-align: center;">
            EtherCAT 연결 상태 이상,<br>
            초기 설정 OK
        </td>
    </tr>
</tbody>
</table>
<br>

{% hint style="info" %}
IO_LED, MOD_LED가 점멸하지 않고 멈춰있으면(꺼져 있거나 계속 켜져 있는 경우) MCU 동작이 정상적이지 않은 상태입니다.
{% endhint %}
