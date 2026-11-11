# 支出データ集計ツール
CSVから支出データを読み込み、集計・分析を行い、その結果を表示するツールです  
一覧表示・絞り込み表示・合計表示・グラフ表示などが行えます

## 使用ファイル
- `main.py` - 実行ファイル
- `expense_loader.py` - CSVを読み込み、`pandas`のDataFrameとして返す
- `expense_summary.py` - CSVに登場する分類を取得・分析する
- `window.py` - メイン画面作成
- `chart.py` - 棒グラフ作成
- `data/expenses.csv` - 使用するCSV
- `requirements.txt` - 使用する外部パッケージ
## 使用パッケージ
- `tkinter` - ウィンドウ作成
- `pandas` - CSV読み込み・DataFrame化
- `matplotlib` - グラフ作成

## 実行
OS：Windows  
Python：`Python3`系  
作業ディレクトリ：`1-python-expense-viewer-practice`

外部パッケージをインストール
```
pip install -r requirements.txt
```

`tkinter`利用確認
```
py -m tkinter
```

実行
```
py main.py
```

## 実行結果
メインウィンドウが開き、`expenses.csv`内のデータが一覧表示される  
表示順はCSV内の記述順と同一となっている
`分類`選択ボックスから分類別の絞り込み表示も行える

件数・合計金額が画面下部・左側に表示される
```
【表示例】
全　体：16件　合計9,660円
食　費： 6件　合計4,330円
交通費： 4件　合計1,030円
日用品： 3件　合計1,010円
娯　楽： 3件　合計3,290円
```
`グラフを表示`ボタンをクリックするとサブウィンドウが開き、分類別の合計金額が棒グラフで表示される  
これらの集計結果は、絞り込み中は選択した分類のもののみ表示される