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

### Llama
1.  Install the [llama_cpp](https://github.com/yoshoku/llama_cpp.rb) gem
```
gem install llama_cpp -- --with-metal
```

2.  Download a model
```
curl -L https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/resolve/main/llama-2-7b-chat.ggmlv3.q4_K_M.bin --output ./models/llama-2-7b-chat.ggmlv3.q4_K_M.bin
```

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

### Llama 2
* [Llama 2 is here - get it on Hugging Face](https://huggingface.co/blog/llama2)
* [Run Llama-2 Locally in 7 Lines!](https://lastmileai.dev/workbooks/clkbifegg001jpheon6d2s4m8)

* [https://github.com/ggerganov/llama.cpp](ggerganov/llama.cpp)
* [Llama-2-7B-Chat-GGML](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML)

### OpenAI
* [ruby-openai](https://github.com/alexrudall/ruby-openai)

### Python
* [pyenv](https://github.com/pyenv/pyenv)
* [Python](https://www.python.org)

### Ruby
* [Bundler](https://bundler.io)
* [rbenv](https://github.com/rbenv/rbenv)
* [Ruby](https://www.ruby-lang.org/en/)