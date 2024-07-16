# apktool

TODO：

* 【已解决】Mac中升级apktool到最新版
* 【已解决】apktool重新打包apk报错：brut.directory.PathNotExist apktool.yml
* 【记录】Mac中再次升级apktool到最新版本2.9.0
* 【记录】用apktool反编译破解迅雷安卓app
* 【记录】用apktool给脱壳后加了smali代码的各种文件重新打包为apk
* 【已解决】pm安装apktool重新打包的apk报错：Failure INSTALL_PARSE_FAILED_NO_CERTIFICATES
* 【已解决】找到jadx反编译的java代码对应的apktool反编译的smali代码
* 【未解决】Mac中用apktool破解反编译安卓apk：adcWallet_release_v2.2.4.apk
* 【部分解决】apktool反编译安卓迅雷apk报错：Baksmaling assets dex Not a valid dex magic value
* 【未解决】apktool重新打包apk报错：Exception in thread org.jf.util.ExceptionWithContext Exception occurred while writing code_item for method
* 【记录】对比确保apktool重新打包的YouTube的apk可以正常安装和使用
* 【已解决】apktool重新打包报错：brut.androlib.AndrolibException brut.common.BrutException could not exec
* 【已解决】安卓逆向Tiktok：用apktool导出文件
* 【已解决】给apktool重新打包的YouTube的apk重签名
* 【已解决】安卓AS调试apk的smali：导入apktool反编译的源码作为项目代码
* 【未解决】安卓手机Google Pixel3中卸载旧版YouTube重新安装apktool重新打包的YouTube的apk

---

* `apktool`
  * 是什么：一个逆向安卓apk的工具
  * 主要功能
    * 解包
      * 输入：`apk`文件
      * 输出：各种安卓`资源文件`
    * 重新打包
  * 典型用途
    * 构建`自动化`工作 -> 取代重复的手动工作
      * 比如自动编译apk等工作
    * 给原有apk`添加额外东西`
      * 比如反编译出apk后
        * 再本地化localizing
        * 添加其他功能
    * `分析`原有apk的功能和逻辑
* 如何安装
  * [Apktool - How to Install](https://ibotpeaches.github.io/Apktool/install/)
* github主页
  * [iBotPeaches/Apktool: A tool for reverse engineering Android apk files](https://github.com/iBotPeaches/Apktool)
* 官网
  * [Apktool - A tool for reverse engineering 3rd party, closed, binary Android apps](https://ibotpeaches.github.io/Apktool/)
  * 官方提示
    * 请不要用apktool用于盗窃破解apk

## apktool语法

```bash
 apktool --help
Unrecognized option: --help
Apktool v2.5.0 - a tool for reengineering Android apk files
with smali v2.4.0 and baksmali v2.4.0
Copyright 2010 Ryszard Wiśniewski <brut.alll@gmail.com>
Copyright 2010 Connor Tumbleson <connor.tumbleson@gmail.com>


usage: apktool
 -advance,--advanced   prints advance information.
 -version,--version    prints the version then exits
usage: apktool if|install-framework [options] <framework.apk>
 -p,--frame-path <dir>   Stores framework files into <dir>.
 -t,--tag <tag>          Tag frameworks using <tag>.
usage: apktool d[ecode] [options] <file_apk>
 -f,--force              Force delete destination directory.
 -o,--output <dir>       The name of folder that gets written. Default is apk.out
 -p,--frame-path <dir>   Uses framework files located in <dir>.
 -r,--no-res             Do not decode resources.
 -s,--no-src             Do not decode sources.
 -t,--frame-tag <tag>    Uses framework files tagged by <tag>.
usage: apktool b[uild] [options] <app_path>
 -f,--force-all          Skip changes detection and build all files.
 -o,--output <dir>       The name of apk that gets written. Default is dist/name.apk
 -p,--frame-path <dir>   Uses framework files located in <dir>.


For additional info, see: https://ibotpeaches.github.io/Apktool/
For smali/baksmali info, see: https://github.com/JesusFreke/smali
```
