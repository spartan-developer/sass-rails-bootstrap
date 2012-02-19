# Sass Rails Bootstrap

Bootstrap is Twitter's toolkit for kickstarting CSS for websites, apps, and more. It includes base CSS styles for typography, forms, buttons, tables, grids, navigation, alerts, and more.

To get started -- checkout http://twitter.github.com/bootstrap!

This gem provides the version of the toolkit with LESS stylesheets converted into SASS for use in Rails 3.1+ projects.


## Installation

This library requires the sass-rails gem to work. So make sure that you have something like this in your Gemfile:

```ruby
group :assets do
  gem 'sass-rails', '~> 3.2.3'
end
```

Then include the following line in your Gemfile and you're all set:

```ruby
gem 'sass-rails-bootstrap', :git => 'git://github.com/voidseeker/sass-rails-bootstrap.git'
```


## Usage

### Stylesheets

The easiest way to use Bootstrap stylesheets is to import `"twitter/bootstrap"` in your `application.css.sass` file:

```css
@import "twitter/bootstrap"
```

Alternatively, you can import each file individually, which allows for some customization.
You'll be able to replace some of the imported files with your own (`variables.css.sass`
would be a good candidate for this), or include just a selected few files for you to use.

Let's say that you want to use just the variables and mixins that come with Twitter Bootstrap.
You can accomplish this by including the following lines in your `.css.sass` file:

```css
@import "twitter/bootstrap/variables"
@import "twitter/bootstrap/mixins"
```

As per the Bootstrap project, `twitter/bootstrap` doesn't include the responsive styles.
You'd have to import the file manually to get them:

```css
@import "twitter/bootstrap/responsive"
```


### Javascripts

As with the stylesheets, you have two options. You can include all of the scripts with a single directive
that goes into your `application.js` file:

```javascript
//= require twitter/bootstrap
```

Or, you could include only the files you need:

```javascript
//= require twitter/bootstrap/alert
//= require twitter/bootstrap/button
//= require twitter/bootstrap/scrollspy
```


## Versioning

This gem will directly track the semantic versioning releases of the Twitter Bootstrap project. Our major and minor versions will always match to theirs.

Currently, the gem reflects the Bootstrap version 2.0.1 up to the commit:
https://github.com/twitter/bootstrap/commit/3d58b4622671bc51c22c857641db3b988e73632a


## Copyright and license

Twitter Bootstrap Project: http://twitter.github.com/bootstrap

Copyright 2012 Twitter, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.