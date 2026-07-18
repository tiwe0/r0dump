# R0DUMP 刷机教程

## 文件

文件 1: [R0DUMP 刷机包](https://r0dump.ivory.cafe/lineage-23.2-r0dump16-RELEASE-lemonade-releasekeys-mtless-20260711_184823.zip)
文件 2: [R0DUMP 定制 GAPPS 注入包](https://r0dump.ivory.cafe/r0dump_gapps_injected_images.zip)

## 刷机

0. 下载`文件 1`（如果需要 Google 框架，`文件 2` **也**要下载）
1. 解压 `文件 1`
2. 使用 [payload-dumper](https://github.com/ssut/payload-dumper-go/releases) 提取
    ```shell
    mkdir output
    payload-dumper-go -o output payload.bin
    ```
3. 手机长按电源键+音量上键重启进入 fastboot
4. fastboot 刷入系统
5. 如果需要 Google 框架，选择 `No`，并继续下面的步骤；不需要 Google 框架可以直接选择 `Yes` 进入系统

## Google 框架刷入

6. 解压 `文件 2`
7. 输入 `fastboot reboot fastboot` 进入 fastbootd
8. 检查当前 slot: `fastboot getvar current-slot`
9. 如果是 a，
    ```shell
    fastboot flash product_a product_gapps.img
    fastboot flash system_ext_a system_ext_gapps.img
    ```
10. 如果是 b，
    ```shell
    fastboot flash product_b product_gapps.img
    fastboot flash system_ext_b system_ext_gapps.img
    ```
11. 重启进入系统: `fastboot reboot`
