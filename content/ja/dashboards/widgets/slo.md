---
title: SLO サマリーウィジェット
kind: documentation
description: SLO を追跡します。
aliases:
  - /ja/monitors/monitor_uptime_widget/
  - /ja/monitors/slo_widget/
  - /ja/graphing/widgets/slo/
  - /ja/dashboards/faq/how-can-i-graph-host-uptime-percentage/
further_reading:
  - link: 'https://www.datadoghq.com/blog/slo-monitoring-tracking/'
    tag: ブログ
    text: Datadog ですべての SLO のステータスを追跡する
---
## セットアップ

SLO サマリーウィジェットを使用して、スクリーンボードとタイムボードで [SLO (サービスレベル目標)][1] を追跡できます。Datadog の[サービスレベル目標ページ][2]で、SLO の新規作成や既存 SLO の一覧表示が可能です。画面上で既存の SLO を選択し、SLO サマリーウィジェットを使用して任意のダッシュボードに SLO を表示させます。

{{< img src="dashboards/widgets/slo/slo_summary_editor.png" alt="SLO サマリーウィジェット"  >}}

### 構成

1. ダッシュボードページで SLO サマリーウィジェットを追加します。
2. ドロップダウンメニューから SLO を選択します。
3. タイムウィンドウは 3 つまで選択できます。

**注:** SLO は 7 日、30 日、90 日間のタイムウィンドウで構成可能です。すべての SLO で `Week to date` タイムウィンドウを選択します。SLO に最低 30 日間のタイムウィンドウ構成が適用されている場合は、`Previous week` タイムウィンドウを選択できます。SLO に 90 日間のタイムウィンドウ構成が適用されている場合は、`Month to date` または `Previous month` タイムウィンドウを選択できます。

### オプション

#### 表示設定

`Show error budget` オプションのトグルで、残りのエラーバジェットの表示/非表示を操作します。複数のグループまたはモニターでモニターベースの SLO を閲覧している場合は、`View mode` を選択します。

- 複数のグループに分割された単一モニターでモニターベースの SLO を構成している場合は、以下の 3 つのビューモードが利用可能です。
  - `Status`: SLO の総合ステータスの割合と目標を表示します
  - `Groups`: 各グループのステータス割合を表形式で表示します
  - `Both`: 総合 SLO ステータスの割合と目標、各グループのステータス割合表の両方を表示します

- 複数モニターでモニターベースの SLO を構成している場合は、以下の 3 つのビューモードが利用可能です。
  - `Status`: SLO の総合ステータスの割合と目標を表示します
  - `Monitors`: 各モニターのステータス割合を表形式で表示します
  - `Both`: 総合 SLO ステータスの割合と目標、各モニターのステータス割合表の両方を表示します

{{< img src="dashboards/widgets/slo/slo_summary-view_mode.png" alt="ビューモード"  >}}

#### タイトル

`Show a title` チェックボックスをオンにして、ウィジェットのカスタムタイトルを表示します。

{{< img src="dashboards/widgets/slo/slo_summary-show_title.png" alt="ウィジェットタイトル"  >}}

オプションで、タイトルのサイズと配置を定義できます。

## その他の参考資料

{{< partial name="whats-next/whats-next.html" >}}

[1]: /ja/monitors/service_level_objectives/
[2]: https://app.datadoghq.com/slo