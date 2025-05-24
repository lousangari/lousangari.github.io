## Install

Ensure Ruby + jekyll + some-deps are installed :
```
sudo apt update
sudo apt install ruby ruby-dev build-essential dh-autoreconf zlib1g-dev libffi-dev libyaml-dev libssl-dev libreadline-dev 
# or:
brew install ruby

# check that ruby at least 3.x !!
ruby --version

# TODO: check if possible to run without sudo (on a brand-new system)
sudo gem update
sudo gem install bundler
```

Create project **once** :
```
sudo gem install jekyll -v '~> 3.10'

cd git/
jekyll new www-lousangari
cd www-lousangari/
vim Gemfile  #and activate "github-pages" (cf comments)
git init
```

Clone on another machine :
```
cd git/
git clone git@github.com:lousangari/lousangari.github.io.git
cd lousangari.github.io/
(sudo) bundle install
```

## Dev
```
bundle exec jekyll serve
bundle exec jekyll clean
```

Update deps:
```
(sudo) bundle update
bundle exec jekyll serve
git diff Gemfile.lock
git add Gemfile.lock; git ci -m "Update all deps"
```
