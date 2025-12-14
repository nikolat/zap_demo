# saori_nostr.dll

## これは何?

デスクトップマスコット、「伺か」で使用できるSAORIの一種です。

Nostrを利用する上で必要な機能を提供します。

## 使い方

Argument0に、使用する機能名を指定して使用します。
指定できる機能は`generate_secret_key`と`create_zap_request`です。

### `generate_secret_key`

+ Result: HEX形式の秘密鍵
+ Value0: HEX形式の公開鍵
+ Value1: HEX形式の秘密鍵
+ Value2: npub形式の公開鍵
+ Value3: nsec形式の秘密鍵

新規に秘密鍵を生成します。

### `create_zap_request`

+ Argument1: Zap対象の公開鍵(HEX形式、npub形式どちらも可)
+ Argument2: amount (millisats)
+ Argument3: Zapコメント
+ Argument4: Zapレシート送信先リレーURL (1つのみ指定可)
+ Argument5: 署名用の秘密鍵(HEX形式、nsec形式どちらも可)

+ Result: イベントのJSON文字列

Zapリクエストイベントを作成します。

## 使用ライブラリ

+ [saori-interface-rs](https://github.com/tukinami/saori-interface-rs) / 月波 清火 (tukinami seika)
+ [ukagaka-dll-macro](https://github.com/tukinami/ukagaka-dll-macro) / 月波 清火 (tukinami seika)
+ [rust-nostr/nostr](https://github.com/rust-nostr/nostr) / rust-nostr

## ライセンス

LICENSEファイルを見てください。

## 作成者

Don

[GitHub](https://github.com/nikolat)
