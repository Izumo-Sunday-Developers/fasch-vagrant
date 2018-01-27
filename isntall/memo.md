
```sh
$ yum install -y zsh
$ cat /etc/shells
/bin/sh
/bin/bash
/sbin/nologin
/usr/bin/sh
/usr/bin/bash
/usr/sbin/nologin
/bin/zsh
$ chsh
# シェル変更
```

あとは適当な /.zshrc を配置してログインし直す

### postgres

公式を参考に
https://www.postgresql.org/download/linux/redhat/

```sh
$ sudo yum -y install https://download.postgresql.org/pub/repos/yum/10/redhat/rhel-7-x86_64/pgdg-centos10-10-1.noarch.rpm
$ sudo yum -y install postgresql10 postgresql10-server postgresql10-contrib
$ psql --version
# 確認
$ sudo /usr/pgsql-10/bin/postgresql-10-setup initdb
$ sudo systemctl enable postgresql-10
$ sudo systemctl start postgresql-10
# postgresユーザにパスワード設定
$ sudo passwd postgres
# ユーザ作る
$ sudo -u postgres psql
postgres=# create user <test_user> with password '<test_pass>';
postgres=# \q

```