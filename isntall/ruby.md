
```sh
$ sudo yum -y install git
$ yum install -y openssl-devel readline-devel zlib-devel
$ git clone https://github.com/sstephenson/rbenv.git ~/.rbenv
$ echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.zshrc
$ echo 'eval "$(rbenv init -)"' >> ~/.zshrc
$ rbenv --version
# 確認
$ git clone https://github.com/sstephenson/ruby-build.git ~/.rbenv/plugins/ruby-build
$ rbenv install 2.5.0
$ gem install bundler --no-ri --no-doc
```