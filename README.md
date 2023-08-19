# rdh/rubyter README

## Introduction
Setting up Jupyter and iruby as described in [Ruby and Jupyter Notebooks](https://nithinbekal.com/posts/ruby-jupyter-notebooks/) on a Mac, from the ground up.

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

5.  Install Rubygems
```
bundle install
```

6.  Install [pyenv](https://github.com/pyenv/pyenv)
```
brew install pyenv
```

7.  Install [Python](https://www.python.org)
```
pyenv install $(cat .python-version)
```

8.  Install [pipenv](https://pipenv.pypa.io)
```
pip install pipenv --user
```
Note: You'll need to add `~/.local/bin` to the `PATH` in your shell.

9.  Install Python packages
```
pipenv install
```

10.  Register Ruby with Jupyter
```
iruby register --force
```

11.  Open Jupyter
```
pipenv run jupyter notebook notebooks/hello.ipynb
```


## How To

### OpenAI

1.  Set up ENV
```
cp notebooks/openai/.env.template notebooks/openai/.env
```
Note: Update the `.env` file with your API key

2.  Open the notebook
```
pipenv run jupyter notebook notebooks/openai/hello.ipynb
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