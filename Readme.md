# summary
やり方は
ワードをembeddingして、biLstmで多分類するつもりです。

そして、embeddingは訓練し済みword vectorを試します。今回はgoogle-news-word(word2vec)とfasttextを使いました。

訓練済みword vectorをもっと有効的に利用するため、訓練データの前処理します。例えば、訓練済みword vectorにいないワードの削除、stop wordの削除、html文字の削除など。word vectorに合わせるために、textを綺麗にしたいです

今回textデータの処理はlocal上でやっていました（pre-fit-embedding.ipynb）
データを訓練処理はkaggle kernel上でやっていました（環境を備えたため、家のパソコンはwindowsなので、deep learningなら使いにくい）

使ったモデルはbilstmです、keras（backend tensorflow）を利用しました。

# 結果
|type |private score|public score|
|---|---|---|
|google-news with no process data | 0.93930 | 0.93277 |
|google-news with process data | 0.96446 | 0.96443 |
|fasttext with no process data | 0.95180 | 0.95430 |
|fasttext with process data|0.95218|0.95155|

提出したsubmission.csvはgoogle-news with process data

# 考察
to be continue
