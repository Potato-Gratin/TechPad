||||
|:-|:-|---|
|**論理エンティティ名**|レビュー|
|**物理エンティティ名**|review|
|**概要**|レビューの情報をまとめたテーブル|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|ID|id|UUID|NN|auto_increment|PK|
|記事id|article_id|UUID|NN||PK FK|
|本文|content|TEXT|NN|||
|投稿日|created_at|DATE|NN|||
|最終更新日|updated_at|DATE|NN||
|ユーザid|user_id|UUID|NN||FK|
|親レビューid|parent_review_id|UUID|NN||FK|