# tAni

## 概要
テキストアニメーションを行うスクリプトです。  
2020/03/15現在で Chorme / FireFox / Opera / Safariの最新版に対応しています。  

## 使用方法

使用したいhtmlの`head`タグ内に  
```html
<link rel="stylesheet" href="lib/text_animation.css">
<script src="lib/text_animation.js"></script>
```
と記述します。  
次に使用したい文字列のみをもつタグのClassに`.text-animation`を指定しその要素の直後または  
`window.onload`イベント時にコンストラクタで対象の要素のidを指定します。  
そのほかにも、出現方向(ランダムあり/なし)や表示速度、出現のタイミングを指定できます。  
いかに例を示します。
```html
<p id="title" class="text-animation">Hello World!</p>
<script>
window.onload = function(){
    var textAnimation = new tAni({
        id    : 'title',
        speed : 100,
        delay : 400,
        dir   : 'top',
        ran   : false
    });
}
</script>
```
  
`id`で対象要素のidを指定、`speed`で表示スピード、`delay`で出現タイミング、`dir`で出現方向、`ran`で出現方向のランダム有無を設定できます。  
`speed`と`delay`はミリ秒で指定します。また`ran`を`true`に設定した場合、`dir`は無効になります。

## サンプル
小規模なのでdemoページはありません。  
sampleディレクトリの`index.html`にサンプルがあります。
