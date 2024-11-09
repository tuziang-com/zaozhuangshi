# 枣庄市专业技术人员继续教育刷课脚本


## 脚本

学习网站：枣庄市专业技术人员继续教育：http://zzzj.yxlearning.com/

脚本地址：[枣庄市专业技术人员继续教育-刷课脚本][2]

## 教程

浏览器安装篡改猴插件后，打开[脚本安装地址][2]，进入后点击安装脚本，安装完成刷新你的学习网页就可以愉快使用了。

## 联系

注：如果需要代学，可以联系我微信yizhituziang或者QQ2422270452

![微信二维码](https://www.tuziang.com/wx.jpg)

## 更多

关键代码分享：
```

  if (location.href.indexOf("/learning/index") != -1) {
    setInterval(function () {
      var video = document.querySelector("video")
      if (video) {
        video.muted = true
      }
      if (video && video.paused) {
        video.play()
      }
      if (video && video.ended) {
        nextVideo()
      }
    }, 1000)
  }

  // 播放下个未完成的视频
  function nextVideo() {
    for (let i = 0; i < document.querySelectorAll(".videoLi").length; i++) {
      let item = document.querySelectorAll(".videoLi")[i]
      if (item.innerHTML.indexOf("icon-dagouyouquan") == -1) {
        item.click()
      }
    }
  }
```


  [1]: https://microsoftedge.microsoft.com/addons/detail/%E7%AF%A1%E6%94%B9%E7%8C%B4/iikmkjmpaadaobahmlepeloendndfphd?refid=bingshortanswersdownload
  [2]: https://greasyfork.org/zh-CN/scripts/508810-%E6%9E%A3%E5%BA%84%E5%B8%82%E4%B8%93%E4%B8%9A%E6%8A%80%E6%9C%AF%E4%BA%BA%E5%91%98%E7%BB%A7%E7%BB%AD%E6%95%99%E8%82%B2%E5%88%B7%E8%AF%BE%E8%84%9A%E6%9C%AC
