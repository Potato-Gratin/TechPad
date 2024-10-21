ルーティングの優先度順
|HTTPメソッド|機能名|機能説明|備考|
|-|-|-|-|
|POST /articles|記事追加|記事データを挿入する||
|GET /articles/search|記事検索|検索文字列とページ数に応じた記事情報を返す|クエリパラメータにq（検索文字列）、page（ページ数）が必須。存在しない場合は 400 Bad Request を返す。検索は記事名との部分一致で行う。|
|GET /articles/:id|記事情報取得|記事情報を取得する|IDが存在しない場合、404 Not Found を返す|
|PATCH /articles/:id|記事情報更新|IDに対する記事の情報を更新する|IDが存在しない場合は 404 Not Found、更新データが存在しない場合は 400 Bad Request を返す。|
|DELETE /articles/:id|記事削除|IDに対する記事を削除する|削除データが存在しない場合は 400 Bad Request を返す|
