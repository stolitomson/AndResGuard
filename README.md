#  Android资源混淆工具使用说明 #

## A fork of https://github.com/shwenzhang/AndResGuard, only bug fixs,no new features.



### Changes

1. only support gradle 7.0+

2. sevenzip support  osx aarch


### change group id:

com.tencent.mm --> io.github.leon406

### change version:
1.2.21 --> 1.2.22.6 /1.2.22.6.SNAPSHOT



### 问题

AGP 4.2.+ 引入资源压缩, 但效果不如AndResGuard,两个同时启用无法正常使用,需要在 grale.properties禁用

```
android.enableResourceOptimizations=false
```

测试AGP 4.2.2 AGP 7.0.4 可以正常使用
