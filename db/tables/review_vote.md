||||
|:-|:-|---|
|**論理エンティティ名**|レビュー票|
|**物理エンティティ名**|review_vote|
|**概要**|レビュワーがレビューに対して送る評価。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|レビューid|review_id|serial|NN||PK <br> FK(review.id)|
|記事id|article_id|UUID|NN||PK <br> FK(review.article_id)|
|ユーザーid|user_id|UUID|NN||PK<br> FK(user.id)|
|票スコア|score|INT|NN|||
|作成日|created_at|TIMESTAMPZ|NN|||
|最終更新日|updated_at|TIMESTAMPZ|NN||
