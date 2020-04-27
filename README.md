# douyindownload-miniapp
##### mosousuo.com 抖音视频去水印微信小程序 记得替换你的appid
### 解析接口是普通接口只能解析短视频
#### 其中用到了读取剪辑版数据和相册保存
#### download 合法域名设置 [https://mp.weixin.qq.com/s/i6ORVdV9tfRjeG3uOirS1A](https://mp.weixin.qq.com/s/i6ORVdV9tfRjeG3uOirS1A)
> 小程序后台先加入合法域名 https://v.ataobao.vip
##### 剪辑版数据
```
    wx.getClipboardData({
      success: res => {
        var str = res.data.trim()
        if (str) {
          that.setData({
            defaultUrl: str
          })
        }
      }
    })
    wx.setClipboardData({
      data: '',
    })
```
##### 保存相册视频
```
wx.saveVideoToPhotosAlbum({
   filePath: file.tempFilePath,
   success: function (o) {
       t.showToast('保存成功', 'success'), setTimeout(function () {
           wx.setClipboardData({
             data: '',
           })
           that.goBack()
       }, 1000)
   },
   fail: function (o) {
       that.showToast('保存失败')
   }
})
```
###### git源码地址: [https://github.com/ithere/douyindownload-miniapp](https://github.com/ithere/douyindownload-miniapp)

###### 增加个交流群
![mosousuo](https://ae01.alicdn.com/kf/H88ac10f6811c40fa99f6745074fb9637e.jpg)

###### demo和本程序使用的是一个接口
![mosousuo](qrcode_ms.jpg)

![mosousuo](mosousuo_1.png)

