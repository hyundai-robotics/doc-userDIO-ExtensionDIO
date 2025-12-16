# 4.1. Verwendungsmethode für DIO

Wenn das Kabel korrekt an den Anschluss von BD681 und BD682 angeschlossen ist, finden Sie im Folgenden Informationen zu den Methoden zur Steuerung der Digitalein- und -ausgänge.
<br>

<mark style="color:green;">**- Verbindung mit den Ein-/Ausgangssignalen der Steuerung**</mark>

Informationen zur Verbindung der Ein-/Ausgangssignale der Steuerung mit den Ein-/Ausgängen der Platine finden Sie im „[Bedienungshandbuch der Robotersteuerung – (Ein-/Ausgangssignaleinstellungen)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/7-system/3-control-parameter/2-io-signal-setting/README)".

<br>

<mark style="color:green;">**- Steuerung der Ein- und Ausgänge der Platine über TP**</mark>

Informationen zur Steuerung der Platinenausgänge und zur Überprüfung der Eingänge über TP finden Sie im „[Bedienungshandbuch der Robotersteuerung – (Allgemeine Ausgänge)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/6-monitoring/2-io/4-user-output)", „[Bedienungshandbuch der Robotersteuerung – (Allgemeine Eingänge)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/6-monitoring/2-io/3-user-input)". 

<br>

<mark style="color:green;">**- Steuerung der Ein- und Ausgänge der Platine über Job**</mark>

Informationen zur Anbindung der Ein- und Ausgänge der Platine in Job finden Sie im „[Handbuch zu den Funktionen der Robotersteuerung – Robotersprache HRScript (fb-Objekt: Digital-E/A)](https://hrbook-hrc.web.app/#/view/doc-hrscript/korean/6-external-comm/1-fb-io/README)".

<br><br>
Darüber hinaus verfügt die Anwender-DIO über eine Funktion zum Einstellen des Status des Digitalausgangs, wenn ein vorübergehender Fehler in der EtherCAT-Kommunikationsverbindung auftritt (Beispiel: Pre-OP-, Safe-OP-Status aufgrund einer Unterbrechung der EtherCAT-Kommunikation usw.).

**- Menüposition: [System] - [Optionales Gerät] - [Einstellungen der Anwender-DIO-Platine]**

![](../_assets/23.연결_오류시_디지털_출력_설정.png)<br>
<Abbildung 1. Einstellung des Digitalausgangs bei Verbindungsfehler><br>

<br>

<Tabelle 1. Informationen zur Einstellung des Digitalausgangs bei Verbindungsfehler>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            Nr.
        </th>
        <th style="width: 110px; text-align: center;">
            Einstellwert
        </th>
        <th style="width: 370px; text-align: center;">
            Anmerkungen
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            Werte zurücksetzen<br>
            (Anfangseinstellwert)
        </td>
        <td> 
             – Bei Auftreten eines Verbindungsfehlers werden alle Ausgangswerte der Platine auf AUS gesetzt.
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            Werte beibehalten
        </td>
        <td> 
             – Bei Auftreten eines Verbindungsfehlers werden die Ausgangswerte der Platine auf die unmittelbar vorherigen Werte beibehalten
        </td>
    </tr>
</tbody>
</table>

<br>
Um den Einstellwert zu ändern, wählen Sie den gewünschten Einstellwert aus und drücken Sie die Taste [v OK]. <br><br>

![](../_assets/24.연결_오류시_디지털_출력_설정값_변경.png)<br>
<Abbildung 2. Änderung des Einstellwerts für den Digitalausgang bei Verbindungsfehler><br>

