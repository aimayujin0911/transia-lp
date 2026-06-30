# 株式会社トランシア LP（リデザイン案）

埼玉発・関東1都6県の物流パートナー「株式会社トランシア」向けの法人荷主向けランディングページ。
Claude Design の handoff（`サイトのリデザイン依頼-handoff.zip` / `Transia LP.dc.html`）を、依存なしの単独静的 HTML（HTML / CSS / Vanilla JS）として実装したもの。

## 公開

- GitHub Pages: https://aimayujin0911.github.io/transia-lp/
- 単一ページ（`index.html`）。ビルド工程なし。`index.html` をブラウザで開けばそのまま動く。

## 構成

```
transia-lp/
├── index.html      # LP 本体（インラインスタイル＋末尾に挙動用の素のJS）
├── img/            # ヒーロー画像・トラック画像・ロゴ
└── .nojekyll       # GitHub Pages の Jekyll 処理を無効化
```

## 機能

- **ヒーロー比較スイッチャー**（画面右上の「HERO 比較案」パネル）
  - 案A（シネマティック全面）／案B（エディトリアル分割）／案C（センターポスター）の3案
  - フォーム位置トグル（通常／FV先頭にフォーム）→ 案A2 / B2 / C2 を表示
  - デザイン提案用の比較UI。掲載案が確定したら、このパネルと未使用ヒーローを削除して1案に固定できる
- スクロール追従ヘッダー／パララックス／reveal-on-scroll アニメーション
- レスポンシブ（860px 以下でグローバルナビを畳み、下部に固定CTAバーを表示）
- `style-hover` / `style-focus` 属性は読み込み時に `:hover` / `:focus` の CSS ルールへ変換（design tool と同挙動）

## 公開前に差し替えるべき項目（TODO）

handoff のデザイン案に含まれるプレースホルダ。正式情報に差し替えてから本公開すること。

- [ ] **電話番号** `0480-44-0780`（ヘッダー / ヒーロー / CTA / フッター / 会社概要に多数）が正しいか確認
- [ ] **会社概要**（所在地 〒340-0113 埼玉県幸手市幸手5339-1 ほか）を最新の正式情報に差し替え（フッターに「記載例」の注記あり）
- [ ] **お客様の声**（Voice セクション）はサンプル文。実際の導入事例に差し替え
- [ ] **お問い合わせフォーム**は送信機能なし（`onsubmit="return false"`）。本番では送信先（フォームサービス or バックエンド）に接続
- [ ] 許認可番号・料金・実績など、掲載に必要な正式情報の確認
- [ ] OGP 画像（`og:image`）が必要なら追加

## 元データ

Claude Design handoff: `サイトのリデザイン依頼-handoff.zip`
（主役デザイン: `untitled/project/uploads/transia-lp/Transia LP.dc.html`）
