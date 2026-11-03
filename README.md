# cepheus KernelSU-Next 内核

为小米9（cepheus）编译集成 **KernelSU Next** 的内核，供 crDroid 14 / Android 14 使用。

## 为什么

crDroid 14 自带内核的 KernelSU 版本过旧（11872），官方 KernelSU Manager 要求更新内核。
本仓库直接用 **crDroid 官方内核源码**（`android_kernel_xiaomi_cepheus`，`14.0` 分支）+
**KernelSU Next 官方集成脚本** 重新编译，得到内核级 root。

## 构建

推到 main 或手动 `workflow_dispatch`，产物 `cepheus-ksu-next.zip`（AnyKernel3 格式）。

## 刷入

AnyKernel3 是内核刷机包，**不动 boot 分区布局**，TWRP 里直接 Install 即可：

1. TWRP → Install → `cepheus-ksu-next.zip`
2. Reboot System
3. 装 KernelSU Next Manager APK（v3.4.2+），打开应显示"工作中"

## 来源

- 内核：https://github.com/crdroidandroid/android_kernel_xiaomi_cepheus (14.0)
- KSU Next：https://github.com/KernelSU-Next/KernelSU-Next (next)
- 工具链：https://github.com/kdrag0n/proton-clang
- 打包：https://github.com/osm0sis/AnyKernel3
