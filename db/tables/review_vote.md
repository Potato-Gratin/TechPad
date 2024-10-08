||||
|:-|:-|---|
|**論理エンティティ名**|レビュー票|
|**物理エンティティ名**|review_vote|
|**概要**|記事の情報をまとめたテーブル|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|レビューid|review_id|UUID|NN|auto_increment|PK|
|ユーザーid|user_id|UUID|NN||PK FK|
|票スコア|score|count|NN||PK FK|
