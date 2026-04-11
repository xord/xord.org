# CLAUDE.md

このファイルは、このリポジトリで作業する Claude (および人間の開発者) 向けの共有メモです。

## サイトの位置付け

- **xord.org** は個人事業の屋号 "xord" のポートフォリオサイト。
- 事業の柱は 2 つ:
  1. 自社インディ iOS アプリの開発・販売 (RubySketch / RubySolitaire など)
  2. Ruby OSS 作者としての活動 (xot / rucy / rays / reflexion / beeps / processing / rubysketch gem 群)
- スタックは Ruby 中心、ネイティブ層で C++ / Swift / Objective-C。

## 技術構成

- **Jekyll + GitHub Pages** で配信 (`CNAME` は `xord.org`)。
- 使用プラグイン: `jekyll-seo-tag`, `jekyll-sitemap` (`_config.yml` 参照)。
- ローカル開発は `bundle install` → `bundle exec jekyll serve`。`Gemfile` で `github-pages` gem を使っているので、本番と同じ Jekyll バージョンが走る。

### ディレクトリ概要

```
_config.yml           サイト設定
_data/apps.yml        Apps セクションのカードデータ
_data/gems.yml        OSS (Gems) セクションのカードデータ
_includes/            head / header / footer の共通パーツ
_layouts/
  default.html        ベース HTML シェル (全ページ共通)
  home.html           ルート index.md 専用 (ランディング)
  page.html           その他サブページ用 (layout defaults で自動適用)
assets/css/main.scss  サイト全体のスタイル
index.md              トップページ (Hero / About / Apps / OSS / Contact)
rubysketch/           RubySketch のサポートページ群 (※下記ポリシー参照)
rubysolitaire/        RubySolitaire のサポートページ群 (※下記ポリシー参照)
```

## 運用ポリシー

### サブページの扱い

- `rubysketch/` と `rubysolitaire/` は **App Store 公開アプリのサポートページ** (プライバシーポリシー / 利用規約 / 紹介など) として既に運用されている。
- これらの **markdown 本文は原則編集しない**。見た目の統一が必要な場合は共通レイアウト (`_layouts/page.html`) とスタイル (`assets/css/main.scss` の `.page-content`) 側で対応する。
- 法務文書の文言を変えると App Store 申請と整合が取れなくなる可能性があるため、コンテンツ変更はユーザー確認必須。

### トップページの情報

- `_data/apps.yml` / `_data/gems.yml` を編集するとカード一覧が更新される。新しいアプリや gem を追加するときはここに一行足すだけ。
- 連絡先 (`hello@xord.org` など) と SNS ハンドルは `index.md` / `_includes/footer.html` / `_config.yml` の 3 か所にあるので変更時は同期する。
- `hello@xord.org` は**仮のプレースホルダ**。屋号ドメインメールの実セットアップは未完了なので、公開前に実在アドレスに差し替える必要がある。

### デザイン方針

- カラフル・プレイフル寄り。太いインクの枠線 + オフセットシャドウ + グラデーションアクセント。
- タイポグラフィは見出しに Fraunces、本文に Inter、等幅に JetBrains Mono (Google Fonts)。
- カラーパレットは `assets/css/main.scss` の `:root` CSS 変数で一元管理。

## よくある作業

- **アプリや gem を追加**: `_data/apps.yml` か `_data/gems.yml` を編集。
- **配色調整**: `assets/css/main.scss` の `:root` 変数を触る。
- **新規サブページ追加**: トップレベルに markdown ファイルを置けば `layout: page` が自動適用される。front matter に `title:` を入れれば SEO タグに反映される。
- **ローカルプレビュー**: `bundle exec jekyll serve` (デフォルト `http://127.0.0.1:4000/`)。
