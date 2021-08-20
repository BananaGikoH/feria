# feria, the gerden of felesitas.cloud

## feriaとは

felesitas.cloudというmastodonサーバーの参加者用の、内部の方同士で交流するためのアプリです。

## felesitas.cloudとは

[felesitas.cloud](https://felesitas.cloud/)
[mastodon](https://github.com/mastodon/mastodon)というマイクロブログ投稿用SNSを運用しています。
[fediverse](https://ja.wikipedia.org/wiki/Fediverse)の一部なので、他のサーバーからfelesitas.cloudの投稿を見ることができます。
2017年6月29日にサーバーを開設し、今日まで運用を続けています。

## 作成経緯

felesitas.cloudを運用し続けてきて、fediverse内で「アカウントを作成してみたい」という声を頂き続け、
少人数ながらお陰様で参加者が増え続けています。
内部の交流を見ていて、設立者の私は、内部の盛り上がりに寄与できる"場"が必要であると感じました。
また、felesitas.cloudでは、アカウントを作成する際にハードルを設けているのですが、
その時にできた参加者の成果物を、内部で相互に見たいという声を頂きました。
また、ハードルを超える際の確認等を、今までは希望者とお話ししながら行っていましたが、
これからはアプリケーションの力を借りながら行いたいと考えました。

## コンセプト

felesitas.cloudは私の個人サーバー、という位置づけで運用していますが、
参加者の方は、「大きなアパートの住人の一人」という感覚を私を含め持っており、"荘"の住人、という発言をスラング的に使うことがたまにあります。
このアプリケーションは、そんな"荘"にある、広い"庭"をイメージして開発を進めています。

## 開発言語

現在はruby on railsで構築されています。
理由は、私がweb開発の初学者であり、mastodonの開発が同アプリでなされていたため、mastodon、ひいてはwebアプリケーションの技術習得になるのではないかと考えて、今回は上記を選択しました。
後に、より適切だと考えるアプリケーションが選択され、再開発される可能性もあります。

## ライセンス

このアプリケーションは、AGPL(the GNU Affero General Public License)のもと、公開しています。
This program is released under license AGPL.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU Affero General Public License for more details.
You should have received a copy of the GNU Affero General Public License along with this program.  If not, see <https://www.gnu.org/licenses/>.
[LICENSE.md](LICENSE.md) もご覧ください。

## 著者
“Copyright 2021, 2021 nagiko”

nagiko
mastodon: [@BananaGiko_cle@felesitas.cloud](https://felesitas.cloud/@BananaGiko_cle)
github: [BananaGikoH](https://github.com/BananaGikoH)
mail: nagiko.felesitas＊protonmail.com (*→@)

## 起動の仕方

このアプリケーションを動かす場合は、まずはリポジトリを手元にクローンしてください。
その後、次のコマンドで必要になる RubyGems をインストールします。

```
$ bundle install --without production
```

その後、データベースへのマイグレーションを実行します。

```
$ rails db:migrate
```

最後に、テストを実行してうまく動いているかどうか確認してください。

```
$ rails test
```

テストが無事に通ったら、Railsサーバーを立ち上げる準備が整っているはずです。

```
$ rails server
```

参考:[*Ruby on Rails チュートリアル*](https://railstutorial.jp/)