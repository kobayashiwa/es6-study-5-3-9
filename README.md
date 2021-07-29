# es6-study-5-3-9
JavaScript 学習コース V > ファイルを分割しよう > 3.値のエクスポート

### 値のエクスポート
ファイルの分割で、エクスポートできるのはクラスだけではない。
文字列や数値や関数など、どんな値でもエクスポートができる。

▼ エクスポートする場合（sample.js）
```
const text = "Hello World";
export default text;　/* 「export default 定数名」とする */
```
