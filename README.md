# qqmsg4l
windows下qq收到新消息时通过http协议+html5推送提醒, 特别适合在linux下工作，同时虚拟机运行windows跑qq的码农
实现原理是通过JNA调用Windows API `GetWindowTextA` 和 `GetClassNameA`

![](https://raw.githubusercontent.com/binaryer/qqmsg4l/master/2016-12-21-110112_1920x1080_scrot.png)

## Usage
### 1. 安装服务端
把 `qq_notice.jsp` 和 `zepto.min.js` 复制到tomcat webapps目录

### 2. 设置QQ  
选中 `允许来消息时自动弹出窗口`

![](https://raw.githubusercontent.com/binaryer/qqmsg4l/master/qqsetting.png)

### 3. windows下运行消息推送端
__Requires Java >= 7__
```bash
# x.x.x.x为步骤1的服务端地址
java -jar qq_notice.jar http://x.x.x.x/qq_notice.jsp
```

### 4. linux下运行消息接收端  
用支持HTML5的浏览器访问 http://x.x.x.x/qq_notice.jsp, QQ收到新消息时会弹出提示


## Author
林春宇@深圳  
chunyu_lin@163.com

## Download
https://github.com/binaryer/qqmsg4l/releases
