
https://pan.wepush.top


插件名字：HBB无后台推送+推送带图
作用：
1.实现多开wx无后台推送，即划掉app也可以正常接收推送消息
2.推送的时候显示推送详情
3.将本插件注入到Frameworks/ProtobufLite.framework/ProtobufLite的依赖中，可以激活微信Plugins组件的所有功能(要求appGroup权限至少4个，否则容易串号)
4.Frameworks只保留ProtobufLite.framework，其它的移到新建的文件夹，就可以用普通巨魔注入器注入了
注意：
如果安装了本插件，划掉后台后没有无后台推送，请按照下面方法处理
1.在iOS系统设置中找到当前多开，关闭消息通知并重新打开，然后启动app等待30秒后划掉，然后查看是否有推送
2.上述方法无用的情况下，请安装无后台推送检测插件

说明：
本插件只需要满足两个条件就可以实现无后台推送

1.推送证书签名-签名证书必须带推送能力

2.ipa的bundleId必须为下方指定的几个
com.tencent.xin (官替)
com.tencent.qy.xin (推荐)
com.tencent.wx (推荐)
com.tencent.mm.xin (只能dev开发证书签名)

强烈建议大家使用开发证书签名，适配的比较好
    开发证书 | 发布证书
xin| 支持   | 支持
qy | 支持   | 支持
wx | 支持   | 支持
mm | 支持   | 不支持

手机签名工具注入说明
注入路径选 @executable
注入目录选 Frameworks/
签名后移除embedded.mobileprovision 这个一定要关闭
App多开 这个一定要关闭

小科普
1.如何判断证书是否带推送能力
mobileprovision 中带 aps-environment 字段为推送能力

2.如何区分 开发证书 和 发布证书
证书中带Development的为开发证书
证书中带Distribution的为发布证书
或者
mobileprovision中搜索aps-environment
aps-environment后跟随 development 为开发证书
aps-environment后跟随 production 为发布证书

3.开发证书 和 发布证书 有啥区别
答：没区别


版本历史

配合声音+图像组件可以实现推送带图
版本号：8.1
发布日期:2025年06月14日
By：HBB
