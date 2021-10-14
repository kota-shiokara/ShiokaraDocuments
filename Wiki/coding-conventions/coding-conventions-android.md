# package名
- 全て小文字

# ファイル、クラス名
- UpperCamelCase
- 名詞
- Activity、Fragment、Adapterなどのコンポーネント名は末尾に付ける

# 関数名
- lowerCamelCase
- 動詞で始める。
  - fetch: インターネットから情報を取得する時
  - is: Booleanを返す時
  - ニュアンスなどが知りたい場合は[こちらの記事](https://php-archive.net/php/words-in-function-names/)を読んでください。
- 引数が複数の場合、カンマの後にスペースを開けましょう。
- 「)」と「{」の間にスペースを開けましょう。
```kotlin
// 良き
fun sendMessage(message: String, subMessage: String) {
}

// ダメ、先頭が大文字のUpperCamelCaseになってる
fun SendMessage(message: String, subMessage: String) {
}

// ダメ、引数のカンマの後や、「)」と「{」の間にスペースが無い
fun sendMessage(message: String,subMessage: String){
}

// ダメ、引数のカンマの後にスペースが無い
object.sendMessage("hogehoge","fugafuga")
```

# 変数名
- lowerCamelCase
- 単語("="など)の間にはスペースを開けましょう。
- 複数行あっても、書き出しの統一などを行うのはやめましょう。
- コロンの後には空白スペースを入れましょう。
- 書かなくてよくても、できる限り変数の型は書きましょう。

```kotlin
// 良き
var itemCount: Int = 0
var groupId: String = getGropId()
var userValue: UserValue = getUserValue()

// ダメ
var itemCount: Int       = 0
var groupId: String      = getGropId()
var userValue: UserValue = getUserValue()

var itemCount: Int = 0
var groupId:   String = getGropId()
var userValue: UserValue = getUserValue()

var itemCount:Int=0
var groupId:String=getGropId()
var userValue:UserValue=getUserValue()
```

# ローカル変数名
- 関数内などで扱う変数名ですが、適切な命名を心がけましょう。
- 使い捨ての変数の場合、`tmp`(temporary)を使用しても構いませんが、あまり望ましくありません。どうしても使用する場合はどのような変数なのかコメントに記述するようにしましょう。

# 定数名
### Intent
- Intentで渡す引数のキーは`EXTRA_`+`'キー名'`

### Fragment
- Fragmentに渡すキーは、`ARG_`+`'キー名'`

# リソース名
- 小文字とアンダースコア(_)のみを用いる。
- activityやfragment、item、ic(iconの意)などの接頭辞を付ける。

```
Fragment = fragment_hoge
CustomView = view_hoge
ItemView = item_view_hoge
```

# id名
- lowerCamelCase
```
<TextView
  android:id="@+id/yasashiTitle" />
<TextView
  android:id="@+id/yasashiContent" />
```

# 参考記事
[Kotlinスタイルガイド](https://developer.android.com/kotlin/style-guide?hl=ja&authuser=1)