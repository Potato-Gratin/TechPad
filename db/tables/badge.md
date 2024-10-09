||||
|:-|:-|---|
|**論理エンティティ名**|バッジ|
|**物理エンティティ名**|badge|
|**概要**|レビュワーがレビューに対して贈るバッジ。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|バッジid|id|UUID|NN||PK|
|レビューid|review_id|UUID|NN||PK<br> FK(review.id)|
|ユーザーid|user_id|UUID|NN||FK(user.id)|
