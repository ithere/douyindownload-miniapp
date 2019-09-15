# douyindownload-miniapp
mosousuo.com 抖音视频去水印微信小程序
### 解析接口是普通接口只能解析短视频
#### 其中用到了读取剪辑版数据和相册保存
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
git源码地址: [https://github.com/ithere/douyindownload-miniapp](https://github.com/ithere/douyindownload-miniapp)
![mosousuo](https://github.com/ithere/douyindownload-miniapp/blob/master/mosousuo_1.png)
