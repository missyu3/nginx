# README
### Nginx
- 基本
  - apacheなどと同じwebサーバの一つ。
  - NginxとRackは直接つなげることができないので、Unicornを挟む必要がある。
  - プロセス数が数千あるので、同時に多くの人に見られても大丈夫。
  - リバースプロキシとして動作する
  - イベント駆動方式

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
- https://qiita.com/morrr/items/929e9cb35914a7f3a652
- https://qiita.com/kawaaa26/items/812e763266fe364045f9#3-nginxのconfigurationファイルの作成


heroku buildpacks　で確認
heroku buildpacks:set heroku/nodejs
heroku buildpacks:add --index 2 heroku/ruby