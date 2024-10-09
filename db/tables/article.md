||||
|:-|:-|---|
|**論理エンティティ名**|記事|
|**物理エンティティ名**|article|
|**概要**|投稿者によってサービスに投稿される記事。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|記事id|id|UUID|NN||PK|
|タイトル|title|TEXT|||CHECK(255文字以下)|
|本文|content|TEXT|||CHECK(300,000文字以下)|
|作成日|created_at|DATE|NN|||
|公開日|published_at|DATE||||
|最終更新日|updated_at|DATE|NN||
|公開フラグ|is_public|boolean|NN|false||
|閲覧数|view_count|count|NN|0||
|投稿者id|user_id|UUID|NN||FK|