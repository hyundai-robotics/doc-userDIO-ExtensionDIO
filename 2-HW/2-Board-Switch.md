# 2.2. 板开关

BD681 板的开关位置如下图所示。<br>

![](../_assets/01.用户DIO_板_开关_位置.png)<br>
< Figure 1. 用户 DIO 板开关位置>
<br>

![](../_assets/03.用户DIO_板_开关_ON_OFF.png)<br>
< Figure 2. 用户 DIO 板开关 ON/OFF>

<br>

< Table 1. 板开关设置>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 100px; text-align: center;">
            BD681 开关 <br>
            开/关
        </th>
        <th style="width: 400px; text-align: center;">备注</th>
    </tr>
</thead>
<tbody>
    <tr>
        <td style="text-align: center;"><strong>1</strong></td>
        <td style="text-align: center;">关</td>
        <td> - 扩展 DIO (BD682) 接口模式<br>
             - 用于基本选项配置 (BD681 + BD682)<br>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">开</td>
        <td> - 用户 DIO (BD681) 独立模式 <br>
             - 不支持扩展 DIO (BD682) 集成<br>
             - 在将 BD681 添加到基本选项配置时使用<br> 
             - 需要第二个添加的 BD681 <br>
        </td>
    </tr>
</tbody>
</table>


{% hint style="warning" %}
在从控制器上拆下电路板以检查开关时，请始终关闭控制器电源，并确保在拆卸之前电路板电源已关闭。
{% endhint %}
< Table 2. 支持的用户 DIO 模式组合>

<table>
<thead>
    <tr>
        <th style="width: 20px; text-align: center;">编号</th>
        <th style="width: 250px; text-align: center;">
            用户 DIO (BD681) /<br> 扩展 DIO (BD682) 数量
        </th>
        <th style="width: 150px; text-align: center;">
            BD681 开关<br>
            开/关
        </th>
        <th style="width: 110px; text-align: center;">
            可用性
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
            开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>2</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA
        </td>
        <td style="text-align: center;">
            关
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>3</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            关
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>4</strong></td>
        <td style="text-align: center;">
            BD681 : 1 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>5</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关打开<br>
            #2 BD681 开关打开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>6</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关关闭<br>
            #2 BD681 开关打开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>7</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 开关打开<br>
            #2 BD681 开关关闭
        </td>        
<font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>8</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 关闭
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>9</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 打开
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>10</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 关闭<br>
            #2 BD681 关闭
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>11</strong></td>
        <td style="text-align: center;">
            BD681 : 2 EA<br>
            BD682 : 1 EA
        </td>
        <td style="text-align: center;">
            #1 BD681 打开<br>
            #2 BD681 关闭
        </td>
        <td style="text-align: center;">O (可用)</td>
    </tr>
    <tr>
        <td style="text-align: center;"><strong>12</strong></td>
        <td style="text-align: center;">
            BD681 : 2 个<br>
            BD682 : 1 个
        </td>
        <td style="text-align: center;">
            #1 BD681 打开<br>
            #2 BD681 打开
        </td>        
        <td style="text-align: center;">
        <font style="color:rgb(255, 0, 0);">X (不可用)</font>
        </td>
    </tr>
</tbody>
</table>
<br>