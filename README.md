## What does this app do?

The raison d'etre of this gem - to enable:

* the *easy* installation of pagy in your Rails app.
* programatic installation of pagy via a script. (This may be particularly useful if you want to programmatically create Rails templates, for example).

## Installation

Manually add to Gemfile:

```ruby
gem 'pagy_rails_generator'
```

or run: 

```sh
    bundle add pagy_rails_generator
```

And then execute:

```sh
    bundle install
```

Or install it yourself as:

```sh
    gem install pagy_rails_generator
```

## Usage

It depends on the options you requrire. For example, if I wanted to use pagy with `bootstrap`, with the `gearbox` extra:

```sh
bin/rails generate pagy:install --extras gearbox bootstrap
```

If I wanted `erb` templates as well:

```sh
bin/rails generate pagy:install --extras gearbox bootstrap --template erb
```

```sh
Usage:
rails generate pagy:install [options]

Options:
  [--skip-namespace], [--no-skip-namespace]                          # Skip namespace (affects only isolated engines)
  [--skip-collision-check], [--no-skip-collision-check]              # Skip collision check
  [--extras=bootstrap gearbox etc]                                   # Add pagy extras - choose from any frontend, backend or features extras: https://ddnexus.github.io/pagy/categories/extra/
                                                                     # Possible values: bootstrap, bulma, foundation, materialize, semantic, uikit, navs, arel, array, calendar, countless, elasticsearch_rails, meilisearch, metadata, searchkick, gearbox, items, overflow, support, trim, i18n
  [--sequels=If sequels needed in frontend_helpers], [--no-sequels]  # Add this option if you are using the metadata extra and you want to use sequels
  [--template= erb (or haml or slim)]                                # Add templates for the following styles: navs, bootstrap, bulma, foundation, uikit, to be copied into your app/views/pagy/ folder. Choose from erb, haml, or slim
                                                                     # Possible values: erb, slim, haml

Runtime options:
  -f, [--force]                    # Overwrite files that already exist
  -p, [--pretend], [--no-pretend]  # Run but do not make any changes
  -q, [--quiet], [--no-quiet]      # Suppress status output
  -s, [--skip], [--no-skip]        # Skip files that already exist
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/benkoshy/pagy_rails_generator. 

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

[Code of conduct](https://github.com/[USERNAME]/pagy_rails_generator/blob/master/CODE_OF_CONDUCT.md).
