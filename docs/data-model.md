# データモデル設計書

## ユーザー情報

| フィールド | 型 | 必須 | 説明 |
|---|---|---|---|
| userId | string | ○ | ユーザーID（一意識別子） |
| handleName | string | ○ | ハンドルネーム |
| gender | 'male' \| 'female' \| 'other' \| 'none' | ○ | 性別（'none' は未設定） |
| birthday | string (ISO 8601: YYYY-MM-DD) | - | 誕生日 |
| registeredAt | string (ISO 8601: YYYY-MM-DD) | ○ | サービス登録日 |

## ユーザー書籍情報マスタ

| フィールド | 型 | 必須 | 説明 |
|---|---|---|---|
| userId | string | ○ | ユーザーID |
| isbn | string | ○ | ISBN |
| folder | string | - | フォルダ名（フォルダ分けをしている場合） |
| status | 'read' \| 'want_to_read' \| 'unread' | ○ | 読書ステータス |
| registeredAt | string (ISO 8601: YYYY-MM-DD) | ○ | 登録日 |
| readAt | string (ISO 8601: YYYY-MM-DD) | - | 既読日 |
| isFavorite | boolean | ○ | お気に入りフラグ |
| rating | number (0.0-5.0) \| null | - | 評価レート（nullは未評価） |
| memo | string | - | メモ |
