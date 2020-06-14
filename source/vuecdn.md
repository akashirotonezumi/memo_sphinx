# Vue.js を使う（CDN）

[DemoPage](./_static/demo/20191211.html)



## CDN読み込み
```
<!-- vue-cdn-dev -->
<script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
```

## 基本
```
<section id="section1">
    <p>{{ blockTitle }}</p>
</section>

<script>
new Vue({
    el: '#section1',
    data: {
        blockTitle: '表示する文字',
    },
});
</script>
```

## PHP + Laravel（blade） + Vue の書き出し
```
<p>@{{ blockTitle }}</p>
```

## 関数
```
<div>{{ rnd() }}</div>

<script>
new Vue({
    el: '#section1',
    data: {
        blockTitle: '表示する文字',
    },
    methods: {
        rnd() {
            return Math.floor(Math.random() * 100);
        }
    }
});
</script>
```



### ボタンをランダムに配置
[DemoPage](./_static/demo/20191213.html)

### Vuejsでプログレスバーふう
[DemoPage](./_static/demo/20191212.html)

