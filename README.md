# auto-release-demo

由 github action 在 Push 進 main 分支時，驅動 nodejs 套件 [semantic-release](https://github.com/semantic-release/semantic-release) 的自動 release 流程

## Outline
1. [前置](#前置)
1. [使用](#使用)

## 前置

需求：須在 Repo Setting 中為 github action 賦權
 * 寫入專案 content
 * Create 和 approve PR review
 * 版號規則參考[Semantic Versioning 2.0.0](https://semver.org/)

![Setting 選單](image\setting_panel.png)
![需求權限](image\permission.png)  

## 使用

1. 在跟目錄定義[配置檔(.releaserc)](#配置檔(.releaserc))
2. Commit 時，Commit Message 輸入特定的詞頭
    * ```!feat:``` 推進大版號
    * ```feat:``` 推進次版號
    * ```fix:``` 推進修訂號


### 配置檔(.releaserc)

semantic-release 的配置檔，定義