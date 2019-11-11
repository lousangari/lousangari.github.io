## Install

Ensure Ruby + jekyll + some-deps are installed :
```
sudo apt update
sudo apt install ruby ruby-dev build-essential dh-autoreconf zlib1g-dev
sudo gem update
sudo gem install bundler jekyll
```

Create project **once** :
```
cd git/
jekyll new www-lousangari
cd www-lousangari/
vim Gemfile  #and activate "github-pages" (cf comments)
git init
```

## Dev
```
bundle exec jekyll serve
bundle exec jekyll clean
```
