# ベースイメージをMySQLに指定
FROM --platform=linux/amd64 mysql:8.0.23

# MySQLの設定ファイルをホストマシンからコピー
COPY ./db/my.cnf /etc/my.cnf

# ログ用ディレクトリ・ファイルの作成および権限を付与
RUN mkdir /var/log/mysql && \
    touch /var/log/mysql/error.log && \
    chmod 777 /var/log/mysql/error.log