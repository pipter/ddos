# 步骤3：设置DDoS防护策略 {#task_221019 .task}

业务接入新BGP高防IP后，默认启用DDoS智能防御模式，无需您进行额外操作。在遇到异常情况或特殊需求时，您可以选择调整DDoS防护策略。

添加网站配置。具体操作请参见[步骤1：添加网站配置](cn.zh-CN/新BGP高防IP/快速入门/防护网站业务/步骤1：添加网站配置.md#)。

支持调整的DDoS防护策略包括：

|DDoS防护策略类型|描述|
|----------|--|
|清洗模式|智能防御模式开启后，需要3天来学习业务流量并建立防御模型；有攻击的话，可以通过源新建连接自动限速功能来辅助防御，3天后智能防御达到最佳防护效果。如果正常模式下的防护效果没有达到预期，您可以尝试调整智能防御模式为严格模式。|
|黑白名单|对于已知的访问量较大的恶意IP，您可以将这类IP添加至黑名单，直接拦截其访问请求；对于企业内部办公网的IP段、业务接口调用IP或其它已确认正常的IP，您可以将这类IP添加至白名单，直接放行其访问请求。|
|黑洞解封|对于已加入新BGP高防防护的网站，如果因为其保底防护带宽或弹性带宽不足被突发大流量攻击造成黑洞，您可以在新BGP高防控制台使用黑洞解封来快速恢复业务。|
|流量封禁|当您遭遇特大流量攻击，且发现攻击流量有超过最大防护能力的趋势时，建议您考虑使用流量封禁，对新BGP高防IP实例中的电信/联通线路的海外流量实行主动封禁。|

1.  登录[云盾新BGP高防IP控制台](https://yundunnext.console.aliyun.com/?p=ddoscoo)。
2.  在左侧导航栏，单击**管理** \> **网站配置**。
3.  在网站配置列表中，定位到要操作的域名，单击其操作列下的**防护设置**。![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970145987_zh-CN.png)


4.  在防护设置页面，打开DDoS防护策略页签，根据需要执行以下操作： 
    -   **清洗模式** 

        定位到要操作的实例，单击操作列下的**修改智能防御模式**，并在修改智能防御模式对话框中选择一个清洗模式。支持的清洗模式包括：

        -   **宽松**：针对攻击特征显著的恶意IP进行防护，防护效果弱，误杀率低。
        -   **正常**：针对攻击特征明显、可疑的恶意IP进行防护，平衡防护效果及误杀率。
        -   **严格**：针对有攻击特征的请求IP进行防护，攻击防御效果强，但存在一定数量的误杀。
        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970245943_zh-CN.png)

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970245944_zh-CN.png)

    -   **黑白名单** 

        **说明：** 黑白名单的配置仅针对单个网站域名生效，而不是针对整个新BGP高防IP实例。

        单击**手动添加**，添加黑名单或白名单。具体操作请参见[网站访问黑白名单配置](cn.zh-CN/新BGP高防IP/用户指南/网络七层防护设置/设置网站访问黑白名单.md#)。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970245949_zh-CN.png)

    -   **黑洞解封** 

        对于处于黑洞状态下的实例，单击其操作列下的**解封**。具体操作请参见[黑洞解封](cn.zh-CN/新BGP高防IP/用户指南/网络四层防护设置/手动解除黑洞状态.md#)。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970245950_zh-CN.png)

    -   **流量封禁** 

        定位到要操作的实例，单击其操作列下的**封禁**，封禁电信或联通线路的海外流量。具体操作请参见[流量封禁](cn.zh-CN/新BGP高防IP/用户指南/网络四层防护设置/主动封禁海外流量.md#)。

        ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/188492/156133970245951_zh-CN.png)


