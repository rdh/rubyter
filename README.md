# rdh/rubyter README

## Introduction
Setting up Jupyter and iruby as described in [Ruby and Jupyter Notebooks](https://nithinbekal.com/posts/ruby-jupyter-notebooks/).

## Getting Started

1.  Install [Homebrew](https://brew.sh)
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2.  Install [rbenv](https://github.com/rbenv/rbenv)
```
brew install rbenv ruby-build
rbenv init
```
Note: Follow the instruction output by rbenv to configure your shell.

3.  Install [Ruby](https://www.ruby-lang.org/en/)
```
rbenv install $(cat .ruby-version)
```  

4.  Install [Bundler](https://bundler.io)
```
gem install bundler
```

5.  Install [pyenv](https://github.com/pyenv/pyenv)
```
brew install pyenv
```

6.  Install [Python](https://www.python.org)
```
pyenv install $(cat .python-version)
```

7.  Install [pipenv](https://pipenv.pypa.io)
```
pip install pipenv --user
```
Note: You'll need to add `~/.local/bin` to the `PATH` in your shell.

8.  Install Python packages
```
pipenv install
```

## References

### Blogs
* [Ruby and Jupyter Notebooks](https://nithinbekal.com/posts/ruby-jupyter-notebooks/)

### Python
* [pyenv](https://github.com/pyenv/pyenv)
* [Python](https://www.python.org)

### Ruby
* [Bundler](https://bundler.io)
* [rbenv](https://github.com/rbenv/rbenv)
* [Ruby](https://www.ruby-lang.org/en/)