# ベースイメージをUbuntuに指定
FROM ubuntu:20.04

# PHPのインストール
RUN apt update                                       && \
    apt install -y software-properties-common        && \
    LC_ALL=C.UTF-8 add-apt-repository ppa:ondrej/php && \
    apt update                                       && \
    apt install -y php8.0 php8.0-mysql

# PHPの設定ファイルをホストマシンからコピー
COPY ./app/mail.ini /etc/php/8.0/cli/conf.d/mail.ini

# msmtpのインストール
RUN apt install -yqq msmtp msmtp-mta

# msmtpの設定ファイルをホストマシンからコピー
COPY ./app/mailrc /etc/msmtprc