# Set up My GitPage Using Jekyll

> Yancy Li
>
> Environment: Mac M1, Ruby 3.0.0, Jekyll 4.2.0

I want to set up my website to visualize my notes and resume. Then I choose Jekyll, which has more function

**Set up a repo**

After signing up for a GitHub account, new a repo.

the repo name: \$your GitHub user name\$.github.io

then setting-pages, inspect the settings, and enter your website to make sure it runs properly

**Install ruby and Jekyll**

install ruby:

```shell
brew install rbenv ruby-build
rbenv install 3.0.0 
rbenv global 3.0.0 
ruby -v rbenv rehash
```

set environment variable 

```shell
echo 'eval "$(rbenv init - zsh)"' >> ~/.zshrc

echo ‘export PATH=”/usr/local/opt/ruby/bin:/usr/local/lib/ruby/gems/3.0.0/bin:$PATH”’ » ~/.zshrc
```

install Jekyll:

`gem install bundler jekyll`

and check if it is successfully installed by running: `jekyll -v`

**Select a module and beatify your page**

choose a module from http://jekyllthemes.org/

fork the module repo, `jekyll new . --force`

if there is an error: Dependency Error..... Then run this code:

`bundle add webrick`

and finish! Now decorate your personal page!

