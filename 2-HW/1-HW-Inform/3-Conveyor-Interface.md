# 2.1.3. 컨베이어 동기화 구성

다음의 그림은 컨베이어 동기화를 위한 엔코더 입력 및 리밋 스위치로 구성 되어 있습니다.<br>
총 2개의 입력 채널로 구성되어 있으며, 입력 채널의 구성은 다음과 같습니다.
각 채널 당, 2종류의 엔코더 타입(오픈컬렉터/라인드라이버)으로 설정 되어 있습니다.<br>

![](../../_assets/33.확장DIO_보드_커넥터_Conveyor.png)<br>
<그림 1. 확장 DIO (BD682) 컨베이어 인터페이스 커넥터>

<표 1. 확장 DIO (BD682) 컨베이어 인터페이스 커넥터>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">핀 번호</th>
        <th style="width: 50px; text-align: center;">신호명</th>
        <th style="width: 220px; text-align: center;">신호 설명</th>        
        <th style="width: 50px; text-align: center;">핀 번호</th>
        <th style="width: 50px; text-align: center;">신호명</th>
        <th style="width: 220px; text-align: center;">신호 설명</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">PA2_P</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            A신호 입력 Positive
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">PA1_P</td>
        <td style="text-align: center;">
            1번 채널 라인드라이버 타입 엔코더<br>
            A신호 입력 Positive
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">PA2_N</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            A신호 입력 Negative
        </td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">PA1_N</td>
        <td style="text-align: center;">
            1번 채널 라인드라이버 타입 엔코더<br>
            A신호 입력 Negative
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">PB2_P</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            B신호 입력 Positive
        </td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">PB1_P</td>
        <td style="text-align: center;">
            1번 채널 라인드라이버 타입 엔코더<br>
            B신호 입력 Positive
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">PB2_N</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            B신호 입력 Negative
        </td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">PB1_N</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            B신호 입력 Negative
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">LDLS2</td>
        <td style="text-align: center;">
            2번 채널 라인드라이버 타입 엔코더<br>
            리밋 스위치
        </td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">LDLS1</td>
        <td style="text-align: center;">
            1번 채널 라인드라이버 타입 엔코더<br>
            리밋 스위치
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">접지</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">접지</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">P2+</td>
        <td style="text-align: center;">
            2번 채널 오픈컬렉터 엔코더 전원
        </td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">P1+</td>
        <td style="text-align: center;">
            1번 채널 오픈컬렉터 엔코더 전원
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">
            2번 채널 오픈컬렉터 타입 엔코더<br>
            A 신호 입력
        </td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">A1</td>
        <td style="text-align: center;">
            1번 채널 오픈컬렉터 타입 엔코더<br>
            A 신호 입력
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">
            2번 채널 오픈컬렉터 타입 엔코더<br>
            B 신호 입력
        </td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B1</td>
        <td style="text-align: center;">
            1번 채널 오픈컬렉터 타입 엔코더<br>
            B 신호 입력
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">OCLS2</td>
        <td style="text-align: center;">
            2번 채널 오픈컬렉터 타입 엔코더<br>
            리밋 스위치
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">OCLS1</td>
        <td style="text-align: center;">
            1번 채널 오픈컬렉터 타입 엔코더<br>
            리밋 스위치
        </td>
    </tr>
</tbody>
</table>
<br>
<br>

<표 2. 확장 DIO (BD682) 컨베이어 인터페이스 입력 신호 전기적 사양>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            신호명
        </th>
        <th style="width: 100px; text-align: center;">
            전기적 사양
        </th>
        <th style="width: 200px; text-align: center;">
            비고
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">
            PA1_P, PA1_N<br>
            PB1_P, PB1_N<br>
            PA2_P, PA2_N<br>
            PB2_P, PB2_N<br>
        </td>
        <td style="text-align: center;">
            0 V ~ 5 V<br>
            100 kHz 이하
        </td>
        <td style="text-align: center;">
            라인드라이브 타입 엔코더 신호
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            LDLS1, LDLS2
        </td>
        <td style="text-align: center;">
            0 V / 5 V
        </td>
        <td style="text-align: center;">
            라인드라이버 타입 엔코더<br>
            리밋 스위치 신호
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            P1+, P2+
        </td>
        <td style="text-align: center;">
            24 V
        </td>
        <td style="text-align: center;">
            오픈컬렉터 엔코더 전원
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            A1, B1<br>
            A2, B2
        </td>
        <td style="text-align: center;">
            0 V ~ 24 V<br>
            100 kHz 이하
        </td>
        <td style="text-align: center;">
            오픈컬렉터 타입 엔코더 신호 
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            OCLS1, OCLS2
        </td>
        <td style="text-align: center;">
            0 V / 24 V
        </td>
        <td style="text-align: center;">
            오픈컬렉터 타입 엔코더<br>
            리밋 스위치 신호
        </td>
    </tr>
</tbody>
</table>
<br>
