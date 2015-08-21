# lita-dig

[![Build Status](https://img.shields.io/travis/brodock/lita-dig/master.svg)](https://travis-ci.org/brodock/lita-dig)
[![MIT License](https://img.shields.io/badge/license-MIT-brightgreen.svg)](https://tldrlegal.com/license/mit-license)
[![RubyGems :: RMuh Gem Version](http://img.shields.io/gem/v/lita-dig.svg)](https://rubygems.org/gems/lita-dig)
[![Coveralls Coverage](https://img.shields.io/coveralls/brodock/lita-dig/master.svg)](https://coveralls.io/r/brodock/lita-dig)
[![Code Climate](https://img.shields.io/codeclimate/github/brodock/lita-dig.svg)](https://codeclimate.com/github/brodock/lita-dig)
[![Gemnasium](https://img.shields.io/gemnasium/brodock/lita-dig.svg)](https://gemnasium.com/brodock/lita-dig)

A DNS record lookup plugin for [Lita](https://github.com/jimmycuadra/lita).

## Installation

Add lita-dig to your Lita instance's Gemfile:

``` ruby
gem "lita-dig"
```

## Configuration

Configuring the default resolver is optional. If nothing specifed, 8.8.8.8 is used.

```
config.handlers.dig.default_resolver = '127.0.0.1'
```

## Usage

Examples:

```
dig example.com [+short]          - Lookup the A record for example.com using the default resolver (optionally just IP addressses)
dig example.com MX                - Lookup the MX record for example.com using the default resolver
dig @8.8.8.8 example.com [+short] - Lookup the A record for example.com using 8.8.8.8 as a resolver (optionally just IP addressses)
dig @8.8.8.8 example.com NS       - Lookup the NS record for example.com using 8.8.8.8 as a resolver
```

The majority of DNS record types (including "any") are supported.

## License

[MIT](http://opensource.org/licenses/MIT)
