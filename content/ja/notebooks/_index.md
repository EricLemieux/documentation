---
title: ノートブック
kind: documentation
aliases:
  - /ja/graphing/notebooks/
further_reading:
  - link: /dashboards/screenboard/
    tag: ドキュメント
    text: スクリーンボードの作成
  - link: /dashboards/timeboard/
    tag: ドキュメント
    text: タイムボードの作成
---
## 概要

ノートブックは、グラフとテキストを組み合わせて 1 列のセル形式で表示し、事後分析、ランブック、ドキュメントなどを作成することで、データの背景情報を調査したり共有したりできるように設計されています。

{{< img src="notebooks/demo_notebook.png" alt="デモノートブック"  style="width:100%;">}}

## ライブコラボレーション

ノートブックは、リアルタイムコラボレーションをサポートします。プレゼンスインジケーターには、特定の時間にノートブックを閲覧しているユーザーが表示されます。インジケーターは、他に編集中のユーザーがいるセルにも表示されます。

{{< img src="notebooks/live_editing.png" alt="ノートブックのライブコラボレーション"  style="width:100%;">}}

ノートブックへの変更は、ページを更新しなくても自動的に反映されます。

ノートブックの閲覧および編集はどのチームメンバーでもできますが、削除ができるのは作成者または管理者のみです。

## ノートブック一覧

[ノートブック一覧][1]で、以前に作成したノートブックの表示と検索ができます。各ノートブックの名前、作成者、最終更新日が表示されます。ノートブックは以下のグループに分けられます。

* **マイノートブック**: 自分が作成したノートブック。
* **他のノートブック**: 同じチームのメンバーが作成したノートブック。

## 新しいノートブック

メインナビゲーションから[新しいノートブック][2]を作成します。: *Notebooks > New Notebook*。

デフォルトでは、新しいノートブックは保存されません。保存するには、**Save** ボタンをクリックしてください。

### コンテンツの種類

ノートブックは可視化とテキストセルをサポートします。

#### 視覚化

ノートブック内のグラフは、Datadog のすべてのデータソースに対応しています（メトリクス、ログイベント、Analyzed Span、ライブプロセス、ネットワークトラフィック、RUM イベント、プロファイリングのメトリクス、セキュリティシグナル）。

{{< img src="notebooks/data_sources.png" alt="ノートブックのライブコラボレーション"  style="width:50%;">}}

グラフは、Datadog クエリエディターで作成されます。ノートブックは以下をサポートします。

* [時系列][3]
* [トップリスト][4]
* [ヒートマップ][5]
* [ディストリビューション][6]
* [ログストリーム][7]

#### テキスト

ノートブック内のテキストは[マークダウン][8]によって書式設定されるため、見出し、小見出し、リンク、画像、箇条書き、コードブロックを含めることができます。

### セルの操作

既存のノートブックを開いた時、セルは閉じた状態にあります。セルを開いて編集するには、セルにカーソルを合わせて `CMD + Click` を使用または **Edit** をクリックします。セルを閉じるには、セルではない場所をクリックしてから、 `ESC` または `CMD + Enter` を押します。一度に 1 つのセルのみ開くことができます。

セルを挿入するには、セルの左側にある **+** ボタンを使用します。セルを共有、クローン作成、削除するには、セルにカーソルを合わせると表示される操作トレイを使用するか、キーボードショートカットを使用します。キーボードショートカットの一覧は、ノートブックのヘッダにあるキーボードボタンをクリックすると表示されます。

### タイムフレーム

デフォルトでは、すべてのグラフセルはノートブックのヘッダに設定されたグローバルなタイムフレームに従いますが、個々のセルのグローバルな時間を解除し独立したタイムフレームを設定することができます。これにより、単一のノートブック内で複数の異なる期間でメトリクスの比較ができるため、インシデント調査に役立ちます。

個々のタイムフレームを設定するには、グラフセルの右上にある時計アイコンをクリックします。次に、*Lock this cell to global time frame* のチェックマークを外し、希望するタイムフレームを設定します。

{{< img src="notebooks/time_selector.png" alt="タイムセレクター"  style="width:60%;">}}

**注**: クリックアンドドラッグしてグラフを拡大しても、セルのグローバルな時間を解除することはできません。この操作を行うと、ノートブックのグローバルなタイムフレームが変更されます。

### 展開

グラフを展開するには、セルの右側にある展開アイコンをクリックします。全画面モードの詳細は、[ウィジェット][9] ページを参照してください。

### レイアウトオプション

レイアウトオプションは、編集モードでセルの右側にあるグリッドアイコンをクリックすると表示されます。

* **グラフサイズ**: `XS`、`S`、`M` (デフォルト)、`L`、`XL`から選択。
* **グラフの凡例**: 凡例を非表示にするには、ボックスのチェックマークを外します。`XS` と `S` サイズのグラフでは、凡例は自動的に無効になります。
* **グループ化**: タグ値ごとに 1 つのグラフを表示し、複数の小さいグループに視覚化します。

{{< img src="notebooks/layout_options.png" alt="レイアウトオプション"  style="width:50%;">}}

**注**: 設定の変更は対象となるセルにのみ影響します。

<!--- KEEP- WILL RE-IMPLEMENT
### 個々のセルへのリンク

特定のセルの URL をコピーするには、セルの右側にあるチェーンリンクアイコンをクリックします。可視化セルおよびマークダウンセルの両方で直リンクを利用できます。

ユーザーが特定のセルの URL にアクセスすると、ノートブックが開き、ビューポートの上部にセルが表示されます。絶対リンクのため、セルの URL はノートブック内で新しい位置に移されたとしても、変わることはありません。--->

## その他の参考資料

{{< partial name="whats-next/whats-next.html" >}}

[1]: https://app.datadoghq.com/notebook/list
[2]: https://app.datadoghq.com/notebook
[3]: /ja/dashboards/widgets/timeseries/
[4]: /ja/dashboards/widgets/top_list/
[5]: /ja/dashboards/widgets/heat_map/
[6]: /ja/dashboards/widgets/distribution/
[7]: /ja/dashboards/widgets/log_stream/
[8]: https://daringfireball.net/projects/markdown/
[9]: /ja/dashboards/widgets/#full-screen