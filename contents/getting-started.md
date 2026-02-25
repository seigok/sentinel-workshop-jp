# はじめる前に（初学者向けガイド）

このワークショップは、すべてを一気にやらなくても大丈夫です。まずは「Sentinel の基本を体験する」ことに集中し、その後に Terraform / Vault / Consul / Nomad 連携へ進める構成になっています。

## 最短ルート（30 〜 45 分）

まずは以下の 3 章だけで、Sentinel の要点を掴めます。

1. [初めての Sentinel](hello-sentinel.md)
2. [Sentinel 設定ファイル](configurations.md)
3. [Tests 1: 設定ファイル](test-configuration.md)

この時点で、以下ができるようになります。
- ポリシーを記述する
- `sentinel apply` で評価する
- `sentinel test` でテストする

## 学習ステップ（おすすめ）

- **Step 1（入門）**: Sentinel の基本構文と評価の流れを理解する
- **Step 2（実践）**: imports と test を使って、実運用を想定した構成にする
- **Step 3（連携）**: Terraform / Vault / Consul / Nomad と連携して Policy as Code を体感する
- **Step 4（運用）**: ポリシー設計・命名規則・CI を取り入れてチーム開発に展開する

## 必須と任意の準備

- **必須（入門まで）**
  - macOS または Linux
  - Sentinel CLI
- **任意（連携章を進める場合）**
  - HCP Terraform
  - Vault / Consul / Nomad
  - Docker
  - jq / cURL
  - GitHub アカウント
  - AWS / Azure / GCP いずれか

## つまずきやすいポイント

- Sentinel CLI のパスが通っていない
- サンプルファイルのパスが相対パスのままズレている
- 連携章で必要なプロダクト（例: HCP Terraform）のセットアップが未完了

うまく動かないときは、まず `sentinel -version` と現在の作業ディレクトリを確認してください。
