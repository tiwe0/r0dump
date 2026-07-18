# R0DUMP 刷机教程

## 文件

文件二选一: 如果不需要 Google 框架，下载 文件 1；否则下载 文件 2。

文件 1: [R0DUMP 刷机包](https://download.ivory.cafe/v2026-07-18/lineage_lemonade-r0dump16-releasekeys-nogapps-fastboot-20260718_123751.zip)
文件 2: [R0DUMP-Google框架 刷机包](https://download.ivory.cafe/v2026-07-18/lineage_lemonade-r0dump16-releasekeys-gapps-fastboot-20260718_123751.zip)
SHA256SUMS: [SHA256SUMS.txt](https://download.ivory.cafe/v2026-07-18/SHA256SUMS.txt)

## 刷机

1. 下载对应的刷机包
2. 手机重启到 fastboot 模式

    ```shell
    adb reboot fastboot
    ```

3. 全量刷机

    ```shell
    fastboot -w update 刷机包路径
    ```

4. 等待重启
