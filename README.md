# es6-study-5-3-9
JavaScript 学習コース V > ファイルを分割しよう > 3.値のエクスポート

### 値のエクスポート
ファイルの分割で、エクスポートできるのはクラスだけではない。
文字列や数値や関数など、どんな値でもエクスポートができる。

▼ エクスポート側（sample01.js）
```
const text = "Hello World";
export default text;　/* 「export default 定数名」とする */
```
▼ インポート側（sample02.js）
```
import text "./sample01" /* 「import 定数名 from "./インポートするファイル名"」とする */
console.log(text);
```
▼ コンソールでの出力結果
```
Hello World
```
