# REPTILE NOTE v0.4.31

予定のクラウド共有を追加しました。

- 予定の新規登録・編集時に `save_event` へ保存
- 共有ノート参加時に `list_events` で予定を読み込み
- オーナー端末はクラウド予定を読み込み、ローカルだけの予定も保持
- 設定画面に既存予定の一括同期ボタンを追加
- 閲覧のみのゲストは保存API側で拒否されます

注意:
- 予定の削除APIは未実装です。画面で削除してもクラウド側には残ります。
- テスト予定や既存予定を一括同期する前に内容を確認してください。


## v0.4.32
- Owner/guest session tokens are restored from browser local storage; guest sessions persist across tabs/restarts.
- Initial local pets, records and events are automatically migrated once per workspace.
- Cloud data is fetched automatically on startup; owner local-only entries and photo data are preserved during merge.
- Share management no longer asks users to paste the owner token; participant list and share-link actions use the current session automatically.
- Existing edit/add handlers continue to sync pets, records and events automatically.
- Deletion sync and photo upload are not included in this version.
