<!-- pre-align:aligned sig=9a6130697b7f -->

<a id="release-notes"></a>
## Cloud Schedulerリリースノート { #release-notes }

**Application Service > Cloud Scheduler > リリースノート**

<a id="april-28-2026"></a>
## 2026. 04. 28. { #april-28-2026 }
<a id="feature-updates"></a>
### 機能改善/変更 { #feature-updates }
* 対象テンプレートを使用してスケジュール/スケジュールテンプレートを作成する際、機密情報が画面に表示されません。
* 対象テンプレートを使用してスケジュール/スケジュールテンプレートをコピーする際、機密情報を除く情報のみコピーされます。

<a id="november-25-2025"></a>
## 2025. 11. 25. { #november-25-2025 }
<a id="added-features"></a>
### 機能追加 { #added-features }
* スケジュール実行結果の検証機能が追加されます。

<a id="september-23-2025"></a>
## 2025. 09. 23. { #september-23-2025 }
<a id="september-23-2025-feature-updates"></a>
### 機能 改善/変更 { #september-23-2025-feature-updates }
* スケジュールの実行に失敗した場合、エラーの原因を簡単に確認できるようにログメッセージを改善しました。

<a id="june-24-2025"></a>
## 2025. 06. 24. { #june-24-2025 }
<a id="bug-fixes"></a>
### バグ修正 { #bug-fixes }
* パラメータ(Request Body)がJSONオブジェクトでのみ入力必須となっていたバグを修正しました。

<a id="may-27-2025"></a>
## 2025. 05. 27. { #may-27-2025 }
<a id="may-27-2025-bug-fixes"></a>
### バグ修正 { #may-27-2025-bug-fixes }
* 開始/終了日時のタイムゾーンに関するコンソールメッセージを修正しました。

<a id="april-29-2025"></a>
## 2025. 04. 29. { #april-29-2025 }
<a id="april-29-2025-bug-fixes"></a>
### バグ修正 { #april-29-2025-bug-fixes }
* スケジュールの作成・修正時に、Cron式を毎週日曜日に設定するとスケジュールの実行時間が表示されないバグを修正しました。

<a id="march-25-2025"></a>
## 2025. 03. 25. { #march-25-2025 }
<a id="march-25-2025-added-features"></a>
### 機能追加 { #march-25-2025-added-features }
* 対象テンプレート機能が追加されます。

<a id="march-25-2025-feature-updates"></a>
### 機能改善/変更 { #march-25-2025-feature-updates }
* スケジュール及びテンプレートの作成・修正時に、パラメータのサイズを256KBに制限するよう修正しました。

<a id="january-21-2025"></a>
## 2025. 01. 21. { #january-21-2025 }
<a id="january-21-2025-feature-updates"></a>
### 機能改善/変更 { #january-21-2025-feature-updates }
* スケジュール作成時の制限条件を追加
  * スケジュール作成及び修正時にURLの長さを255文字に制限するように修正しました。
  * スケジュール作成及び修正時にパラメータのサイズを56KBに制限するように修正しました。
  * スケジュール作成及び修正時に開始日時を現在時刻から5分以降にのみ設定できるように修正しました。
* スケジュール及びテンプレートの検索時、検索キーワードの前後のスペースを無視するよう修正しました。
* エラーメッセージを修正しました。

<a id="december-24-2024"></a>
## 2024. 12. 24. { #december-24-2024 }
<a id="december-24-2024-added-features"></a>
### 機能追加 { #december-24-2024-added-features }
* スケジュールテンプレート機能が追加されます。

<a id="november-26-2024"></a>
## 2024. 11. 26. { #november-26-2024 }
<a id="november-26-2024-bug-fixes"></a>
### バグ修正 { #november-26-2024-bug-fixes }
* スケジュールの実行が断続的に失敗するバグを修正しました。

<a id="oct-29-2024"></a>
## 2024. 10. 29. { #oct-29-2024 }
<a id="release-of-a-new-service"></a>
### 新規サービスリリース { #release-of-a-new-service }
* Cloud Schedulerは、様々なタスクを好きなスケジュールで実行するように設定できるサービスです。
