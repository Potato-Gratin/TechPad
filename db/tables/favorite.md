||||
|:-|:-|---|
|**論理エンティティ名**|いいね|
|**物理エンティティ名**|favorite|
|**概要**|閲覧者が記事に対して送るいいね。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|ユーザーid|user_id|UUID|NN||PK<br>FK(user.id)|
|記事id|article_id|UUID|NN||PK<br>FK(article.id)|
|作成日|created_at|TIMSTAMPZ|NN|||
|最終更新日|updated_at|TIMSTAMPZ|NN||

