# 网络概述
## 网络环境

[私有网络](http://docs.jdcloud.com/virtual-private-cloud/product-overview)（Virtual Private Cloud,VPC）为京东云为您提供自定义的逻辑隔离的网络空间，与您在数据中心搭建的传统网络类似，此私有网络空间由用户完全掌控，支持自定义网段划分、路由策略等。用户可以在VPC内创建和管理多种云产品，如云主机实例、负载均衡等，同时可配置网络内的资源连接Internet。另外，您可以通过VPN/专线接入，打通您的IDC内网和京东云网络，实现应用的混合云部署，以及应用的平滑迁移上云。

## 弹性公网IP

[弹性公网IP](https://docs.jdcloud.com/elastic-ip/product-overview)是可以独立申请的公网IP地址，支持与云主机实例、负载均衡等资源进行动态绑定和解绑。弹性公网IP的主要作用是屏蔽实例故障对外网访问服务的影响，通过手动配置的方式，当实例出现故障时弹性公网IP可以漂移到冗余实例上，从而达到快速响应故障的目的。

弹性公网IP支持带宽调整，可根据业务流量需求变化随时更改带宽，修改即时生效。支持包年包月、按配置和按用量三种计费类型，用户可根据实际业务需求选择合适的计费类型，同时提供共享带宽包，可实现多个IP资源的聚合计费和管理。

## 弹性网卡

[弹性网卡](http://docs.jdcloud.com/cn/elastic-network-interface/product-overview)是一种虚拟网络接口，您可以在实例上绑定弹性网卡以使实例接入不同网络。弹性网卡可以在构建业务流量分离、多业务承载以及网络高可用等应用场景时提供支持。

京东云提供无可用区属性弹性网卡，弹性网卡可以绑定私有网络内任意一台实例。单台实例可以绑定多块弹性网卡，绑定数量需依据实例规格而定。

## 网络访问

**公网访问**：京东云提供的弹性公网IP与您的账户关联，可以将其与同地域下的任意实例、NAT网关等资源关联，实现实例的外网访问，同时可根据网络实际使用情况调整带宽带宽、更改绑定实例。京东云为弹性公网IP提供最高2GB的免费DDoS防护，无间断抵御网络攻击。

**内网访问**：部署在京东云上的实例之间可以通过内网IP进行互访，不同地域、不同用户间的网络默认互相隔离，同地域下私有网络间的互访可通过VPC对等连接实现。

## 网卡多队列

单个vCPU处理网络中断存在瓶颈，您可以通过配置网卡多队列将实例中的网卡中断分散给不同的vCPU处理，提升网络处理性能。

## 相关参考

[私有网络](http://docs.jdcloud.com/cn/virtual-private-cloud/product-overview)

[弹性公网IP](https://docs.jdcloud.com/elastic-ip/product-overview)

[弹性网卡](http://docs.jdcloud.com/cn/elastic-network-interface/product-overview)

