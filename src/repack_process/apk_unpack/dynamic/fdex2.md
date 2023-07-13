# FDex2

参考自己的教程 [FDex2 · 安卓应用的安全和破解](https://book.crifan.org/books/android_app_security_crack/website/android_crack_tool/app_to_dex/fdex2.html)

去用 `Nox`+`Xposed`+`FDex2`去导出dex文件。

## 举例

### 用FDex2导出迅雷的dex

![nox_enable_fdex2](../../../../assets/img/nox_enable_fdex2.png)

![export_xunlei_downloadprovider](../../../../assets/img/export_xunlei_downloadprovider.png)

![fdex2_save_xunlei_ok](../../../../assets/img/fdex2_save_xunlei_ok.png)

动态导出迅雷的12个`dex`文件：

![exported_xunlei_12_dex](../../../../assets/img/exported_xunlei_12_dex.png)

从Nox夜神模拟器中拷贝文件到Mac中，用VSCode打开，效果是：

![vscode_xunlei_dex_files](../../../../assets/img/vscode_xunlei_dex_files.png)
