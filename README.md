#  Android资源混淆工具使用说明 #

## A fork of https://github.com/shwenzhang/AndResGuard, only bug fixs,no new features.



## Changes

#### 1.2.22.6

1. only support gradle 7.0+
2. sevenzip support  osx aarch

#### 1.2.23-SNAPSHOT (from 1.2.22.6 )

1. update sevenzip version to **21.07** (except windows)
2. add new arch linux-arm_32/ linux-aarch_64

### How to Use(refer [origin repo](https://github.com/shwenzhang/AndResGuard),and modify as belows)


### change group id:

com.tencent.mm --> io.github.leon406

### change version:
- **stable(mavenCentral):** 1.2.21 --> 1.2.22.6

- **snapshot:** 1.2.21 -->1.2.23.1-SNAPSHOT

  ​	add snapshots repo to your build.gradle

```
maven {
    url "https://s01.oss.sonatype.org/content/repositories/snapshots/"
}
```



### 问题及临时解决方案

1. 无法进行混淆

   AGP 4.2.+ 引入资源压缩, 但效果不如AndResGuard,两个同时启用无法正常使用,需要在 gradle.properties禁用

   ```
   android.enableResourceOptimizations=false
   ```

   测试AGP 4.2.2 AGP 7.0.4 可以正常使用

2. 7zip无法运行

   配置本地7zip文件路径

   ```
   sevenzip {
           path = "xxxx/SevenZip-windows-x86_64.exe"
       }
   ```

   

