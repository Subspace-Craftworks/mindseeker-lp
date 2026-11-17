# mindseeker-lp

Mindseeker のランディングページ (https://www.subspace-craftworks.jp/)。Vite + React。
[Subspace-Craftworks/Mindseeker](https://github.com/Subspace-Craftworks/Mindseeker) の `lp/` から履歴ごと切り出したリポジトリです。

## 開発 / ビルド

```sh
npm ci
npm run dev     # ローカル開発
npm run build   # dist/ に出力 (index.html と privacy/index.html)
```

`/privacy` は `privacy/index.html` の静的ページです。原本は `docs/privacy_policy.md` で、更新時は HTML 側も同じ内容に更新してください。

## CI

`.github/workflows/ci.yml`: `npm ci` → ビルド → リンクチェック (lychee) → Lighthouse CI (Performance >= 90)。Dependabot が npm / GitHub Actions を週次で更新します。

## デプロイ

Vercel プロジェクト `mindseeker-lp` (Git 連携先をこのリポジトリへ付け替え予定)。依存は `latest` を使わず固定バージョンで管理します。
