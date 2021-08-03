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

### データ定義部分の分割（Dogインスタンスのエクスポート）
「dogData.js」はDogクラスをインポートし、Dogインスタンスである定数dogをエクスポート。
「script.js」は定数dogをインポートするようにする。

▼ ディレクトリ／ファイル構成
```
【src】
・script.js
・dataDog.js（新規作成）
・dog.js
・animal.js
```
#### 変更前
▼ script.js
```
import dog from "./dog"
const dog = new Dog("レオ", 4, "チワワ");
dog.info();
```
#### 変更後
▼ dogData.js
```
import dog from "./dog"
const dog = new Dog("レオ", 4, "チワワ");
export default dog;
```
▼ script.js
```
import dog from "./dogData"
dog.info();
```

## コーディングトレーニング
「GA technologies」のレイアウト構造をレスポンシブで写経する。

#### サイト構造
```
- header > logo - nav/toggle
- main > section（sitetop-hero） - section（sitetop-news） - section（sitetop-aboutus） - section（sitetop-careers） - section（siteinfo） - section（siteinfo）
- footer
```
