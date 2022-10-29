# 重签名

TODO：

* 【已解决】给apktool重新打包的YouTube的apk重签名
* 【记录】用jarsigner给重新打包的安卓迅雷apk签名
* 【已解决】用keytool去给apk生成keystore证书

---

典型步骤是：

* 先用`keytool`生成证书文件
* 再用`jarsigner`去重新签名

举例：

## 迅雷的apk

### 用keytool去生成keystore证书

```bash
keytool -genkeypair -v -keystore thunderRepack.keystore -keyalg RSA -keysize 2048 -validity 10000 -alias thunderRepack
```

* 参数解释
  * `-genkeypair`：生成密码对（公钥和私钥）
  * `-v`：表示verbose，输出详细信息
  * `-keystore thunderRepack.keystore`：生成的keystore文件名
  * `-keyalg RSA`：秘钥算法用RSA
  * `-keysize 2048`：key的大小采用2048
    * 此处也是RSA算法的默认大小值
  * `-validity 10000`
  * `-alias thunderRepack`：设置别名，确保别名值是唯一，不重复的
    * 默认值是：`mykey`
    * 注：后续apk签名会用到这个alias值

* 输出：
  * `keystore文件`：thunderRepack.keystore

* 其他说明
  * 期间有个秘钥的密码，要记住，以备后用
    * 此处设置的密码是：thunderRepack
  * 设置一堆信息后，最后需要确认
  * 最后确认信息时，（由于此处是中文提示信息），要输入：是
    * 如果像我输入yes，搞错了，就要重复再确认一遍。。。

### 用jarsigner签名

```bash
jarsigner -verbose -digestalg SHA1 -sigalg SHA1withRSA -keystore thunderRepack.keystore -signedjar thunderRepack_changedVersion_jarSigned.apk thunderRepack_changedVersion.apk thunderRepack
```

* 参数解释
  * `-verbose`：输出详情
  * `-digestalg SHA1`：摘要算法用SHA1
  * `-sigalg SHA1withRSA`：签名算法用SHA1withRSA
  * `-keystore thunderRepack.keystore`：keystore文件，用的是前面keytool生成的
  * `-signedjar thunderRepack_changedVersion_jarSigned.apk`：output输出的，签名后的，apk文件名
  * `thunderRepack_changedVersion.apk`：要签名的apk文件
  * `thunderRepack`：前面（keytool生成的）keystore（指定的）的alias别名
