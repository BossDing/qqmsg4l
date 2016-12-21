# qqmsg4l
windows下qq收到新消息时提醒linux, 特别适合虚拟机环境linux host + windows guest

## 使用步骤 
### 1. 安装服务端
把 `qq_notice.jsp` 和 `zepto.min.js` 复制到tomcat webapps目录

### 2. 设置QQ  
选中"允许来消息时自动弹出窗口"

### 3. windows下运行消息推送端
```bash
java -jar qqnotice.jar http://x.x.x.x/qq_notice.jsp
```

### 4. linux下运行消息接收端  
用支持HTML5的浏览器访问 http://x.x.x.x/qq_notice.jsp
