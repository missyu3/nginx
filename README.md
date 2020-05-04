# README
### Nginx
- 基本
  - apacheなどと同じwebサーバの一つ。
  - NginxとRackは直接つなげることができないので、Unicornを挟む必要がある。
  - プロセス数が数千あるので、同時に多くの人に見られても大丈夫。

### コマンド
- Install
  - brew install nginx
- 起動
  - nginx
    - ターミナルには何も出力されない
- 停止
  - nginx -s stop
  - ターミナルには何も表示されない
- Version確認
  - nginx -v

- URL
  - http://localhost:8080/

### キーワード
- rack
  - rubyで書かれた様々なwebフレームワークとwebサーバーをrack自身の柔軟性によって繋いでくれるもので、webサーバ、webフレームワークのどちらが変わってもサイトとしてうまく機能をするようにしてくれているものです。
- Unicorn
  - NginxとRackをうまく繋いでくれるWebサーバとアプリケーションサーバの中間のような存在。
  - UnicornとRackだけでRailsを動かすことも可能。しかし、プロセス数が少ないため、大勢のアクセスへの対処が難しい。
  - Unicornのドキュメントでもnginxと組み合わせることを推奨しているため、Unicornを選ぶ際にwebサーバも自然とNginxになる。

### 参考
- https://qiita.com/takahiro1127/items/fcb81753eaf381b4b33c