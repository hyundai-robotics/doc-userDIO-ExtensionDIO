# 3.2. Überprüfung des Platinenschalters


Wenn die Platine bereits in der Steuerung eingebaut ist, können Sie den Status des internen Schalters auf dem TP-Bildschirm wie unten gezeigt überprüfen.<br>

- Menüposition: [System] - [Optionales Gerät] - [Einstellungen der Anwender-DIO-Platine]*

Sie können dies in der „Anwender-DIO-Liste” unter dem Punkt „Anwender-DIO-Modus” überprüfen.

{% hint style="info" %}
Um die korrekte Überprüfung in [Einstellungen der Anwender-DIO-Platine] durchzuführen, muss die EtherCAT-Verbindung von BD681 normal sein.
{% endhint %}


![](../_assets/02.사용자DIO_보드_설정_TP.png)<br>
<Abbildung 1. TP-Benutzeroberfläche „Einstellungen der Anwender-DIO-Platine”><br>

<br>

<Tabelle 1. Punkt „Anwender-DIO-Modus”

<table>
<thead>
<tr>
<th style="width: 20px; text-align: center;">No.</th>
<th style="width: 100px; text-align: center;">
BD681-Schalter<br>
ON/OFF
</th>
<th style="width: 110px; text-align: center;">
Anwender-DIO-Modus
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"><strong>1</strong></td>
<td style="text-align: center;">OFF</td>
<td style="text-align: center;">
Use Ext_DIO <br>
(BD681 + BD682)
</td>
</tr>
<tr>
<td style="text-align: center;"><strong>2</strong></td>
<td style="text-align: center;">ON</td>
<td style="text-align: center;">
Only UserDIO <br>
(BD681)
</td>
</tr>
</tbody>
</table>
<br>


Bei Verwendung von zwei Anwender-DIO-Platinen wird der Fehler <strong>„E55005 Fehler bei der Einstellung des Schalters der zweiten Anwender-DIO-Platine erkannt”</strong> ausgegeben, wenn der Schalter der zweiten Anwender-DIO-Platine ausgeschaltet ist.
Um diesen Fehler zu beheben, müssen Sie den Schalter der zweiten Anwender-DIO-Platine auf EIN stellen.

{% hint style="warning" %}
Wenn der Fehler „E55005 Fehler bei der Einstellung des Schalters der zweiten Anwender-DIO-Platine erkannt“ auftritt, können die Anwender-DIO-Platine und die Erweiterungs-DIO-Platine nicht normal verwendet werden. Sie müssen die Einstellung des Platinenschalters vor der Verwendung korrekt ändern.
{% endhint %}

<br>

<Tabelle 2. Verwendbarkeit der Anwender-DIO-Modus-Kombination>

<table>
<thead>
<tr>
<th style="width: 20px; text-align: center;">No.</th>
<th style="width: 150px; text-align: center;">
Anwender-DIO-(BD681), <br>
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
BD681 : 1 EA
</td>
<td style="text-align: center;">
ON<br>
(Only UserDIO)
</td>
<td style="text-align: center;">O (verfügbar)</td>
</tr>
<tr>
<td style="text-align: center;"><strong>2</strong></td>
<td style="text-align: center;">
BD681 : 1 EA
</td>
<td style="text-align: center;">
OFF<br>
(Use Ext_DIO)
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
OFF<br>
(Use Ext_DIO)
</td>
<td style="text-align: center;">O (verfügbar)</td>
</tr>
<tr>
<td style="text-align: center;"><strong>4</strong></td>
<td style="text-align: center;">
BD681 : 1 EA<br>
BD682 : 1 EA
</td>
<td style="text-align: center;">
ON<br>
(Only UserDIO)
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
(Use Ext_DIO)<br><br>
#2 BD681-Schalter EIN<br>
(Only UserDIO)
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
(Use Ext_DIO)<br><br>
#2 BD681-Schalter AUS<br>
(Use Ext_DIO)
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
(Only UserDIO)<br><br>
#2 BD681-Schalter AUS<br>
(Use Ext_DIO)
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
(Only UserDIO)<br><br>
#2 BD681-Schalter EIN<br>
(Only UserDIO)
</td>
<td style="text-align: center;">X (nicht verfügbar)</td>
</tr>
</tbody>
</table>
<br>
