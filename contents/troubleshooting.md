# トラブルシューティング

ワークショップで頻出するエラーと対処をまとめます。

## 1. `sentinel: command not found`

**原因**
- Sentinel CLI が未インストール、または PATH 未設定

**対処**
- `sentinel -version` で実行可否を確認
- CLI バイナリ配置先が PATH に含まれているか確認

## 2. `Error loading configuration`

**原因**
- `sentinel.hcl` のパス/構文エラー
- `source` の相対パス不整合

**対処**
- `sentinel.hcl` の `source` が実ファイルを指しているか確認
- 作業ディレクトリを `pwd` で確認

## 3. `Fail - <policy>.sentinel` の意図がわからない

**原因**
- 失敗時トレースの読み方に慣れていない

**対処**
- まず `Rule "main"` の値が `false` になっているか確認
- ロジックを段階的に簡略化して再実行

## 4. テストの mock データが読み込まれない

**原因**
- test 設定の import path と mock ファイル配置の不整合

**対処**
- test 設定ファイルの import 定義を再確認
- パス区切り・ファイル名の typo を確認

## 5. 連携章（Terraform / Vault / Consul / Nomad）が進まない

**原因**
- 依存プロダクトのセットアップ不足

**対処**
- 先に [初めての Sentinel](hello-sentinel.md) と test 章で基本操作を完了
- 連携は「必須」ではなく段階的に進める

---

不明点がある場合は、実行コマンドとエラーメッセージをそのまま残しておくと、切り分けが速くなります。
