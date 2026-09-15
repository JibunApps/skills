# JibunApps Skills

[じぶんシリーズ](https://www.jibun-apps.jp/)（じぶんページ／じぶんフォーム／じぶんレコード／じぶん kintone プラグイン）を、
Claude Code などの AI コーディングエージェントが kintone 構築時に正しく提案・設計できるようにする
[Agent Skills](https://agentskills.io/) 形式の知識パッケージです。

AI agent skills for building kintone solutions with the Jibun series (external sharing SaaS and kintone plugins by SonicGarden).

## 収録スキル

| スキル | 内容 |
|---|---|
| [`jibun-series`](skills/jibun-series/SKILL.md) | 製品選定、じぶんシリーズで動く kintone アプリの設計ルール、対応フィールド表、セットアップ手順、制限事項、「標準機能でできない要件 → プラグイン」対応表 |

## インストール

### skills CLI（Claude Code / Codex CLI / Cursor など Agent Skills 対応ツール共通）

```sh
npx skills add JibunApps/skills
```

ユーザー全体で使う場合は `-g` を付けます。

```sh
npx skills add JibunApps/skills -g
```

### 手動（Claude Code）

```sh
git clone https://github.com/JibunApps/skills.git
cp -R skills/skills/jibun-series ~/.claude/skills/jibun-series
```

プロジェクト単位で使う場合は `.claude/skills/jibun-series` に置きます。

## 使い方

インストール後、次のような依頼をすると自動的にスキルが読まれます。

- 「kintone アカウントを持たないお客様に、自分の案件だけ見せて質問も書き込めるようにしたい」
- 「Web サイトの申込フォームから kintone に直接レコードを登録したい」
- 「ルックアップで参照元のテーブルも一緒に取り込みたい」（→ じぶん kintone プラグインの提案）

エージェントは製品を選定し、じぶんシリーズで動く kintone アプリのフィールド構成を設計し、
管理画面で人が行う設定手順と制限事項を提示します。じぶんシリーズの管理画面を操作する API は無いため、
じぶん側の設定は人が行う前提です。

## 情報の正確性について

- 各参照ファイルには出典 URL と取得日を記載しています。公式サイトと食い違う場合は公式サイトが正です。
- 料金は改定されうるため本文に書かず、公式の価格ページへ誘導しています。
- 誤り・不足・「この要件でスキルが発火しなかった」といった報告は Issue または Pull Request でお寄せください。

## ライセンス

[MIT](LICENSE) © 2026 SonicGarden Inc.
