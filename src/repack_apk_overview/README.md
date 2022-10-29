# 重新打包apk概览

[Android逆向开发](https://book.crifan.org/books/android_reverse_dev/website/)期间，经常会涉及到，给安卓的apk重新打包。

* Android重新打包apk
  * 主要流程：用逆向工具(`Apktool`等)反编译apk，得到各种资源和文件，编辑相关的内容，再用工具(`Apktool`等)重新打包成apk。
  * 期间涉及
    * 逆向工具：`Apktool`等
    * 重签名：签名和证书等
    * 优化：对齐等
  * 典型用途
    * 正向
      * 汉化
      * 技术研究和学习
    * 逆向
      * 破解
        * 免会员
        * 去广告
      * 黑灰产
        * 加上广告 -> 重新分发 -> 广告引流，挣钱
        * 加上病毒 -> 恶意事件：盗取数据，勒索等
