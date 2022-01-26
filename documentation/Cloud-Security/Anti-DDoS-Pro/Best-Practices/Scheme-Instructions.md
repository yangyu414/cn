# DDoS IP高防结合应用安全网关方案说明

DDoS IP高防+应用安全网关在不增加额外性能开销的情况下，为京东云用户提供全面的安全防护。

# 部署架构
![部署架构](https://github.com/jdcloudcom/cn/blob/edit/image/Advanced%20Anti-DDoS/Best-Practice03.png)<Br/>
DDoS IP高防+应用安全网关的最佳部署架构如下：
- 京东云的安全调度中心，通过DNS解析，将用户域名解析到DDoS IP高防CNAME。
- 用户正常访问流量和DDoS攻击流量经过DDoS IP高防清洗，回源至京东云私有网络负载均衡集群。
- 应用安全网关部署在负载均衡上，负责Web应用层安全防护。
- 应用安全网关与负载均衡绑定，即可以防御来自互联网的攻击，也可防御来自VPC内部的攻击。

# 方案优势
1. 应安全网关为用户提供独享资源，动态扩容，规则独立定制，无相互影响。
2. 应用安全网关无需依赖DNS调度，无额外带宽资源消耗，网络延时低于1ms。
3. HTTPS证书保存在用户VPC内部，外网无法监听和窃取。
###测试视频播放
!{video}[ src="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/0860c194-bc12-4434-a3ad-95c9c172b65220200109153030.mp4",width="300",height="500",controls="controls", preload="auto",autoplay="autoplay",x5-video-player-type="h5",poster="//jdcloud-portal.oss.cn-north-1.jcloudcs.com/video/b8923ecf-4a19-4e66-98e3-1d847604a86620200109154726.jpg" ]
