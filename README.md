jQuery SmoothScroll JS
======================
今さら感たっぷりなスムーススクロールプラグイン

デモ
------
・シンプルスクロール
http://dev.creatorish.com/demo/smooth-scroll/index.html

・上下左右スクロール
http://dev.creatorish.com/demo/smooth-scroll/tile.html

・スクロールミニゲーム（ネタ）
http://dev.creatorish.com/demo/smooth-scroll/game.html

使い方
------
### HTML ###

href属性にスクロール先のIDを記述します。

    <body id="top">
    <!--略-->
    <a href="#top" class="hoge">scroll top</a>

### JavaScript ###

jquery.smoothScroll.jsを読み込んで以下のように記述します。

    $(".hoge").smoothScroll();

オプション
------

smoothScrollの第一引数でオプションを指定できます。

    $(".hoge").smoothScroll({
        easing: "swing",
        duration: 500,
        cancel: true,
        start: function(x,y) {},
        step: function(x,y){},
        canceled: function(x,y) {},
        complete: function(x,y){}
    });

+    easing: スクロールに使うイージング名。jQuery Easing Pluginが使えます。
+    duration: スクロール時間
+    cancel: スクロール開始後にマウスホイール操作やクリック操作が行われたらスクロールを中止するかどうか
+    start: スクロールが開始されたときに実行する処理
+    step: スクロールの度に実行する処理
+    canceled: スクロールがキャンセルされたときに実行する処理
+    complete: スクロールが完了したときに実行する処理

TODO
------

+    overflow:hiddenやautoの要素のスムーススクロール

ライセンス
--------
[MIT]: http://www.opensource.org/licenses/mit-license.php
Copyright &copy; 2012 creatorish.com
Distributed under the [MIT License][mit].

作者
--------
creatorish yuu  
Weblog: <http://creatorish.com>  
Facebook: <http://facebook.com/creatorish>  
Twitter: <http://twitter.jp/creatorish>