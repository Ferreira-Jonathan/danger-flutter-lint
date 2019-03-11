# danger-flutter_lint

[![Build Status](https://travis-ci.org/mateuszszklarek/danger-flutter_lint.svg?branch=master)](https://travis-ci.org/mateuszszklarek/danger-flutter_lint)
[![codecov](https://codecov.io/gh/mateuszszklarek/danger-flutter_lint/branch/master/graph/badge.svg)](https://codecov.io/gh/mateuszszklarek/danger-flutter_lint)

A Danger Plugin to lint dart files using `flutter analyze` command line interface.

## Installation

Add this line to your application's Gemfile:

	$ gem 'danger-fluter_lint'

Or install it yourself as:

    $ gem install danger-fluter_lint

## Usage

Just add below line to your Dangerfile

```ruby
flutter_lint.lint
```

it's equivalent of

```ruby
flutter_lint.lint(inline_mode: false)
```

This will add markdown table with summary into your PR.

Or make Danger comment directly on the line instead of printing a Markdown table (GitHub only)

```ruby
flutter_lint.lint(inline_mode: true)
```

#### Lint only added/modified files

If you're dealing with a legacy project, with tons of warnings, you may want to lint only new/modified files. You can easily achieve that, setting the `only_modified_files` parameter to `true`.

```ruby
flutter_lint.only_modified_files = true
flutter_lint.lint
```

## Development

1. Clone this repo
2. Run `bundle install` to setup dependencies.
3. Run `bundle exec rake spec` to run the tests.
4. Use `bundle exec guard` to automatically have tests run as you make changes.
5. Make your changes.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/mateuszszklarek/danger-flutter_lint.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
