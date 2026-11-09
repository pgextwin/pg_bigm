# pg_bigm — Windows x64 バイナリ

[English](README.md) | 日本語

[pg_bigm](https://github.com/pgbigm/pg_bigm)の**非公式Windows x64バイナリ**です。2-gram方式のGINインデックスを利用した全文検索機能を提供します。

## ダウンロードと対応環境

[最新の公開Release](https://github.com/pgextwin/pg_bigm/releases/latest)から、PostgreSQLメジャーバージョンに一致するZIPを選んでください。[過去のReleases](https://github.com/pgextwin/pg_bigm/releases)も確認できます。PostgreSQL **14〜18**向けの配布状況は[pgextwinカタログ](https://pgextwin.github.io/website/ja/)を参照してください。PostgreSQL 14のコミュニティサポートは2026年11月12日に終了します。

## インストール

1. バックアップを取り、[上流のpg_bigmドキュメント](https://github.com/pgbigm/pg_bigm)で必要条件を確認します。
2. 既存ファイルの置き換え前にPostgreSQLを停止します。対応するZIP内のlib/とshare/extension/以下を、PostgreSQLの同名ディレクトリへ配置します。
3. 利用方法に応じて`shared_preload_libraries`または`session_preload_libraries`でpg_bigmをロードするよう設定してください。共有の事前ロード設定を変更した場合はPostgreSQLの再起動が必要です。ファイルの配置と必要な設定を終えてからPostgreSQLを起動します。
4. 利用するデータベースで`CREATE EXTENSION pg_bigm;`を実行します。

Windowsでの詳しい手順は[導入ガイド](docs/windows_ja.md)を参照してください。

ダウンロードしたZIPを、Releaseに掲載された`SHA256SUMS.txt`と照合してください。SPDX形式のSBOM、脆弱性レポート、署名付き証明の有無はReleaseで確認できます。本番環境に導入する前に、検証環境で動作を確認してください。

## ライセンス

機能、設定、制限事項は上流プロジェクトのドキュメントを参照してください。本配布は非公式のWindows版です。再配布条件は同梱のライセンス表記に従います。
