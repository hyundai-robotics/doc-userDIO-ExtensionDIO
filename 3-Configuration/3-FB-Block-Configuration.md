# 3.3. FB-Block-Einstellungen

Die FB-Block-Einstellungen können im folgenden Menü vorgenommen werden.

- Menüposition: [System] - [2: Steuerungsparameter] - [2: Ein-/Ausgangssignal-Einstellungen] - [6: FB-Block-Zuweisung]*

![](../_assets/12.FB블럭할당.png)<br>
<Abbildung 1. Menü „FB-Block-Zuweisung“><br><br>

Wählen Sie den zuweisbaren FB-Block aus und setzen Sie ihn auf „Anwender-DIO”.

![](../_assets/13.fb1_사용자DIO할당.png)<br>
<Abbildung 2. Beispiel für die Zuweisung von fb1 zu Anwender-DIO><br><br>

자세한 사항은 "[Weitere Informationen finden Sie in der „Bedienungsanleitung der Robotersteuerung – (FB-Block-Zuweisung)”.](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/korean-tp630/7-system/3-control-parameter/2-io-signal-setting/9-dio-block-assign)" 을 참고하시기 바랍니다.

Sie können in den Menüs [6: FB-Block-Zuweisung] und [Einstellungen der Anwender-DIO-Platine] überprüfen, ob der FB-Block für Anwender-DIO zugewiesen wurde.

![](../_assets/14.사용자DIO_FB_미할당.png)<br>
<Abbildung 3. FB-Block für Anwender-DIO nicht zugewiesen><br><br>

![](../_assets/15.사용자DIO_FB3_할당.png)<br>
<Abbildung 4. Anwender-DIO-Zuweisung für fb3><br>

{% hint style="warning" %}
Auch wenn Anwender-DIO mehreren FB-Blöcken zugewiesen ist, <strong>kann es nur im FB-Block mit der niedrigsten Nummer verwendet werden, und die übrigen zugewiesenen FB-Blöcke werden für die Steuerung ignoriert</strong>.
{% endhint %}

Wenn FB-Blöcke wie in der Abbildung unten zugewiesen sind, ist die Anwender-DIO-Steuerung in fb2 möglich, und in fb5 eingegebene Werte werden ignoriert.

![](../_assets/16.사용자DIO_FB_다중할당.png)<br>
<Abbildung 5. Beispiel für die Mehrfachzuweisung von Anwender-DIO-FB><br>
