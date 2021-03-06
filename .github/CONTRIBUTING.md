# Contributing Guide

チーム開発時のGithubの取り扱い方に慣れていないため、ブランチ名やコミットメッセージの規約などをお試しで設定して運用していく。

## コミットメッセージ

以下の記事の通りにコミットメッセージを作成する。なお運用に応じて都度改善していく。

- [[Qiita] 僕が考える最強のコミットメッセージの書き方](https://qiita.com/konatsu_p/items/dfe199ebe3a7d2010b3e)

記事中で提示されているコミットの **Type** は以下になる。

- feat: 新しい機能
- fix: バグの修正
- docs: ドキュメントのみの変更
- style: 空白、フォーマット、セミコロン追加など
- refactor: 仕様に影響がないコード改善(リファクタ)
- perf: パフォーマンス向上関連
- test: テスト関連
- chore: ビルド、補助ツール、ライブラリ関連

記事の元ネタである[angular/angular.js](https://github.com/angular/angular.js/blob/master/DEVELOPERS.md#type)では、実際のコミットメッセージは上記のTypeに合わせて次のようになっていることが多い。

```bash
type(<scope>): 理由付きのコミット内容
```

## ブランチ運用

Gitのブランチモデルとしては、「[Github-Flow](http://scottchacon.com/2011/08/31/github-flow.html)」を採
用する。

基本的に作成するブランチは以下の2つのみにする。

- mainブランチ
- featureブランチ

作業の流れは以下である。

1. `main`ブランチから作業用ブランチを作成する
2. 作業用ブランチ名は`feature/<作業内容>`
3. 作業用ブランチに定期的にプッシュする
4. プルリクエストを実施
5. プルリクエストが承認されたら`main`ブランチにマージ
6. 作業用ブランチの削除

## issue依頼

以下に記載しているテンプレートに従う形式でISSUEの依頼をよろしくお願いします！

[https://github.com/KeisukeShimokawa/praha-challenges/issues/new/choose](https://github.com/KeisukeShimokawa/praha-challenges/issues/new/choose)

## pull request

プルリク時はテンプレートにしたがって記載をお願いします。

説明文にissueなどを紐づけていただけるとありがたいです。

## 文書作成時の注意点

文書中にIPアドレスなどを記載する場合は、以下を参考にする。

| RFC                                            | 内容                                                       | 例                                                | 
| ---------------------------------------------- | ---------------------------------------------------------- | ------------------------------------------------- | 
| [RFC1918](https://tools.ietf.org/html/rfc1918) | プライベートネットワークのために、予約されているIPアドレス | 10.0.0.0/8<br>172.16.0.0/12<br>192.168.0.0/16     | 
| [RFC5737](https://tools.ietf.org/html/rfc5737) | ドキュメントなどで使用するテスト用のIPアドレス             | 192.0.2.0/24<br>198.51.100.0/24<br>203.0.113.0/24 | 
