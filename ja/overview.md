# Cloud Scheduler概要

**Application Service > Cloud Scheduler > 概要**

Cloud Schedulerは、様々なタスクを好きなスケジュールで実行するように設定できるサービスです。特定のタスクを決められたスケジュールに一度だけ実行したり、クロン(cron)式または間隔を設定して繰り返し実行できます。タスクは、APIエンドポイントを介して設定できます。APIエンドポイントは、事前に設定されたNHN Cloudサービスだけでなく、様々なサービスのAPIを自由に入力できます。設定した間隔に応じて繰り返しNHN Cloud Object StorageのオブジェクトをコピーするようなタスクがCloud Schedulerを利用したタスクの代表的な例です。

Cloud Schedulerで設定したスケジュールは、開始と終了日時を指定し、希望する期間のみ実行することができ、実行を望まない場合、無効にすることで簡単に実行を止めることができます。また、API呼び出しの失敗などでタスクが正常に完了しない場合、タスクを再実行するように再試行ポリシーを設定することもできます。

Cloud SchedulerはNHN Cloudの全てのリージョンで使用できます。


![Cloud Scheduler概要イメージ](https://static.toastoven.net/prod_cloud_scheduler/CloudScheduler_overview_ja_800.png)


<br>
この記事では、NHN CloudのCloud Schedulerサービスの主な機能、使用方法、用語を案内します。

## Cloud Schedulerの主な機能

* **様々な実行タイプ**
    * 指定した時点に一度だけ実行する一回限りの実行をサポートします。
    * Cron式とRateベースの繰り返し実行をサポートします。
* **便利なスケジュール管理**
    * スケジュールを有効化/無効化できます。
    * スケジュール実行履歴を通じて、成否、リクエスト及びレスポンスデータなどの詳細情報を把握できます。
    * スケジュールに基づくタスクが失敗した場合、再試行を設定できます。
* **NHN Cloudサービス連動をサポート**
    * NHN Cloudの様々なサービスの機能を対象テンプレートとして提供して簡単なスケジュール登録が可能です。
* (今後提供予定) **APIに対する対象テンプレート作成可能**
    * NHN Cloudサービスだけでなく、様々なAPIを直接入力することで対象テンプレートの作成が可能です。

## Cloud Schedulerを始める

* [スケジュール作成](create-schedule)
* [スケジュール管理](manage-schedule)

## 用語整理


| 用語 | 説明 |
| --- | --- |
| スケジュール | Cloud Schedulerを使用して作成したリソースで、実行タイプ、対象、再試行ポリシーなどの追加設定をすべて含む概念。 |
| Cron | 一定の時間間隔や特定の時刻にタスクを実行させるUNIXベースのタスクスケジューラ。Cron固有の表現式で作成する |
