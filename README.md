# towane-legal

アプリ「トワネ（towane）」の法務ページ。GitHub Pages で公開している。

https://ueda-daiki-albato.github.io/towane-legal/

| ページ | URL |
|---|---|
| トップ | `/` |
| プライバシーポリシー | `/privacy.html` |
| 利用規約 | `/terms.html` |
| 特定商取引法に基づく表記 | `/tokushoho.html` |

## ⚠️ 原本はここではない

**編集は本体リポジトリの `docs/*.html` で行う。** このリポジトリはそれを配置しているだけ。
ここを直接直すと、次に本体からコピーしたときに黙って上書きされる。

アプリからのリンクは `src/lib/legal.ts` の `LEGAL_URLS`。**ファイル名を変えない**こと
（審査に出したあとにリンク切れになる）。

## 内容を変えるときの注意

- 利用規約の本文を変えたら、本体の `TERMS_VERSION`（`src/features/auth/store.tsx`）を上げる。
  上げると既存ユーザーに再同意を求める
- 有効期限や価格を変えたら、`terms.html` / `tokushoho.html` / `src/features/premium/catalog.ts` /
  `functions/src/coins.ts` の**4箇所が揃っているか**を確認する
