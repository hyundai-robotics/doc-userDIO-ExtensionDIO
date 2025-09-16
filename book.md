# Hi6a 로봇제어기 기능설명서 - 사용자DIO, 확장DIO

{% hint style="warning" %}
본 제품 설명서에서 제공되는 정보는 현대로보틱스의 자산입니다.

현대로보틱스의 서면에 의한 동의 없이 전부 또는 일부를 무단 전재 및 재배포할 수 없으며, 제3자에게 제공되거나 다른 목적에 사용할 수 없습니다.



본 설명서는 사전 예고 없이 변경될 수 있습니다.



**Copyright ⓒ 2025 by Hyundai Robotics**
{% endhint %}

# 1. 개요

Hi6a 제어기에서 '사용자 DIO 보드(BD681)'와 '확장 DIO 보드(BD682)'를 활용하여 범용 입출력 신호와 컨베이어 엔코더 동기를 진행할 수 있습니다.

{% hint style="info" %}
매뉴얼에서 DIO는 디지털 입출력(Digital Input and Output)을 의미합니다.
{% endhint %}

'확장 DIO 보드(BD682)'는 단독으로는 사용할 수 없으며 '사용자 DIO 보드(BD681)'와 같이 사용해야 합니다.

<br>

<표 1. 보드 사양>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            보드명<br>
            (보드 식별자)
        </th>
        <th style="width: 300px; text-align: center;">
            보드 기능 정보
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            사용자 DIO 보드<br>
            ( BD681 )
        </td>
        <td> 
             - 범용 입력 16 채널 <br>
             - 범용 출력 16 채널 <br>
             - 단독 사용 가능
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            확장 DIO 보드<br>
            ( BD682 )
        </td>
        <td> 
             - 범용 입력 16 채널 <br>
             - 범용 출력 16 채널 <br> 
             - 컨베이어 엔코더 2채널 <br> 
             - 단독 사용 불가 (BD681과 같이 사용 필요)
        </td>
    </tr>
</tbody>
</table>

<br>
BD681 2개와 BD682 1개를 이용하여 최대 48 채널의 입출력을 제어할 수 있습니다.
<br><br>

사용자 DIO 및 확장 DIO 를 정상적으로 사용하기 위해서는 아래 항목들에 대한 설정 및 확인이 필요합니다.<br>

1. 보드 스위치 확인<br>
2. 이더캣 통신 연결<br>
3. FB 블록 설정<br>
4. 내장 PLC 사용 여부 확인<br>
5. 센서 동기 설정<br>

# 2. 사용자 DIO, 확장 DIO 설정 방법
# 2.1. 보드 스위치 확인

보드 스위치 위치는 아래 사진과 같습니다.<br>

![](../_assets/01.사용자DIO_보드_스위치_위치.png)<br>
<그림 1. 사용자DIO 보드 스위치 위치>
<br>

{% hint style="warning" %}
보드를 분리할때는 반드시 제어기 전원을 <strong>OFF</strong> 하고 보드 전원이 <strong>OFF</strong> 되었는지 확인 후 분리하시기 바랍니다.
{% endhint %}

<br>
아래와 같은 TP화면에서도 내부 스위치 상태를 확인할 수 있습니다.<br><br>

**- 메뉴 위치 : [시스템] - [옵션장치] - [사용자DIO 보드 설정]**

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

# 2.2. EtherCAT 설정

EtherCAT 설정은 다음과 같이 진행합니다.

제어기를 **OFF** 한 상태에서 LAN 케이블을 올바르게 연결해야 합니다.

<mark style="color:green;">**- BD681 1개 구성 ( BD681 + BD682 )**</mark>

![](../_assets/05.BD681_1개_케이블_연결.png)<br>
<그림 1. BD681 1개 케이블 연결>

위의 그림과 같이 BD642의 아래쪽 랜커넥터와 BD681 위쪽 랜커넥터를 연결한 후 제어기 전원을 **ON** 합니다. 정상적으로 EtherCAT이 연결되면 아래와 같이 TP에서 '사용자DIO 목록'으로 확인 가능합니다.

