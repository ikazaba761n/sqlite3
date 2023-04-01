# sqlite3
sqlite3の使い方


/mnt/c/Users/sqlite$ sqlite3 rdtest.sqls

sqlite3 　データベースフィル名　retest.sqls  上記　表示のように続けて入力する。




SQLite version 3.27.2 2019-02-25 16:06:06
Enter ".help" for usage hints.
sqlite>

バージョン名が表示される
　.help　の入力で　使い方のヒントが 表示されるとメッセージ

 .tables  テーブル名を取得　.ドットをつけていることに注意
sqlite> .tables
test3       test_table  user

test3 テーブル名       test_table テーブル名　  user テーブル名　　
三個のテーブルがあることを表示された。



次は　test3の内容を　表示する　select * アスタリングで　すべてを表示


sqlite>  SELECT * FROM test3;
1|Yamada|706
2|suzuki|706
3|sato|706
4|tanaka|706
5|saito|707

カラム名を表示させるのには　pragma　を使う　カラムとは 行列で表現される表の「列」
sqlite> PRAGMA table_info('test3');


0|id|int|0||1
1|name|text|0||0
2|date|int|0||0



pragma　コマンドを　テーブル名を指定して入力

ここで　ドットを入力していないことを注意　コマンドと　sql文の混同するが覚えるしかない

取得した構造の説明をすると　左から一番目は　数字データ　二番目はテキスト文字　三番目は数字データ　

id　name　date　の名前となる
