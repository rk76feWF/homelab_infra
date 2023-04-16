# `homelab_infra`

@rk76feWFのオンプレ環境のうち、公開可能な箇所を管理するレポジトリです。

![](https://raw.githubusercontent.com/rk76feWF/homelab_infra/images/proxmox-manager.png?token=GHSAT0AAAAAABWTSBCC5RIVJ6HH5O34XXSMY74KWEA)

## スペック

- homelab-cluster
    - pve01
        - i7-4710MQ
        - 16GB MEM
        - 256G SSD
    - pve02
        - i5-6200U
        - 8GB MEM
        - 256G SSD
    - pve03
        - i5-6200U
        - 8GB MEM
        - 256G SSD

- test-environment
    - ~~pve04~~
        - ~~i5-2540M~~
        - ~~6GB MEM~~
        - ~~1TG HDD~~
    - pve05
        - i5-2540M
        - 4GB MEM
        - 1TG HDD

## 今やっていること

- homelabネットワークへの踏み台サーバ
- YouTube等録画用サーバ
- 新しいバージョンや使ったことのないディストリビュートのLinuxの検証
- VLAN・リングアグリゲーションの検証
- NASにてmacのTimeMachineバックアップ
- Cephを使い、可用性を向上。（3台HA構成）

- 業務用ルータの導入
    - RTX1200 <- 導入
    - IX2215 <- 導入
    - ~~IX2105~~
    - ~~C891F~~

## 今後の予定

- 二重ルータ状態の解消
    - DMZ等を使う、親の許可待ち
- 設定自動化
    - test-environmentで検証中
- VLANを使って回線の冗長化
    - メイン: NTT光回線
    - サブ: JCON CATV回線
    - メイン回線のインターネットとの接続が切れたら自動的にサブ回線にスイッチ
    - （マルチホームは閾が高い）
- UPSの導入
    - 未定
- リブータの導入
    - 現状はTPLinkのスマートプラグにて代用中
    - 明京電気
    - raritan
- PXEブートの検証
- k8sの検証
- 新規でNASの導入、iSCSIでVMを動かす
    - Cephは耐障害性が高いが速度が遅い
