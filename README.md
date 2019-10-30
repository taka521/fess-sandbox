# Fess Sandbox

オープンソースの全文検索サーバである、FESSの検証リポジトリ

* https://fess.codelibs.org/ja/


## ビルド＆実行

`/book` ディレクトリに任意のPDF等を格納し、以下のコマンドを実行

```bash
$ docker-compose build
$ docker-compose up
```

`localhost:8080` にアクセスし、FESSのTOPページが表示されればOK

<img src="./img/01.png" width="50%">

## ファイルクローリング

1.FESSのTOPページから「ログイン」をクリック。

2.ユーザ名とパスワードを入力して「ログイン」をクリック。  
* ユーザ名；admin
* パスワード；admin

<img src="./img/02.png" width="50%">

3.メニューの「クローラ」＞「ファイルシステム」を選択。  
<img src="./img/03.png" width="50%">

4.「新規作成」をクリック。  
<img src="./img/04.png" width="50%">

5.「名前」には任意の値、「パス」には `file:/var/tmp/books` を入力して、一番下の「作成」クリック。
<img src="./img/05.png" width="50%">

6.メニューの「クローラ」＞「ファイルシステム」を選択し、先ほど作成したクローラ名をクリック。  
<img src="./img/06.png" width="50%">

7.一番下までスクロールし、「新しいジョブの作成」をクリック。  
<img src="./img/07.png" width="50%">

8.「作成」をクリック。  
<img src="./img/08.png" width="50%">

9.ジョブスケジューラ一覧画面に遷移するので、先ほど作成したスケジューラ名をクリックし、「今すぐ開始」をクリック。   
<img src="./img/09.png" width="50%">

10.しばらく待って、TOPページから検索を行ってヒットすればOK。  
<img src="./img/10.png" width="50%">


## 残件

- [ ] Elasticsearchをクラスタ化する