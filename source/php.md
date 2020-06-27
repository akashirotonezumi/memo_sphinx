# PHPのコードメモ

## 文字列系
### 数字のみを抜き出す
```
$_num = (int)preg_replace('/[^0-9]/', '', 'abc1-b3');
```

### 指定の文字が含まれる
```
$str = 'this is a pen.';  
if (strpos($str,'this') !== FALSE) {  
    // 含まれる  
} else {  
    // 含まれない  
}
```
> 0位置に含まれる = falseとなってしまうため型比較  

### 全角チルダを波ダッシュへ置換
```
$value = str_replace(hex2bin("E3809C"), hex2bin("EFBD9E"), $value);
```
> とり方：
echo bin2hex('～');
echo bin2hex('〜');

