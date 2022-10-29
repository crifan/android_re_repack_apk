# zipalign


* `对齐`
  * 常用工具：`zipalign`
  * 为何要对齐 = 对齐的目的：优化性能
    * 对齐之前：CPU访问apk内部的未压缩的资源文件，需要额外复制到RAM中，再去访问
      * 增加了内存使用量
    * 对齐后：直接用`mmap`去访问apk内部的资源文件
      * 无需消耗额外RAM，降低了内存使用量，提高了性能和效率

> #### warning:: 对齐的时机
> * 如果您使用的是`apksigner`，只能在为APK文件签名之前执行`zipalign`
>   * 如果您在使用`apksigner`为APK签名之后对APK做出了进一步更改，签名便会失效
> * 如果您使用的是`jarsigner`，只能在为APK文件签名之后执行`zipalign`

语法：

* 对齐
  ```bash
  zipalign -p -f -v 4 infile.apk outfile.apk
  ```
* 验证是否对齐
  ```bash
  zipalign -c -v 4 existing.apk
  ```

## zipalign语法

```bash
 zipalign -h
Zip alignment utility
Copyright (C) 2009 The Android Open Source Project

Usage: zipalign [-f] [-p] [-v] [-z] <align> infile.zip outfile.zip
       zipalign -c [-p] [-v] <align> infile.zip

  <align>: alignment in bytes, e.g. '4' provides 32-bit alignment
  -c: check alignment only (does not modify file)
  -f: overwrite existing outfile.zip
  -p: memory page alignment for stored shared object files
  -v: verbose output
  -z: recompress using Zopfli
```
