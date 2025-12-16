# 2.2. Platinenschalter

Die Position des BD681-Platinenschalters ist auf dem Foto unten dargestellt.<br>

![](../_assets/01.사용자DIO_보드_스위치_위치.png)<br>
<Abbildung 1. Position des Schalters der Anwender-DIO-Platine>
<br>

![](../_assets/03.사용자DIO_보드_스위치_ON_OFF.png)<br>
<Abbildung 2. Anwender-DIO-Platinenschalter EIN/AUS>

<br>

<Tabelle 1. Informationen zur Einstellung des Platinenschalters>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 100px; text-align: center;">
            BD681-Schalter<br>
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">Anmerkungen</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">OFF</td>
<td> - Verbindungsmodus für Erweiterungs-DIO (BD682)<br>
- Verwendung in der Grundkonfiguration (BD681 + BD682)<br>
</td>
</tr>
<tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">ON</td>
        <td> - Standalone-Modus für Anwender-DIO (BD681) <br>
             - Erweiterungs-DIO (BD682) kann nicht verbunden werden <br>
             - Verwendung beim Hinzufügen von BD681 zur Grundkonfiguration <br> 
             - Muss auf die hinzugefügte zweite BD681 angewendet werden <br>
        </td>
    </tr>
</tbody>
</table>


{% hint style="warning" %}
Wenn Sie die Platine von der Steuerung trennen müssen, um den Schalter zu überprüfen, stellen Sie bitte sicher, dass die Stromversorgung der Steuerung ausgeschaltet ist und überprüfen Sie, ob die Stromversorgung der Platine ausgeschaltet ist, bevor Sie sie trennen.
{% endhint %}

<Tabelle 2. Verwendbarkeit der Anwender-DIO-Modus-Kombination>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">No.</th>
        <th style="width: 150px; text-align: center;">
            Anwender-DIO-(BD681),<br> 
            Erweiterungs-DIO (BD682), Anzahl
        </th>
        <th style="width: 150px; text-align: center;">
            BD681-Schalter<br>
            ON/OFF
        </th>
        <th style="width: 110px; text-align: center;">
            Verwendbarkeit
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">
            BD681: 1 EA
        </td>
        <td style="text-align: center;">
            ON
        </td>
        <td style="text-align: center;">O (verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF
        </td>
        <td style="text-align: center;">X (nicht verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            OFF
        </td>
        <td style="text-align: center;">O (verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681: 1 EA<br>
            BD682: 1 EA
        </td>
        <td style="text-align: center;">
            ON
        </td>
        <td style="text-align: center;">X (nicht verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681-Schalter AUS<br>
            #2 BD681-Schalter EIN
        </td>
        <td style="text-align: center;">O (verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681-Schalter AUS<br>
            #2 BD681-Schalter AUS
        </td>
        <td style="text-align: center;">X (nicht verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681-Schalter EIN<br>
            #2 BD681-Schalter AUS
        </td>
        <td style="text-align: center;">X (nicht verfügbar)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681-Schalter EIN<br>
            #2 BD681-Schalter EIN
        </td>
        <td style="text-align: center;">X (nicht verfügbar)</td>
    </tr>
</tbody>
</table>
<br>

