||||
|:-|:-|---|
|**論理エンティティ名**|バッジ|
|**物理エンティティ名**|badge|
|**概要**|バッジをまとめたテーブル|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|バッジid|id|UUID|NN|auto_increment|PK|
|レビューid|review_id|UUID|NN||PK FK|
|ユーザーid|user_id|UUID|NN||FK|
