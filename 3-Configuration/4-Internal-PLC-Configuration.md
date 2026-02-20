# 3.4. 嵌入式 PLC 配置检查

要正确连接使用 FB 块的用户 DIO，有必要检查嵌入式 PLC 设置。

**- 嵌入式 PLC 关闭（未使用）**<br>

嵌入式 PLC 的功能将被关闭。当发生这种情况时，机器人控制器的逻辑输出 FB0.DO0-FB9.DO959 将自动输出为物理输出（即绕过），FB0.Y0-FB9.Y959，物理输入 FB0.X0-FB9.X959 将自动输入为逻辑输入 FB0.DI0-FB9.DI595。<br><br>

**- 嵌入式 PLC 使用中**

由于从嵌入式 PLC 加载的梯形逻辑会影响 FB 块的输入和输出，因此需要谨慎操作。

![](../_assets/17.래더로직_FB_입출력_연결.png)<br>
< Figure 1. 梯形逻辑中 FB1 的逻辑/物理 I/O 连接示例><br>

有关嵌入式 PLC 的更多详细信息，请参阅 "[机器人控制器功能手册 - 嵌入式 PLC](https://hrbook-hrc.web.app/#/view/doc-hi6-embedded-plc/en/README?cont_model=Hi7)"