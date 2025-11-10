# 前言

随着移动设备的普及，短视频应用已经成为人们日常生活中不可或缺的一部分。本项目是基于微信小程序的短视频系统，采用SSM框架（Spring、Spring MVC、MyBatis）进行开发。下面将为您详细介绍本项目的相关内容。

# 内容介绍

本项目主要实现了短视频的拍摄、上传、浏览、评论、点赞等基本功能。用户可以通过微信小程序轻松访问，浏览各类有趣的短视频内容。同时，系统后台提供了强大的管理功能，方便管理员对短视频内容进行审核、发布、删除等操作。

# 技术介绍

## 语言：Java
## 使用框架：Spring、Spring MVC、MyBatis，微信小程序
## 前端技术：JS、Vue、CSS3，Uniapp
## 开发工具：IDEA/Eclipse，Uniapp
## 数据库：MySQL 5.7/8.0
## 数据库管理工具：phpstudy/Navicat
## JDK版本：jdk1.8
## Maven：apache-maven 3.8.1-bin
## 前端环境：Node.Js 12\14\16

# 核心代码

以下是本项目中的一个核心代码片段，展示了如何实现短视频的点赞功能：

```java
// 短视频点赞接口
@RequestMapping("/likeVideo")
@ResponseBody
public String likeVideo(@RequestParam("videoId") int videoId, HttpSession session) {
    // 从session中获取当前用户
    User user = (User) session.getAttribute("user");

    if (user != null) {
        // 查询当前用户是否已经点赞过该视频
        VideoLike videoLike = videoLikeService.findByUserIdAndVideoId(user.getId(), videoId);

        if (videoLike == null) {
            // 如果没有点赞过，新增点赞记录
            videoLikeService.addLike(user.getId(), videoId);
            // 更新视频的点赞数
            videoService.updateLikeCount(videoId, 1);
            return "success";
        } else {
            return "alreadyliked";
        }
    } else {
        return "nologin";
    }
}
```

# 免费源码获取

```
5000套系统成品在线演示视频，复制到流浪器： 
```
```
https://www.yuque.com/yuqueyonghux32e1j/kxdc9g/ad8oz3bamkxmay0e#Cxun
```
![下载](https://img12.360buyimg.com/ddimg/jfs/t1/339687/11/1349/28408/68ad865fF412d7877/adaa650483a100f2.jpg)

# 项目截图
![封面图片](https://img10.360buyimg.com/ddimg/jfs/t1/335057/35/12964/84824/68c6258dF6653a30d/bbedfc30f994b26e.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/350104/21/3105/31040/68c62565F5d571f95/be94eead49675ac3.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/337980/17/10600/13158/68c62565F7e1be995/b2e88da2054d35ca.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/324660/33/19484/30757/68c62565F407e849f/55de6768c870c292.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/326160/36/19819/18860/68c62566Fbf9f56a5/38b3d1e750b2fdc6.jpg)

![介绍图片](https://img10.360buyimg.com/ddimg/jfs/t1/334996/28/13078/14800/68c62566F07306b86/6ab881024227c9e2.jpg)

![介绍图片](https://img14.360buyimg.com/ddimg/jfs/t1/350459/39/2969/86313/68c62566Fb79d004f/b92ce30fdc366310.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/337958/23/7508/40885/68c62567Fedf24d1d/facb97f4cf717ce6.jpg)

![介绍图片](https://img13.360buyimg.com/ddimg/jfs/t1/330634/4/12960/47054/68c62567Fca71eefb/0d868d54208b7fd7.jpg)

![介绍图片](https://img12.360buyimg.com/ddimg/jfs/t1/325791/12/19763/90178/68c62568Fe90acfed/e39f553d092996a7.jpg)


## 万字文档
![文档介绍](https://img14.360buyimg.com/ddimg/jfs/t1/338393/1/3576/156947/68b1ad0cF74dc525c/ff9cd6c574295685.jpg)
