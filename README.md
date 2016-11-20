# OUT OF DATE => NEW VERSION IS [HERE](https://github.com/codeforaotearoa/opendata-toolkit)

### Open Data Tool Kit

For the theme, and basic layout, we're using a fork of the [Federalist Docs](https://github.com/18F/federalist-docs) theme with a [Jekyll](https://jekyllrb.com) install.

The original Federalist license can be found in the bottom half of the **LICENSE.md** file

## How do I access the toolkit?

You can see a live, currently broken version at [https://codeforaotearoa.github.io/open-data-tool-kit](https://codeforaotearoa.github.io/open-data-tool-kit)

It's broken due to the styles not looking in the right place and since content is the priority at the moment, it hasn't been fixed yet.

Until then, you can just download the repo and serve it locally

## How do I run the tool kit locally?

Assuming you have [Ruby](https://www.ruby-lang.org) installed, you'll need to go ahead and install the Bundler gem if you don't already have it, like so:

```ruby
gem install bundler
```

At present, *__we've had issues with the latest Bundler (version 1.13.6) throwing out permission errors__*. If you have that same error occur, try removing bundler and installing an earlier version, like so:

```ruby
gem uninstall bundler
gem install bundler:1.13
```

Once that's up and running, install the other remaining dependencies

```ruby
bundle install
```

Finally, using the **go** script, serve the toolkit

```sh
./go serve
```

The toolkit will then be available at **http://localhost:4000**.

## What about building the toolkit?

If you need to generate HTML, which will have broken CSS (see "How do I access the toolkit"), the **go** script will automate that for you

```sh
./go build
```

The generated files can then be found in the **docs** folder.

The reasoning behind the **docs** folder is that Github Pages allows you to host the docs folder out of the master branch, saving us having to host out of a different branch or repo.

## How do I edit the styles?

At the moment, the styles are hosted at [https://github.com/codeforaotearoa/odtk-style](https://github.com/codeforaotearoa/odtk-style) which is a Ruby gem.

It's also a fork of the 18F styles which we'll eventually pull into this repo at some point.

Until then, you'll have to fork the styles as well and edit the Gemfile to pull in your fork instead of ours
