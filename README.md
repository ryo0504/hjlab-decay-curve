# hjlab_decay_curve
dockerで環境を構築し、Jupyter Labで使用することを想定しています。
docker run の際にホストのディレクトリをマウントするようにしてあります。

dockerのインストール: https://hub.docker.com/editions/community/docker-ce-desktop-windows/

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
- docker build .
- docker run -p <任意のport番号>:8888 -v <srcのディレクトリを指定>/:/work --name <任意のコンテナ名> <コンテナID>
- (例)docker run -p 8888:8888 -v ~/Desktop/test_dir/src/:/work --name test_name 74f45e4b8084

