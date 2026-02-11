# 4.1. DIO 사용 방법

BD681, BD682 의 커넥터에 올바르게 케이블을 연결하였다면, 디지털 입출력을 제어하기 위한 방법은 아래 내용들을 참고하시기 바랍니다.
<br>

<mark style="color:green;">**- 제어기의 입출력 신호와 연동**</mark>

제어기의 입출력 신호와 보드의 입출력 연동에 대한 부분은 "[로봇제어기 조작설명서 - (입출력 신호 설정)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-hi6a-tp630/7-system/3-control-parameter/2-io-signal-setting/README)" 을 참고하시기 바랍니다.

<br>

<mark style="color:green;">**- TP를 이용한 보드 입력, 출력 제어**</mark>

TP에서 보드 출력을 제어하고 입력을 확인하는 부분은 "[로봇제어기 조작설명서 - (범용 출력)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-hi6a-tp630/6-monitoring/2-io/4-user-output)", "[로봇제어기 조작설명서 - (범용 입력)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-hi6a-tp630/6-monitoring/2-io/3-user-input)" 을 참고하시기 바랍니다. 

<br>

{% hint style="info" %}
BD681, BD682 조합에 따라 제어되는 IO 범위가 다르니 주의하시기 바랍니다.
{% endhint %}

![](../_assets/38.DIO_ctrl.png)<br>
<그림 1. 조합에 따른 IO 제어 범위 예시><br>

<br>

<mark style="color:green;">**- Job을 이용한 보드 입력, 출력 제어**</mark>

Job에서 보드 입력, 출력을 연동하는 부분은 "[로봇제어기 기능설명서 - 로봇언어 HRScript (fb객체 : 디지털 I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/ko/6-external-comm/1-fb-io/README?cont_model=Hi7)" 을 참고하시기 바랍니다.

<br><br>
추가적으로 사용자 DIO 에는 EtherCAT 통신 연결이 순간적으로 오류가 발생했을 경우 (예시: EtherCAT 통신 끊어짐 등으로 인한 Pre-OP, Safe-OP 상태) 디지털 출력 상태를 설정하는 기능이 있습니다.

**- 메뉴 위치 : [시스템] - [옵션장치] - [사용자DIO 보드 설정]**

![](../_assets/23.연결_오류시_디지털_출력_설정.png)<br>
<그림 2. 연결 오류시 디지털 출력 설정><br>

<br>

<표 1. 연결 오류시 디지털 출력 설정 정보>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            설정값
        </th>
        <th style="width: 370px; text-align: center;">
            비고
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            값 초기화<br>
            (초기 설정값)
        </td>
        <td> 
             - 연결 오류 발생시, 보드 출력값을 전부 OFF 로 변경
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            값 유지
        </td>
        <td> 
             - 연결 오류 발생시, 보드 출력값을 바로 직전 값으로 유지
        </td>
    </tr>
</tbody>
</table>

<br>
설정값을 변경하려면 원하는 설정값을 선택하고 [v확인] 버튼을 누르면 됩니다.<br><br>

![](../_assets/24.연결_오류시_디지털_출력_설정값_변경.png)<br>
<그림 3. 연결 오류시 디지털 출력 설정값 변경><br>

