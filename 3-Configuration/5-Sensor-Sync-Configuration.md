# 3.5. Sensorsynchronisationseinstellungen

{% hint style="info" %}
Wenn Sie die Förderband-Encoder-Schnittstelle nicht verwenden, müssen Sie die Einstellungen für die „Sensorsynchronisation” nicht vornehmen.
{% endhint %}

Wenn Sie die Förderband-Encoder-Schnittstelle des BD682 verwenden, sind Einstellungen für die „Sensorsynchronisation“ erforderlich. 

**- Menüposition: [System] - [4: Anwendungsparameter] - [4: Sensorsynchronisation]**

![](../_assets/18.센서동기_설정_UI.png)<br>
<Abbildung 1. Benutzeroberfläche für die Sensorsynchronisationseinstellungen><br><br>

Sie können die Förderband-Encoder-Schnittstelle verwenden, indem Sie den Punkt „Synchronisationsstatus“ in den „Parametereinstellungen“ auf „Förderband“ setzen und „Eingangssignalzuweisung“ und „Ausgangssignalzuweisung“ korrekt einstellen.


![](../_assets/19.동기_상태_컨베이어_설정.png)<br>
<Abbildung 2. Setzen des Synchronisationsstatus auf „Conveyor“ (Förderband)><br>

Ausführliche Informationen zu den „Parametereinstellungen“ finden Sie im „[Handbuch zu den Funktionen der Robotersteuerung – Sensorsynchronisation (Parameter für die Sensorsynchronisation)](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/3-user-interface/3-3-sensor-sync-parameter)“.

<br>
Da die Förderband-Encoder-Schnittstelle des BD682 mit dem System-Eingang/Ausgang verbunden ist, ist eine Zuweisung der Eingangs-/Ausgangssignale erforderlich.

Drücken Sie die **Taste [BD640T BD68X]** unten in der Benutzeroberfläche, wie in der Abbildung unten gezeigt, um die festgelegten Eingangs-/Ausgangsnummern einzugeben. Drücken Sie abschließend die **Taste [v OK]**, um die Einstellungen zu übernehmen.

![](../_assets/20.채널1_시스템_입출력_설정.png)<br>
<Abbildung 3. Einstellungen für System-Ein-/Ausgänge von Kanal 1><br><br>

![](../_assets/21.채널2_시스템_입출력_설정.png)<br>
<Abbildung 4. Einstellungen für System-Ein-/Ausgänge von Kanal 2><br><br>

Darüber hinaus können Sie den Impulszählertyp und die Impulskommunikationsmethode (Encodertyp) auswählen. Bitte beachten Sie die folgenden Tabelleninhalte.
<br>

<Tabelle 1. Informationen zu Impulszählertyp und Impulskommunikationsmethode (Encodertyp)>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            Ausgangssignalzuweisung
        </th>
        <th style="width: 30px; text-align: center;">
            ON/OFF
        </th>
        <th style="width: 250px; text-align: center;">
            Anmerkungen
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>1</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
Impulszählertyp
</td>
<td style="text-align: center;">
ON<br>(1)
</td>
        <td> 
            Aufwärts-/Abwärtszählmethode
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Aufwärtszählmethode (Anfangswert)
        </td>
    </tr>
        <tr>
        <td rowspan="2" style="text-align: center;">
            <strong>2</strong>
        </td>
        <td rowspan="2" style="text-align: center;">
            Impulskommunikationsmethode<br>
            (Encodertyp)
        </td>
        <td style="text-align: center;">
            ON<br>(1)
        </td>
        <td> 
            Open-Collector-Encoder
        </td>
    </tr>        
        <td style="text-align: center;">
            OFF<br>(0)
        </td>
        <td> 
            Line-Drive-Encoder (Anfangswert)
        </td>
    </tr>
</tbody>
</table>

<br>

Sie können diese Option aktivieren, indem Sie das Kontrollkästchen wie in der Abbildung unten gezeigt anklicken.<br>
Um die Einstellungen zu übernehmen, müssen Sie unbedingt die **Schaltfläche [v OK]** drücken.

![](../_assets/22.출력신호할당_ON.png)<br>
<Abbildung 5. Impulszählertyp EIN-Anwendung><br>

Ausführliche Informationen finden Sie im Abschnitt „[Handbuch zu den Funktionen der Robotersteuerung – Sensorsynchronisation](https://hrbook-hrc.web.app/#/view/doc-sensor-sync/korean/README)” unter „Förderband”.
