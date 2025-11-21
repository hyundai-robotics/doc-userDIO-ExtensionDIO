# 3.4. Überprüfung der Einstellungen der Embedded-SPS

Um Anwender-DIO normal mit FB-Blöcken verwenden zu können, müssen die Einstellungen der Embedded-SPS überprüft werden.

*- Embedded-SPS aus (nicht verwendet)**<br>

Die logischen Ausgänge (Logical Output) FB0.DO0 bis FB9.DO959 der Robotersteuerung werden automatisch an die physikalischen Ausgänge (Physical Output) FB0.Y0 bis FB9.Y959 ausgegeben (Bypass), und die physikalischen Eingänge FB0.X0 bis FB9.X959 werden automatisch in die logischen Eingänge FB0.DI0 bis FB9.DI595 eingegeben, sodass Anwender-DIO normal verwendet werden kann.<br><br>

- Embedded-SPS verwendet*

Die von der Embedded-SPS geladene Kontaktplanlogik wirkt sich auf die FB-Block-Ein-/Ausgänge aus, daher ist Vorsicht geboten.

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
<Abbildung 1. Beispiel für die Verbindung von logischen/physikalischen Ein-/Ausgängen der Kontaktplanlogik fb1><br>

내장 PLC에 대한 자세한 사항은 "[Weitere Informationen zur Embedded-SPS finden Sie im „Handbuch zu den Funktionen der Robotersteuerung – Embedded-SPS”.](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/korean/README)" 를 참고하시기 바랍니다.
