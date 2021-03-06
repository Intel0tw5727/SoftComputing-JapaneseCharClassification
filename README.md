# JapaneseCharClassification

## 概要
このリポジトリは講義ソフトコンピューティングにて使用するリポジトリとなっています。残りの3回の講義で使用する予定ですので各自リポジトリをクローンしてください。

また講義を重ねるごとにリポジトリを更新しますので、授業が始まる前には`git pull`などで最新の状態にしておいてください。

## ディレクトリ説明

+ data
    + ひらがな・漢字データセットを展開しておくディレクトリ
+ fig
    + notebookの説明の際に加える図が入っています(特に追加や編集はしない)
+ models
    + 学習したパラメータやモデルを保存するディレクトリ
+ notebooks
    + Jupyter Notebookを保存するディレクトリ

## データセット追加手順

+ ひらがな73文字データセット
> https://lab.ndl.go.jp/cms/hiragana73

~~上記サイトから「文字画像データセット(平仮名73文字版)」をダウンロードしてdataディレクトリで展開してください。~~
万が一、サイトが落ちていてアクセスができない場合以下のリンクからダウンロードしてください。7月17日(火)朝8時現在で公式サイトにアクセスできないので以下のリンクからダウンロードしてください。

> https://ie.u-ryukyu.ac.jp/~e155727/Downloads/hiragana73.tar.gz

tarファイルの解凍は以下のコマンドで実行できます( -C オプションは解凍先指定 )

```shell
tar xvzf hiragana73.tar.gz -C data/
```

## 使用モジュール
箇条書きで示すモジュールはnotebook内で使用するため、データセットダウンロードが終わり次第、以下のコマンドを実行してインストールしてください。

```shell
pip install -r requirements.txt
```

+ numpy
    + 数値計算ライブラリ。ここではデータの加工などに使用。
+ pandas 
    + データ解析支援ライブラリ。ここではデータセットラベルとの対応表として使用。
+ matplotlib 
    + グラフ描画ライブラリ。ここではモデルの予測結果やデータセットの確認に使用。
+ OpenCV(cv2)
    + 画像加工ライブラリ。ここではデータセットの前処理に使用。
+ scikit-learn
    + 機械学習ライブラリ。ここでは訓練データとテストデータの分割に使用。
+ keras
    + Tensorflowをバックエンドとした深層学習ライブラリ。今回の講義のメインで使用。
+ tqdm
    + プログレスバー表示ライブラリ。大規模なfor文における進捗を管理するために使用。
+ os, sys
    + Python標準ライブラリ。osライブラリではディレクトリの探索に使用。
