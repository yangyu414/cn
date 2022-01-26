# 黑白名单配置
非网站类防护规则中如需针对每条四层转发规则配置黑白名单，需引入转发配置中的[IP黑/白名单库](../../../../../documentation/Cloud-Security/Anti-DDoS-Pro/Operation-Guide/Blacklist-And-Whitelist-Settings.md)。</BR>
配置前，需要定位到非网站转发规则处，步骤如下：
- 首先需要登录 [DDoS IP高防 控制台](https://ip-anti-console.jdcloud.com/instancelist)。
- 找到需要配置的实例，单击实例名称，进入 **实例详情** 页面。
- 切换到 **非网站转发配置** 
   ![非网站转发规则](../../../../../image/Advanced%20Anti-DDoS/net-service-protection-rule-03.png)


### 操作步骤
1. 单击 **防护规则** ，进入非网站类防护规则界面，开启黑/白名单开关。</BR>
 ![非网站防护规则](../../../../../image/Advanced%20Anti-DDoS/net-service-protection-rule-06.png)
2. 选择IP黑/白名单库中创建的黑/白名单规则，点击确定。</BR>
 ![非网站防护规则](../../../../../image/Advanced%20Anti-DDoS/net-service-protection-rule-07.png)
3. 单击编辑图标可修改引用的黑/白名单规则。</BR>
 ![非网站防护规则](../../../../../image/Advanced%20Anti-DDoS/net-service-protection-rule-08.png)


###测试视频播放
!{video}[ src="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/0860c194-bc12-4434-a3ad-95c9c172b65220200109153030.mp4",width="300",height="500",controls="controls", preload="auto",autoplay="autoplay",x5-video-player-type="h5",poster="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/b8923ecf-4a19-4e66-98e3-1d847604a86620200109154726.jpg" ]
