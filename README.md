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

### データ定義部分の分割
下の例のように、「script.js」でDogインスタンスを定義している部分を、新しく作る「dogData.js」に移動する。

▼ ディレクトリ／ファイル構成
```
【src】
・script.js（記述の一部を新規作成のdogData.jsに移動）
・dataDog.js（新規作成してscript.jsから記述を移動）
・dog.js
・animal.js
```
