||||
|:-|:-|---|
|**論理エンティティ名**|記事|
|**物理エンティティ名**|article|
|**概要**|記事の情報をまとめたテーブル|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|ID|id|UUID|NN|auto_increment|PK|
|タイトル|title|TEXT|NN|||
|本文|content|TEXT|NN|||
|投稿日|created_at|DATE|NN|||
|最終更新日|updated_at|DATE|NN||
|公開フラグ|is_public|boolean|NN||
|閲覧数|view_count|count||0||
|投稿者id|user_id|UUID|NN||FK|