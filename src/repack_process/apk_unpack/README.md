# apk解包

TODO：

* 【已解决】Mac中升级apktool到最新版
* 【记录】用apktool反编译破解迅雷安卓app

---

* 目标：得到`dex`文件
* 方法=手段
  * 安卓apk
    * 未加固 -> 静态导出dex
      * `apktool`
    * 已加固 -> 动态导出dex
      * `FDex2`
      * `DexExtractor`
        * 注：只支持有限的加固（梆梆加固等）方案，不支持其他的（腾讯乐固等），所以不推荐
