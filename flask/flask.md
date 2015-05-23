class: middle center
# Flaskで作る<br>Webアプリケーション
.center[### Hiroki MIZUMOTO]
.center[**May,  2015**]

---
## Webアプリケーション

* Webブラウザから利用するアプリケーション
    * Webページ
    * Webゲーム
    * インターネットバンク
    * ネットショップ.etc

* スマートフォンからでもブラウザを利用すればWebアプリケーションに
    * アプリストアで落とせるのはネイティブアプリと呼ばれるもの
    * Facebookをアプリから使うと*ネイティブアプリ*
    * Facebookをブラウザから使うと*Webアプリ*を使ってることになる

---
## Webアプリケーションの仕組み
***Webアプリケーションはクライアントサーバモデル***
* クライアント(PCとかスマフォ)がサーバに「要求」し  
サーバがそれに「応答」する

---
## Webアプリケーションの仕組み
* サーバではクライアントに渡すデータを作成
    * データベースからデータを取り出したり
    * 複雑な計算を行ったり

* クライアントではサーバから受け取ったデータをレンダリング
    * CSSで綺麗な見た目
    * JSでリッチな操作感

---
## Flaskについて
* `Python`製のWebアプリケーションフレームワーク
* DBの操作や処理を`Python`で行える
* 非常に軽量なフレームワークなので学習コストが少ない(多分)
    * 大規模なアプリケーションを作成するときは....

* テンプレートエンジンは`jinja2`を使用
    * Pythonで作ったデータを簡単にHTMLに埋め込める!

* 他のPython製Webフレームワーク
    * Django
    * bottole
    * CherryPy
    * Pyramid

---
## Flaskのインストールと起動
* install

```shell
$ pip install Flask
```

* Flaskサンプルアプリ(```hello.py```)

```python:hello.py
from flask import Flask
app = Flask(__name__)

@app.route("/")
def hello():
    return "Hello World!"

if __name__ == "__main__":
    app.run()
```

* Flaskアプリケーションの起動

```shell
$ python hello.py
> * Running on http://localhost:5000/ (Press CTRL+C to quit)
```

---
## ページの確認
http://localhost:500/  
にアクセスするとHello World!と書かれたページが表示される

![img](http://i.gyazo.com/cce11997e848d51a17a1b97ed67c7f29.png)
