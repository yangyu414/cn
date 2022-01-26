# 放行回源IP

此步骤仅针对源站有安全防护策略例如使用防火墙/安全组/ACL/iptable的用户，**不是必须步骤**。
<Br/>若您的源站配置了安全防护策略，为了保证不对DDoS IP高防的服务产生影响，请将DDoS IP高防的回源IP加入白名单。

## 前提条件
- 已成功购买了DDoS IP高防，且计费状态正常。

## 操作步骤
1. 登录 [DDoS IP高防 控制台](https://ip-anti-console.jdcloud.com/instancelist)。
2. 在“实例列表”页面，选择目标实例，点击 **实例名称** 或**转发配置**，进入实例详情页面。
![网站类实例](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/non-web%2004.png)
3. 请在下图红框处所示，获取需要加入白名单的DDoS IP高防回源IP段。
![高防回源](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/instance06.png)
## 相关参考

- [入门概述](Overview.md)
- [创建实例](Create-Instance.md)
- [非网站类规则](Non-Web-Service-Forwarding-Rule.md)
- [网站类规则](Web-Service-Forwarding-Rule.md)
- [计费规则](../Pricing/Billing-Rules.md)

###测试视频播放
!{video}[ src="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/0860c194-bc12-4434-a3ad-95c9c172b65220200109153030.mp4",width="300",height="500",controls="controls", preload="auto",autoplay="autoplay",x5-video-player-type="h5",poster="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/b8923ecf-4a19-4e66-98e3-1d847604a86620200109154726.jpg" ]
