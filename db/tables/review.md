||||
|:-|:-|---|
|**論理エンティティ名**|レビュー|
|**物理エンティティ名**|review|
|**概要**|レビュワーが記事に対して送るレビュー。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|レビューid|id|UUID|NN||PK|
|記事id|article_id|UUID|NN||PK<br>FK(article.id)|
|本文|content|TEXT|NN||CHECK(10,000文字以下)|
|作成日|created_at|TIMESTAMPZ|NN|||
|最終更新日|updated_at|TIMESTAMPZ|NN||
|ユーザーid|user_id|UUID|NN||FK(user.id)|
|親レビューid|parent_review_id|UUID|||FK(review.id)|
|親記事id|parent_article_id|UUID|||FK(review.article_id)|
