# pipenv-consumer-example
How to install a package from a private PyPI server (Gemfury)

To see how to push a (Poetry) package to a private PyPI repository see: https://github.com/edkrueger/poetry-package-template.  

## Pulling from Private PyPI

### Environmental Variables
Environmental variables are a good way to keep our tokens secret and our options configurable. To set them, copy `sample.envrc` to `.envrc` and change the values.  
To load `.envrc`, one could just run `.envrc` as a shell script, but direnv will make things easier by automatically loading the variable when you enter the directory, once allowed.  
To install direnv on a mac running zsh, use brew to install with `brew install direnv` and hook in into your shell by adding `eval "$(direnv hook zsh)"` to your `.zshrc` file. For other install instructions see: https://direnv.net/.  
To allow direnv to load `.envrc` in a directory run `direnv allow`.  

### Pull from Private PyPI
In the `Pipfile`, modify the second source. You can change the `name` value if you like, but as long as it is consistent within the file, it will not matter. You should change the `url` value to your URL.  
From here simply run `pipenv install`.  
