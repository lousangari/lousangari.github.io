## Install

Ensure Ruby + jekyll + some-deps are installed :
```
sudo apt update
sudo apt install ruby ruby-dev build-essential dh-autoreconf zlib1g-dev
sudo gem update
sudo gem install bundler
sudo gem install jekyll -v '~> 3.8'
```

Create project **once** :
```
cd git/
jekyll new www-lousangari
cd www-lousangari/
vim Gemfile  #and activate "github-pages" (cf comments)
git init
```

Clone on another machine :
```
cd git/
git clone XXXXX
cd lousangari.github.io/
bundle install
```

## Dev
```
bundle exec jekyll serve
bundle exec jekyll clean
```

Update deps:
```
bundle update
bundle exec jekyll serve
git diff Gemfile.lock
git add Gemfile.lock; git ci -m "Update all deps"
```
