# iOS/Flutter开发工程师

## 个人信息

* 张鹏辉,男,1995年
* 工作年限：4年/本科
* 技术博客：https://juejin.cn/user/2101921961221943/posts
* Github：https://github.com/semperhhh
* 到岗时间: 2~4周

## 联系方式

- 手机：17600115409
- Email：zphui5409@163.com
- 微信号：zhishuxinqing

## 工作经历

### 河北苏米互动科技有限公司(2021年11月~2022年3月)

* 责任描述: 任职期间负责云听App和VideoDownloaderApp的iOS端开发任务

[云听](https://apps.apple.com/cn/app/id496145505)

1. 使用Objective-C完成UI开发, 埋点统计等;
2. 负责云听6.38.0版本的云医模块的开发任务;
3. 负责云听6.37.0版本的音频圈子的开发任务;

[VideoDownloader]

1. 项目主要使用Swift进行开发,混编部分Objective-C三方库;
2. 使用IJKPlayer完成App的视频播放开发任务并封装视频控制层manager;
3. 使用AVAudioPlayer完成App的音频播放开发任务并封装音频控制层;

### 石家庄友曼科技有限公司(2020年10月~2021年11月)

* 责任描述: 任职期间负责游民星空App的iOS端开发任务.

[游民星空](https://apps.apple.com/cn/app/you-min-xing-kong/id886118205)

1. 负责游民星空线上5.0版本的更新迭代和维护.游民星空体验版6.0的重新架构和开发任务.迁移5.0功能,和中间微服务端配合对接.
2. App使用MVVM作为架构基础,同时导航模式使用URL路由方案架构.内容页可以导航到任意一个其他的页面.这种路由架构以内容和体验为导向,以解耦为目标.
3. 开发App的Dark模式,和UI设计配合完善Dark模式的开发规范.

### 北京中体联合数据科技有限公司 (2019年2月 ~ 2020年10月)

> 移动端app是针对健身房会员的会员端以及健身房教练和店主的私教端. 

* 责任描述: 任职期间与同事合作开发练多多会员端2.0、场馆端2.0的iOS客户端; 独自负责光猪圈会员端、私教端的iOS版本,与产品经理的沟通评审与迭代更新,配合pc端saas系统,上线了霸王卡、通店卡、到店红包以及微信连续包月卡等业务需求;

[光猪圈健身APP](https://apps.apple.com/cn/app/光猪圈健身/id1027673267)

1. 使用Objective-C开发,封装的网络日志工具类,方便测试同事定位问题;
2. 解决App开屏广告加载时的白屏问题;
3. 使用Runtime封装TableView的空数据状态展示,修改ViewController中View类的isa指向,监听View的点击事件;
4. 完善iOS同组代码开发规范,代码合并以及版本发布;

[光猪圈教练APP](https://apps.apple.com/cn/app/光猪圈教练/id1180466459)

1. 项目使用Objective-C,后期新的业务功能开始汇编Swift;
2. 下拉界面dropMenu界面根据产品需求点击任意地方即收回,采用object_setClass动态创建UIView的子类替换ViewController的view,使用自定义的HitTest方法监听view的点击时间并发送相应的通知
3. 汇编导致项目结构混乱,尝试分离基础模块,采用NSClassFormString初步分离业务模块.

练多多会员端2.0

1. Swift 作为项目主语言,混编部分Objective-c库,负责 [练多多场馆端2.0] 的私教会员模块以及 [练多多会员端2.0] 50%的开发任务,和同事合作完成app开发;
2. 学习Swift,使用Swift语言的特性减少了客户端crash的发生率;Struct代替原本的Class模型,使用SwiftyJSON转换;利用计算属性扩展String等;


### 北京多友科技有限公司 （ 2016年5月 ~ 2019年2月 ）

> 多友科技是一家网络营销与在线客服工具提供商.移动端app方向是电商平台和即时通讯及对应的SDK.

* 责任描述: 负责Talk99的iOS版本迭代更新及相应SDK的功能开发与维护;

[Talk99](https://apps.apple.com/cn/app/talk99/id702672310)

1. 负责 Talk99 的iOS端开发与维护,与Boss交流项目需求,与服务端共同制定前后端所需数据结构及开发任务;

2. 负责公司SDK日常开发与维护,与售后技术工程师交流不同客户需求,开发不同定制版本SDK,封装原生UI视图供客户App自定义SDK调用以实现个性化,编写相应的技术文档;

3. talk99及SDK核心模块是即时通讯IM,使用WebSocket编写聊天功能组件;使用FMDB进行数据持久化开发;使用CellModel中间层提前计算不同类型聊天消息的宽高,避免重复计算,同时提升列表滑动流畅性.

## 个人分享

[Flutterapp](https://github.com/semperhhh/zhishu_card) :

1. 个人app项目,记录时间的app,使用 Flutter 进行开发,实现iOS和Android双端同时开发;
2. 使用 sqflite 数据持久化完成主要功能, flutter_screenutil 屏幕适配iphone和ipad;
3. 封装自定义的弹窗Widget,了解Flutter的工厂模式;
4. 通过项目了解熟悉Flutter框架,了解Flutter布局模式和 Dart 语言特性;

[SemmmProject](https://github.com/semperhhh/SemmmProject) :

1. 个人博客项目,原基于Swift的Perfect框架的服务端(项目链接:[SemperProject](https://github.com/semperhhh/SemperProject));
2. 使用MySQL记录数据,nginx作反向代理服务及一些基于Mustache的动态html界面,css样式大部分引用bootStrap.
3. 后选择将后台迁移成node.js,html++css+vue实现页面展示,前后端分离.
4. 通过项目学习Swift语言特性及后端知识,对后端,数据库有个概念,工作中可以更好地和后台配合.过程受益大于产出结果.

[iOS-控件封装为framework来使用](https://juejin.im/post/5c0a117be51d4538994af76b) :

记录封装自定义控件为framework静态库使用总结的过程,添加.bundle文件资源以及通过简单的lipo命令合并.a文件使兼容模拟器和真机的文章.

## 技能特长

* 主要开发语言为Objective-C,Swift;
* 了解Flutter语言,使用Flutter开发个人项目;
* 了解前端开发,有个人博客搭建项目;
* 追求工作效率,熟悉git等多人协作开发工具;

- - -

## 致谢

感谢您花时间阅读我的简历，期待能有机会和您共事。
      
