# jarsigner

* jarsigner：签名，JDK提供的针对jar包签名的通用工具
  * 位置
    * Win：`JDK/bin/jarsigner.exe`
  * 用法
    ```bash
    jarsigner -verbose -keystore demo.keystore demo.apk demo.keystore
    jarsigner -verify [待验证的apk]
    ```
