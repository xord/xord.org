---
title: Midified
description: MIDI コントローラーを Mac のキーボードにする、メニューバーのアプリ。
lang: ja
permalink: /midified/ja/
url_en: /midified/
url_ja: /midified/ja/
---

# Midified

MIDI コントローラーを Mac のキーボードにする、メニューバーのアプリです。複雑なショートカットを鍵盤やパッドに割り当てたり、ノブを回して動画編集のタイムラインをシークしたり。どのアプリでも使えます。割り当ては Ruby の設定ファイルに書きます。

## 使い方

- 初めて起動したときに尋ねられたら、システム設定の「プライバシーとセキュリティ」>「アクセシビリティ」で Midified を許可してください。キーを送るのに必要です。
- メニューバーのメニューから「Open Config」を選び、ノートやコントロールをキーに割り当てます。

```ruby
note 36 => :space                 # ノートが鳴っているあいだ Space を押す
note 37 => command(:b)            # Command+B
note 38 => shift(command(:z))     # Shift+Command+Z

cc 20 do |value|                  # ノブを回すたびに、0..127
  key(value < 64 ? :left : :right)
end
```

- 設定を保存すると、自動で読み込み直します。
- 「Show MIDI Monitor」で、機器の名前、触ったパッドやノブの番号、送ったキーを確かめられます。

## よくある質問

### キーが送られません。

メニューバーのアイコンが「!」付きで薄くなっていれば、メニューの先頭に理由が出ています。項目を選ぶと、設定で Midified を許可したり、MIDI Monitor で設定のエラーを確かめたりできます。

### 許可したのに、まだキーが送られません。

Mac App Store 版は、起動し直したときに許可に気づきます。メニューから「Relaunch Midified」を選んでください。

### 設定はどこに保存されますか？

お使いの Mac の、このアプリ専用のデータ用フォルダーに保存します。「Open Config」で開けます。[プライバシーポリシー](/midified/privacy_policy.html)をご覧ください。

## サポート

ご質問、不具合、ご要望は [support@xord.org](mailto:support@xord.org) までお送りください。Midified と macOS のバージョン、MIDI 機器の名前を添えていただけると助かります。

- [プライバシーポリシー](/midified/privacy_policy.html)

----

&copy; 2026 xord.org
