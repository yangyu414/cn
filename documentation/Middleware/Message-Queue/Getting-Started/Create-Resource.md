# 创建资源
在消息队列 JCQ中，消息的生产和消费需要通过主题订阅的形式，故用户首先要创建消息主题（topic），发送消息到某个指定的消息主题，而消费者通过订阅该消费主题进行消息消费。

## 前提条件
- 已注册京东云账号，并完成实名认证，且保证账户处于正常状态，没有在黑名单中。如果还没有账号请 [注册](https://user.jdcloud.com/register)，并 [实名认证](https://uc.jdcloud.com/account/certify)。
- 因为产品的计费类型为按用量计费，请确认您的账户不能处于欠费状态。

## 注意事项
- 用户默认在一个region最多只能创建10个topic，如有需要可以提工单增加。
- 对于某个topic的订阅Consumer Group数量没有限制。

## 步骤一：创建消费主题

1. 进入京东云控制台，菜单互联网中间件-消息队列 JCQ-Topic管理；
2. 首先选择想要创建资源的区域（比如华北），然后点击“新建”按钮，创建topic；
3. 选择Namespace，在指定Namespace下创建Topic,可缺省；
4. 创建topic中需要填写“topic名称”和备注信息；
5. 指定Topic类型：若您使用JCQ的SDK或OpenAPI接入服务则Topic类型选择JCQ，若您使用RocketMQ客户端接入服务则Topic类型选择RocketMQ;
6. 指定消息类型：选定Topic类型后，选择该Topic类型下，使用的消息类型，根据Topic类型不同，消息类型有不同。

### 说明：

1. 不同的Namespace下面的Topic允许重名, Topic的名称在用户Namespace内唯一。若用户创建Topic时未指定Namespace，则服务会将该Topic创建在默认default的Namespace下。
2. Namespace名称长度 3-100 个字符，支持字母、数字、连字符(-)、下划线(_)。
3. topic名称为全局唯一或用户Namespace下唯一，如果有相同名称的topic被创建，则无法创建成功。Topic命名长度 3-100 个字符，支持字母、数字、连字符(-)、下划线(_)。
4. 消息类型：
- 普通消息：不保证先入先出（FIFO）的顺序消费，包含普通消息和延时消息。
- 全局顺序消息：消息的生产和消费按照消息的发布顺序进行（FIFO）。
- 分区顺序消息：消息根据Sharding Key进行分区，同一个分区的消息将严格按照先入先出的方式进行顺序发布和顺序消费，可以提高并发度和整体性能。
- 事务消息：事务消息提供类似 X/Open XA 的分布事务功能，通过事务消息能达到分布式事务的最终一致。

## 步骤二：添加订阅

1. 在Topic管理页面中，找到想要订阅的topic，在操作中可以选择订阅。
2. 在添加订阅者中需要新建/绑定已有Consumer Group ID。
3. 填写取出消息隐藏时长、死信队列设置和最大接收次数等参数，如果无特殊需求可保持默认配置不变。

### 说明：

1. Consumer Group ID为全局唯一，如果有相同名称的Consumer Group ID被创建，则无法创建成功。并且Consumer Group ID只能包含字母、数字、连字符(-)和下划线(_)，长度7-64字符。
2. Consumer Group ID 和topic的关系是多对多关系（N：M），同一个Consumer Group ID可以订阅多个topic，同一个topic可以对应多个Consumer Group ID。
3. 取出消息隐藏时长为接收的消息对于其他消费者不可见的时间长度，范围：30秒-600秒 。
4. 死信队列设置参数决定是否开启topic的死信队列。
5. 最大接收次数是将消息发送到死信队列之前允许接收该消息的最大次数，范围：0-16次。

## 步骤三：创建 AccessKey和 SecretKey
在调用消息队列 JCQ的SDK或者openAPI进行消息的发送消费和管理操作时候，还需要验证用户的身份信息，即需要在控制台创建AccessKey和 SecretKey。
### 创建方法：
在京东云用户中心账户管理下的[AccessKey管理页面](https://uc.jdcloud.com/account/accesskey)申请AccessKey和SecretKey密钥对（简称AK/SK）。
AK/SK信息请妥善保管，如果遗失可能会造成非法用户使用此信息操作您在云上的资源，给你造成数据和财产损失。AK/SK密钥对允许启用、禁用，启用后可用其调用OpenAPI，禁用后不能用其调用OpenAPI。
