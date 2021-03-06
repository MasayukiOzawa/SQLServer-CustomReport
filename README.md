# SSMSCustomReport
別名「えろす師匠鰻奢ってくださいレポート」

SQL Server Management Studio のカスタムレポートを使用し、SQL Server の各種情報をダッシュボードとして表示します。

以下の情報を表示することができます。
- インスタンス基本情報
  - 代表的な sp_configure の設定
  - トレースフラグ
  - 代表的な待ち事象
- データベースファイル情報
  - データベースファイル使用状況
  - ファイル I/O
  - 自動拡張の発生状況
- インデックス情報
  - インデックス使用状況
  - 欠落しているインデックス
- キャッシュ情報
  - キャッシュ使用状況
  - データキャッシュの比率
  - プランキャッシュの比率
    - クエリ情報 (TOP 100)
      - 実行回数の高いクエリ
      - 平均 CPU 時間の高いクエリ
      - 平均実行時間の高いクエリ
      - 平均読み取り回数の高いクエリ
      - 平均書き込み回数の高いクエリ
      - 類似クエリ
- バックアップ取得状況 (直近 100 件)

# 動作確認環境
- SQL Server 2012 + SQL Server 2014 Management Studio
- SQL Server 2014 SP1 + SQL Server 2016 CTP 2.2 Management Studio
- SQL Server 2016 CTP 2.2 + SQL Server 2016 CTP 2.2 Management Studio

# 使用方法
1.「@Template.rdl」以外の RDL ファイルをダウンロードして同一のフォルダーに配置します。  
(レポート内から各レポートにリンクをしているため、同一のフォルダー内にファイルを格納します)  
2.SQL Server Management Studio を開き、右クリックメニューの「レポート」→「カスタムレポート」から「Instance.info.rdl」を開きます。  
3.警告メッセージが表示された場合は「OK」をクリックして許可してください。  
(カスタムレポートを表示する際には警告が表示されます。)  

これで SSMS でカスタムレポートとして、本レポートが表示されます。

# 作成環境
[Microsoft® SQL Server® 2014 SP1 レポート ビルダー ](http://www.microsoft.com/ja-jp/download/details.aspx?id=46695) 
