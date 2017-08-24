# node-react-proxy
react初心者が作ったAPIのCORS環境を乗り越えるための設定

# How to use
1. webpack.config.js のproxy設定を変更
`your-api-server-host:port` をproxyしたいバックエンドのサーバにする
```
'/api/*': {
  target: 'http://your-api-server-host:port',
  secure: false
}
```

2. index.htmlをいじってサンプルのajaxリクエストを確認する
```
res = $.get('/api/v1/users'); // this is sample url. FIXME!!
console.log(res);
```

3. start server
```
$ yarn install
$ npm start
```

4. http://localhost:8080 にアクセス  
コンソールにAPIアクセスのログが出ていればok

# Special Thanks
以下のQiitaの記事を参考にさせていただきました  
http://qiita.com/yutasuzuki/items/83d2bfdfa58341a1e99e
