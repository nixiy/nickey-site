# Nickey44A Product Site

Nickey44Aの製品紹介ランディングページです。AstroとTypeScriptで構成した静的サイトで、GitHub Pagesへの公開を想定しています。

公開URL: https://nixiy.github.io/nickey-site/

## ローカル開発

Node.js 22以上を推奨します。

```sh
npm install
npm run dev
```

開発サーバーの表示URL（通常は `http://localhost:4321/nickey-site/`）をブラウザで開いてください。

## ビルド

```sh
npm run build
```

静的ファイルは `dist/` に生成されます。ローカルでビルド結果を確認する場合は `npm run preview` を実行します。

## 画像

製品画像は `public/images/` に配置します。画像がない場合もグレーのPlaceholderを表示するため、レイアウトやビルドは壊れません。

| ファイル | 用途 |
| --- | --- |
| `hero.jpg` | Hero |
| `layout.jpg` | 44 KEYS |
| `aaa-powered.jpg` | AAA POWERED |
| `wireless.jpg` | WIRELESS SPLIT |
| `thin-light.jpg` | THIN & LIGHT |
| `weight-body.jpg` | Body only |
| `weight-battery.jpg` | With AAA batteries |
| `weight-switches.jpg` | With switches |
| `weight-full.jpg` | Fully assembled |
| `detail-main.jpg` | DESIGN / DETAIL |
| `gallery-01.jpg` 〜 `gallery-05.jpg` | Gallery |
| `og.jpg` | OGP（推奨 1200 × 630 px） |

同名ファイルを置くだけで差し替えられます。Hero以外は遅延読み込みされ、コンポーネント側で縦横比を予約しています。

## GitHub Pages

`astro.config.mjs` には `site: https://nixiy.github.io` と `base: /nickey-site/` を設定しています。

`.github/workflows/deploy.yml` が `main` ブランチへのpush時にビルドとデプロイを行います。初回のみGitHubのリポジトリ設定で **Settings → Pages → Build and deployment → Source** を **GitHub Actions** に設定してください。

## 現在の仮要素

- BOOTHの商品URL、FirmwareのGitHub URL
- Build Kit / Fully Assembledの商品説明と販売状態
- Concept、各Feature、Design / Detailの製品コピー
- `public/images/` 内に未配置の製品写真
