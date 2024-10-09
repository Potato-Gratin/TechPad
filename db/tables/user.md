||||
|:-|:-|---|
|**論理エンティティ名**|ユーザー|
|**物理エンティティ名**|user|
|**概要**|サービスを利用するユーザー。|
|||

|論理名|物理名|データ型|Not null|デフォルト|備考|
|---|---|---|---|---|---|
|ユーザーid|id|UUID|NN||PK|
|表示id|display_id|TEXT|NN||UNIQUE<br>CHECK(1文字以上、15文字以下)|
|ユーザー名|name|TEXT|NN||CHECK(1文字以上、15文字以下)|
|説明|description|TEXT|||CHECK(400文字以下)|
|作成日|created_at|TIMESTAMP|NN|||
|最終更新日|updated_at|TIMESTAMP|NN||
