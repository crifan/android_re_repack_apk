# 确认成功

TODO：

* 【记录】对比确保apktool重新打包的YouTube的apk可以正常安装和使用
* 【已解决】给腾讯乐固加固的安卓app脱壳后重新打包apk的逻辑和思路

---

* 验证重新打包apk成功
  * 用jadx反编译
    * 看看是否能成功反编译，看到源码
  * 用aapt查看apk信息
    ```bash
    aapt dump badging yourRepackedSigned.apk
    ```
      * 确保能输出正常的信息，包括包名，版本等
