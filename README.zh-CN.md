<p align="center">
  <img src="logo/logo-256.png" width="128" alt="YUNSH Logo" />
</p>

<p align="center">
  <a href="README.md">English</a> | <strong>中文</strong>
</p>

# YUNSH OS OpenHarmony

面向 Raspberry Pi 5 的 YUNSH OS 独立 OpenHarmony 支线。

所有基于 Linux 的 YUNSH OS 版本都属于主线，包括当前的 `v3.1.6`。本仓库是独立的 OpenHarmony 发布通道，拥有自己的镜像、OTA 清单、版本号、校验值和回滚路径，不会替代或更新任何 Linux 主线系统。

## 本仓库发布的内容

这是一个二进制发布仓库，不是完整源码仓库。它用于发布经过测试的签名镜像、OTA 包与清单、校验值、Release 说明、功能介绍以及下载/刷写教程。Pi 5 底层移植、驱动、配对、权限桥接和其他未开源的实现细节不包含在本仓库中。

## 产品边界

- OpenHarmony 是系统层；这不是一个复制了 HAP 的 Debian 镜像。
- 不包含 Android 和 Waydroid。
- 应用使用原生 OpenHarmony HAP 软件包。
- YUNSH 液态玻璃表面、空间窗口、浏览器、蓝牙运动追踪、Link、Orbit、输入、相册、录制、媒体和 5K 显示是目标功能集；各功能只有通过对应测试闸门后才会发布。
- 视觉语言属于 YUNSH 自己：明亮的光学显示表面、半透明层级、直接操作、可中断弹簧动效、减少动效和增强对比度。它不是 Apple 的复制品，也不使用 Apple 私有协议。

## 首次启动与 OTA

基础镜像内置启动固件、驱动、OpenHarmony 运行时以及进入首次使用所需的桌面，不依赖 GitHub 才能启动。可选组件可以联网下载，但下载失败不得阻塞桌面。

更新只使用本仓库自己的签名 Release 清单和 OTA 资产，绝不使用 Linux 主线 OTA 通道。不要在该支线上安装主线镜像或 OTA。

## 当前状态

原生 OpenHarmony 构建、干净首次启动和 QEMU 启动证据全部通过之前，不会把任何公开镜像标记为可用。Raspberry Pi 5 硬件、显示、蓝牙、IMU 和 HAP 安装能力都必须有对应的真实设备证据，并在每个 Release 中分别列出。

当前经过测试的下载内容请查看本仓库的 Releases 页面。
