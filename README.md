# auto_test_service
工业自动化测试服务

## 需求
1. 测试界面显示与测试过程完全解耦，由后台服务完成测试过程处理。
2. 测试服务通过长连接服务提供测试过程控制、测试数据反馈以及特殊事件上报。
3. 测试界面由数据驱动，展示测试进度、测试结果以及特殊事件。
## 设计

以单台PC为例
测试开始时会启动一个《服务》，并按配置加载《项目》，同时运行指定的《后台执行者》，并启动已配置的服务《组件》。
客户端获取配置使用请求的方式，实时数据显示使用长连接推送的方式。

效果：
PC(WEB和客户端) Android iOS 三端连上同一《服务》后，尽管显示界面会因展示效果有些许差异，但显示测试信息完全一致，同时还能多端控制。
