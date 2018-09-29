# clone from git
```
cd ~/git
git clone git@github.com:heroku/ruby-rails-sample.git
```
# deploy
```
dokku apps:create ruby-rails-sample
dokku postgres:create rails-database
dokku postgres:link rails-database ruby-rails-sample
cd ~/git/ruby-rails-sample
git remote add dokku dokku@dokku.ven.li:ruby-rails-sample
git push dokku master
```
# enable HTTPS
```
dokku config:set --no-restart ruby-rails-sample DOKKU_LETSENCRYPT_EMAIL=<e-mail>
dokku letsencrypt  ruby-rails-sample
```
# un-deploy
```
cd ~/git/ruby-rails-sample
dokku postgres:unlink rails-database ruby-rails-sample
dokku postgres:destroy rails-database
dokku apps:destroy ruby-rails-sample
```
