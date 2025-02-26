## 群组空间

在首页，左侧菜单栏的**群组列表**，展示您所参与的群组，选择您要查看的群组名称，即可查看该群组下的仓库，群组成员，以及群组活动，该群组的Owner 或者Master可以对群组进行设置。
![img](../../All-Image/team.assets/team_new.jpg)

### 新建群组

1. 点击菜单栏右上方的➕，选择**新建群组**，即可新建群组。如上图：

2. 在新建群组界面，填写**群组名称**，**群组描述（可选项）**，选择相应的**访问级别**；

>[!Note|label:说明]
>
>1. 群组名称：是群组中的唯一标识，创建群组后，将不能修改。命名规则：可由字母（不区分大小写）、数字、点、中划线，下划线随机组合，且必须以字母或数字开头、结尾。

>2. 群组负责人：默认将创建者设置为群组的owner，并赋予master权限。

>3. 访问级别：根据代码群组的实际情况设置访问级别。

![img](../../All-Image/team.assets/new_team1.jpg)

3. 点击**创建群组**，即可完成创建。

### 群组仓库列表

在首页，选择您要查看的群组，进入群组后，默认展示该群组的**仓库**信息，您可以通过输入仓库名称来查找您想查看的仓库，点击仓库地址即可进入仓库。如果您的群组还未创建代码仓库，点击**新建仓库**即可。

![img](../../All-Image/team.assets/team_repo.jpg)

### 群组成员

在群组空间内，点击**成员**页签，即可查看该群组下的所有成员信息，以及成员在群组中的角色信息。

* 如果该群组下成员见多，您可以通过输入成员ERP来查找群组成员。
* 如果您所负责的业务发生了变化，不再为该群组下的代码贡献代码，可以点击**离开**，退出该群组。
* 如果您该群组的Owner时，请在**设置**页签，**高级设置**中先将该群组移交给群组下的某个成员，然后在成员设置，或者群组成员中退出即可

![img](../../All-Image/team.assets/team_member.jpg)

### 群组活动

在群组空间内，点击**活动**页签，即可查看该群组下的所有代码库的操作记录（比如：代码库的提交情况，评审情况和代码库的成员变化等），群组团队成员的变化情况，以及该群组本身设置的操作记录。

### 群组设置

在群组空间内，点击**设置**页签，即可对该群组的通用信息，群组成员，以及高级设置。

#### 通用设置

在**通用设置**界面，您可以对群组的描述信息，以及访问级别进行设置，设置完成后，点击**保存设置**即可。

>[!Note|label:说明]
>
>1. 群组名称是群组的唯一标识，创建完成后，将不能修改。

>2. 目前群组的访问权限，默认是公开，暂时无法设置权限，正在开发，敬请期待

![img](../../All-Image/team.assets/team_setting1.jpg)

#### 成员设置

>[!Note|label:说明]
>
>1. 群组成员角色权限定义与仓库成员角色权限一致：
>
>* Master：可以添加tag、管理分支、仓库设置、克隆、提交、拉取代码。
>* Developer：可以克隆、提交、拉取代码。
>* Visitor：只能浏览代码。

>2. 仓库成员角色与群组成员角色的关系：当用户在群组和仓库中同时增加了角色权限，则以仓库中的设置为准。

1. 在群组空间内，点击**设置**按钮，点击左侧的**群组成员**菜单，即进入群组成员管理页面。

2. 在成员管理界面，您可以对成员进行以下操作：
   * 增加成员，在erp输入框和角色输入框分别输入erp和角色，点击添加按钮，即可添加群组成员。
   * 修改成员角色，点击成员列表右侧角色下拉列表，即可修改成员角色。
   * 删除仓库成员，点击成员列表右侧移除按钮，即可删除仓库成员。
     ![img](../../All-Image/team.assets/team_setting2.jpg)



#### 高级设置

高级设置中，您可以将本群组的负责人转移到群组下的其他成员，也可以删除该群组。


>[!Tip|label:高级设置，只有群组的负责人有操作权限.]

#### 转移群组

>[!Note|label:说明]
>您可以将群组负责人转移群组下的任何一位成员，转移操作完成后，您还在该群组下，同时被赋予"Master"权限。

高级设置中，在选择要接收群组的成员。点击**转移群组**，在弹出框中，再次输入群组名称，点击**确认**，即可完成群组的转移操作。
![img](../../All-Image/team.assets/team_setting3.jpg)

#### 删除群组

>[!Danger|label:删除操作无法恢复！]
>
>1. 删除群组将会连同其相关的所有数据（包括 群组成员）一起删除。

>2. 如果群组下有仓库存在，则无法删除群组。

高级设置中，点击**删除群组**，在弹出框中，再次输入群组名称，点击**确认**，即可完成群组的删除操作。

![img](../../All-Image/team.assets/team_setting4.jpg)

