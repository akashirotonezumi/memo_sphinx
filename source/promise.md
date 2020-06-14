# 非同期処理について

[DemoPage](./_static/demo/20191215.html)



APIなど取得に時間がかかる処理を非同期でさせると
取得完了を待たず描画処理に進んでしまいエラーになる

読み込みや取得完了後に、結果が返ってきたことを確認してから
実行するようにする→ Promise

> 外部サイト「JavaScript Promiseの本」<br>
> [https://azu.github.io/promises-book/](https://azu.github.io/promises-book/)



## 〇秒後に実行させる関数
```
async promiseMin(min) {
    return new Promise((resolve) => {
        setTimeout(
            () => {
                resolve(`${min}秒後の実行 - ${this.time()}<br>`);
            }, min * 1000,
        );
    });
},
```

## 順番に実行させる関数
```
let self = this;
async function promiseAwait() {
    self.txt += await self.promiseMin(3);
    self.txt += await self.promiseMin(5);
};
```

## 同時に開始してすべての完了を待つ関数
```
let self = this;
async function promiseAll() {
    return Promise.all([self.promiseMin(5), self.promiseMin(10)]);
}
```

## エラーの場合
[DemoPage](./_static/demo/20191216.html)


