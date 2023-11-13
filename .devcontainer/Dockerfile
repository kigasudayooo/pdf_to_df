# DockerHubのベースとなるイメージを指定
FROM python:3.10.12-slim

#JAVAの環境変数を設定する(これがないとtabulaが使えない)
ENV JAVA_HOME /usr/lib/jvm/java-8-oracle

# 作業ディレクトリを変更
WORKDIR /pdf_to_table

# ローカルPCのファイルをコンテナのカレントディレクトリにコピー
COPY requirements.txt ${pwd}


RUN apt update && \
    apt install -y software-properties-common vim gcc libgraphviz-dev openjdk-8-jre

# pipのアップデート
RUN pip install --upgrade pip

# pythonパッケージをインストール
RUN pip install -r requirements.txt &&\
 rm -rf requirements.txt

# コンテナ起動時に実行するコマンドを指定
CMD ["/bin/bash"]


