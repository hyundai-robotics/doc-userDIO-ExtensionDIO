# 1. Übersicht

In der Hi7-Steuerung können Sie digitale Ein-/Ausgangssignale und eine Förderbandschnittstelle mithilfe der „Anwender-DIO-Platine (BD681)” und der „Erweiterungs-DIO-Platine (BD682)” ausführen.

{% hint style="info" %}
In diesem Handbuch steht DIO für „Digital Input and Output“ (digitaler Ein- und Ausgang).
{% endhint %}

Die „Erweiterungs-DIO-Platine (BD682)” muss zusammen mit der „Anwender-DIO-Platine (BD681)” verwendet werden und darf nicht alleine verwendet werden.

<br>

<Tabelle 1. Spezifikationen der Platine>

<table>
<thead>
<tr>
<th style="width: 50px; text-align: center;">
No.
</th>
<th style="width: 110px; text-align: center;">
Platinenbezeichnung<br>
(Platinenkennung)
</th>
<th style="width: 300px; text-align: center;">
Informationen zur Platinenfunktion
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;">
<strong>1</strong>
</td>
<td style="text-align: center;">
Anwender-DIO-Platine<br>
( BD681 )
</td>
<td>
- 16 digitale Eingangskanäle<br>
- 16 digitale Eingangskanäle
</td>
</tr>
<tr>
<td style="text-align: center;">
<strong>2</strong>
</td>
<td style="text-align: center;">
Erweiterungs-DIO-Platine<br>
( BD682 )
</td>
<td>
- 16 digitale Eingangskanäle<br>
- 16 digitale Ausgangskanäle (einschließlich 8 Relaisausgangskanäle)<br>
- 2 Kanäle für Förderbandschnittstelle<br>
- Kann nicht allein verwendet werden (muss zusammen mit BD681 verwendet werden)
</td>
</tr>
</tbody>
</table>

<br>
Mit zwei BD681 und einem BD682 können Sie bis zu 48 Ein-/Ausgangskanäle steuern.
<br><br>

Um Anwender-DIO und Erweiterungs-DIO normal verwenden zu können, müssen die folgenden Punkte eingestellt und überprüft werden.<br>

1. EtherCAT-Kommunikationsanschluss<br>
2. Überprüfung des Platinenschalters<br>
3. FB-Block-Einstellungen<br>
4. Bestätigung der Verwendung der Embedded-SPS<br>
5. Sensorsynchronisationseinstellungen<br>