**- 메뉴 위치: [시스템] - [옵션 장치] - [사용자 DIO 보드 설정]**

![](../_assets/07.BD681_1개_사용자DIO_보드_설정.png)<br>
<그림 2. BD681 1개 사용자DIO 보드 설정><br>

![](../_assets/08.BD681_상태표시_LED.png)<br>
<그림 3. BD681 상태표시 LED><br>

BD681 보드의 상태표시 LED는 정상적으로 연결이 완료 될 경우, 아래와 같이 동작합니다.  

- BD681 보드 상태표시 LED 동작
1. 2초 점등 (EtherCAT 연결 대기중)
2. 0.25초 점등 (EtherCAT 연결 Ok, 초기 설정값 대기중)
3. 0.75초 점등 (EtherCAT 연결 Ok, 초기 설정 Ok)
<br><br>

<mark style="color:green;">**- BD681 2개 구성 ( #1_BD681 + BD682 + #2_BD681 )**</mark>

![](../_assets/09.BD681_2개_케이블_연결.png)<br>
<그림 4. BD681 2개 케이블 연결>

위의 그림과 같이 #1 BD681 자리 옆에 #2 BD681을 꽂아 넣습니다.

{% hint style="info" %}
#2 BD681은 보드 스위치가 <strong>ON</strong> 되어야 합니다.
{% endhint %}

보드 스위치에 대한 세부 내용은 "[2.1 보드 스위치 확인](./1-Board-Switch-Configuration.md)" 매뉴얼을 참고하시기 바랍니다.

BD642의 아래쪽 랜커넥터와 #1 BD681 위쪽 랜커넥터를 연결한 후, #1 BD681 아래쪽 랜커넥터와 #2 BD681 위쪽 랜커넥터를 연결합니다. 그리고 제어기 전원을 **ON** 합니다. 정상적으로 EtherCAT이 연결되면 아래와 같이 TP에서 확인 가능합니다.

![](../_assets/11.BD681_2개_사용자DIO_보드_설정.png)<br>
<그림 5. BD681 2개 사용자DIO 보드 설정><br>

BD681 보드의 상태표시 LED는 정상적으로 연결 될 경우, 'BD681 1개 구성'의 'BD681 보드 상태표시 LED 동작' 과 동일하게 동작합니다.


# 2.3. FB 블럭 설정

FB 블럭 설정은 다음 메뉴에서 진행할 수 있습니다.

**- 메뉴 위치: [시스템] - [2:제어 파라미터] - [2:입출력 신호 설정] - [6:fb블럭 할당]**

![](../_assets/12.FB블럭할당.png)<br>
<그림 1. FB 블럭 할당 메뉴><br><br>

할당하고 싶은 fb 블럭을 선택하여 '사용자 DIO'로 설정을 진행하면 됩니다.

![](../_assets/13.fb1_사용자DIO할당.png)<br>
<그림 2. fb1에 사용자DIO 할당 예시><br><br>

자세한 사항은 "[로봇제어기 조작설명서 - (FB 블록 할당)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)" 을 참고하시기 바랍니다.

사용자 DIO에 대한 FB블럭이 할당 되었는지는 [6:fb블럭 할당] 및 [사용자DIO 보드 설정] 메뉴에서 확인 가능합니다.

![](../_assets/14.사용자DIO_FB_미할당.png)<br>
<그림 3. 사용자DIO FB블록 미할당><br><br>

![](../_assets/15.사용자DIO_FB3_할당.png)<br>
<그림 4. 사용자DIO fb3 할당><br>

{% hint style="warning" %}
사용자DIO를 여러 FB블럭에 할당하여도 <strong>가장 번호가 낮은 FB블럭에서 사용 가능하며, 나머지 할당된 FB블럭은 제어가 무시</strong> 됩니다.
{% endhint %}

아래 그림과 같이 FB블럭이 할당 되었을 경우, fb2에서 사용자 DIO 제어가 가능하며, fb5에 입력된 값은 무시됩니다.

![](../_assets/16.사용자DIO_FB_다중할당.png)<br>
<그림 5. 사용자DIO fb 다중 할당 예시><br>
# 2.4. 내장 PLC 설정 확인

FB블럭을 사용하여 정상적으로 사용자 DIO를 연동하기 위해서는 내장 PLC 설정 확인이 필요합니다.

**- 내장 PLC off (미사용)**<br>

로봇제어기의 논리적 출력(Logical Output)인 FB0.DO0~FB9.DO959이 물리적 출력(Physical Output)인 FB0.Y0~FB9.Y959로 자동 출력(bypass)되고, 물리적 입력인 FB0.X0~FB9.X959가 논리적 입력인 FB0.DI0~FB9.DI595로 자동 입력되어 사용자 DIO를 정상적으로 사용가능 합니다.<br><br>

**- 내장 PLC 사용**

내장 PLC에서 불러오는 래더 로직(Ladder Logic)이 FB블럭 입출력에 영향을 주게 되므로 주의가 필요합니다.

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
<그림 1. 래더 로직의 fb1 논리적/물리적 입출력 연결 예시><br>

내장 PLC에 대한 자세한 사항은 "[로봇제어기 기능설명서 - 내장 PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/korean/README)" 를 참고하시기 바랍니다.
# 2.5. 센서 동기 설정

{% hint style="info" %}
컨베이어 엔코더 인터페이스를 사용하지 않을 경우는 "센서 동기" 설정을 진행하지 않아도 됩니다.
{% endhint %}

BD682의 컨베이어 엔코더 인터페이스 사용할 경우 "센서 동기" 설정이 필요합니다. 

**- 메뉴 위치: [시스템] - [4: 응용 파라미터] - [4: 센서 동기]**

![](../_assets/18.센서동기_설정_UI.png)<br>
<그림 1. 센서 동기 설정 UI><br><br>

'파라미터 설정'의 '동기 상태' 항목을 '컨베이어'로 설정하고 '입력 신호 할당', '출력 신호 할당'을 정상적으로 설정해야 컨베이어 엔코더 인터페이스를 사용할 수 있습니다.


![](../_assets/19.동기_상태_컨베이어_설정.png)<br>
<그림 2. 동기 상태를 컨베이어로 설정><br>

'파라미터 설정'에 대한 세부 정보는 "[로봇제어기 기능설명서 - 센서 동기 (센서 동기 파라미터)](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/3-user-interface/3-3-sensor-sync-parameter)"를 참고하시기 바랍니다.

<br>
BD682의 컨베이어 엔코더 인터페이스는 시스템 입출력에 연동되므로 입출력 신호 할당이 필요합니다. 

아래 그림과 같이 UI 밑에 위치한 **[BD640T BD68X] 버튼**을 누르면 지정된 입출력 번호를 입력해 줍니다. 그리고 최종적으로 **[v확인] 버튼**을 누르면 설정을 적용할 수 있습니다.

![](../_assets/20.채널1_시스템_입출력_설정.png)<br>
<그림 3. 채널1 시스템 입출력 설정><br><br>

![](../_assets/21.채널2_시스템_입출력_설정.png)<br>
<그림 4. 채널2 시스템 입출력 설정><br><br>

추가적으로 펄스 카운터 타입, 펄스 통신 방식(엔코더 종류)을 선택할 수 있습니다. 아래의 표 내용을 참고하시기 바랍니다.
<br>

<표 1. 펄스 카운터 타입, 펄스 통신 방식(엔코더 종류) 정보>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            출력 신호 할당
        </th>
        <th style="width: 30px; text-align: center;">
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">
            비고
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>1</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            펄스 카운터 타입
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            Up / Down 카운터 방식
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Up 카운터 방식 (초기값)
        </td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>2</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            펄스 통신 방식<br>
            (엔코더 종류)
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            오픈 콜렉터 엔코더
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            라인드라이브 엔코더 (초기값)
        </td>
    </tr>
</tbody>
</table>

<br>

아래 그림처럼 체크박스를 클릭하면 ON으로 입력할 수 있습니다.<br>
적용을 위해서는 반드시 **[v확인] 버튼**을 눌러야 합니다.

![](../_assets/22.출력신호할당_ON.png)<br>
<그림 5. 펄스 카운터 타입 ON 적용><br>

세부적인 내용은 "[로봇제어기 기능설명서 - 센서 동기](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/README)"의 컨베이어 관련 부분을 참고하시기 바랍니다.
# 3. 사용자 DIO 사용 방법# 3.1. DIO 사용 방법

BD681, BD682의 DIO를 사용하기 위해서는 우선 "[제어기 보수 설명서 - (하드웨어 정보)](https://hrbook-hrc.web.app/#/view/doc-hi6a-n-maintenance/korean/5-optional-components/5-UserDIO/2-HW-Inform)" 매뉴얼을 참고하여 BD681, BD682의 커넥터에 올바르게 입출력 배선을 연결합니다.
<br>그리고 입출력을 제어하기 위한 방법은 아래 내용들을 참고하시기 바랍니다.

<br>

<mark style="color:green;">**- 제어기의 입출력 신호와 연동**</mark>

제어기의 입출력 신호와 보드의 입출력 연동에 대한 부분은 "[로봇제어기 조작설명서 - (입출력 신호 설정)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/7-system/3-control-parameter/2-io-signal-setting/README)" 을 참고하시기 바랍니다.

<br>

<mark style="color:green;">**- TP를 이용한 보드 입력, 출력 제어**</mark>

TP에서 보드 출력을 제어하고 입력을 확인하는 부분은 "[로봇제어기 조작설명서 - (범용 출력)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/6-monitoring/2-io/4-user-output)", "[로봇제어기 조작설명서 - (범용 입력)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/6-monitoring/2-io/3-user-input)" 을 참고하시기 바랍니다. 

<br>

<mark style="color:green;">**- Job을 이용한 보드 입력, 출력 제어**</mark>

Job에서 보드 입력, 출력을 연동하는 부분은 "[로봇제어기 기능설명서 - 로봇언어 HRScript (fb객체 : 디지털 I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/korean/6-external-comm/1-fb-io/README)" 을 참고하시기 바랍니다.

<br><br>
추가적으로 사용자 DIO 에는 EtherCAT 통신 연결이 순간적으로 오류가 발생했을 경우 (예시: EtherCAT 통신 끊어짐 등으로 인한 Pre-OP, Safe-OP 상태) 디지털 출력 상태를 설정하는 기능이 있습니다.

**- 메뉴 위치 : [시스템] - [옵션장치] - [사용자DIO 보드 설정]**

![](../_assets/23.연결_오류시_디지털_출력_설정.png)<br>
<그림 1. 연결 오류시 디지털 출력 설정><br>

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
<그림 2. 연결 오류시 디지털 출력 설정값 변경><br>

# 3.2. 컨베이어 엔코더 인터페이스 사용 방법

BD681, BD682의 컨베이어 엔코더 인터페이스를 사용하기 위해서는 우선 "[제어기 보수 설명서 - (하드웨어 정보)](https://hrbook-hrc.web.app/#/view/doc-hi6a-n-maintenance/korean/5-optional-components/5-UserDIO/2-HW-Inform)" 매뉴얼을 참고하여 BD682의 커넥터에 올바르게 엔코더 배선을 연결합니다. 그리고 연동하기 위한 방법은 아래 내용들을 참고하시기 바랍니다.

<br>

<mark style="color:green;">**- 제어기와 컨베이어 엔코더 연동**</mark>

보드를 이용한 제어기와 컨베이어 엔코더 연동에 대한 세부 내용은 "[로봇제어기 기능설명서 - 센서 동기](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/README)" 매뉴얼의 컨베이어 관련 부분을 참고하시기 바랍니다.
