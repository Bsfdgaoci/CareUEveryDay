# 由于最近请求量过多 该秘钥被高德封禁了 后续大家只能使用自己的高德秘钥啦

## 近日发现代码中的高德地图的配额每天几乎都超限了(一天5000配额)..建议大家申请自己的高德地图秘钥进行使用 避免因为超限导致的调用失败
[点我进入高德开放平台](https://lbs.amap.com)  进行申请，申请成功后大家修改 `/src/main/java/cn/ofpp/core/GaodeUtil.java` 这个文件中的key为自己申请的key即可


最近在抖音上的看到挺多人发的
然后就自己随便做了一个玩了一下

本项目不需要服务器
基于Github Actions实现每天固定运行一次

`友情提示： 本分支支持推送响应`

博客可能有些慢 我将内容移植到了语雀笔记 国内访问会很快
[点击访问语雀笔记](https://www.yuque.com/docs/share/66a239d8-f272-4a90-81bc-b2f5e30ccce6#3cfdeb22)

为了照顾小白，特地写了一篇完整详细的详细教程放到了我的博客以供参考
[点击访问我的博客](https://blog.ofpp.cn)

由于 博客服务器托管在GitPage节点在国外且前段时间cdn到期了 可能会访问比较慢～

 
 
#### 公众号模板内容 可以根据自己的需要变更内容
```text
你叫{{friendName.DATA}}
今年{{howOld.DATA}}
距离下一次生日{{nextBirthday.DATA}}天
具体我们的下一次纪念日{{nextMemorialDay.DATA}}天
现在在{{province.DATA}}{{city.DATA}}
当前天气{{weather.DATA}}
当前气温{{temperature.DATA}}
风力描述{{winddirection.DATA}}
风力级别{{windpower.DATA}}
空气湿度{{windpower.DATA}}
{{author.DATA}}
{{origin.DATA}}
{{content.DATA}}
```
其中
```text
{{author.DATA}}
{{origin.DATA}}
{{content.DATA}}
```
是古诗的变量，如果`Bootstrap`中配置未开启随机古诗 那么这三个就是不要的


#### 核心类介绍

```
Application.java          // 启动类
Bootstrap.java            // 一些启动配置(公众号信息在这里配置)
core/MessageFactory.java  // 创建微信消息对象的代码就在这里面 有需要可以自己修改下变量
```
