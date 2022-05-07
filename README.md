# Ding-dongMonitor
叮咚运力监控，监控叮咚首页公告信息获取当前运力情况与货品有货情况，通过bark app通知到手机。本工具不需要抓包，只需要获取经纬度坐标即可  
经纬度获取： https://lbs.amap.com/tools/picker  

# 更新
### 2022-5-7 405问题修复
# 运行效果  

<img width="361" alt="image" src="https://user-images.githubusercontent.com/13680422/167243237-59933c2d-867b-48a5-8fc8-5cb76a65732d.png">



# 使用说明
1. 自己使用Charles、Fiddler等工具对叮咚买菜小程序、App抓包，获取config.yaml中需要的参数。
2. 不想抓包或者不会抓包可以直接在配置文件填写家里的经纬度。经纬度获取： https://lbs.amap.com/tools/picker
3. 不想build可以直接下release包 https://github.com/czqu/dingdongMonitor/releases
# 运行
目前提供两种方式运行，
### 本机运行
##### 构建:
```
go build
```
##### 运行:
1.将config.example.yaml改名为config.yaml  
2.根据提示设置配置文件  
3.直接打开程序运行。在本机将根据配置文件设置的频率在未登录的情况下访问叮咚首页信息，设置过于频繁可能会导致**封IP**  
#### GitHub Action运行
1.fork本仓库  
2.将config.example.yaml改名为config.yaml，设置好所需信息  
3.根据monitor.yml设置好相应的secrets,并解除注释  
monitor.yml配置方法参见：  
[GitHub Actions文档 - GitHub Docs](https://docs.github.com/cn/actions)  
[Crontab.guru - The cron schedule expression editor](https://crontab.guru/)   
填好之后大概是这样的，不懂yaml格式的可以看看(隐私信息已做处理)： 
<img width="544" alt="image" src="https://user-images.githubusercontent.com/13680422/167242543-94519c6c-90a5-4564-89cb-02cac0474436.png">

