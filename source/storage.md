# ブラウザセッションを使う

[DemoPage](./_static/demo/20191214.html)


## 保存
```
sessionStorage.setItem('セッション名',
    JSON.stringify({
        abc: 'じょうほう',
    })
);
```

## 取得
```
var hensuu = JSON.parse(sessionStorage.getItem('セッション名'));
```


## 削除
```
sessionStorage.removeItem('セッション名');
```


