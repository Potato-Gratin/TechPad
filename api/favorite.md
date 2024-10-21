ルーティングの優先度順
|HTTPメソッド|機能名|機能説明|備考|
|-|-|-|-|
|GET /articles/:id/favorites/count|いいね数取得|記事についているいいね数を取得する|指定した記事が存在しない場合、400 Bad Request を返す|
|POST /articles/:id/favorites|いいね追加|指定した記事に対していいねを送信する|記事IDが存在しない場合、400 Bad Request を返す|
|DELETE /articles/:id/favorites|いいね削除|指定した記事に送っていたいいねを取り消す|削除するいいねが存在しない場合、400 Bad Request を返す|
|||||
