# hjlab-decay-curve
dockerで環境を構築し、Jupyter Labで使用することを想定しています。
ホストのディレクトリをマウントするようにしてあります。

- [動作例](https://github.com/ryo0504/hjlab-decay-curve#%E5%8B%95%E4%BD%9C%E4%BE%8B)
- [ファイルの扱いと環境構築について](https://github.com/ryo0504/hjlab-decay-curve#%E3%83%95%E3%82%A1%E3%82%A4%E3%83%AB%E3%81%AE%E6%89%B1%E3%81%84%E3%81%A8%E7%92%B0%E5%A2%83%E6%A7%8B%E7%AF%89%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6)

## 動作例
![sample](https://i.gyazo.com/6c18cf1b2e80c59ba69d24af58c0c890.gif)

## ファイルの扱いと環境構築について

### env_build
Dockerfileが入ってます。

### src
ソースコードが入っています。
### src/make_an_inputfile.ipynb
時系列データをcsvファイルに変換します。

### src/select_curves.ipynb
変換したcsvのデータをグラフに表示し、インタラクティブにカーブを取り出します。

### src/result
src/make_an_inputfile.ipynbの出力ファイルが格納されます

### src/時系列
基本的に処理したいデータはここに置きます

### src/時系列/csv
src/select_curves.ipynbの出力ファイルが保存されます。

### 環境構築の基本的な手順
- git clone https://github.com/ryo0504/hjlab_decay_curve.git
- cd env_build
- docker-compose up


