ルーティングの優先度順
401 Unautholized については明記していない

|HTTPメソッド|機能名|機能説明|備考|
|-|-|-|-|
|**user**||||
|POST /users|ユーザー追加|新しいユーザーデータを挿入する|ユーザー名、表示IDが必須。重複する表示IDが既に存在する場合、409 Conflict を返す|
|GET /users/search|ユーザー検索|検索文字列とページ数に応じたユーザー情報を返す|クエリパラメータにq（検索文字列）が必須、page（ページ数）が任意で付与できる（ない場合のデフォルト値は1）。1ページにつき30件を取得する。パラメータがない場合は 400 Bad Request を返す。検索はユーザー名との部分一致で行う。|
|GET /users/:id|ユーザー情報取得|ユーザー情報を取得する|ユーザーIDが必要。表示IDが存在しない場合、404 Not Found を返す|
|GET /users/:displayId|ユーザー情報取得|ユーザー情報を取得する|ユーザーIDが必要。表示IDが存在しない場合、404 Not Found を返す|
|PATCH /users/:displayId|ユーザー情報更新|ユーザーの情報を更新する|更新データに不備がある場合は 400 Bad Request を返す。ユーザーIDが更新後に重複する場合、409 Conflict を返す|
|**article**||||
|POST /articles|記事追加|記事データを挿入する||
|GET /articles/search|記事検索|検索文字列とページ数に応じた記事情報を返す|クエリパラメータにq（検索文字列）が必須、page（ページ数）が任意で付与できる（ない場合のデフォルト値は1）。1ページにつき30件を取得する。パラメータがない場合は 400 Bad Request を返す。検索は記事名との部分一致で行う。|
|GET /articles/:id|記事情報取得|記事情報を取得する|IDが存在しない場合、404 Not Found を返す|
|GET /articles/users/:displayId|ユーザー記事情報取得|ユーザーのプロフィールに書いた記事を一覧表示する|ユーザーIDが存在しない場合、404 Not Found を返す|
|PATCH /articles/:id|記事情報更新|IDに対する記事の情報を更新する|IDが存在しない場合は 404 Not Found、更新データに不備がある場合は 400 Bad Request を返す。|
|DELETE /articles/:id|記事削除|IDに対する記事を削除する|削除データが存在しない場合は 400 Bad Request を返す|
|**favorite**||||
|GET /articles/:id/favorites/count|いいね数取得|記事についているいいね数を取得する|記事が存在しない場合、404 Not Found を返す|
|POST /articles/:id/favorites|いいね追加|指定した記事に対していいねを送信する|記事IDが存在しない場合、404 Not Found を返す|
|DELETE /articles/:id/favorites|いいね削除|指定した記事に送っていたいいねを取り消す|削除するいいねが存在しない場合、404 Not Found を返す|
|**review**||||
|GET /reviews/articles/:articlesId|記事ごとのレビュー情報取得||クエリパラメータにpage（ページ数）が付与できる（付与しない場合のデフォルト値は1）。1ページ当たり10件を取得する。|
|POST /reviews/articles/:articleId|レビュー追加|レビューを投稿する|記事IDが存在しない場合、404 Not Found を返す|
|GET /reviews/users/:displayId|ユーザーごとのレビュー情報取得|ユーザーが投稿したレビューの一覧を取得する。|ユーザーが存在しない場合は 404 Not Found を返す|
|DELETE /reviews/:reviewId/articles/:articleId|レビュー削除||記事ID、レビューが存在しない場合、404 Not Found を返す|
|**review_vote**||||
|GET /review_votes/score/articles/:articleId/reviews/:reviewId|レビュースコア取得|レビューについているスコアの総計を取得する|記事、レビューが存在しない場合、404 Not Found を返す|
|PUT /review_votes/articles/:articleId/reviews/:reviewId|レビュー票追加・更新|指定したレビューに対してレビュー票を送信する。既に存在していた場合、置き換える|記事、レビューが存在しない場合、404 Not Found を返す|
|DELETE /articles/:id/reviews/:reviewId/users/:userId|レビュー票削除|指定したレビューに送っていたレビュー票を取り消す|取り消すレビュー票が存在しない場合、404 Not Found を返す|
|**badge**||||
|POST /budges/articles/:articleId/reviews/:reviewId|バッジ追加|記事、レビューが存在しない場合、404 Not Found を返す|
|GET /budges/articles/:articleId/reviews/:reviewId|レビューごとのバッジ情報取得|記事、レビューが存在しない場合、404 Not Found を返す|
|GET /budges/receive/users/:displayId|自分が受け取ったバッジ一覧取得|ユーザーが存在しない場合、404 Not Found を返す|
|GET /budges/send/users/:displayId|自分が贈ったバッジ一覧取得|ユーザーが存在しない場合、404 Not Found を返す|
|**badge_text**||||
|GET /badge_texts|バッジテキスト一覧取得|||
|GET /badge_texts/:budgeTextId|バッジテキスト取得|バッジテキストが存在しない場合、404 Not Found を返す|
|**badge_flame**||||
|GET /badge_flames|バッジフレーム取得|||
|GET /badge_flames/:badgeFlameId|バッジフレーム一覧取得||バッジフレームが存在しない場合、404 Not Found を返す|
