# i3-8100-B360-EFI
 i3-8100+微星 B360 迫击炮EFI
# Hackintosh EFI for MSI B360M MORTAR + i3-8100

<div align="center">

![macOS](https://img.shields.io/badge/macOS-Sonoma%2014%2B-brightgreen)
![OpenCore](https://img.shields.io/badge/OpenCore-1.0.2-blue)
![CPU](https://img.shields.io/badge/CPU-i3--8100-orange)
![Motherboard](https://img.shields.io/badge/Motherboard-MSI%20B360M%20MORTAR-red)

**OpenCore EFI configuration for Intel i3-8100 + MSI B360M MORTAR Hackintosh**

[简体中文](#简体中文) | [繁體中文](#繁體中文) | [廣東話](#廣東話) | [English](#english)

</div>

---

## 简体中文

### 🖥️ 硬件配置

| 硬件 | 型号 | 驱动状态 |
|------|------|----------|
| **CPU** | Intel Core i3-8100 @ 3.60GHz | ✅ 完美驱动 |
| **主板** | 微星 B360M MORTAR（迫击炮） | ✅ 完美支持 |
| **内存** | DDR4 2400 MHz 8GB | ✅ 正常识别 |
| **硬盘** | 英特尔 720p 128GB SSD | ✅ 原生支持 |
| **核显** | Intel UHD Graphics 630 | ✅ 硬件加速 |
| **有线网卡** | 英特尔有线网卡 | ✅ 原生驱动 |
| **无线网卡** | Intel AX210 Wi-Fi 6E | ✅ 正常工作 |
| **蓝牙** | Intel AX210 Bluetooth 5.3 | ✅ 正常工作 |
| **声卡** | Realtek ALC892 | ✅ 布局ID: 1 |
| **USB** | 全部端口 | ✅ 已定制 |

### ✨ 功能特性

- ✅ **CPU 电源管理** - 原生XCPM，变频正常
- ✅ **核显加速** - UHD 630 完整硬件加速，支持HEVC/H.264硬解
- ✅ **睡眠唤醒** - 正常睡眠、唤醒
- ✅ **音频** - 前后音频接口、麦克风正常工作
- ✅ **网络** - 有线网卡原生驱动，AX210 Wi-Fi + 蓝牙完整支持
- ✅ **USB** - 所有USB端口已定制，无端口限制
- ✅ **iMessage/FaceTime** - 正常工作（需自行生成三码）
- ✅ **App Store** - 正常登录下载
- ✅ **接力/通用剪贴板** - 支持连续互通功能

### 🚀 支持的 macOS 版本

- macOS Sonoma 14.x
- macOS Ventura 13.x
- macOS Monterey 12.x

### ⚙️ BIOS 设置

**必须关闭：**
- ❌ Secure Boot
- ❌ CFG Lock (MSR 0xE2 write protection)
- ❌ Intel VT-d (如无法关闭请在config.plist中启用`DisableIoMapper`)
- ❌ CSM
- ❌ Intel SGX

**必须开启：**
- ✅ VT-x
- ✅ UEFI Boot Mode
- ✅ Above 4G decoding
- ✅ Hyper-Threading
- ✅ Execute Disable Bit
- ✅ EHCI/XHCI Hand-off
- ✅ OS type: Windows 8.1/10 UEFI Mode
- ✅ DVMT Pre-Allocated(iGPU Memory): 64MB 以上

### 📦 驱动说明

**核心驱动：**
- `Lilu.kext` - 核心依赖库
- `VirtualSMC.kext` - SMC 仿真
- `WhateverGreen.kext` - 显卡补丁
- `AppleALC.kext` - 声卡驱动
- `IntelMausi.kext` - 英特尔有线网卡

**无线网卡驱动：**
- `AirportItlwm.kext` - Intel AX210 Wi-Fi 驱动
- `IntelBluetoothFirmware.kext` - 蓝牙固件
- `IntelBluetoothInjector.kext` - 蓝牙注入
- `BlueToolFixup.kext` - 蓝牙修复（Monterey+）

### ⚠️ 重要提示

1. **三码生成**：请使用 OpenCore Configurator 或 ProperTree 自行生成 MLB、Serial、UUID
2. **机型设置**：本 EFI 使用 `iMac19,1`，适合 8 代酷睿平台
3. **BIOS 更新**：建议升级到最新版 BIOS
4. **安装前**：请使用 `Debug` 版本进行排错，确认无误后再切换到 `Release`

---

## 繁體中文

### 🖥️ 硬體規格

| 硬體 | 型號 | 驅動狀態 |
|------|------|----------|
| **CPU** | Intel Core i3-8100 @ 3.60GHz | ✅ 完美驅動 |
| **主機板** | 微星 B360M MORTAR（迫擊砲） | ✅ 完美支援 |
| **記憶體** | DDR4 2400 MHz 8GB | ✅ 正常辨識 |
| **硬碟** | 英特爾 720p 128GB SSD | ✅ 原生支援 |
| **內顯** | Intel UHD Graphics 630 | ✅ 硬體加速 |
| **有線網卡** | 英特爾有線網卡 | ✅ 原生驅動 |
| **無線網卡** | Intel AX210 Wi-Fi 6E | ✅ 正常運作 |
| **藍牙** | Intel AX210 Bluetooth 5.3 | ✅ 正常運作 |
| **音效卡** | Realtek ALC892 | ✅ 配置ID: 1 |
| **USB** | 全部連接埠 | ✅ 已定制 |

### ✨ 功能特性

- ✅ **CPU 電源管理** - 原生XCPM，變頻正常
- ✅ **內顯加速** - UHD 630 完整硬體加速，支援HEVC/H.264硬解
- ✅ **睡眠喚醒** - 正常睡眠、喚醒
- ✅ **音訊** - 前後音訊介面、麥克風正常運作
- ✅ **網路** - 有線網卡原生驅動，AX210 Wi-Fi + 藍牙完整支援
- ✅ **USB** - 所有USB連接埠已定制，無連接埠限制
- ✅ **iMessage/FaceTime** - 正常運作（需自行產生三碼）
- ✅ **App Store** - 正常登入下載
- ✅ **接力/通用剪貼板** - 支援連續互通功能

### 🚀 支援的 macOS 版本

- macOS Sonoma 14.x
- macOS Ventura 13.x
- macOS Monterey 12.x

### ⚙️ BIOS 設定

**必須關閉：**
- ❌ Secure Boot
- ❌ CFG Lock (MSR 0xE2 write protection)
- ❌ Intel VT-d (如無法關閉請在config.plist中啟用`DisableIoMapper`)
- ❌ CSM
- ❌ Intel SGX

**必須開啟：**
- ✅ VT-x
- ✅ UEFI Boot Mode
- ✅ Above 4G decoding
- ✅ Hyper-Threading
- ✅ Execute Disable Bit
- ✅ EHCI/XHCI Hand-off
- ✅ OS type: Windows 8.1/10 UEFI Mode
- ✅ DVMT Pre-Allocated(iGPU Memory): 64MB 以上

### 📦 驅動說明

**核心驅動：**
- `Lilu.kext` - 核心依賴函式庫
- `VirtualSMC.kext` - SMC 模擬
- `WhateverGreen.kext` - 顯示卡修補
- `AppleALC.kext` - 音效卡驅動
- `IntelMausi.kext` - 英特爾有線網卡

**無線網卡驅動：**
- `AirportItlwm.kext` - Intel AX210 Wi-Fi 驅動
- `IntelBluetoothFirmware.kext` - 藍牙韌體
- `IntelBluetoothInjector.kext` - 藍牙注入
- `BlueToolFixup.kext` - 藍牙修復（Monterey+）

### ⚠️ 重要提醒

1. **三碼產生**：請使用 OpenCore Configurator 或 ProperTree 自行產生 MLB、Serial、UUID
2. **機型設定**：本 EFI 使用 `iMac19,1`，適合 8 代酷睿平台
3. **BIOS 更新**：建議升級到最新版 BIOS
4. **安裝前**：請使用 `Debug` 版本進行除錯，確認無誤後再切換到 `Release`

---

## 廣東話

### 🖥️ 硬件規格

| 硬件 | 型號 | 驅動狀態 |
|------|------|----------|
| **CPU** | Intel Core i3-8100 @ 3.60GHz | ✅ 完美驅動 |
| **主板** | 微星 B360M MORTAR（迫擊炮） | ✅ 完美支援 |
| **內存** | DDR4 2400 MHz 8GB | ✅ 正常識別 |
| **硬盤** | 英特爾 720p 128GB SSD | ✅ 原生支援 |
| **核顯** | Intel UHD Graphics 630 | ✅ 硬件加速 |
| **有線網卡** | 英特爾有線網卡 | ✅ 原生驅動 |
| **無線網卡** | Intel AX210 Wi-Fi 6E | ✅ 正常運作 |
| **藍牙** | Intel AX210 Bluetooth 5.3 | ✅ 正常運作 |
| **聲卡** | Realtek ALC892 | ✅ 布局ID: 1 |
| **USB** | 全部端口 | ✅ 已定制 |

### ✨ 功能特性

- ✅ **CPU 電源管理** - 原生XCPM，變頻正常
- ✅ **核顯加速** - UHD 630 完整硬件加速，支持HEVC/H.264硬解
- ✅ **睡眠喚醒** - 正常瞓覺、醒返
- ✅ **音頻** - 前後音頻接口、麥克風正常用
- ✅ **網絡** - 有線網卡原生驅動，AX210 Wi-Fi + 藍牙完整支援
- ✅ **USB** - 所有USB端口已定制，冇端口限制
- ✅ **iMessage/FaceTime** - 正常用（要自己生成三碼）
- ✅ **App Store** - 正常登錄下載
- ✅ **接力/通用剪貼板** - 支持連續互通功能

### 🚀 支持嘅 macOS 版本

- macOS Sonoma 14.x
- macOS Ventura 13.x
- macOS Monterey 12.x

### ⚙️ BIOS 設置

**一定要關：**
- ❌ Secure Boot
- ❌ CFG Lock (MSR 0xE2 write protection)
- ❌ Intel VT-d (如果關唔到就係config.plist度開`DisableIoMapper`)
- ❌ CSM
- ❌ Intel SGX

**一定要開：**
- ✅ VT-x
- ✅ UEFI Boot Mode
- ✅ Above 4G decoding
- ✅ Hyper-Threading
- ✅ Execute Disable Bit
- ✅ EHCI/XHCI Hand-off
- ✅ OS type: Windows 8.1/10 UEFI Mode
- ✅ DVMT Pre-Allocated(iGPU Memory): 64MB 以上

### 📦 驅動說明

**核心驅動：**
- `Lilu.kext` - 核心依賴庫
- `VirtualSMC.kext` - SMC 模擬
- `WhateverGreen.kext` - 顯卡補丁
- `AppleALC.kext` - 聲卡驅動
- `IntelMausi.kext` - 英特爾有線網卡

**無線網卡驅動：**
- `AirportItlwm.kext` - Intel AX210 Wi-Fi 驅動
- `IntelBluetoothFirmware.kext` - 藍牙固件
- `IntelBluetoothInjector.kext` - 藍牙注入
- `BlueToolFixup.kext` - 藍牙修復（Monterey+）

### ⚠️ 重要提醒

1. **三碼生成**：請用 OpenCore Configurator 或者 ProperTree 自己生成 MLB、Serial、UUID
2. **機型設置**：呢個 EFI 用 `iMac19,1`，適合 8 代酷睿平台
3. **BIOS 更新**：建議升級到最新版 BIOS
4. **安裝前**：先用 `Debug` 版本排錯，確認冇問題再轉去 `Release`

---

## English

### 🖥️ Hardware Specifications

| Hardware | Model | Status |
|----------|-------|--------|
| **CPU** | Intel Core i3-8100 @ 3.60GHz | ✅ Fully Working |
| **Motherboard** | MSI B360M MORTAR | ✅ Fully Supported |
| **Memory** | DDR4 2400 MHz 8GB | ✅ Recognized |
| **Storage** | Intel 720p 128GB SSD | ✅ Native Support |
| **iGPU** | Intel UHD Graphics 630 | ✅ Hardware Acceleration |
| **Ethernet** | Intel Gigabit LAN | ✅ Native Driver |
| **Wi-Fi** | Intel AX210 Wi-Fi 6E | ✅ Working |
| **Bluetooth** | Intel AX210 Bluetooth 5.3 | ✅ Working |
| **Audio** | Realtek ALC892 | ✅ Layout ID: 1 |
| **USB** | All Ports | ✅ Customized |

### ✨ Features

- ✅ **CPU Power Management** - Native XCPM with proper frequency stepping
- ✅ **iGPU Acceleration** - Full UHD 630 hardware acceleration, HEVC/H.264 decoding
- ✅ **Sleep/Wake** - Proper sleep and wake functionality
- ✅ **Audio** - Front/Rear audio jacks and microphone working
- ✅ **Network** - Native Intel Ethernet, full AX210 Wi-Fi + Bluetooth support
- ✅ **USB** - All USB ports customized, no port limit issues
- ✅ **iMessage/FaceTime** - Working (generate your own SMBIOS)
- ✅ **App Store** - Normal login and downloads
- ✅ **Handoff/Universal Clipboard** - Continuity features supported

### 🚀 Supported macOS Versions

- macOS Sonoma 14.x
- macOS Ventura 13.x
- macOS Monterey 12.x

### ⚙️ BIOS Settings

**Must Disable:**
- ❌ Secure Boot
- ❌ CFG Lock (MSR 0xE2 write protection)
- ❌ Intel VT-d (enable `DisableIoMapper` in config.plist if you can't disable)
- ❌ CSM
- ❌ Intel SGX

**Must Enable:**
- ✅ VT-x
- ✅ UEFI Boot Mode
- ✅ Above 4G decoding
- ✅ Hyper-Threading
- ✅ Execute Disable Bit
- ✅ EHCI/XHCI Hand-off
- ✅ OS type: Windows 8.1/10 UEFI Mode
- ✅ DVMT Pre-Allocated(iGPU Memory): 64MB or higher

### 📦 Kexts Included

**Core Kexts:**
- `Lilu.kext` - Core patching framework
- `VirtualSMC.kext` - SMC emulator
- `WhateverGreen.kext` - Graphics patching
- `AppleALC.kext` - Audio driver
- `IntelMausi.kext` - Intel Ethernet driver

**Wi-Fi & Bluetooth Kexts:**
- `AirportItlwm.kext` - Intel AX210 Wi-Fi driver
- `IntelBluetoothFirmware.kext` - Bluetooth firmware
- `IntelBluetoothInjector.kext` - Bluetooth injector
- `BlueToolFixup.kext` - Bluetooth fix for Monterey+

### ⚠️ Important Notes

1. **SMBIOS Generation**: Please generate your own MLB, Serial, and UUID using OpenCore Configurator or ProperTree
2. **SMBIOS Model**: This EFI uses `iMac19,1` which is ideal for 8th Gen Intel platforms
3. **BIOS Update**: Recommended to update to the latest BIOS version
4. **Before Installation**: Use the `Debug` version for troubleshooting first, then switch to `Release` once confirmed working

---

## 📝 License

This EFI configuration is provided for educational purposes only. Users are responsible for their own Hackintosh builds.

## 🙏 Credits

- [Acidanthera](https://github.com/acidanthera) for OpenCore and all core kexts
- [OpenIntelWireless](https://github.com/OpenIntelWireless) for Intel Wi-Fi and Bluetooth drivers
- Hackintosh community for testing and documentation

---

<div align="center">

**If this EFI works for you, please give a ⭐ Star!**

</div>
