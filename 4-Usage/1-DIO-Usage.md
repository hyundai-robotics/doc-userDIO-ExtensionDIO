# 4.1. 如何使用 DIO

如果电缆正确连接到 BD681 和 BD682 的连接器，请参考以下指令以控制数字输入和输出。
<br>

<mark style="color:green;">**- 与控制器输入/输出信号的联动**</mark>

有关控制器 I/O 信号与板 I/O 之间联动的详细信息，请参考 "[机器人控制器操作手册 - (输入/输出信号设置)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/7-system/3-control-parameter/2-io-signal-setting/README)"。

<br>

<mark style="color:green;">**- 使用 TP 进行板输入/输出控制**</mark>

有关控制板输出和检查来自 TP 的输入的信息，请参考 "[机器人控制器操作手册 - (公共输出)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/4-user-output)" 和 "[机器人控制器操作手册 - (公共输入)](https://hrbook-hrc.web.app/#/view/doc-hi6-operation/en-tp630/6-monitoring/2-io/3-user-input)"。

<br>

{% hint style="info" %}
请注意，受控 I/O 范围取决于 BD681 和 BD682 的组合。
{% endhint %}

![](../_assets/38.DIO_ctrl.png)<br>
< Figure 1. 根据板组合的 I/O 控制范围示例><br>

<br>

<mark style="color:green;">**- 使用作业进行板输入/输出控制**</mark>

有关在作业中链接板输入和输出的信息，请参考 "[机器人控制器功能手册 - 机器人语言 HRScript (FB 对象: 数字 I/O)](https://hrbook-hrc.web.app/#/view/doc-hrscript/en/6-external-comm/1-fb-io/README?cont_model=Hi7)"。

<br><br>
此外，用户 DIO 提供了一种功能，可以在发生瞬时 EtherCAT 通信错误时配置数字输出状态（例如，由于通信错误而过渡到 Pre-OP 或 Safe-OP 状态）。

**- 菜单位置: [系统] - [12: 选项系统] - [用户 DIO 板设置]**

![](../_assets/23.연결_오류시_디지털_출력_설정_en.png)<br>
< Figure 2. 连接错误时的数字输出设置><br>

<br>

< Table 1. 连接错误时的数字输出设置信息>

<table>
<thead>
    <tr>
        <th style="width: 50px; text-align: center;">
            No.
        </th>
        <th style="width: 110px; text-align: center;">
            设置值
        </th>
        <th style="width: 370px; text-align: center;">
            注释
        </th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;">
            <strong>1</strong>
        </td>
        <td style="text-align: center;">
            清除值<br>
            （默认）
        </td>
        <td> 
             - 连接错误时将所有板输出设置为 OFF
        </td>
    </tr>
    <tr>
        <td style="text-align: center;">
            <strong>2</strong>
        </td>
        <td style="text-align: center;">
            保持值
        </td>
        <td> 
             - 在连接错误时，将板输出保持在最后一个值
        </td>
    </tr>
</tbody>
</table>

<br>
如果您想更改配置的值，请选择所需的设置并按[v OK]按钮。<br><br>

![](../_assets/24.连接_错误时_数字输出_设置值_更改_en.png)<br>
< Figure 3. 连接错误时数字输出设置的更改><br>