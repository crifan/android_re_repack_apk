# Android逆向：重新打包apk

* 最新版本：`v0.8`
* 更新时间：`20230713`

## 简介

介绍Android逆向开发期间，如何重新打包apk。先是安卓apk重新打包的概览；然后详细介绍重新打包apk的典型流程，包括apk解包、改动、重新打包apk、重签名、对齐，最后确认成功；期间涉及常用工具apktool、签名相关的keytool、jarsigner、apksigner、优化相关的对齐工具zipalign；然后总结常见问题和相关心得；

## 源码+浏览+下载

本书的各种源码、在线浏览地址、多种格式文件下载如下：

### HonKit源码

* [crifan/android_re_repack_apk: Android逆向：重新打包apk](https://github.com/crifan/android_re_repack_apk)

#### 如何使用此HonKit源码去生成发布为电子书

详见：[crifan/honkit_template: demo how to use crifan honkit template and demo](https://github.com/crifan/honkit_template)

### 在线浏览

* [Android逆向：重新打包apk book.crifan.org](https://book.crifan.org/books/android_re_repack_apk/website/)
* [Android逆向：重新打包apk crifan.github.io](https://crifan.github.io/android_re_repack_apk/website/)

### 离线下载阅读

* [Android逆向：重新打包apk PDF](https://book.crifan.org/books/android_re_repack_apk/pdf/android_re_repack_apk.pdf)
* [Android逆向：重新打包apk ePub](https://book.crifan.org/books/android_re_repack_apk/epub/android_re_repack_apk.epub)
* [Android逆向：重新打包apk Mobi](https://book.crifan.org/books/android_re_repack_apk/mobi/android_re_repack_apk.mobi)

## 版权和用途说明

此电子书教程的全部内容，如无特别说明，均为本人原创。其中部分内容参考自网络，均已备注了出处。如发现有侵权，请通过邮箱联系我 `admin 艾特 crifan.com`，我会尽快删除。谢谢合作。

各种技术类教程，仅作为学习和研究使用。请勿用于任何非法用途。如有非法用途，均与本人无关。

## 鸣谢

感谢我的老婆**陈雪**的包容理解和悉心照料，才使得我`crifan`有更多精力去专注技术专研和整理归纳出这些电子书和技术教程，特此鸣谢。

## 其他

### 作者的其他电子书

本人`crifan`还写了其他`150+`本电子书教程，感兴趣可移步至：

[crifan/crifan_ebook_readme: Crifan的电子书的使用说明](https://github.com/crifan/crifan_ebook_readme)

### 关于作者

关于作者更多介绍，详见：

[关于CrifanLi李茂 – 在路上](https://www.crifan.org/about/)
