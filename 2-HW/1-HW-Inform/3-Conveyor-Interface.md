# 2.1.3. Konfiguration der Förderbandsynchronisation

Die folgende Abbildung und Tabelle zeigen die Pin-Konfiguration des Anschlussblocks für die Förderbandsynchronisation, bestehend aus Encoder-Eingang und Endschalter.<br>
Er besteht aus insgesamt 2 Eingangskanälen, wobei jeder Kanal durch Auswahl eines von zwei Encodertypen (Open Collector/Line Driver) angeschlossen werden kann.<br>


![](../../_assets/33.확장DIO_보드_커넥터_Conveyor.png)<br>
<Abbildung 1. Anschluss für Förderbandschnittstelle der Erweiterungs-DIO (BD682)>

<Tabelle 1. Anschluss für Förderbandschnittstelle der Erweiterungs-DIO (BD682)>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">Pin-Nummer</th>
        <th style="width: 50px; text-align: center;">Signalname</th>
        <th style="width: 220px; text-align: center;">Signalbeschreibung</th>        
        <th style="width: 50px; text-align: center;">Pin-Nummer</th>
        <th style="width: 50px; text-align: center;">Signalname</th>
        <th style="width: 220px; text-align: center;">Signalbeschreibung</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">1</td>
        <td style="text-align: center;">PA2_P</td>
        <td style="text-align: center;">
            Kanal 2 Line-Driver-Encodertyp<br>
            A-Signaleingang positiv
        </td>
        <td style="text-align: center;">11</td>
        <td style="text-align: center;">PA1_P</td>
        <td style="text-align: center;">
            Kanal 1 Line-Driver-Encodertyp<br>
            A-Signaleingang positiv
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">2</td>
        <td style="text-align: center;">PA2_N</td>
        <td style="text-align: center;">
            Kanal 2 Line-Driver-Encodertyp<br>
            A-Signaleingang negativ
        </td>
        <td style="text-align: center;">12</td>
        <td style="text-align: center;">PA1_N</td>
        <td style="text-align: center;">
            Kanal 1 Line-Driver-Encodertyp<br>
            A-Signaleingang negativ
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">3</td>
        <td style="text-align: center;">PB2_P</td>
        <td style="text-align: center;">
            Kanal 2 Line-Driver-Encodertyp<br>
            B-Signaleingang positiv
        </td>
        <td style="text-align: center;">13</td>
        <td style="text-align: center;">PB1_P</td>
        <td style="text-align: center;">
            Kanal 1 Line-Driver-Encodertyp<br>
            B-Signaleingang positiv
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">4</td>
        <td style="text-align: center;">PB2_N</td>
        <td style="text-align: center;">
            Kanal 2 Line-Driver-Encodertyp<br>
            B-Signaleingang negativ
        </td>
        <td style="text-align: center;">14</td>
        <td style="text-align: center;">PB1_N</td>
        <td style="text-align: center;">
            Kanal 1 Line-Driver-Encodertyp<br>
            B-Signaleingang negativ
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">5</td>
        <td style="text-align: center;">LDLS2</td>
        <td style="text-align: center;">
            Kanal 2 Line-Driver-Encodertyp<br>
            Endschalter
        </td>
        <td style="text-align: center;">15</td>
        <td style="text-align: center;">LDLS1</td>
        <td style="text-align: center;">
            Kanal 1 Line-Driver-Encodertyp<br>
            Endschalter
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">6</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">Masse</td>
        <td style="text-align: center;">16</td>
        <td style="text-align: center;">GND</td>
        <td style="text-align: center;">Masse</td>
    </tr>
    <tr>
        <td style="text-align: center;">7</td>
        <td style="text-align: center;">P2+</td>
        <td style="text-align: center;">
            Kanal 2 Open-Collector-Encoder-Stromversorgung
        </td>
        <td style="text-align: center;">17</td>
        <td style="text-align: center;">P1+</td>
        <td style="text-align: center;">
            Kanal 1 Open-Collector-Encoder-Stromversorgung
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">8</td>
        <td style="text-align: center;">A2</td>
        <td style="text-align: center;">
            Kanal 2 Open-Collector-Encoder<br>
            A-Signaleingang
        </td>
        <td style="text-align: center;">18</td>
        <td style="text-align: center;">A1</td>
        <td style="text-align: center;">
            Kanal 1 Open-Collector-Encoder<br>
            A-Signaleingang
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">9</td>
        <td style="text-align: center;">B2</td>
        <td style="text-align: center;">
            Kanal 2 Open-Collector-Encoder<br>
            B-Signaleingang
        </td>
        <td style="text-align: center;">19</td>
        <td style="text-align: center;">B1</td>
        <td style="text-align: center;">
            Kanal 1 Open-Collector-Encoder<br>
            B-Signaleingang
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">10</td>
        <td style="text-align: center;">OCLS2</td>
        <td style="text-align: center;">
            Kanal 2 Open-Collector-Encoder<br>
            Endschalter
        </td>
        <td style="text-align: center;">20</td>
        <td style="text-align: center;">OCLS1</td>
        <td style="text-align: center;">
            Kanal 1 Open-Collector-Encoder<br>
            Endschalter
        </td>
    </tr>
</tbody>
</table>
<br>
<br>

<Tabelle 2. Elektrische Spezifikationen für das Eingangssignal der Förderbandschnittstelle der Erweiterungs-DIO (BD682)>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">Nr.</th>
        <th style="width: 100px; text-align: center;">
            Signalname
        </th>
        <th style="width: 100px; text-align: center;">
            Elektrische Spezifikationen
        </th>
        <th style="width: 200px; text-align: center;">
            Anmerkungen
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
            0 V – 5 V<br>
            100 kHz oder weniger
        </td>
        <td style="text-align: center;">
            Line-Drive-Encoder-Signal
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
            Line-Driver-Encodertyp<br>
            Endschaltersignal
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
            Open-Collector-Encoder-Stromversorgung
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            A1, B1<br>
            A2, B2
        </td>
        <td style="text-align: center;">
            0 V – 24 V<br>
            100 kHz oder weniger
        </td>
        <td style="text-align: center;">
            Open-Collector-Encoder-Signal 
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
            Open-Collector-Encodertyp<br>
            Endschaltersignal
        </td>
    </tr>
</tbody>
</table>
<br>
