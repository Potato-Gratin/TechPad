||||
|:-|:-|---|
|**論理エンティティ名**|バッジ|
|**物理エンティティ名**|badge|
|**概要**|レビュワーがレビューに対して贈るバッジ。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|バッジid|id|UUID|NN||PK|
|レビューid|review_id|serial|NN||FK(review.id)|
|記事id|article_id|UUID|NN||FK(review.article_id)|
|ユーザーid|user_id|UUID|NN||FK(user.id)|
|作成日|created_at|TIMESTAMP|NN|||
|最終更新日|updated_at|TIMESTAMP|NN||
