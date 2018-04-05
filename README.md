# simplecov-shield

[![Gem Version](https://badge.fury.io/rb/simplecov-shield.svg)](http://badge.fury.io/rb/simplecov-shield)
[![Build Status](https://travis-ci.org/aterris/simplecov-shield.svg?branch=master)](https://travis-ci.org/aterris/simplecov-shield)
[![Code Climate](http://img.shields.io/codeclimate/github/aterris/simplecov-shield.svg)](https://codeclimate.com/github/aterris/simplecov-shield)
[![Coverage Status](https://img.shields.io/coveralls/aterris/simplecov-shield.svg)](https://coveralls.io/r/aterris/simplecov-shield?branch=master)
[![Dependency Status](https://gemnasium.com/aterris/simplecov-shield.svg)](https://gemnasium.com/aterris/simplecov-shield)
[![License](http://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)


[SimpleCov](https://github.com/colszowka/simplecov) Formatter to generate coverage badge via [Shields.io](http://shields.io/)

Now with more badges styles and is compatible with last SimpleCov
release!

### Next TODO

ability to choose the file name of badge


## Install

Add this line to your application's Gemfile
```ruby
gem 'simplecov-shield'
```
Or install it yourself
```ruby
gem install simplecov-shield
```
## Usage

Add this lines on `rails_helper/spec_helper` (or whatever is the file you put the
SimpleCov.start line) file end
```ruby
SimpleCov.formatter = SimpleCov::Formatter::ShieldFormatter
```
Badge will be generated at `coverage/coverage.svg`

## Examples

Normal:

![Normal](https://img.shields.io/codecov/c/github/codecov/example-python.svg)

Flat:

![flat badge](https://cdn.rawgit.com/aterris/simplecov-shield/master/spec/assets/coverage-flat.svg)

Flat-square:

![Codecov](https://img.shields.io/codecov/c/github/codecov/example-python.svg?style=flat-square)

Plastic:

![Codecov](https://img.shields.io/codecov/c/github/codecov/example-python.svg?style=plastic)

For-the-badge:

![Codecov](https://img.shields.io/codecov/c/github/codecov/example-python.svg?style=for-the-badge)

Social:

![Codecov](https://img.shields.io/codecov/c/github/codecov/example-python.svg?style=social)

## Configuration
```ruby
SimpleCov::Formatter::ShieldFormatter.config[:option] = value
```
Put the config line before the `SimpleCov.formatter` call

## Options

<table>
  <thead>
    <tr>
      <th>:option</th>
      <th>Description</th>
      <th>Default</th>
      <th>Value allowed</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>:badge_name</td>
      <td>badge title</td>
      <td>'coverage'</td>
      <td>String</td>
    </tr>
    <tr>
      <td rowspan="5">:style</td>
      <td rowspan="5">badge style</td>
      <td rowspan="5">nil</td>
      <td>'flat'</td>
    </tr>
    <tr>
      <td>'plastic'</td>
    </tr>
    <tr>
      <td>'for-the-badge'</td>
    </tr>
    <tr>
      <td>'flat-square'</td>
    </tr>
    <tr>
      <td>'social'</td>
    </tr>
    <tr>
      <td>:precision</td>
      <td>coverage percent precision</td>
      <td>0</td>
      <td>Integer</td>
    </tr>
  </tbody>
</table>

## Contributing

see [CONTRIBUTING.md](CONTRIBUTING.md)

## Copyright

Copyright (c) 2014 Andrew Terris, Lesley Dennison
