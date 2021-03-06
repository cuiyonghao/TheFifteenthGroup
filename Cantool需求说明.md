## CanToolApp需求说明 ##
1. 能够搜索到本机所有可使用的COM串口，并在弹出式ComboBox中以列表方式让用户选择CanTool装置在上位机中映射的COM口。并设置相应COM口波特率115200、数据位数8、停止位数1。这些设定内容可保存到CanToolApp设定文件中，供下次使用。
2. 能够实现CANtool装置的CAN速率设置、进入CAN工作状态（Open）、进入CAN初始化状态（ Close）。这些设定内容可保存到CanToolApp设定文件中，供下次使用
3. 能够对接收到的多个CAN信息，通过CAN信息及CAN信号数据库进行解析，将CAN信息原始数据进行显示。并能对CAN信息中的CAN信号的物理值实时数据进行显示。
4. 显示时可以让用户选择仪表盘方式显示接收到CAN信号物理值。这些用户选择的显示方式可保存到CanToolApp设定文件中，供下次使用。
5. 可以让用户选择某些接收到的CAN信号，显示其变化的实时物理值曲线。
6. 可以将接收到的所有CAN信息数据，实时保存为数据文件。
7. 能够指定要发送的多个CAN信息，并允许用户设定CAN信息中的CAN信号物理值。可以指定CAN信息的发送周期（0-65535ms即0x0000-0xFFFF）。
8. App可将用户设定的物理值转换为CAN信号值，将CAN信息中包含的所有CAN信号合成完整的CAN信息后，发送给CanTool装置，发送到CAN总线上。
9. 可以加载用户提供的CAN信息和信号数据库，完成CAN信号数据的解析以及CAN发送信息的组装。可以显示CAN信号在CAN信息的布局。未加载数据库的情况下，只显示CAN信号的原始值，即phy=A*x+B中的A=1，B=0。加载的数据库文件相关信息，可保存到CanToolApp设定文件中，供下次使用。
10. 加载用户提供的CAN信息和信号数据库，可以树状结构显示在GUI界面中。
11. 可以将用户提供的CAN信息和信号数据库另存为xml和JSON (JavaScript Object Notation)格式。也可以将xml或Json格式的数据库，转换为CAN信息和信号数据库格式。
12. 可以将所有CAN信息实时数据、CAN设定信息等 通过WEB API方式更新到远程数据库。此时CanToolApp作为客户端与远程的Web API服务进行数据交换。此功能需要完成WebAPI服务器端的get\post等服务，实现数据的增删改查、可视化数据显示，实现数据共享。（此功能可以独立一个项目完成）。
13. 将总线上采集的CAN信息发送到上位机，可以是Android、IOS、WindowsPC。
14. 通过USB串口或蓝牙RFComm，实现CanTool装置与CanToolApp上位机的uART串口通信。

####第十五组 何洋、李天鹏、谢东升、崔雍浩
