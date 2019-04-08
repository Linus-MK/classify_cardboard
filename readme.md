## ファイル構成

* hog.ipynb 学習用notebook
* test_model.ipynb 検証用notebook

## 画像フォルダへのパスについて
hog.ipynbの中では、画像が存在するフォルダへのパスを読み込んでいます。  
path.py というファイルを用意して、その中に
```
img_path = "path/to/folder/"
```
のような形式で、画像フォルダのパスを指定してください。（path.pyはリポジトリ内に含めていません。）  
"path/to/folder/OK" の下にOKの画像が、  
"path/to/folder/NG" の下にNGの画像があることを想定しています。

## do_pickle_file_existフラグについて
画像のHOG特徴量を計算したあと、pickle化して保存しています。  
初回実行時はこのpickleが存在しないため、  
do_pickle_file_exist = Falseと変更してください。  
