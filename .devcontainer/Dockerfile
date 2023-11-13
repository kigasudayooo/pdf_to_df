# DockerHubのベースとなるイメージを指定
FROM python:3.10.12-slim


# 作業ディレクトリを変更
WORKDIR /pdf_to_table

# ローカルPCのファイルをコンテナのカレントディレクトリにコピー
COPY requirements.txt ${pwd}


RUN apt update
RUN apt install -y software-properties-common vim gcc libgraphviz-dev 


#JAVAのinstall
RUN apt install -y openjdk-17-jre


# pipのアップデート
RUN pip install --upgrade pip

# pythonパッケージをインストール
RUN pip install -r requirements.txt &&\
 rm -rf requirements.txt

# コンテナ起動時に実行するコマンドを指定
CMD ["/bin/bash"]


