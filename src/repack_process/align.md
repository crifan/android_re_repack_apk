# 对齐

TODO：

* 【已解决】用zipalign给重新打包后的apk去对齐

---

举例：

## 迅雷apk

### 给迅雷的apk对齐

```bash
zipalign -p 4 thunderRepack_changedVersion_jarSigned.apk thunderRepack_changedVersion_jarSigned_aligned.apk
```

* 参数解释
  * `-p` ：memory page alignment for stored shared object files
  * 如果要强制覆盖输出的文件，加`-f`
    * `zipalign -f -p 4 xxx.apk xxx_aligned.apk`
  * 如果要输出详情，加`-v`
    * `zipalign -v -f -p 4 xxx.apk xxx_aligned.apk`
